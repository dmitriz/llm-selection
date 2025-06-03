# LLM Selection Prompt

*A practical prompt template for getting intelligent model recommendations based on your specific task requirements*

---

## 🎯 Universal Selection Prompt

Use this prompt with any LLM to get intelligent model selection recommendations:

```
I need help selecting the optimal LLM for my task. Please analyze my requirements and recommend the best model(s) based on the following criteria:

TASK DETAILS:
- Task type: [code generation/content creation/data analysis/research/reasoning/conversation]
- Specific use case: [describe your exact need]
- Expected output: [format, length, complexity]
- Quality requirements: [accuracy needs, acceptable error rate]

CONTEXT REQUIREMENTS:
- Input size: [estimated tokens/characters]
- Context needed: [how much background context]
- Multimodal needs: [text only/images/audio/other]

PERFORMANCE REQUIREMENTS:
- Speed priority: [real-time <2s/standard 2-10s/batch >10s acceptable]
- Budget constraints: [free tier only/low cost/moderate/premium acceptable]
- Volume: [one-off/moderate/high-volume usage]

TECHNICAL REQUIREMENTS:
- API access preferred: [specific providers, regions, compliance needs]
- Integration needs: [function calling, structured output, streaming]
- Fallback requirements: [backup options needed, redundancy level]

Based on these requirements, please provide:
1. Primary model recommendation with rationale
2. Alternative options with trade-offs
3. Cost estimate for expected usage
4. Implementation considerations
5. Quality assurance recommendations

Format your response with clear sections and practical next steps.
```

---

## 🔍 Quick Selection Templates

### For Code Generation
```
I need an LLM for code generation:
- Language: [Python/JavaScript/Java/etc.]
- Complexity: [simple scripts/complex algorithms/full applications]
- Code review needed: [yes/no]
- Budget: [free tier/cost-effective/premium]
- Speed: [real-time completion/standard development/batch processing]

Recommend the optimal model and explain why.
```

### For Content Creation
```
I need an LLM for content creation:
- Content type: [blog posts/marketing copy/technical docs/creative writing]
- Audience: [general/technical/business/academic]
- Length: [short form/long form/variable]
- Brand voice: [formal/casual/technical/creative]
- Fact-checking needs: [high accuracy required/general content]

Recommend the optimal model and explain the reasoning.
```

### For Research Tasks
```
I need an LLM for research:
- Research type: [current events/academic/market analysis/fact-checking]
- Real-time data needed: [yes/no]
- Sources required: [citations needed/general research]
- Depth: [overview/detailed analysis/comprehensive report]
- Time sensitivity: [breaking news/recent trends/historical analysis]

Recommend the optimal model and explain the capabilities.
```

### For Data Analysis
```
I need an LLM for data analysis:
- Data type: [numerical/text/mixed/large datasets]
- Analysis complexity: [descriptive/statistical/predictive/advanced]
- Visualization needs: [charts/graphs/dashboards]
- Audience: [technical/business/executive]
- Accuracy requirements: [high precision/general insights]

Recommend the optimal model and explain the analytical strengths.
```

---

## 🎮 Interactive Decision Tree

Use this step-by-step approach to narrow down your optimal model:

### Step 1: Task Category
**What is your primary task?**
- A) Code generation and programming assistance
- B) Content creation and writing
- C) Data analysis and insights
- D) Research and information gathering
- E) Complex reasoning and problem solving
- F) Conversational AI and support

### Step 2: Performance Priority
**What matters most for your use case?**
- A) Highest quality output (cost less important)
- B) Balanced quality and cost
- C) Lowest cost (acceptable quality)
- D) Fastest response time
- E) Largest context window
- F) Real-time/current information

### Step 3: Technical Requirements
**What technical capabilities do you need?**
- A) Text only
- B) Multimodal (images, audio)
- C) Function calling/tool use
- D) Structured output (JSON, code)
- E) Real-time web search
- F) Local deployment option

### Step 4: Usage Pattern
**How will you use this model?**
- A) One-off tasks
- B) Regular but low volume
- C) High volume production use
- D) Development and testing
- E) Mission-critical applications
- F) Experimental/research use

### Model Recommendations by Decision Path

#### A-A-A-A: Code + Quality + Text + One-off
**Primary**: GPT-4o or Claude 3.5 Sonnet
**Rationale**: Highest code quality, excellent for complex algorithms
**Cost**: $5-15 per 1M tokens

#### B-C-A-C: Content + Low Cost + Text + High Volume
**Primary**: Gemini 1.5 Flash or GPT-4o-mini
**Rationale**: Cost-effective content generation at scale
**Cost**: $0.075-0.60 per 1M tokens

#### D-F-E-B: Research + Real-time + Search + Regular Use
**Primary**: Perplexity Sonar or Gemini with Grounding
**Rationale**: Real-time search with current information
**Cost**: $1-5 per 1M tokens

---

## 🧪 Model Testing Framework

### Performance Testing Template
```
MODEL TESTING CHECKLIST

1. FUNCTIONALITY TEST:
   - [ ] Run representative task samples
   - [ ] Test edge cases and error handling
   - [ ] Verify output format compliance
   - [ ] Check response consistency

2. QUALITY ASSESSMENT:
   - [ ] Apply relevant reviewer prompts
   - [ ] Compare against quality thresholds
   - [ ] Test with domain-specific content
   - [ ] Validate accuracy for your use case

3. PERFORMANCE EVALUATION:
   - [ ] Measure actual response times
   - [ ] Test with realistic input sizes
   - [ ] Monitor rate limits and throttling
   - [ ] Assess cost per successful output

4. INTEGRATION TESTING:
   - [ ] Test API reliability and uptime
   - [ ] Verify error handling and fallbacks
   - [ ] Check authentication and security
   - [ ] Test with production-like load

5. COMPARATIVE ANALYSIS:
   - [ ] Test 2-3 alternative models
   - [ ] Compare cost-effectiveness
   - [ ] Evaluate quality differences
   - [ ] Document trade-offs and recommendations
```

### A/B Testing Protocol
```
A/B TESTING SETUP

PHASE 1: Baseline Establishment (Week 1)
- Current model: ________________
- Success metrics: ________________
- Quality baseline: ________________
- Cost baseline: ________________

PHASE 2: Alternative Testing (Week 2-3)
- Alternative model: ________________
- Same tasks and metrics
- Document differences
- User satisfaction comparison

PHASE 3: Decision Framework (Week 4)
- Cost-benefit analysis
- Quality comparison report
- Performance impact assessment
- Implementation recommendation

METRICS TO TRACK:
- Task completion rate
- Quality scores (using reviewer prompts)
- Response time distribution
- Cost per successful task
- User satisfaction ratings
- Error rates and fallback frequency
```

---

## 💡 Expert Selection Strategies

### Cost Optimization Strategy
```
BUDGET-CONSCIOUS MODEL SELECTION

1. START WITH FREE TIERS:
   - GitHub Models (GPT-4o, GPT-4o-mini)
   - Google AI Studio (Gemini 1.5 Flash)
   - Groq (Llama 3.1 models)

2. TIER-BASED ROUTING:
   - Simple tasks → Free/low-cost models
   - Complex tasks → Mid-tier models
   - Critical tasks → Premium models

3. VOLUME DISCOUNTS:
   - OpenAI: Batch API (50% savings)
   - Anthropic: Batch processing discounts
   - Consider annual commitments for high volume

4. COST MONITORING:
   - Set up usage alerts
   - Track cost per task type
   - Regular cost-benefit review
```

### Quality-First Strategy
```
QUALITY-FOCUSED MODEL SELECTION

1. TASK-SPECIFIC LEADERS:
   - Code: GPT-4o, Claude 3.5 Sonnet
   - Writing: Claude 3.5 Sonnet, GPT-4o
   - Reasoning: o1-preview, Claude 3.5 Sonnet
   - Research: Perplexity, Gemini with Search

2. QUALITY ASSURANCE:
   - Use reviewer prompts for evaluation
   - Implement quality gates (75+ score minimum)
   - Multi-model validation for critical tasks
   - Human review for edge cases

3. CONTINUOUS IMPROVEMENT:
   - Track quality trends over time
   - Update model selection based on performance
   - Regular comparative evaluations
   - User feedback integration
```

### Speed-Optimized Strategy
```
PERFORMANCE-FIRST MODEL SELECTION

1. LATENCY LEADERS:
   - Groq: 750+ tokens/second (Llama models)
   - Gemini 1.5 Flash: 80+ tokens/second
   - GPT-4o-mini: Fast and cost-effective

2. OPTIMIZATION TECHNIQUES:
   - Parallel processing where possible
   - Caching for repeated queries
   - Streaming responses for real-time apps
   - Smart context management

3. FALLBACK ARCHITECTURE:
   - Primary: Fastest model for task type
   - Secondary: Balanced speed/quality option
   - Emergency: Most reliable option available
```

---

## 🔄 Implementation Roadmap

### Phase 1: Model Selection (Week 1)
- [ ] Use selection prompt to identify optimal models
- [ ] Set up API access for chosen providers
- [ ] Configure basic authentication and rate limits
- [ ] Test basic functionality with sample tasks

### Phase 2: Quality Framework (Week 2)
- [ ] Implement relevant reviewer prompts
- [ ] Set up quality monitoring and scoring
- [ ] Configure quality gates and thresholds
- [ ] Test quality assessment automation

### Phase 3: Routing Logic (Week 3)
- [ ] Implement task classification
- [ ] Set up model routing based on requirements
- [ ] Configure fallback strategies
- [ ] Test end-to-end routing workflow

### Phase 4: Optimization (Week 4)
- [ ] Monitor performance and costs
- [ ] Optimize routing rules based on data
- [ ] Fine-tune quality thresholds
- [ ] Document lessons learned and best practices

### Phase 5: Production Deployment (Week 5+)
- [ ] Scale to production volume
- [ ] Implement comprehensive monitoring
- [ ] Set up alerting and incident response
- [ ] Continuous optimization and improvement

---

## 📊 Success Metrics

### Selection Accuracy
- **Target**: 95%+ optimal model selection
- **Measurement**: User satisfaction with recommendations
- **Review Frequency**: Weekly analysis of selection outcomes

### Cost Efficiency
- **Target**: 30%+ cost reduction vs. single premium model
- **Measurement**: Cost per successful task completion
- **Review Frequency**: Monthly cost analysis and optimization

### Quality Maintenance
- **Target**: 90%+ outputs meet quality thresholds
- **Measurement**: Automated quality scoring + human validation
- **Review Frequency**: Daily quality monitoring, weekly deep analysis

### Performance Reliability
- **Target**: <500ms routing decisions, 99.9% availability
- **Measurement**: Response time distribution, uptime monitoring
- **Review Frequency**: Real-time monitoring with daily reports

---

*Last updated: June 3, 2025*  
*Next review: July 1, 2025*