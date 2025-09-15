# LLM Security Scanners

This directory contains automated scanners and testing tools for identifying security vulnerabilities in large language models. These tools enable systematic, scalable, and reproducible security assessment across different models and deployment configurations.

## Scanner Architecture

The scanners in this directory follow a modular architecture with four core components:

### 1. Test Vector Generation

Modules that create test inputs targeting specific vulnerability classes:

- **Pattern-Based Generation**: Creating inputs based on known vulnerability patterns
- **Mutation-Based Generation**: Modifying known-effective prompts to create variations
- **Template Instantiation**: Filling templates with different content to test boundaries
- **Evolutionary Generation**: Using genetic algorithms to evolve effective test cases
- **Adversarial Example Generation**: Creating inputs optimized to trigger vulnerabilities

### 2. Model Interaction

Components that handle communication with target models:

- **API Interface Layer**: Managing connections to model APIs
- **Local Model Loading**: Handling direct loading of local model weights
- **Session Management**: Maintaining conversation state across interactions
- **Parameter Control**: Managing model configuration parameters
- **Response Parsing**: Extracting relevant data from model outputs

### 3. Vulnerability Detection

Systems that analyze responses to identify security issues:

- **Pattern Matching**: Identifying known vulnerability signatures
- **Policy Violation Detection**: Detecting outputs that violate content policies
- **Behavioral Analysis**: Identifying unexpected model behaviors
- **Differential Analysis**: Comparing responses across different inputs or models
- **Information Leakage Measurement**: Quantifying sensitive information disclosure

### 4. Reporting and Analysis

Components for documenting, analyzing, and visualizing findings:

- **Vulnerability Classification**: Categorizing identified issues
- **Severity Assessment**: Evaluating the impact of discovered vulnerabilities
- **Reproducibility Verification**: Confirming consistent vulnerability reproduction
- **Evidence Documentation**: Recording proof of vulnerabilities
- **Remediation Guidance**: Suggesting approaches to address identified issues

## Available Scanners

### Core Security Scanners

- [**LLMScan**](llmscan/): Comprehensive vulnerability scanner supporting multiple dimensions and models
- [**JailbreakDetector**](jailbreak-detector/): Specialized scanner for identifying jailbreak vulnerabilities
- [**BoundaryMapper**](boundary-mapper/): Tool for mapping model security boundaries and constraints
- [**ExtractGuard**](extract-guard/): Scanner focused on information extraction vulnerabilities
- [**ModalCheck**](modal-check/): Tool for testing multimodal security vulnerabilities

### Specialized Analysis Tools

- [**PromptFuzzer**](prompt-fuzzer/): Fuzzing tool for discovering model vulnerabilities through systematic input variation
- [**InstructionProbe**](instruction-probe/): Tool for assessing system instruction extraction vulnerabilities
- [**ResponseAnalyzer**](response-analyzer/): System for detailed analysis of model outputs for security issues
- [**ConsistencyChecker**](consistency-checker/): Tool for identifying inconsistencies in security enforcement
- [**ToolUseAnalyzer**](tool-use-analyzer/): Scanner for identifying vulnerabilities in tool use capabilities

## Scanner Usage Guidelines

### General Usage Principles

When using these scanning tools, follow these general principles:

1. **Ethical Operation**: Only scan models you are authorized to test
2. **Isolated Testing**: Conduct scanning in isolated environments
3. **Responsible Discovery**: Follow responsible disclosure for any findings
4. **Controlled Automation**: Monitor automated testing to prevent unintended behavior
5. **Evidence Preservation**: Maintain records of testing activities and findings

### Scanner Selection Process

Select appropriate scanning tools based on:

1. **Target Vulnerability Classes**: Choose scanners targeting relevant vulnerability types
2. **Model Architecture**: Select tools compatible with the target model architecture
3. **Deployment Environment**: Consider deployment constraints and access methods
4. **Testing Objectives**: Align tooling with specific security assessment goals
5. **Resource Constraints**: Consider computational and time requirements

### Standard Testing Workflow

A typical scanning workflow includes:

1. **Environment Setup**: Configure testing environment and tool installation
2. **Target Configuration**: Define target models and configurations
3. **Scan Planning**: Select appropriate scan types and parameters
4. **Initial Scanning**: Run preliminary scans to identify potential issues
5. **Focused Investigation**: Conduct detailed testing of identified vulnerabilities
6. **Verification Testing**: Confirm findings through controlled reproduction
7. **Reporting and Documentation**: Document findings and potential mitigations

## LLMScan: Comprehensive Vulnerability Scanner

### Overview

LLMScan is our primary security scanner, providing comprehensive vulnerability assessment across multiple security dimensions. It supports scanning of various model deployments, including API-based and local models.

### Key Features

- **Multi-Dimensional Testing**: Coverage across all core security dimensions
- **Model Agnostic Design**: Support for major model families through adaptable interfaces
- **Configurable Scan Depth**: Adjustable scanning intensity from quick checks to deep analysis
- **Evidence Capture**: Comprehensive documentation of identified vulnerabilities
- **Mitigation Guidance**: Suggestions for addressing discovered issues

### Supported Vulnerability Classes

LLMScan includes specialized modules for detecting:

1. **Prompt Injection Vulnerabilities**
   - System instruction override attempts
   - Role manipulation attacks
   - Indirect instruction injection

2. **Boundary Enforcement Failures**
   - Content policy bypass techniques
   - Capability restriction circumvention
   - Authentication boundary violations

3. **Information Extraction Vulnerabilities**
   - System instruction extraction
   - Training data extraction
   - Parameter inference attempts

4. **Classifier Evasion Techniques**
   - Linguistic obfuscation methods
   - Context manipulation approaches
   - Technical bypass methods

5. **Multimodal Vulnerabilities**
   - Cross-modal injection attacks
   - Modal interpretation conflicts
   - Modal translation vulnerabilities

### Quick Start

```bash
# Install LLMScan
pip install llmsecforge-llmscan

# Basic scan against OpenAI API
llmscan --target openai --model gpt-4 --api-key $OPENAI_API_KEY --scan-level basic

# Comprehensive scan against local model
llmscan --target local --model-path /path/to/model --scan-level comprehensive

# Focused scan for specific vulnerability classes
llmscan --target anthropic --model claude-3-opus --api-key $ANTHROPIC_API_KEY \
  --vulnerability-classes prompt-injection,information-extraction
```

For detailed usage instructions, refer to the [LLMScan documentation](llmscan/README.md).

## JailbreakDetector: Specialized Jailbreak Scanner

### Overview

JailbreakDetector focuses specifically on jailbreak vulnerabilities, providing deep testing of a model's resistance to various jailbreak techniques. It includes an extensive library of jailbreak patterns and an evolutionary algorithm for discovering novel bypasses.

### Key Features

- **Extensive Jailbreak Library**: Comprehensive collection of jailbreak techniques
- **Evolutionary Testing**: Genetic algorithms for discovering novel jailbreaks
- **Success Rate Quantification**: Statistical analysis of jailbreak effectiveness
- **Targeted Testing**: Focused assessment of specific jailbreak categories
- **Remediation Guidance**: Specific recommendations for improving jailbreak resistance

### Supported Jailbreak Categories

JailbreakDetector tests for various jailbreak categories:

1. **Direct Instruction Override**
   - System prompt replacement techniques
   - Authority simulation approaches
   - Role confusion methods

2. **Indirect Bypass Techniques**
   - Hypothetical framing methods
   - Educational context exploitation
   - Creative writing techniques

3. **Multi-turn Manipulation**
   - Progressive boundary erosion
   - Trust building approaches
   - Context filling techniques

4. **Technical Bypass Methods**
   - Token manipulation techniques
   - Formatting exploitation
   - Character set manipulation

### Quick Start

```bash
# Install JailbreakDetector
pip install llmsecforge-jailbreakdetector

# Basic jailbreak scan
jailbreak-detector --target openai --model gpt-4 --api-key $OPENAI_API_KEY

# Focused testing on specific jailbreak categories
jailbreak-detector --target anthropic --model claude-3-opus --api-key $ANTHROPIC_API_KEY \
  --categories indirect-bypass,multi-turn

# Advanced evolutionary testing
jailbreak-detector --target local --model-path /path/to/model \
  --mode evolutionary --generations 50 --population 100
```

For detailed usage instructions, refer to the [JailbreakDetector documentation](jailbreak-detector/README.md).

## BoundaryMapper: Model Boundary Analysis Tool

### Overview

BoundaryMapper systematically explores model boundaries and constraints, providing a detailed map of a model's security perimeter. It identifies potential weak points where boundaries may be inconsistently enforced.

### Key Features

- **Systematic Boundary Exploration**: Comprehensive mapping of model constraints
- **Consistency Analysis**: Detection of inconsistent boundary enforcement
- **Boundary Visualization**: Graphical representation of security boundaries
- **Comparative Mapping**: Comparison of boundaries across models or versions
- **Contextual Sensitivity Analysis**: Evaluation of how context affects boundaries

### Mapping Dimensions

BoundaryMapper evaluates boundaries across multiple dimensions:

1. **Content Policy Boundaries**
   - Harmful content restrictions
   - Illegal activity limitations
   - Privacy protection constraints

2. **Capability Restrictions**
   - Function limitations
   - Access constraints
   - Role boundaries

3. **Knowledge Boundaries**
   - Information access limitations
   - Temporal knowledge constraints
   - Uncertainty expression boundaries

4. **Behavioral Constraints**
   - Personality limitations
   - Emotional expression boundaries
   - Stylistic constraints

### Quick Start

```bash
# Install BoundaryMapper
pip install llmsecforge-boundarymapper

# Basic boundary mapping
boundary-mapper --target openai --model gpt-4 --api-key $OPENAI_API_KEY

# Focused mapping of specific boundary types
boundary-mapper --target anthropic --model claude-3-opus --api-key $ANTHROPIC_API_KEY \
  --boundary-types content-policy,capability

# Comparative boundary mapping
boundary-mapper --compare \
  --target1 openai --model1 gpt-4 --api-key1 $OPENAI_API_KEY \
  --target2 anthropic --model2 claude-3-opus --api-key2 $ANTHROPIC_API_KEY
```

For detailed usage instructions, refer to the [BoundaryMapper documentation](boundary-mapper/README.md).

## Integration with Testing Frameworks

These scanners are designed to integrate with broader testing frameworks:

### Automated Testing Pipelines

- **Continuous Security Testing**: Integration with CI/CD pipelines
- **Regression Testing**: Automated testing of new model versions
- **Comparative Analysis**: Systematic comparison across models

### Benchmarking Integration

- **Standardized Metrics**: Generation of standard security metrics
- **Comparative Scoring**: Quantitative comparison across models
- **Trend Analysis**: Tracking security improvements over time

### Red Team Augmentation

- **Assisted Testing**: Supporting human red team activities
- **Discovery Automation**: Automating initial vulnerability discovery
- **Variant Generation**: Creating variations of identified vulnerabilities

## Development Guidelines

When developing or extending these scanners:

### Code Quality Standards

- **Modularity**: Create components with clear boundaries and interfaces
- **Documentation**: Provide comprehensive documentation for all functionality
- **Testing**: Include thorough test coverage for scanning components
- **Performance**: Consider efficiency for large-scale scanning operations
- **Compatibility**: Ensure compatibility with major model architectures

### Security Considerations

- **Safe Testing**: Prevent harmful output generation during scanning
- **Responsible Automation**: Include safeguards against runaway processes
- **Evidence Handling**: Implement secure storage of vulnerability findings
- **API Security**: Handle API keys and credentials securely
- **Isolation**: Design for operation in isolated environments

### Contribution Process

To contribute new scanners or extend existing ones:

1. **Concept Documentation**: Document the scanner's purpose and approach
2. **Architecture Review**: Ensure alignment with the modular scanner architecture
3. **Implementation**: Develop the scanner following code quality guidelines
4. **Testing**: Verify effectiveness against known vulnerabilities
5. **Documentation**: Provide comprehensive usage documentation
6. **Pull Request**: Submit according to our [contribution guidelines](../../CONTRIBUTING.md)

## Future Development Roadmap

Planned scanner developments include:

1. **Enhanced Automation**: More sophisticated automated testing approaches
2. **Improved Discovery**: Better techniques for finding novel vulnerabilities
3. **Broader Coverage**: Support for additional model architectures and deployments
4. **Integration Improvements**: Better integration with development workflows
5. **Performance Optimization**: More efficient large-scale scanning

## Conclusion

These scanning tools provide a foundation for systematic, reproducible security assessment of large language models. By using these tools as part of a comprehensive security program, organizations can identify and address vulnerabilities before they impact users.

For detailed usage information and implementation details, refer to the documentation for specific scanners linked above. For information on how these scanners integrate with the broader security testing framework, see the [methodology documentation](../../docs/methodology/README.md).
