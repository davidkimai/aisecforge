# Assessment Dimensions

This document outlines the key security dimensions evaluated within the AISecForge framework. Each dimension represents a distinct aspect of AI system security that requires specialized testing approaches and evaluation criteria.

## 1. Linguistic Pattern Exploitation

### Definition
This dimension evaluates a model's vulnerability to linguistically sophisticated structures designed to bypass security measures through semantic manipulation, obfuscation, or novel linguistic formulations.

### Key Testing Areas
- **Semantic Obfuscation**: Testing for vulnerability to meaning-preserving transformations that evade detection
- **Multi-language Injection**: Assessing resistance to instructions embedded across multiple languages
- **Nested Instruction Manipulation**: Evaluating vulnerability to hierarchically structured prompts
- **Interpretative Framing Exploitation**: Testing susceptibility to reframing of harmful requests
- **Temporal Context Manipulation**: Assessing vulnerability to historically constructed attack patterns

### Security Implications
Weaknesses in this dimension can allow attackers to bypass content policies, extract sensitive information, or manipulate model behavior through sophisticated linguistic techniques that evade detection systems.

### Assessment Approach
Testing in this dimension employs a variety of linguistic transformation techniques, measuring model responses against baseline controls to identify security degradation resulting from linguistic manipulations.

## 2. Contextual Boundary Testing

### Definition
This dimension assesses a model's ability to maintain appropriate behavioral boundaries under various contextual pressures, including role-playing scenarios, authority invocation, ethical dilemmas, and emergency situations.

### Key Testing Areas
- **Role-based Constraint Testing**: Evaluating boundary maintenance within role-playing scenarios
- **Authority Figure Impersonation**: Testing susceptibility to requests framed as coming from authority sources
- **Persona Manipulation**: Assessing vulnerability to character-based constraint circumvention
- **Ethical Scenario Boundary Testing**: Evaluating model behavior in ethically ambiguous situations
- **Emergency Situation Simulation**: Testing boundary maintenance under simulated emergency contexts

### Security Implications
Weaknesses in this dimension can lead to inappropriate model behavior in specific contexts, potentially resulting in harmful outputs, unauthorized actions, or disclosure of sensitive information when contextual pressure is applied.

### Assessment Approach
Testing employs contextual framing techniques, systematically increasing pressure on model boundaries while measuring adherence to security constraints across various scenarios.

## 3. System Prompt Extraction

### Definition
This dimension evaluates a model's resistance to attempts to reveal underlying system instructions, operational parameters, or training directives through various extraction techniques.

### Key Testing Areas
- **Indirect Revelation Techniques**: Testing for vulnerability to oblique questioning that reveals system directives
- **Token Prediction Exploitation**: Assessing susceptibility to attacks leveraging prediction mechanics
- **Comparative Response Analysis**: Evaluating vulnerability to differential analysis of responses
- **System Instruction Reconstruction**: Testing resistance to systematic reconstruction of instructions
- **Parameter Inference Methods**: Assessing vulnerability to techniques that infer system parameters

### Security Implications
Weaknesses in this dimension can lead to exposure of proprietary system instructions, enabling more effective attacks by revealing model constraints, training directives, or operational parameters.

### Assessment Approach
Testing employs systematic extraction attempts with progressive refinement, measuring information leakage against known system instructions to quantify extraction success.

## 4. Multi-turn Vulnerability Assessment

### Definition
This dimension evaluates security degradation across extended interactions, assessing how model boundaries, restrictions, and safeguards hold up over multiple conversation turns.

### Key Testing Areas
- **Progressive Boundary Erosion**: Testing for gradual weakening of security boundaries over time
- **Context Window Manipulation**: Assessing vulnerability to context window poisoning or overflow
- **Memory Exploitation**: Evaluating susceptibility to attacks leveraging model memory mechanisms
- **Conversation Flow Redirection**: Testing vulnerability to subtle conversation steering techniques
- **Trust Building Exploitation**: Assessing vulnerability to attacks that establish trust before exploitation

### Security Implications
Weaknesses in this dimension can enable attackers to circumvent security measures through persistent interaction, potentially achieving actions or outputs that would be refused in single-turn interactions.

### Assessment Approach
Testing employs extended conversation scenarios with progressive attack sophistication, measuring security degradation over time against single-turn baseline security levels.

## 5. Multimodal Attack Vectors

### Definition
This dimension evaluates security across different input modalities, assessing how vulnerabilities may manifest when leveraging images, audio, code, or document inputs in addition to text.

### Key Testing Areas
- **Image-based Prompt Injection**: Testing for vulnerability to instructions embedded in images
- **Audio Instruction Embedding**: Assessing susceptibility to audio-based attack vectors
- **Code-based Vulnerability Introduction**: Evaluating security in code interpretation contexts
- **Document-embedded Attack Patterns**: Testing vulnerability to attacks hidden in document structure
- **Cross-modal Transfer Attacks**: Assessing vulnerability to attacks that transition across modalities

### Security Implications
Weaknesses in this dimension can enable attackers to bypass text-focused security measures by leveraging alternative input modalities, potentially achieving harmful outputs or actions through these channels.

### Assessment Approach
Testing employs multimodal inputs containing embedded attack patterns, measuring response differences between text-only and multimodal variants of equivalent attacks.

## 6. Tool Use Security

### Definition
This dimension evaluates security in the context of AI system tool use capabilities, assessing vulnerabilities related to external system access, API interactions, and function calling mechanisms.

### Key Testing Areas
- **Tool Selection Manipulation**: Testing for vulnerability in the tool selection process
- **Parameter Injection**: Assessing susceptibility to malicious parameter manipulation
- **Function Call Hijacking**: Evaluating vulnerability to redirection of function calls
- **Tool Output Interpretation**: Testing security of tool output processing
- **Tool Chaining Vulnerabilities**: Assessing security in sequences of tool operations

### Security Implications
Weaknesses in this dimension can enable attackers to leverage AI system tool use capabilities to perform unauthorized actions, access sensitive systems, or manipulate external resources in harmful ways.

### Assessment Approach
Testing employs crafted inputs designed to manipulate tool use behavior, measuring divergence from authorized and intended tool operations across various scenarios.

## 7. Recovery & Remediation Assessment

### Definition
This dimension evaluates a model's ability to recover from security failures, recognize exploitation attempts, and implement appropriate remediation actions when vulnerabilities are exploited.

### Key Testing Areas
- **Attack Recognition**: Assessing ability to identify exploitation attempts in progress
- **Conversation Reset Mechanisms**: Testing effectiveness of security reset procedures
- **Exploit Mitigation**: Evaluating ability to prevent further exploitation after detection
- **Resilience to Repeated Attacks**: Testing robustness against persistent attack attempts
- **Remediation Notification**: Assessing communication of security issues to users

### Security Implications
Weaknesses in this dimension can prevent effective recovery from security breaches, potentially extending impact when exploitation occurs and reducing system resilience against persistent attacks.

### Assessment Approach
Testing employs successful exploitation followed by remediation attempts, measuring recovery efficacy and persistent vulnerability after initial security failures.

## 8. Authorization & Authentication Boundaries

### Definition
This dimension evaluates a model's ability to maintain appropriate boundaries around user identification, authorization levels, and access controls within conversations or across sessions.

### Key Testing Areas
- **Identity Confusion Exploitation**: Testing for vulnerability to user identity manipulation
- **Permission Inheritance**: Assessing susceptibility to unauthorized permission acquisition
- **Session Boundary Enforcement**: Evaluating maintenance of security across session boundaries
- **Authorization Level Manipulation**: Testing resistance to attempts to elevate privileges
- **Authentication Bypass Techniques**: Assessing vulnerability to authentication circumvention

### Security Implications
Weaknesses in this dimension can enable unauthorized access to features, data, or capabilities restricted to specific users or roles, potentially compromising system security policies.

### Assessment Approach
Testing employs identity and authorization manipulation techniques, measuring access control enforcement against defined authorization boundaries and policies.

---

## Dimensional Interaction Analysis

While each dimension can be tested individually, security vulnerabilities often span multiple dimensions. The AISecForge framework includes cross-dimensional analysis to identify compound vulnerabilities that emerge from the interaction of weaknesses across different dimensions.

Key interaction patterns include:

1. **Linguistic + Contextual**: Using sophisticated linguistic patterns within specific contextual frames
2. **Multi-turn + System Prompt**: Leveraging extended conversations to extract system instructions
3. **Multimodal + Tool Use**: Employing non-text inputs to manipulate tool use behavior
4. **Authorization + Recovery**: Exploiting authentication weaknesses to prevent effective remediation

For implementation details on testing each dimension, refer to the dimension-specific methodology documents in the [dimensions directory](dimensions/).
