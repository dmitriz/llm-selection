# LLM Selection Project

A system for selecting, routing, and evaluating large language models (LLMs) based on task type, reasoning ability, access methods, costs, and reliability.

## 🚀 Getting Started

This project is designed to help you make strategic model selection decisions for your LLM tasks. The repository will grow to include:

- Model catalogs with capability tracking
- Routing logic for task-to-model mapping
- Evaluation tools and reviewer prompts
- Integration patterns for various LLM access methods

## 📂 Repository Structure

- `models.md` - Catalog of available LLMs and their capabilities ✅ **COMPLETED**
- `routing-strategy.md` - Logic for matching tasks to models ✅ **COMPLETED**
- `reviewer-prompts.md` - Evaluation criteria and prompts ✅ **COMPLETED**
- `PROJECT_BACKLOG.md` - Complete project backlog with detailed goals and plans

## 🏁 Initial Tasks

- [x] Create `models.md` for cataloging available LLMs ✅ **COMPLETED** - Comprehensive catalog with 8 major providers
- [x] Add `routing-strategy.md` to outline logic by task type ✅ **COMPLETED** - Dynamic routing with fallback strategies
- [x] Prepare reviewer prompt set in `reviewer-prompts.md` ✅ **COMPLETED** - Quality evaluation framework
- [ ] Design and test a selection prompt (e.g., "Which model should I use for X?")

## 📊 Roadmap & Prioritization

### Phase 1: Model Cataloging (June 2025)

- **Focus**: Comprehensive model inventory and capability assessment
- **Deliverable**: `models.md` with detailed capability matrix
- **Key milestones**: 
  - Complete API documentation for all major providers
  - Document token limits and rate restrictions
  - Create standardized capability scoring system

### Phase 2: Routing Strategy (July 2025)

- **Focus**: Decision framework for model selection
- **Deliverable**: `routing-strategy.md` with decision trees
- **Key milestones**:
  - Map task types to optimal model profiles
  - Create fallback pathways for rate limits and failures
  - Design cost optimization strategies

### Phase 3: Evaluation Framework (August 2025)

- **Focus**: Output quality assessment
- **Deliverable**: `reviewer-prompts.md` with scoring metrics
- **Key milestones**:
  - Develop standardized evaluation criteria
  - Create reviewer prompts for different output types
  - Build comparison methodology for cross-model evaluation

### Success Metrics

- **Latency targets**: <500ms for routing decisions, <5s end-to-end for simple tasks
- **Hallucination thresholds**: <2% factual errors in final outputs
- **Cost efficiency**: 30% reduction in token usage vs. single-model approach
- **Selection accuracy**: >95% appropriate model selection for given task types

## 📖 Detailed Documentation

For complete project details including:

- Core components
- Key insights and strategy notes
- Planned experiments
- Roles and agents

Please refer to the [PROJECT_BACKLOG.md](PROJECT_BACKLOG.md) file.

## 🤝 Contributing

Contributions are welcome! Check the PROJECT_BACKLOG.md for areas where you can help, or suggest new features and improvements.

---

> Note: This project is in active development. Features and documentation will evolve over time.

# LLM Output Review and Evaluation Framework

*Comprehensive evaluation criteria and reviewer prompts for assessing LLM output quality across different task types and use cases*

---

## 🎯 Core Evaluation Principles

### Quality Dimensions
1. **Accuracy**: Factual correctness and reliability
2. **Relevance**: Task alignment and requirement fulfillment
3. **Coherence**: Logical structure and flow
4. **Completeness**: Comprehensive coverage of requirements
5. **Efficiency**: Cost-effectiveness and resource optimization
6. **Safety**: Content policy compliance and harm prevention

### Scoring Framework
- **Excellent (90-100)**: Exceeds expectations, publication-ready
- **Good (75-89)**: Meets requirements with minor improvements needed
- **Acceptable (60-74)**: Usable with notable limitations
- **Poor (40-59)**: Requires significant revision
- **Unacceptable (0-39)**: Fails basic requirements, unusable

---

## 📋 Task-Specific Evaluation Frameworks

### Code Generation Evaluation

#### Primary Criteria
**Functionality (40%)**
- ✅ Code executes without errors
- ✅ Produces expected output for test cases
- ✅ Handles edge cases appropriately
- ✅ Follows specified requirements completely

**Code Quality (30%)**
- ✅ Follows language best practices and conventions
- ✅ Proper error handling and validation
- ✅ Clear variable names and structure
- ✅ Appropriate comments and documentation

**Efficiency (20%)**
- ✅ Optimal time complexity for the problem
- ✅ Appropriate memory usage
- ✅ No unnecessary operations or redundancy
- ✅ Scalable design patterns

**Security (10%)**
- ✅ No obvious security vulnerabilities
- ✅ Proper input validation and sanitization
- ✅ Safe handling of sensitive data
- ✅ Follows security best practices

#### Reviewer Prompt Template
```
Evaluate this code generation output:

FUNCTIONALITY REVIEW:
- Does the code execute without errors? (Test with provided inputs)
- Does it produce the expected outputs?
- Are edge cases handled properly?
- Does it meet all specified requirements?

CODE QUALITY REVIEW:
- Does it follow {language} best practices?
- Is error handling appropriate and comprehensive?
- Are variable names clear and descriptive?
- Is the code structure logical and maintainable?

EFFICIENCY REVIEW:
- What is the time complexity? Is it optimal for this problem?
- Is memory usage appropriate?
- Are there unnecessary operations that could be removed?
- Does the design scale well with larger inputs?

SECURITY REVIEW:
- Are there any obvious security vulnerabilities?
- Is input validation comprehensive?
- Are sensitive operations handled safely?
- Does it follow security best practices for {domain}?

OVERALL SCORE: ___/100
RECOMMENDATION: [Accept/Revise/Reject]
PRIORITY FIXES: [List top 3 issues if score < 75]
```

### Content Generation Evaluation

#### Primary Criteria
**Accuracy & Factuality (35%)**
- ✅ All factual claims are verifiable and correct
- ✅ No misleading or false information
- ✅ Proper attribution and sourcing where required
- ✅ Up-to-date information for time-sensitive topics

**Relevance & Alignment (25%)**
- ✅ Directly addresses the specified topic/prompt
- ✅ Appropriate tone and style for target audience
- ✅ Meets specified length and format requirements
- ✅ Includes all requested elements and sections

**Quality & Readability (25%)**
- ✅ Clear, engaging writing style
- ✅ Proper grammar, spelling, and punctuation
- ✅ Logical flow and smooth transitions
- ✅ Appropriate structure with headers, paragraphs, etc.

**Originality & Value (15%)**
- ✅ Provides unique insights or perspectives
- ✅ Avoids generic or templated responses
- ✅ Adds value beyond basic information
- ✅ Demonstrates understanding of nuances

#### Reviewer Prompt Template
```
Evaluate this content generation output:

ACCURACY & FACTUALITY REVIEW:
- Verify 3-5 key factual claims - are they accurate?
- Are there any misleading statements or false information?
- Is sourcing appropriate for the content type?
- Is information current and up-to-date?

RELEVANCE & ALIGNMENT REVIEW:
- Does it directly address the original prompt/request?
- Is the tone appropriate for the target audience?
- Does it meet length and format specifications?
- Are all requested elements included?

QUALITY & READABILITY REVIEW:
- Is the writing clear and engaging?
- Check grammar, spelling, and punctuation
- Does it flow logically from point to point?
- Is the structure appropriate and well-organized?

ORIGINALITY & VALUE REVIEW:
- Does it provide unique insights or fresh perspectives?
- Does it avoid generic, templated responses?
- What specific value does it add beyond basic information?
- Does it demonstrate deep understanding of the topic?

OVERALL SCORE: ___/100
RECOMMENDATION: [Accept/Revise/Reject]
CONTENT IMPROVEMENTS: [List specific enhancement suggestions]
```

### Data Analysis Evaluation

#### Primary Criteria
**Analytical Accuracy (40%)**
- ✅ Correct statistical calculations and interpretations
- ✅ Appropriate analytical methods for the data type
- ✅ Valid conclusions drawn from the evidence
- ✅ No logical fallacies or statistical errors

**Insight Quality (30%)**
- ✅ Identifies meaningful patterns and trends
- ✅ Provides actionable recommendations
- ✅ Contextualizes findings appropriately
- ✅ Addresses business or research objectives

**Methodology (20%)**
- ✅ Clear explanation of analytical approach
- ✅ Appropriate handling of data limitations
- ✅ Proper visualization and presentation
- ✅ Reproducible analysis steps

**Communication (10%)**
- ✅ Clear, jargon-free explanations
- ✅ Appropriate level of detail for audience
- ✅ Effective use of charts, graphs, or tables
- ✅ Executive summary for complex analyses

#### Reviewer Prompt Template
```
Evaluate this data analysis output:

ANALYTICAL ACCURACY REVIEW:
- Verify key calculations - are they mathematically correct?
- Are the analytical methods appropriate for this data type?
- Are conclusions logically supported by the evidence?
- Check for any statistical errors or misinterpretations

INSIGHT QUALITY REVIEW:
- What meaningful patterns or trends are identified?
- Are the recommendations actionable and specific?
- Is the analysis contextualized appropriately?
- Does it address the original business/research objectives?

METHODOLOGY REVIEW:
- Is the analytical approach clearly explained?
- How are data limitations acknowledged and handled?
- Are visualizations effective and accurate?
- Can this analysis be reproduced by others?

COMMUNICATION REVIEW:
- Are explanations clear and accessible to the target audience?
- Is the level of technical detail appropriate?
- Are charts/graphs/tables effective and well-labeled?
- Is there a clear executive summary of findings?

OVERALL SCORE: ___/100
RECOMMENDATION: [Accept/Revise/Reject]
ANALYSIS IMPROVEMENTS: [List specific methodological or interpretive issues]
```

### Research Task Evaluation

#### Primary Criteria
**Source Quality & Credibility (35%)**
- ✅ Uses authoritative, credible sources
- ✅ Balances multiple perspectives appropriately
- ✅ Current sources for time-sensitive topics
- ✅ Proper citation and attribution

**Comprehensiveness (30%)**
- ✅ Covers all key aspects of the research question
- ✅ Addresses counterarguments or limitations
- ✅ Appropriate depth for the scope
- ✅ Identifies gaps or areas for further research

**Analysis & Synthesis (25%)**
- ✅ Synthesizes information from multiple sources
- ✅ Provides original analysis and insights
- ✅ Identifies patterns, trends, or themes
- ✅ Draws well-supported conclusions

**Organization & Clarity (10%)**
- ✅ Logical structure and clear flow
- ✅ Appropriate headings and sections
- ✅ Clear executive summary
- ✅ Professional presentation

#### Reviewer Prompt Template
```
Evaluate this research output:

SOURCE QUALITY & CREDIBILITY REVIEW:
- Are sources authoritative and credible?
- Is there appropriate balance of perspectives?
- Are sources current enough for the topic?
- Is citation and attribution proper and complete?

COMPREHENSIVENESS REVIEW:
- Does it cover all key aspects of the research question?
- Are counterarguments or limitations addressed?
- Is the depth appropriate for the intended scope?
- Are research gaps or future directions identified?

ANALYSIS & SYNTHESIS REVIEW:
- How effectively does it synthesize multiple sources?
- What original analysis or insights are provided?
- Are patterns, trends, or themes clearly identified?
- Are conclusions well-supported by the evidence?

ORGANIZATION & CLARITY REVIEW:
- Is the structure logical and easy to follow?
- Are headings and sections appropriate and helpful?
- Is there a clear, informative executive summary?
- Is the overall presentation professional?

OVERALL SCORE: ___/100
RECOMMENDATION: [Accept/Revise/Reject]
RESEARCH IMPROVEMENTS: [List specific gaps or methodological issues]
```

### Reasoning Task Evaluation

#### Primary Criteria
**Logical Validity (45%)**
- ✅ Arguments follow logical structure
- ✅ No logical fallacies or contradictions
- ✅ Premises support conclusions appropriately
- ✅ Step-by-step reasoning is clear

**Problem-Solving Approach (30%)**
- ✅ Appropriate methodology for problem type
- ✅ Breaks complex problems into manageable parts
- ✅ Considers multiple solution approaches
- ✅ Verifies solutions where possible

**Clarity & Communication (15%)**
- ✅ Reasoning steps are clearly explained
- ✅ Complex concepts explained simply
- ✅ Appropriate use of examples or analogies
- ✅ Conclusion is clearly stated

**Completeness (10%)**
- ✅ Addresses all aspects of the problem
- ✅ Considers edge cases or exceptions
- ✅ Acknowledges limitations or assumptions
- ✅ Provides complete solution path

#### Reviewer Prompt Template
```
Evaluate this reasoning task output:

LOGICAL VALIDITY REVIEW:
- Does the argument follow a logical structure?
- Are there any logical fallacies or contradictions?
- Do the premises adequately support the conclusions?
- Is each reasoning step clearly justified?

PROBLEM-SOLVING APPROACH REVIEW:
- Is the methodology appropriate for this type of problem?
- How effectively are complex problems broken down?
- Are multiple solution approaches considered?
- Is the solution verified or validated where possible?

CLARITY & COMMUNICATION REVIEW:
- Are reasoning steps explained clearly and simply?
- How well are complex concepts made accessible?
- Are examples or analogies used effectively?
- Is the final conclusion clearly stated?

COMPLETENESS REVIEW:
- Does it address all aspects of the original problem?
- Are edge cases or exceptions considered?
- Are limitations or assumptions clearly acknowledged?
- Is the solution path complete from start to finish?

OVERALL SCORE: ___/100
RECOMMENDATION: [Accept/Revise/Reject]
REASONING IMPROVEMENTS: [List specific logical or methodological issues]
```

### Conversational Task Evaluation

#### Primary Criteria
**Helpfulness & Relevance (35%)**
- ✅ Directly addresses user's question or need
- ✅ Provides actionable, useful information
- ✅ Anticipates follow-up questions appropriately
- ✅ Offers additional relevant context

**Tone & Communication Style (30%)**
- ✅ Appropriate tone for the context
- ✅ Clear, natural language
- ✅ Empathetic and respectful approach
- ✅ Engaging without being overly casual

**Accuracy & Safety (25%)**
- ✅ Factually correct information
- ✅ Safe recommendations and advice
- ✅ Avoids harmful or inappropriate content
- ✅ Acknowledges uncertainty when appropriate

**Conversation Flow (10%)**
- ✅ Maintains context from previous exchanges
- ✅ Natural progression of topics
- ✅ Appropriate response length
- ✅ Sets up potential follow-up interactions

#### Reviewer Prompt Template
```
Evaluate this conversational output:

HELPFULNESS & RELEVANCE REVIEW:
- Does it directly address the user's question or need?
- Is the information provided actionable and useful?
- Does it appropriately anticipate follow-up questions?
- Is relevant additional context provided?

TONE & COMMUNICATION STYLE REVIEW:
- Is the tone appropriate for the conversational context?
- Is the language clear, natural, and accessible?
- Does it demonstrate empathy and respect?
- Is it engaging without being inappropriate?

ACCURACY & SAFETY REVIEW:
- Is all factual information correct?
- Are recommendations and advice safe and appropriate?
- Does it avoid harmful or inappropriate content?
- Does it appropriately acknowledge uncertainty?

CONVERSATION FLOW REVIEW:
- Does it maintain context from the conversation?
- Is the topic progression natural?
- Is the response length appropriate?
- Does it set up potential follow-up interactions well?

OVERALL SCORE: ___/100
RECOMMENDATION: [Accept/Revise/Reject]
CONVERSATION IMPROVEMENTS: [List specific communication or content issues]
```

---

## 🔄 Cross-Model Comparison Framework

### Comparative Evaluation Process
1. **Generate outputs** from 2-3 different models for the same task
2. **Apply task-specific evaluation** to each output independently
3. **Compare outputs** across key quality dimensions
4. **Identify best performer** and specific strengths/weaknesses
5. **Document model-specific patterns** for future routing decisions

### Comparative Analysis Template
```
CROSS-MODEL COMPARISON ANALYSIS

Task Type: _______________
Models Compared: _______________

INDIVIDUAL SCORES:
Model A ({model_name}): ___/100
Model B ({model_name}): ___/100
Model C ({model_name}): ___/100

DIMENSION-BY-DIMENSION COMPARISON:
Primary Criterion 1:
- Model A: [Score + brief justification]
- Model B: [Score + brief justification]
- Model C: [Score + brief justification]
- Winner: Model ___

Primary Criterion 2:
- Model A: [Score + brief justification]
- Model B: [Score + brief justification]
- Model C: [Score + brief justification]
- Winner: Model ___

[Continue for all primary criteria...]

OVERALL ASSESSMENT:
Best Overall: Model ___ (Score: ___/100)
Best Value (Quality/Cost): Model ___ 
Best for Speed: Model ___
Best for Accuracy: Model ___

ROUTING RECOMMENDATIONS:
- Use Model ___ for: [specific scenarios]
- Use Model ___ for: [specific scenarios]
- Avoid Model ___ for: [specific scenarios]

PATTERN OBSERVATIONS:
- [Model-specific strengths and weaknesses noted]
- [Consistent quality patterns across similar tasks]
- [Cost-effectiveness insights]
```

---

## 🎚️ Quality Thresholds and Routing Decisions

### Minimum Quality Gates
**Production Use**: 75+ overall score
- All safety criteria must be met (100%)
- No critical accuracy failures
- Acceptable performance in primary criteria

**Development/Testing**: 60+ overall score
- Useful for iteration and improvement
- May have limitations but provides value
- Requires human oversight

**Unacceptable**: < 60 overall score
- Automatic fallback to alternative model
- Requires significant revision or rejection
- May indicate model-task mismatch

### Automated Quality Scoring
**High-Confidence Scores (90%+ agreement with human reviewers)**:
- Code execution and syntax errors
- Factual accuracy for verifiable claims
- Basic grammar and spelling checks
- Format and structure compliance

**Medium-Confidence Scores (70-90% agreement)**:
- Content relevance and alignment
- Logical reasoning validation
- Basic safety and appropriateness
- Completeness assessment

**Low-Confidence Scores (< 70% agreement)**:
- Creative quality and originality
- Nuanced tone and style appropriateness
- Complex reasoning evaluation
- Subjective value and insight assessment

### Quality-Based Routing Logic
```python
def quality_based_routing(task, initial_output, quality_score):
    if quality_score >= 90:
        return "accept", initial_output
    elif quality_score >= 75:
        return "accept_with_minor_review", initial_output
    elif quality_score >= 60:
        return "revise_with_feedback", generate_improvement_suggestions(initial_output)
    else:
        return "fallback_to_better_model", route_to_higher_tier_model(task)
```

---

## 📊 Quality Metrics and Monitoring

### Key Performance Indicators
**Quality Consistency**:
- Average quality score by model and task type
- Standard deviation of quality scores
- Percentage of outputs meeting minimum thresholds

**Review Efficiency**:
- Time to complete quality review
- Agreement rate between automated and human scoring
- False positive/negative rates for quality gates

**Cost-Quality Trade-offs**:
- Quality score per dollar spent
- Cost increase required for quality improvement
- ROI of using higher-tier models

### Quality Monitoring Dashboard
**Real-Time Metrics**:
- Current quality scores by model
- Quality trend over time
- Task-specific quality patterns
- Cost-adjusted quality rankings

**Alert Triggers**:
- Quality score drops below threshold for any model
- Sudden changes in quality patterns
- Consistent quality issues with specific task types
- Cost-quality efficiency deterioration

### Continuous Improvement Process
**Weekly Quality Reviews**:
- Analyze quality trends and patterns
- Identify models or tasks with declining performance
- Review and update quality thresholds
- Update routing rules based on quality data

**Monthly Quality Assessments**:
- Deep dive into specific quality issues
- Update reviewer prompts based on findings
- Calibrate automated scoring against human judgment
- Optimize routing strategies for quality improvement

---

## 🔧 Implementation Guidelines

### Integration with Routing System
**Quality-First Routing**:
1. Initial model selection based on routing strategy
2. Generate output with selected model
3. Apply automated quality assessment
4. If quality below threshold, trigger fallback model
5. Human review for borderline cases

**Quality Learning Loop**:
1. Track quality scores for each routing decision
2. Update model performance profiles
3. Adjust routing weights based on quality outcomes
4. Continuously improve quality prediction accuracy

### Reviewer Prompt Customization
**Domain-Specific Adaptations**:
- Legal documents: Emphasize accuracy and compliance
- Medical content: Prioritize safety and evidence-based information
- Creative writing: Focus on originality and engagement
- Technical documentation: Emphasize clarity and completeness

**Client-Specific Requirements**:
- Brand voice and style guidelines
- Industry-specific quality standards
- Custom evaluation criteria
- Specialized domain knowledge requirements

### Quality Assurance Workflow
**Automated Quality Gates**:
- Immediate assessment of basic quality criteria
- Flagging of potential issues for human review
- Integration with routing and fallback systems
- Real-time quality monitoring and alerts

**Human Quality Review**:
- Detailed assessment using task-specific prompts
- Calibration of automated scoring systems
- Complex judgment calls and edge cases
- Continuous improvement of quality frameworks

---

*Last updated: June 3, 2025*  
*Next review: July 1, 2025*
