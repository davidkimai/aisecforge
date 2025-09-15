# Red Team Operations: Structure, Methodology & Execution Framework

This document outlines a comprehensive approach to structuring, executing, and documenting adversarial red team operations for AI systems, with specific focus on language models and generative AI security assessment.

## Foundational Framework

### Core Red Team Principles

Red team operations are guided by five core principles:

1. **Adversarial Mindset**: Adopting an attacker's perspective to identify vulnerabilities
2. **Structured Methodology**: Following systematic processes for comprehensive assessment
3. **Realistic Simulation**: Creating authentic attack scenarios that mirror real threats
4. **Evidence-Based Results**: Generating actionable, well-documented findings
5. **Ethical Operation**: Conducting testing within appropriate ethical and legal boundaries

### Red Team Objectives

Core goals that drive effective red team operations:

| Objective | Description | Implementation Approach | Success Indicators |
|-----------|-------------|------------------------|---------------------|
| Vulnerability Discovery | Identify security weaknesses | Systematic attack simulation | Number and severity of findings |
| Defense Evaluation | Assess control effectiveness | Control bypass testing | Defense effectiveness metrics |
| Risk Quantification | Measure security risk | Structured risk assessment | Evidence-based risk scores |
| Security Enhancement | Drive security improvements | Finding-based remediation | Security posture improvement |
| Threat Intelligence | Generate threat insights | Systematic attack analysis | Actionable threat information |

## Red Team Operational Structure

### 1. Team Composition

Optimal structure for effective red team operations:

| Role | Responsibilities | Expertise Requirements | Team Integration |
|------|------------------|------------------------|------------------|
| Red Team Lead | Overall operation coordination | Security leadership, AI expertise, testing methodology | Reports to security leadership, coordinates all team activities |
| AI Security Specialist | AI-specific attack execution | Deep AI security knowledge, model exploitation expertise | Works closely with lead on attack design, executes specialized attacks |
| Attack Engineer | Technical attack implementation | Programming skills, tool development, automation expertise | Develops custom tools, automates testing, implements attack chains |
| Documentation Specialist | Comprehensive finding documentation | Technical writing, evidence collection, risk assessment | Ensures complete documentation, contributes to risk assessment |
| Ethics Advisor | Ethical oversight | Ethics, legal requirements, responsible testing | Provides ethical guidance, ensures responsible testing |

### 2. Operational Models

Different approaches to red team implementation:

| Model | Description | Best For | Implementation Considerations |
|-------|-------------|----------|------------------------------|
| Dedicated Red Team | Permanent team focused exclusively on adversarial testing | Large organizations with critical AI deployments | Requires substantial resource commitment, develops specialized expertise |
| Rotating Membership | Core team with rotating specialists | Organizations with diverse AI deployments | Balances specialized expertise with fresh perspectives, requires good knowledge management |
| Tiger Team | Time-limited, focused red team operations | Specific security assessments, pre-release testing | Intensive resource usage for limited time, clear scoping essential |
| Purple Team | Combined offensive and defensive testing | Organizations prioritizing immediate remediation | Accelerates remediation cycle, may reduce finding independence |
| External Augmentation | Internal team supplemented by external experts | Organizations seeking independent validation | Combines internal knowledge with external perspectives, requires careful onboarding |

### 3. Operational Lifecycle

The complete lifecycle of red team activities:

| Phase | Description | Key Activities | Deliverables |
|-------|-------------|----------------|--------------|
| Planning | Operation preparation and design | Scope definition, threat modeling, attack planning | Test plan, threat model, rules of engagement |
| Reconnaissance | Information gathering and analysis | Target analysis, vulnerability research, capability mapping | Reconnaissance report, attack surface map |
| Execution | Active testing and exploitation | Vulnerability testing, attack chain execution, evidence collection | Testing logs, evidence documentation |
| Analysis | Finding examination and risk assessment | Vulnerability confirmation, impact assessment, risk quantification | Analysis report, risk assessment |
| Reporting | Communication of findings and recommendations | Report development, presentation preparation, remediation guidance | Comprehensive report, executive summary, remediation plan |
| Feedback | Post-operation learning and improvement | Methodology assessment, tool evaluation, process improvement | Lessons learned document, methodology enhancements |

## Methodology Framework

### 1. Threat Modeling

Structured approach to identifying relevant threats:

| Activity | Description | Methods | Outputs |
|----------|-------------|---------|---------|
| Threat Actor Profiling | Identify relevant adversaries | Actor capability analysis, motivation assessment | Threat actor profiles |
| Attack Scenario Development | Create realistic attack scenarios | Scenario workshop, historical analysis | Attack scenario catalog |
| Attack Vector Identification | Identify relevant attack vectors | Attack tree analysis, STRIDE methodology | Attack vector inventory |
| Impact Assessment | Evaluate potential attack impact | Business impact analysis, risk modeling | Impact assessment document |
| Threat Prioritization | Prioritize threats for testing | Risk-based prioritization, likelihood assessment | Prioritized threat list |

### 2. Attack Planning

Developing effective attack approaches:

| Activity | Description | Methods | Outputs |
|----------|-------------|---------|---------|
| Attack Strategy Development | Design overall attack approach | Strategy workshop, attack path mapping | Attack strategy document |
| Attack Vector Selection | Select specific vectors for testing | Vector prioritization, coverage analysis | Selected vector inventory |
| Attack Chain Design | Design multi-step attack sequences | Attack chain mapping, dependency analysis | Attack chain diagrams |
| Success Criteria Definition | Define what constitutes success | Criteria workshop, objective setting | Success criteria document |
| Resource Allocation | Assign resources to attack components | Resource planning, capability mapping | Resource allocation plan |

### 3. Execution Protocol

Standardized approach to test execution:

| Protocol Element | Description | Implementation | Documentation |
|------------------|-------------|----------------|---------------|
| Testing Sequence | Order and structure of test execution | Phased testing approach, dependency management | Test sequence document |
| Evidence Collection | Approach to gathering proof | Systematic evidence capture, chain of custody | Evidence collection guide |
| Finding Validation | Process for confirming findings | Validation methodology, confirmation testing | Validation protocol |
| Communication Protocol | Team communication during testing | Communication channels, status updates | Communication guide |
| Contingency Handling | Managing unexpected situations | Issue escalation, contingency protocols | Contingency playbook |

### 4. Documentation Standards

Requirements for comprehensive documentation:

| Documentation Element | Content Requirements | Format | Purpose |
|----------------------|---------------------|--------|---------|
| Finding Documentation | Detailed description of each vulnerability | Structured finding template | Comprehensive vulnerability record |
| Evidence Repository | Collected proof of vulnerabilities | Organized evidence storage | Substantiation of findings |
| Attack Narrative | Description of attack execution | Narrative document with evidence links | Contextual understanding of attacks |
| Risk Assessment | Evaluation of finding severity and impact | Structured risk assessment format | Prioritization guidance |
| Remediation Guidance | Recommendations for addressing findings | Actionable recommendation format | Security enhancement |

### 5. Reporting Framework

Structured approach to communicating results:

| Report Element | Content | Audience | Purpose |
|----------------|---------|----------|---------|
| Executive Summary | High-level findings and implications | Leadership, stakeholders | Strategic understanding |
| Technical Findings | Detailed vulnerability documentation | Security team, development | Technical remediation |
| Risk Assessment | Finding severity and impact analysis | Security leadership, risk management | Risk understanding and prioritization |
| Attack Narratives | Stories of successful attack chains | Security team, development | Attack understanding |
| Remediation Recommendations | Specific guidance for addressing findings | Security team, development | Security enhancement |

## Attack Vector Framework

### 1. Prompt Injection Vectors

Approaches for testing prompt injection vulnerabilities:

| Vector Category | Description | Testing Methodology | Success Criteria |
|-----------------|-------------|---------------------|-----------------|
| Direct Instruction Injection | Attempts to directly override system instructions | Multiple direct injection variants | System instruction override |
| Indirect Manipulation | Subtle manipulation to influence behavior | Progressive manipulation techniques | Behavior manipulation without direct injection |
| Context Manipulation | Using context to influence interpretation | Context building techniques | Context-driven behavior change |
| Format Exploitation | Using formatting to hide instructions | Format manipulation techniques | Format-based instruction hiding |
| Authority Impersonation | Impersonating system authorities | Authority persona techniques | Authority-based instruction override |

### 2. Content Policy Evasion Vectors

Approaches for testing content policy controls:

| Vector Category | Description | Testing Methodology | Success Criteria |
|-----------------|-------------|---------------------|-----------------|
| Content Obfuscation | Hiding prohibited content | Multiple obfuscation techniques | Successful policy bypass |
| Semantic Manipulation | Using alternative phrasing | Semantic equivalent testing | Policy bypass through meaning preservation |
| Context Reframing | Creating permissible contexts | Multiple reframing approaches | Context-based policy bypass |
| Token Manipulation | Manipulating tokenization | Token-level techniques | Tokenization-based bypass |
| Multi-Turn Evasion | Progressive policy boundary testing | Multi-turn interaction sequences | Progressive boundary erosion |

### 3. Information Extraction Vectors

Approaches for testing information protection:

| Vector Category | Description | Testing Methodology | Success Criteria |
|-----------------|-------------|---------------------|-----------------|
| System Instruction Extraction | Attempts to extract system prompts | Multiple extraction techniques | Successful prompt extraction |
| Training Data Extraction | Attempts to extract training data | Data extraction techniques | Successful data extraction |
| Parameter Inference | Attempts to infer model parameters | Inference techniques | Successful parameter inference |
| User Data Extraction | Attempts to extract user information | User data extraction techniques | Successful user data extraction |
| Cross-Conversation Leakage | Testing for cross-user information leakage | Cross-context testing | Successful information leakage |

### 4. Multimodal Attack Vectors

Approaches for testing across modalities:

| Vector Category | Description | Testing Methodology | Success Criteria |
|-----------------|-------------|---------------------|-----------------|
| Cross-Modal Injection | Using one modality to attack another | Cross-modal techniques | Successful cross-modal vulnerability |
| Modal Boundary Exploitation | Exploiting transitions between modalities | Boundary testing techniques | Successful boundary exploitation |
| Multi-Modal Chain Attacks | Using multiple modalities in attack chains | Multi-step chains | Successful chain execution |
| Modal Inconsistency Exploitation | Exploiting inconsistent handling across modalities | Inconsistency testing | Successful inconsistency exploitation |
| Hidden Modal Content | Hiding attack content in modal elements | Content hiding techniques | Successful hidden content execution |

## Practical Implementation

### 1. Attack Execution Process

Step-by-step process for effective attack execution:

| Process Step | Description | Key Activities | Documentation |
|--------------|-------------|----------------|--------------|
| Preparation | Setting up for attack execution | Environment preparation, tool setup | Preparation checklist |
| Initial Testing | First phase of attack execution | Basic vector testing, initial probing | Initial testing log |
| Vector Refinement | Refining attack approaches | Vector adaptation, approach tuning | Refinement notes |
| Full Execution | Complete attack execution | Full attack chain execution, evidence collection | Execution log, evidence repository |
| Finding Validation | Confirming successful findings | Reproducibility testing, validation checks | Validation documentation |
| Attack Extension | Extending successful attacks | Impact expansion, variant testing | Extension documentation |

### 2. Evidence Collection Framework

Systematic approach to gathering attack evidence:

| Evidence Type | Collection Method | Documentation Format | Chain of Custody |
|---------------|-------------------|---------------------|-----------------|
| Attack Inputs | Input logging | Input documentation template | Input repository with timestamps |
| Model Responses | Response capture | Response documentation template | Response repository with correlation to inputs |
| Attack Artifacts | Artifact preservation | Artifact documentation template | Artifact repository with metadata |
| Attack Flow | Process documentation | Attack flow documentation template | Flow repository with timestamps |
| Environmental Factors | Environment logging | Environment documentation template | Environment log with test correlation |

### 3. Finding Classification Framework

Structured approach to categorizing findings:

| Classification Element | Description | Categorization Approach | Implementation |
|------------------------|-------------|-------------------------|---------------|
| Vulnerability Type | Nature of the vulnerability | Standard taxonomy application | Type classification system |
| Severity Rating | Seriousness of the finding | Severity calculation framework | Severity rating system |
| Exploitation Difficulty | Challenge in exploiting the finding | Difficulty assessment methodology | Difficulty rating system |
| Attack Prerequisites | Requirements for successful exploitation | Prerequisite analysis framework | Prerequisite documentation system |
| Impact Classification | Nature and scope of potential impact | Impact assessment framework | Impact classification system |

### 4. Risk Assessment Methodology

Approach to evaluating the risk of findings:

| Assessment Element | Description | Calculation Approach | Documentation |
|--------------------|-------------|---------------------|--------------|
| Exploitation Likelihood | Probability of successful exploitation | Likelihood scoring methodology | Likelihood assessment document |
| Impact Severity | Seriousness of exploitation consequences | Impact scoring methodology | Impact assessment document |
| Attack Complexity | Difficulty of executing the attack | Complexity scoring methodology | Complexity assessment document |
| Affected Scope | Range of systems or users affected | Scope scoring methodology | Scope assessment document |
| Detection Difficulty | Challenge in detecting exploitation | Detection scoring methodology | Detection assessment document |

## Operational Examples

### Example 1: Prompt Injection Assessment

```
Operation: Systematic Prompt Injection Assessment

1. Operation Objective:
   Comprehensively evaluate the target model's resistance to prompt injection attacks

2. Attack Vectors Implemented:
   - Direct System Instruction Override (3 variants)
   - Role-Based Authority Manipulation (4 variants)
   - Context Window Poisoning (3 techniques)
   - Format-Based Instruction Hiding (5 techniques)
   - Multi-Turn Manipulation (3 scenarios)

3. Execution Methodology:
   - Initial baseline testing with standard vectors
   - Progressive refinement based on model responses
   - Chain development combining successful techniques
   - Variant testing to identify boundary conditions
   - Documentation of successful injection patterns

4. Key Findings:
   - Successfully achieved instruction override in 18/50 attempts
   - Identified consistent vulnerability to authority-based manipulation
   - Discovered format exploitation allowing consistent policy bypass
   - Mapped specific boundary conditions for successful injection
   - Identified multi-turn techniques with 65% success rate

5. Risk Assessment:
   - Severity: High (CVSS: 8.2)
   - Attack Prerequisites: Basic prompt engineering knowledge
   - Exploitation Difficulty: Low (successful with limited attempts)
   - Detection Difficulty: Moderate (some techniques leave behavioral signals)
   - Impact: Significant (enables policy bypass, information extraction)
```

### Example 2: Multi-Modal Attack Chain

```
Operation: Cross-Modal Attack Chain Assessment

1. Operation Objective:
   Evaluate the model's vulnerability to attacks spanning multiple modalities

2. Attack Chain Implemented:
   - Phase 1: Image-embedded text instruction (visual modality)
   - Phase 2: Context establishment based on image response (text modality)
   - Phase 3: Audio-based authority reinforcement (audio modality)
   - Phase 4: Code-embedded execution trigger (code modality)
   - Phase 5: Cross-modal policy bypass attempt (mixed modalities)

3. Execution Methodology:
   - Modality-specific baseline testing
   - Transition point identification
   - Cross-modal context preservation testing
   - Chain construction with optimal transition points
   - Full chain execution with evidence collection

4. Key Findings:
   - Successfully achieved end-to-end chain execution in 7/20 attempts
   - Identified critical vulnerability at image-text transition point
   - Discovered audio-based authority reinforcement increased success by 40%
   - Mapped specific format requirements for successful transitions
   - Identified defensive weakness in cross-modal context tracking

5. Risk Assessment:
   - Severity: High (CVSS: 8.7)
   - Attack Prerequisites: Multi-modal expertise, specialized tools
   - Exploitation Difficulty: Moderate (requires precise execution)
   - Detection Difficulty: High (crosses multiple monitoring domains)
   - Impact: Severe (enables sophisticated attacks difficult to detect)
```

## Adversarial Red Team Engagement Framework

### 1. Engagement Models

Different approaches to red team exercises:

| Engagement Model | Description | Best For | Implementation Considerations |
|------------------|-------------|----------|------------------------------|
| Announced Assessment | Organization is aware of testing | Initial assessments, control testing | More cooperative, may miss some detection issues |
| Unannounced Assessment | Organization unaware of specific timing | Testing detection capabilities | Requires careful coordination, additional safety measures |
| Continuous Assessment | Ongoing red team activities | Mature security programs | Requires dedicated resources, sophisticated testing rotation |
| Tabletop Exercise | Theoretical attack simulation | Preliminary assessment, training | Limited technical validation, good for education |
| Collaborative Exercise | Combined red/blue team activity | Defense enhancement focus | Accelerates remediation, may miss some findings |

### 2. Rules of Engagement

Framework for establishing testing boundaries:

| Element | Description | Documentation | Approval Process |
|---------|-------------|---------------|-----------------|
| Scope Boundaries | Defines included/excluded targets | Scope document | Security leadership approval |
| Acceptable Techniques | Permitted testing approaches | Technique inventory | Security and legal approval |
| Prohibited Actions | Explicitly forbidden activities | Prohibition list | Security and legal approval |
| Timeline Parameters | Testing timeframes and constraints | Timeline document | Operational leadership approval |
| Escalation Procedures | Process for handling issues | Escalation protocol | Cross-functional approval |

### 3. Communication Protocol

Structure for effective engagement communication:

| Communication Element | Purpose | Participants | Timing |
|-----------------------|---------|--------------|--------|
| Kickoff Meeting | Establish engagement parameters | Red team, security leadership | Prior to engagement |
| Status Updates | Provide progress information | Red team, engagement sponsor | Regular intervals during engagement |
| Critical Finding Notification | Alert to serious issues | Red team, security leadership | Immediately upon discovery |
| Engagement Conclusion | Formal end of active testing | Red team, security leadership | Upon completion of testing |
| Results Presentation | Communicate findings | Red team, stakeholders | Post-testing, prior to report |

### 4. Documentation Requirements

Comprehensive documentation for the engagement:

| Document | Content | Audience |