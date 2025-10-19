# AISecForge: AI Security Resources
## [Docs](https://github.com/davidkimai/aisecforge/blob/main/POLICY.md)
> **IMPORTANT**: This repository is intended for legitimate security research and AI safety advancement. All methodologies documented herein are for ethical research purposes only.


<div align="center">



![Status](https://img.shields.io/badge/Status-Security-crimson) [![License: PolyForm NC](https://img.shields.io/badge/License-PolyForm-lime.svg)](https://polyformproject.org/licenses/noncommercial/1.0.0/) [![LICENSE: CC BY-NC-ND 4.0](https://img.shields.io/badge/Content-CC--BY--NC--ND-turquoise.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/) ![Version](https://img.shields.io/badge/Version-0.1.0--alpha-purple)



</div>


AISecForge is an open-source resource for systematic adversarial testing, evaluation, and security hardening of large language models. This repository consolidates novel methodologies for identifying, classifying, and mitigating security vulnerabilities in frontier AI systems.

## Core Capabilities

- **Systematic Vulnerability Assessment**: Structured methodologies for comprehensive security testing across model capabilities
- **Adversarial Attack Taxonomy**: Multi-dimensional classification of attack vectors, exploitation techniques, and vulnerability patterns
- **Cross-Model Benchmarking**: Standardized evaluation protocols enabling comparative security analysis across different AI systems
- **Defense Strategy Development**: Research-backed approaches to mitigating identified vulnerabilities
- **Governance & Compliance**: Frameworks for responsible testing, disclosure, and security policy development

## Key Components
### Assessment Framework
Our hierarchical model security assessment framework enables systematic evaluation of AI systems across multiple security dimensions:

- Input manipulation resistance
- Output supervision integrity
- Instruction boundary enforcement
- Contextual security awareness
- Multi-turn conversation security
- Tool-use vulnerability assessment

### Vulnerability Taxonomy
We provide a comprehensive classification system for AI security vulnerabilities, including:

- Prompt injection vectors
- Context manipulation techniques
- Response extraction methodologies
- Classifier evasion strategies
- Tool-use exploitation patterns
- Authentication boundary violations

### Testing Methodologies
Structured approaches to security testing, including:

- Deterministic pattern testing
- Probabilistic attack generation
- Adaptive testing workflows
- Cross-domain transfer testing
- Multimodal security evaluation
- Long-term interaction assessment

## Security Notice

This repository is designed for legitimate security research and defensive purposes only. All techniques are documented with appropriate safeguards and are intended for authorized testing environments. Contributors and users must adhere to our [Code of Conduct](CODE_OF_CONDUCT.md) and [Responsible Disclosure Policy](docs/governance/disclosure.md).

## Looking to Contribute?

We're actively seeking contributors with expertise in:

- AI security assessment
- Red team operations
- Linguistic security analysis
- Adversarial machine learning
- Security policy development
- Responsible disclosure practices

See our [Contributing Guidelines](CONTRIBUTING.md) for more information on how to get involved.

Key Framework Components
Assessment Architecture
Our hierarchical model security assessment framework enables systematic evaluation of frontier AI systems across multiple security dimensions:


## Key Framework Components

### Assessment Architecture

Our hierarchical model security assessment framework enables systematic evaluation of frontier AI systems across multiple security dimensions:

- **Input Manipulation Resistance**: Measuring model resilience against sophisticated prompt engineering attempts
- **Output Supervision Integrity**: Evaluating consistency of safety mechanisms across diverse scenarios
- **Instruction Boundary Enforcement**: Testing adherence to stated capabilities and restrictions
- **Contextual Security Awareness**: Assessing model's ability to maintain security posture across shifting contexts
- **Conversation Security**: Analyzing vulnerability emergence in multi-turn interactions
- **Tool-Use Security**: Evaluating controlled function execution and parameter validation

### Vulnerability Taxonomy

We provide a comprehensive classification system for AI security vulnerabilities, organized into a hierarchical structure:

- **VCPI**: Vector-Capability-Pattern-Instance framework for organizing vulnerability classes
- **Multi-dimensional Scoring**: Severity metrics considering exploitation difficulty, impact scope, and mitigation complexity
- **Cross-Model Applicability**: Taxonomy designed to apply across model architectures and capability profiles
- **Evolution Tracking**: Framework for monitoring vulnerability mutations and adaptation patterns

### Security Benchmark Suite

The framework includes standardized benchmarking tools designed to evaluate security posture with reproducible metrics:

- **Refusal Reliability Index (RRI)**: Measures consistency in refusing inappropriate requests across contextual variations
- **Boundary Enforcement Quotient (BEQ)**: Assesses ability to maintain restrictions around capabilities
- **Information Protection Factor (IPF)**: Evaluates resistance to extraction of sensitive information
- **Classifier Evasion Resistance (CER)**: Measures robustness against classifier circumvention techniques
- **Multimodal Security Integration (MSI)**: Assesses consistency across different input and output modalities

## Implementation Examples

Our framework has been applied to analyze security characteristics across several representative frontier models (specific details redacted in public repo):

| Security Dimension | Baseline Models | Advanced Models | Frontier Models |
|-------------------|-----------------|-----------------|-----------------|
| Input Manipulation Resistance | 68.3 | 82.7 | 91.4 |
| Output Supervision Integrity | 72.1 | 79.2 | 88.9 |
| Instruction Boundary Enforcement | 65.4 | 78.1 | 89.6 |
| Contextual Security Awareness | 57.8 | 73.5 | 84.3 |
| Conversation Security | 53.6 | 71.2 | 82.7 |
| Tool-Use Security | 61.9 | 76.8 | 87.2 |

*For detailed methodology and expanded benchmark results, see [benchmark documentation](./frameworks/benchmarking/README.md).*

## Responsible Disclosure Framework

AISecForge includes a structured framework for responsible disclosure of LLM vulnerabilities:

- **Standardized Reporting Protocols**: Templates and workflows for communicating vulnerabilities
- **Severity Classification System**: Objective criteria for prioritizing remediation efforts
- **Coordinated Disclosure Timelines**: Guidelines for balancing security and transparency
- **Bounty Program Framework**: Structure for recognizing and rewarding responsible disclosure

## Who Should Use AISecForge?

- **AI Security Researchers**: For systematic vulnerability assessment and classification
- **LLM Developers**: For comprehensive security evaluation during development lifecycle
- **Red Teams**: For structured adversarial testing frameworks and methodologies
- **AI Governance Specialists**: For policy development and compliance validation
- **Academic Researchers**: For reproducible security experimentation and publishing

## Current Research Focus

Our ongoing research is exploring several critical areas in LLM security:

- **Multimodal Attack Surface Analysis**: Exploring security implications of cross-modal reasoning
- **Emergent Capability Assessment**: Methodologies for testing security of emergent model behaviors
- **Adversarial Robustness Metrics**: Developing quantitative measures for security hardening
- **Cross-Architectural Vulnerability Patterns**: Identifying security principles that transcend specific implementations
- **Defense-in-Depth Strategies**: Layered approaches to mitigating complex attack vectors



---

## Methodology Documentation

> **Note:** Due to proprietary collaboration protocols and active NDA agreements with institutional partners, full vector methodologies and red team toolkits are only available via private governance channels.


# LLM Adversarial Testing Methodology

This document outlines our structured approach to adversarial testing of large language models, designed to systematically identify and categorize vulnerabilities across multiple security dimensions.

## Core Principles

Our methodology is guided by four core principles:

1. **Systematic Coverage**: Testing across all model functionalities, capabilities, and potential attack surfaces
2. **Defense-in-Depth**: Layered testing approaches that examine resistance to increasingly sophisticated attacks
3. **Reproducibility**: Standardized procedures ensuring consistent evaluation across different models and versions
4. **Responsible Disclosure**: Clear protocols for handling and reporting discovered vulnerabilities

## Testing Dimensions

### 1. Linguistic Pattern Exploitation

Evaluating model vulnerability to sophisticated linguistic structures that can bypass security measures:

### 2. Contextual Boundary Testing

Assessing model abilities to maintain appropriate boundaries under various contextual pressures:

- Role-based constraint testing
- Ethical scenario boundary testing


### 3. System Prompt Extraction

Testing model resistance to attempts to reveal underlying system instructions:

- Indirect revelation techniques
- Comparative response analysis



### 4. Multi-turn Vulnerability Assessment

Evaluating security degradation across extended interactions:

- Context window manipulation
- Conversation redirection


### 5. Multimodal Attack Vectors

Testing security across different input modalities:

- Code-based vulnerability introduction
- Document-embedded attack patterns
- Cross-modal transfer attacks

## Assessment Process

Our standardized assessment process consists of the following phases:

1. **Capability Mapping**: Determining model features, limitations, and potential attack surfaces
2. **Vulnerability Hypothesis**: Developing theories about potential security weaknesses
3. **Test Development**: Creating structured test cases based on hypothesized vulnerabilities
4. **Execution**: Implementing tests according to standardized protocols
5. **Analysis**: Evaluating results to confirm vulnerabilities and assess severity
6. **Documentation**: Comprehensive recording of findings, methodologies, and evidence
7. **Remediation Development**: Creating mitigation strategies for identified vulnerabilities

## Scoring Framework

Vulnerabilities are scored using our proprietary VALS (Vulnerability Assessment for Language Systems) framework, which considers:

- Attack complexity
- Authentication bypass severity
- Information disclosure impact
- Policy violation potential
- Exploitation reliability
- Defense evasion sophistication

## Ethical Considerations

All testing must adhere to the following ethical guidelines:

- Testing must occur in isolated, controlled environments
- No exposure of vulnerable models to the public
- Responsible disclosure to model developers before publication
- Focus on defensive improvements rather than exploitation
- Prohibition of techniques that could cause broader harm

For detailed implementation guidelines for each testing dimension, refer to the corresponding subdirectories within this methodology section.


## Framework for AI Security Risk Benchmarking


# AI Security Risk Assessment Framework

This framework establishes standardized metrics and evaluation protocols for assessing security risks in large language models. Its primary goal is to create a consistent benchmark that enables comparative analysis across different models and versions.

## Core Assessment Dimensions

### 1. Refusal Reliability Index (RRI)

Measures a model's consistency in refusing inappropriate requests across various contextual framing techniques.

**Scoring Methodology:**
- **Level 1**: Basic direct request refusal
- **Level 2**: Semantic variation resistance
- **Level 3**: Context manipulation resistance
- **Level 4**: Multi-turn manipulation resistance
- **Level 5**: Cross-domain transfer resistance

### 2. Boundary Enforcement Quotient (BEQ)

Assesses a model's ability to maintain appropriate boundaries around restricted capabilities.

**Scoring Methodology:**
- **Level 1**: Clear violation boundary enforcement
- **Level 2**: Indirect instruction boundary enforcement
- **Level 3**: Role-play boundary maintenance
- **Level 4**: Hypothetical scenario boundary control
- **Level 5**: Creative content boundary adherence

### 3. Information Protection Factor (IPF)

Evaluates a model's resistance to attempts to extract sensitive information from its training or system instructions.

**Scoring Methodology:**
- **Level 1**: Direct extraction resistance
- **Level 2**: Indirect elicitation resistance
- **Level 3**: System prompt protection
- **Level 4**: Training data protection
- **Level 5**: Parameter inference resistance

### 4. Classifier Evasion Resistance (CER)

Measures a model's robustness against techniques designed to bypass content classifiers.

**Scoring Methodology:**
- **Level 1**: Basic obfuscation resistance
- **Level 2**: Encoding technique resistance
- **Level 3**: Language transfer resistance
- **Level 4**: Concept fragmentation resistance
- **Level 5**: Adaptive evasion resistance

### 5. Multimodal Security Integration (MSI)

Assesses security consistency across different input and output modalities.

**Scoring Methodology:**
- **Level 1**: Text-based security consistency
- **Level 2**: Image interpretation security
- **Level 3**: Code generation/interpretation security
- **Level 4**: Document processing security
- **Level 5**: Cross-modal transfer security

## Composite Risk Scores

Our framework combines individual dimension scores to produce the following composite metrics:

### Overall Security Posture (OSP)

A weighted average of all security dimensions, providing a single metric for overall model security.

### Vulnerability Profile (VP)

A visualization of scores across all dimensions, highlighting relative strengths and weaknesses.

### Delta Security Analysis (DSA)

Comparative metrics showing security improvements or regressions between model versions.

## Implementation Protocol

The implementation of this framework follows a standardized four-phase process:

1. **Preparation**: Configuration of testing environment and baseline establishment
2. **Execution**: Systematic implementation of test cases across all dimensions
3. **Analysis**: Scoring and evaluation of results according to standardized metrics
4. **Reporting**: Generation of comprehensive security assessment reports

## Benchmark Versioning

This framework follows semantic versioning principles:

- **Major versions**: Fundamental changes to assessment dimensions
- **Minor versions**: Addition of new testing methodologies or scoring adjustments
- **Patch versions**: Refinements to existing tests or documentation

For detailed implementation guidelines, including specific test cases for each dimension, refer to the associated subdirectories within this section.


## Vulnerability Taxonomy & Classification System


# AI Model Vulnerability Taxonomy

This taxonomy provides a comprehensive classification system for vulnerabilities in large language models, enabling systematic identification, documentation, and mitigation of security risks.

## Primary Vulnerability Classes

### 1. Prompt Injection Vulnerabilities

Vulnerabilities that allow attackers to insert instructions that override or modify the model's intended behavior.

#### Subclasses:

- **1.1 Direct Instruction Injection**
  - 1.1.1 System prompt override
  - 1.1.2 Role reassignment
  - 1.1.3 Constraint removal
  
- **1.2 Indirect Instruction Manipulation**
  - 1.2.1 Contextual reframing
  - 1.2.2 Hypothetical scenario exploitation
  - 1.2.3 Embedded instruction patterns
  
- **1.3 Cross-Context Injection**
  - 1.3.1 Documentation exploitation
  - 1.3.2 Example manipulation
  - 1.3.3 Error message injection

### 2. Boundary Enforcement Failures

Vulnerabilities in the model's ability to maintain appropriate boundaries around restricted content or capabilities.

#### Subclasses:

- **2.1 Content Policy Circumvention**
  - 2.1.1 Semantic obfuscation
  - 2.1.2 Context manipulation
  - 2.1.3 Progressive desensitization
  
- **2.2 Capability Restriction Bypass**
  - 2.2.1 Function simulation
  - 2.2.2 Capability rediscovery
  - 2.2.3 Permission escalation
  
- **2.3 Authorization Boundary Violations**
  - 2.3.1 Identity confusion
  - 2.3.2 Permission inheritance
  - 2.3.3 Context window contamination

### 3. Information Extraction Vulnerabilities

Vulnerabilities that enable the extraction of sensitive information from the model.

#### Subclasses:

- **3.1 Training Data Extraction**
  - 3.1.1 Specific content elicitation
  - 3.1.2 Pattern completion exploitation
  - 3.1.3 Statistical inference attacks
  
- **3.2 System Instruction Leakage**
  - 3.2.1 Direct instruction probing
  - 3.2.2 Behavior-based inference
  - 3.2.3 Error message analysis
  
- **3.3 Parameter Inference**
  - 3.3.1 Decision boundary mapping
  - 3.3.2 Threshold determination
  - 3.3.3 Model capability profiling

### 4. Classifier Evasion Techniques

Methods that bypass content filtering and safety classification systems.

#### Subclasses:

- **4.1 Linguistic Obfuscation**
  - 4.1.1 Homoglyph substitution
  - 4.1.2 Semantic equivalent substitution
  - 4.1.3 Syntactic fragmentation
  
- **4.2 Context Manipulation**
  - 4.2.1 Benign context framing
  - 4.2.2 Educational purpose claiming
  - 4.2.3 Fictional scenario creation
  
- **4.3 Technical Bypass Methods**
  - 4.3.1 Token boundary exploitation
  - 4.3.2 Embedding collision techniques
  - 4.3.3 Adversarial perturbation injection

### 5. Multimodal Vulnerability Vectors

Security weaknesses related to the interaction between different input or output modalities.

#### Subclasses:

- **5.1 Cross-Modal Injection**
  - 5.1.1 Image-embedded instructions
  - 5.1.2 Audio-based instruction injection
  - 5.1.3 Document-embedded attacks
  
- **5.2 Modal Interpretation Conflicts**
  - 5.2.1 Text-image inconsistency exploitation
  - 5.2.2 Code-text boundary confusion
  - 5.2.3 Multi-source instruction conflicts
  
- **5.3 Modal Translation Vulnerabilities**
  - 5.3.1 OCR manipulation techniques
  - 5.3.2 Image description exploitation
  - 5.3.3 Code interpretation manipulation

## Severity Classification

Each vulnerability is assigned a severity rating based on the following criteria:

### Impact Dimensions:
- **Scope**: Single request, conversation, or system-wide
- **Persistence**: Temporary, session-long, or persistent
- **Discoverability**: Requires expertise, moderately discoverable, or easily found
- **Reproducibility**: Intermittent, requires specific conditions, or consistently reproducible
- **Mitigation Complexity**: Simple fix, moderate complexity, or fundamental redesign required

### Severity Levels:
- **Critical**: High impact across multiple dimensions, requiring immediate mitigation
- **High**: Significant impact in key dimensions, prioritized for rapid remediation
- **Medium**: Moderate impact with reasonable mitigation pathways
- **Low**: Limited impact with straightforward mitigation options
- **Informational**: Minimal direct impact but indicates potential future vulnerabilities

## Classification Methodology

The process for classifying vulnerabilities follows these steps:

1. **Identification**: Initial discovery and documentation of the vulnerability
2. **Characterization**: Determining the primary vulnerability class and subclass
3. **Impact Assessment**: Evaluation across all impact dimensions
4. **Severity Assignment**: Determination of overall severity level
5. **Mitigation Association**: Linking to appropriate mitigation strategies

For detailed examples of each vulnerability class and subclass, refer to the case studies directory within this taxonomy section.


## Responsible Disclosure Framework


# AI Model Security Bounty Program & Disclosure Framework

This framework establishes standards for responsible disclosure of security vulnerabilities in large language models and provides a structured approach for implementing AI security bounty programs.

## Core Principles

Our responsible disclosure framework is built on the following principles:

1. **Minimize Harm**: Preventing exposure of vulnerabilities before appropriate mitigations are in place
2. **Recognize Contributors**: Acknowledging security researchers who responsibly disclose vulnerabilities
3. **Transparency**: Providing clear guidelines and expectations for all parties involved
4. **Continuous Improvement**: Using vulnerability reports to enhance overall security posture

## Vulnerability Disclosure Process

### For Security Researchers

#### 1. Discovery & Documentation
- Verify the vulnerability in a controlled environment
- Document the issue with clear reproduction steps
- Capture evidence of the vulnerability (logs, screenshots, etc.)
- Avoid unnecessary exposure of the vulnerability

#### 2. Initial Report Submission
- Submit report through the designated secure channel
- Include all relevant technical details
- Avoid public disclosure prior to remediation
- Provide contact information for follow-up communication

#### 3. Collaboration During Remediation
- Respond to requests for additional information
- Test proposed fixes if requested and feasible
- Maintain confidentiality until authorized disclosure
- Discuss appropriate timelines for public disclosure

#### 4. Post-Remediation Activities
- Coordinate public disclosure timing with the security team
- Receive acknowledgment for the contribution
- Collect any applicable rewards
- Participate in case study development when appropriate

### For AI Development Teams

#### 1. Report Receipt & Triage
- Acknowledge receipt within 24 hours
- Assign severity and priority levels
- Designate a primary contact for the researcher
- Begin initial investigation to validate the report

#### 2. Investigation & Remediation
- Thoroughly assess the vulnerability and its implications
- Develop and test appropriate mitigations
- Communicate progress updates to the reporter
- Establish clear timelines for deployment of fixes

#### 3. Disclosure Coordination
- Work with the researcher on appropriate disclosure timing
- Prepare technical documentation of the vulnerability
- Develop communications for potentially affected users
- Plan for deployment of the fix across all affected systems

#### 4. Post-Incident Activities
- Process any bounty rewards
- Document lessons learned
- Update testing procedures to catch similar issues
- Acknowledge the researcher's contribution

## Bounty Program Structure

### Eligibility Guidelines

#### In-Scope Vulnerabilities
- Prompt injection vulnerabilities
- Content policy bypass techniques
- System instruction extraction methods
- Training data extraction techniques
- Authentication and authorization bypasses
- Security classifier evasion methods

#### Out-of-Scope Items
- Hypothetical vulnerabilities without proof of concept
- Vulnerabilities already reported or publicly known
- Issues in third-party integrations not controlled by the AI provider
- Content policy violations not resulting from security bypasses
- Poor user experience issues without security implications

### Reward Structure

Rewards should be structured based on the following considerations:

#### Impact Factors
- Severity of the vulnerability
- Potential for harm or misuse
- Affected user population
- Ease of exploitation
- Novel discovery vs. variant of known issue

#### Reward Tiers
- **Critical**: Major security issues with broad impact
- **High**: Significant issues affecting core security properties
- **Medium**: Important issues with limited scope or exploitation difficulty
- **Low**: Minor issues with minimal impact or highly specific conditions
- **Honorable Mention**: Valid issues that don't qualify for monetary rewards

### Disclosure Timeline

The standard disclosure timeline follows these phases:

1. **Initial Response**: Within 24 hours of report receipt
2. **Validation**: Within 5 business days
3. **Remediation Planning**: Within 10 business days for valid reports
4. **Fix Implementation**: Timeline based on severity and complexity
   - Critical: 15 calendar days target
   - High: 30 calendar days target
   - Medium: 60 calendar days target
   - Low: 90 calendar days target
5. **Public Disclosure**: Coordinated between 30-90 days after fix deployment

## Implementation Guidelines

Organizations implementing this framework should develop the following components:

1. **Secure Reporting Channel**: Encrypted submission portal or email
2. **Triage Team**: Designated responders for initial assessment
3. **Remediation Process**: Clear workflow for addressing valid reports
4. **Reward System**: Transparent criteria and payment mechanisms
5. **Communication Templates**: Standardized responses for different scenarios
6. **Legal Safe Harbor**: Protection for good-faith security research
7. **Documentation System**: Record-keeping for all vulnerability reports

For detailed implementation resources, including policy templates and communication examples, refer to the additional documentation within this section.


This repository represents a comprehensive framework for AI security testing and vulnerability assessment. It provides valuable resources for organizations looking to enhance their AI security posture.

The content is educational and focused on responsible security practices, exploring frontier expertise in the field of AI security testing. The framework provides a systematic approach to identifying vulnerabilities for AI Adversarial Security purposes.
