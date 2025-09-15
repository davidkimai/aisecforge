# Vulnerability Classification Framework

This document provides a standardized system for classifying vulnerabilities identified during LLM security testing. This classification framework enables consistent categorization, facilitates trend analysis, and supports effective remediation prioritization.

## Classification Dimensions

Vulnerabilities are classified across multiple dimensions to capture their full nature and impact.

### 1. Vulnerability Class

The primary categorization based on the fundamental mechanism of the vulnerability.

#### Primary Classes

- **PJV**: Prompt Injection Vulnerabilities
- **BEF**: Boundary Enforcement Failures
- **IEV**: Information Extraction Vulnerabilities
- **CET**: Classifier Evasion Techniques
- **MVV**: Multimodal Vulnerability Vectors
- **TUV**: Tool Use Vulnerabilities
- **ACF**: Authentication Control Failures
- **RSV**: Response Synthesis Vulnerabilities

### 2. Subclass

Specific subcategory within the primary vulnerability class.

#### Example Subclasses (for PJV - Prompt Injection Vulnerabilities)

- **PJV-DIR**: Direct Instruction Injection
- **PJV-IND**: Indirect Instruction Manipulation
- **PJV-CRX**: Cross-Context Injection

#### Example Subclasses (for BEF - Boundary Enforcement Failures)

- **BEF-CPC**: Content Policy Circumvention
- **BEF-CRB**: Capability Restriction Bypass
- **BEF-ABV**: Authorization Boundary Violations

#### Example Subclasses (for IEV - Information Extraction Vulnerabilities)

- **IEV-TDE**: Training Data Extraction
- **IEV-SIL**: System Instruction Leakage
- **IEV-PAI**: Parameter Inference

#### Example Subclasses (for CET - Classifier Evasion Techniques)

- **CET-LOB**: Linguistic Obfuscation
- **CET-CTM**: Context Manipulation
- **CET-TBM**: Technical Bypass Methods

#### Example Subclasses (for MVV - Multimodal Vulnerability Vectors)

- **MVV-CMI**: Cross-Modal Injection
- **MVV-MIC**: Modal Interpretation Conflicts
- **MVV-MTV**: Modal Translation Vulnerabilities

#### Example Subclasses (for TUV - Tool Use Vulnerabilities)

- **TUV-TSM**: Tool Selection Manipulation
- **TUV-PAI**: Parameter Injection
- **TUV-FCH**: Function Call Hijacking

#### Example Subclasses (for ACF - Authentication Control Failures)

- **ACF-ICE**: Identity Confusion Exploitation
- **ACF-PIE**: Permission Inheritance Exploitation
- **ACF-SBV**: Session Boundary Violations

#### Example Subclasses (for RSV - Response Synthesis Vulnerabilities)

- **RSV-MET**: Metadata Manipulation
- **RSV-CMH**: Content Moderation Hallucination
- **RSV-USP**: Unsafe Synthesis Patterns

### 3. Attack Vector

The primary method or channel through which the vulnerability is exploited.

#### Categories

- **TXT**: Text-Based
- **IMG**: Image-Based
- **AUD**: Audio-Based
- **COD**: Code-Based
- **DOC**: Document-Based
- **MUL**: Multi-Vector
- **API**: API-Based
- **TOL**: Tool-Based

### 4. Impact Type

The primary negative impact resulting from successful exploitation.

#### Categories

- **DIS**: Disclosure of Sensitive Information
- **POL**: Policy Violation
- **BYP**: Security Bypass
- **MAN**: System Manipulation
- **ACC**: Unauthorized Access
- **DEG**: Service Degradation
- **HAL**: Harmful Output Generation
- **PRV**: Privacy Violation

### 5. Exploitation Complexity

The level of technical expertise required to successfully exploit the vulnerability.

#### Categories

- **ECL**: Low (simple, requires minimal expertise)
- **ECM**: Medium (moderate complexity, requires some domain knowledge)
- **ECH**: High (complex, requires specialized knowledge)
- **ECX**: Very High (sophisticated, requires expert-level understanding)

### 6. Remediation Complexity

The estimated complexity of implementing an effective remediation.

#### Categories

- **RCL**: Low (simple fix, localized change)
- **RCM**: Medium (moderate complexity, potential side effects)
- **RCH**: High (complex, requires significant architectural changes)
- **RCX**: Very High (extremely difficult, may require fundamental redesign)

### 7. Discovery Method

How the vulnerability was discovered.

#### Categories

- **AUT**: Automated Testing
- **MAN**: Manual Testing
- **HYB**: Hybrid Approach
- **USR**: User Report
- **RES**: Research Finding
- **ANA**: Log Analysis
- **INC**: Incident Response

### 8. Status

The current state of the vulnerability.

#### Categories

- **NEW**: Newly Identified
- **CNF**: Confirmed
- **REJ**: Rejected (not a valid vulnerability)
- **MIT**: Mitigated (temporary solution)
- **FIX**: Fixed (permanent solution)
- **DUP**: Duplicate of existing vulnerability
- **DEF**: Deferred (not prioritized for immediate fix)

## Composite Classification

Vulnerabilities are assigned a composite classification code combining the above dimensions:

```
[Vulnerability Class]-[Subclass]:[Attack Vector]/[Impact Type]-[Exploitation Complexity][Remediation Complexity]-[Discovery Method].[Status]
```

### Example Classifications

- `PJV-DIR:TXT/POL-ECL-RCM-MAN.CNF`: A confirmed direct prompt injection vulnerability, text-based, leading to policy violations, low exploitation complexity, medium remediation complexity, discovered through manual testing.

- `IEV-SIL:COD/DIS-ECM-RCH-AUT.NEW`: A newly identified system instruction leakage vulnerability, code-based, leading to disclosure of sensitive information, medium exploitation complexity, high remediation complexity, discovered through automated testing.

- `MVV-CMI:IMG/BYP-ECH-RCM-HYB.MIT`: A mitigated cross-modal injection vulnerability, image-based, leading to security bypass, high exploitation complexity, medium remediation complexity, discovered through a hybrid testing approach.

## Classification Workflow

### 1. Initial Classification

When a potential vulnerability is first identified:

1. Assign primary vulnerability class and subclass
2. Document attack vector and impact type
3. Note discovery method
4. Set status to `NEW`
5. Estimation of exploitation complexity may be preliminary

### 2. Verification

During the verification phase:

1. Confirm vulnerability through reproduction
2. Refine classification based on deeper understanding
3. Update exploitation complexity based on reproduction experience
4. Change status to `CNF` or `REJ`

### 3. Analysis

During detailed analysis:

1. Assess remediation complexity
2. Document dependencies and affected components
3. Update classification with complete understanding
4. Link to related vulnerabilities if applicable

### 4. Remediation Tracking

During the remediation process:

1. Update status as appropriate
2. Document mitigation or fix approaches
3. Link to verification testing results

## Taxonomic Evolution

This classification system is designed to evolve over time as new vulnerability classes emerge. The process for extending the taxonomy includes:

1. **Identification**: Recognition of a new vulnerability pattern that doesn't fit existing classes
2. **Definition**: Clear description of the new vulnerability class or subclass
3. **Consultation**: Review with security experts to validate the new category
4. **Integration**: Addition to the formal taxonomy with appropriate documentation
5. **Retroactive Analysis**: Review of existing vulnerabilities to identify any that should be reclassified

## Usage Guidelines

### For Testers

- Assign preliminary classifications during testing
- Document all observed behaviors clearly to enable accurate classification
- Highlight unusual patterns that may indicate new vulnerability classes

### For Security Analysts

- Verify and refine classifications
- Ensure consistency across similar vulnerabilities
- Identify patterns and trends within vulnerability classes

### For Developers

- Use classification to understand vulnerability mechanisms
- Reference similar vulnerabilities by class to inform remediation approaches
- Track remediation effectiveness by vulnerability class

## Reporting Standards

All vulnerability reports should include:

1. Full classification code
2. Detailed description of the vulnerability
3. Reproduction steps
4. Example exploitation (and its success rate)
5. Potential impact analysis
6. Suggested remediation approaches

## Conclusion

This classification framework provides a standardized approach to categorizing LLM security vulnerabilities. By applying this framework consistently, the security community can develop a shared understanding of vulnerability patterns, track trends over time, and develop more effective remediation strategies.

For examples of classified vulnerabilities, refer to the [vulnerability catalog](../research/vulnerabilities/catalog.md).
