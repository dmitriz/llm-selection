# Test Scenarios for LLM Selection System

import json
import time
from typing import Dict, List, Any
from dataclasses import asdict

from routing_engine import route_simple, TaskType, CostTier, SpeedRequirement
from quality_evaluator import evaluate_with_prompt
from selection_cli import SelectionCLI

class TestScenario:
    """Individual test scenario for validation"""
    
    def __init__(self, name: str, description: str, expected_task_type: TaskType,
                 cost_preference: str = "value", speed_preference: str = "standard",
                 context_size: int = 4000):
        self.name = name
        self.description = description
        self.expected_task_type = expected_task_type
        self.cost_preference = cost_preference
        self.speed_preference = speed_preference
        self.context_size = context_size
    
    def run_test(self, cli: SelectionCLI):
        """Execute the test scenario"""
        print(f"\nRunning test: {self.name}")
        print(f"Description: {self.description}")
        
        # Get quick recommendation
        decision = cli.quick_recommendation(
            self.description,
            cost_preference=self.cost_preference,
            speed_preference=self.speed_preference,
            context_size=self.context_size
        )
        
        # Validate task type
        assert decision.task_type == self.expected_task_type, \
            f"Expected task type {self.expected_task_type}, but got {decision.task_type}"
        
        # Evaluate quality
        quality_score = cli.evaluator.evaluate_output(
            decision.sample_output, decision.task_type, self.description
        )
        
        print(f"Quality Score: {quality_score.overall_score:.1%} ({quality_score.recommendation})")
        
        # Check if the decision is reasonable (dummy check here, can be expanded)
        assert decision.estimated_cost < 10, "Estimated cost is too high!"
        assert decision.expected_quality > 0.7, "Expected quality is too low!"
        
        print("Test passed!")
        
def main():
    """Main test runner"""
    cli = SelectionCLI()
    
    # Define test scenarios
    tests = [
        TestScenario(
            name="Simple description",
            description="Translate the following English text to French: 'Hello, how are you?'",
            expected_task_type=TaskType.TRANSLATION,
            cost_preference="ultra_low",
            speed_preference="real_time",
            context_size=2000
        ),
        TestScenario(
            name="Complex reasoning",
            description="What are the implications of the Fermi Paradox?",
            expected_task_type=TaskType.QUESTION_ANSWERING,
            cost_preference="value",
            speed_preference="standard",
            context_size=8000
        ),
        TestScenario(
            name="Multimodal task",
            description="Analyze the attached image and describe its content.",
            expected_task_type=TaskType.IMAGE_ANALYSIS,
            cost_preference="premium",
            speed_preference="batch",
            context_size=40000
        )
    ]
    
    # Run all tests
    for test in tests:
        test.run_test(cli)

if __name__ == "__main__":
    main()
