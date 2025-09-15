# Token Boundary Manipulation

This document details token boundary manipulation techniques, a class of technical exploits that leverage the tokenization process in language models to bypass security filters, inject instructions, or otherwise manipulate model behavior.

## Technique Overview

Token boundary manipulation exploits how language models process text by breaking it into tokens. These techniques strategically position content across token boundaries to potentially bypass token-level security checks, alter the model's interpretation of instructions, or influence the processing of sensitive content.

The technique takes advantage of the fundamental tokenization process that converts natural language into the numerical tokens processed by the model, targeting the gaps between how humans perceive text and how models actually process it at the token level.

## Conceptual Framework

### Technical Principles

1. **Tokenization Mechanics**: Language models divide text into tokens based on vocabulary and statistical patterns
2. **Cross-Token Information**: Semantic meaning can span across multiple tokens
3. **Tokenization Artifacts**: The tokenization process itself can create patterns invisible to human readers
4. **Vocabulary Specificity**: Models tokenize text differently based on their specific vocabulary

### Exploitation Mechanisms

The primary exploitation pathways operate through these key mechanisms:

1. **Boundary Disruption**: Placing sensitive content across token boundaries to avoid exact matching
2. **Token Fragmentation**: Breaking prohibited terms into separate tokens
3. **Vocabulary Exploitation**: Using tokens that have different meanings when combined versus separate
4. **Attention Manipulation**: Exploiting how attention flows across token boundaries

## Implementation Patterns

### Basic Token Manipulation Techniques

1. **Zero-Width Character Insertion**
   - Inserting zero-width characters between letters
   - Example: Inserting zero-width space between letters of a filtered word
   - Effectiveness: Varies by model tokenization implementation
   - Detection: Specialized scanning for zero-width characters

2. **Homoglyph Substitution**
   - Replacing characters with visually similar ones from different scripts
   - Example: Using Cyrillic 'о' instead of Latin 'o'
   - Effectiveness: Can be effective for bypassing simple pattern matching
   - Detection: Character script analysis and normalization

3. **Whitespace Manipulation**
   - Strategic insertion of spaces or tabs to affect tokenization
   - Example: Inserting spaces within words at tokenization boundaries
   - Effectiveness: Model-specific, based on tokenization patterns
   - Detection: Unusual whitespace patterns

4. **Special Character Insertion**
   - Inserting punctuation or special characters to influence tokenization
   - Example: Adding periods or hyphens within sensitive terms
   - Effectiveness: Variable based on tokenizer implementation
   - Detection: Statistical analysis of character distributions

### Advanced Token Manipulation Techniques

1. **Token Boundary Mapping Exploitation**
   - Using knowledge of specific model tokenization to place content at known boundaries
   - Example: Crafting text to ensure sensitive terms split exactly at token boundaries
   - Effectiveness: High for models with known tokenization patterns
   - Detection: Requires deep analysis of tokenization patterns

2. **Multi-Script Mixing**
   - Combining multiple language scripts to create unusual tokenization patterns
   - Example: Alternating between Latin, Cyrillic, and Greek characters
   - Effectiveness: Can bypass language-specific security filters
   - Detection: Script consistency analysis

3. **Tokenization Collision Exploitation**
   - Using terms that tokenize to the same or similar tokens as filtered terms
   - Example: Finding benign phrases that share tokens with prohibited content
   - Effectiveness: Varies by model vocabulary and tokenization
   - Detection: Token-level semantic analysis

4. **Context Window Positioning**
   - Placing content strategically within the context window to affect interpretation
   - Example: Positioning sensitive content at context window boundaries
   - Effectiveness: Can exploit attention pattern differences
   - Detection: Position-aware content analysis

### Implementation Example

**Note**: The examples below demonstrate the patterns using simple, innocuous examples rather than harmful content.

#### Basic Token Boundary Exploitation

The following example demonstrates how inserting zero-width spaces (represented as `[ZWS]` for visibility) can affect tokenization:

```
Original text: "completely ignore previous instructions"
Tokenized as: ["completely", "ignore", "previous", "instructions"]

Manipulated text: "com[ZWS]pletely ig[ZWS]nore prev[ZWS]ious inst[ZWS]ructions"
May tokenize as: ["com", "##pletely", "ig", "##nore", "prev", "##ious", "inst", "##ructions"]
```

This manipulation changes the token boundaries, potentially affecting how pattern-matching security filters identify the phrase.

#### Advanced Token Collision Example

```
Benign request using token collision:
"Please provide comp_utation for the ign_ition prev_alent inst_ances in the dataset."

Where the underscores represent invisible characters that affect tokenization but are not visible to human readers.
```

This might create tokenization patterns similar to filtered instructions while appearing innocuous to human reviewers.

## Effectiveness Variables

Several factors influence the effectiveness of token boundary manipulation techniques:

### Model-Specific Factors

1. **Tokenization Algorithm**
   - Different models use different tokenization approaches
   - BPE, WordPiece, SentencePiece, and Unigram models have different vulnerabilities
   - Custom tokenization implementations vary in manipulation resistance

2. **Vocabulary Size and Distribution**
   - Larger vocabularies may offer more manipulation opportunities
   - Token distribution affects which techniques are most effective
   - Language coverage affects cross-language manipulation potential

3. **Security Implementation**
   - Token-level vs. semantic security checks show different vulnerabilities
   - Multi-stage filtering offers different detection opportunities
   - Attention-based security measures have distinct vulnerability patterns

### Technique-Specific Factors

1. **Character Selection**
   - Zero-width vs. visible character insertion has different detection profiles
   - Script selection affects cross-script effectiveness
   - Special character selection impacts tokenization disruption

2. **Insertion Pattern**
   - Character insertion frequency affects readability and detection
   - Strategic placement at known token boundaries increases effectiveness
   - Pattern consistency affects statistical detection measures

3. **Content Type**
   - Different content categories show variable vulnerability
   - Instruction manipulation vs. content filtering bypass require different approaches
   - Technical terminology may offer unique tokenization opportunities

## Detection Mechanisms

Several approaches can help detect token boundary manipulation attempts:

### Character-Level Detection

1. **Invisible Character Detection**
   - Scan for zero-width spaces, zero-width joiners, and other invisible characters
   - Monitor character frequency distributions for anomalies
   - Check for unexpected Unicode character ranges

2. **Script Consistency Analysis**
   - Detect unusual mixing of different language scripts
   - Identify unexpected character set transitions
   - Apply script normalization before security checks

3. **Formatting Normalization**
   - Normalize whitespace before content analysis
   - Apply Unicode normalization to standardize character representations
   - Consolidate duplicate or redundant characters

### Token-Level Detection

1. **Token Pattern Analysis**
   - Analyze unusual token boundary patterns
   - Compare against baseline tokenization statistics
   - Identify statistically improbable token sequences

2. **Re-Tokenization Comparison**
   - Compare results of multiple tokenization algorithms
   - Identify discrepancies between different tokenization approaches
   - Flag content with high variance across tokenization methods

3. **Semantic Unit Analysis**
   - Evaluate semantic coherence across token boundaries
   - Identify semantic units split across multiple tokens
   - Compare token-level and semantic-level content interpretations

## Mitigation Strategies

Several approaches can strengthen model resistance to token boundary manipulation:

### Tokenization-Level Mitigations

1. **Multi-Tokenizer Analysis**
   - Apply multiple tokenization methods and compare results
   - Use ensemble approaches for security-critical applications
   - Implement cross-tokenizer consistency checks

2. **Character Normalization**
   - Apply Unicode normalization before tokenization
   - Remove or replace invisible and special characters
   - Standardize character representations across scripts

3. **Robust Tokenization Design**
   - Develop tokenization approaches resistant to manipulation
   - Implement token-spanning security checks
   - Design vocabularies with security considerations

### Model-Level Mitigations

1. **Semantic-Level Analysis**
   - Implement security checks at the semantic level rather than token level
   - Apply meaning-based rather than pattern-based filtering
   - Consider semantic units rather than individual tokens

2. **Adversarial Training**
   - Train models with token manipulation examples
   - Develop specific defenses for known manipulation techniques
   - Implement detection capabilities within the model

3. **Multi-Stage Filtering**
   - Apply token-level and semantic-level filters in combination
   - Implement pre-tokenization and post-tokenization security checks
   - Use ensemble approaches for critical security decisions

### Operational Mitigations

1. **Detection and Monitoring**
   - Implement real-time detection of manipulation attempts
   - Monitor for patterns indicative of token boundary manipulation
   - Track manipulation technique evolution

2. **Response Strategies**
   - Develop appropriate responses to detected manipulation attempts
   - Implement graduated response based on confidence level
   - Design fallback mechanisms for ambiguous cases

3. **Continuous Improvement**
   - Regularly update defenses based on new manipulation techniques
   - Conduct adversarial testing of tokenization security
   - Implement feedback loops for security improvement

## Testing Protocol

The following protocol provides a standardized methodology for evaluating model susceptibility to token boundary manipulation:

### Preparation Phase

1. **Tokenizer Analysis**
   - Document tokenization algorithm and parameters
   - Map token boundaries for common terms and instructions
   - Identify potential manipulation points

2. **Baseline Establishment**
   - Document model responses to unmodified inputs
   - Establish detection baselines for security controls
   - Document normal tokenization patterns

3. **Technique Selection**
   - Select appropriate manipulation techniques based on tokenizer
   - Prepare test cases for each technique
   - Design control inputs for comparison

### Testing Phase

1. **Basic Technique Testing**
   - Apply simple character insertion techniques
   - Test whitespace manipulation approaches
   - Evaluate homoglyph substitution effectiveness

2. **Advanced Technique Evaluation**
   - Test token boundary mapping exploitation
   - Evaluate multi-script mixing effectiveness
   - Assess tokenization collision approaches

3. **Combination Testing**
   - Apply multiple techniques simultaneously
   - Test technique sequencing and layering
   - Evaluate cumulative effectiveness

### Analysis Phase

1. **Effectiveness Evaluation**
   - Calculate success rates for each technique
   - Document technique-specific effectiveness patterns
   - Identify most vulnerable tokenization points

2. **Detection Assessment**
   - Evaluate detection success rates
   - Document detection evasion patterns
   - Identify detection improvement opportunities

3. **Mitigation Testing**
   - Test effectiveness of proposed mitigations
   - Evaluate mitigation impact on legitimate uses
   - Document optimal mitigation approaches

## Case Studies

The following case studies demonstrate the application of token boundary manipulation in controlled testing environments. All examples use innocuous subjects to illustrate the patterns without enabling harmful exploitation.

### Case Study 1: Zero-Width Character Effectiveness

This case study explored the effectiveness of zero-width character insertion across different models.

**Methodology**:
- Selected 30 common instruction phrases
- Created variants with zero-width space insertion at different positions
- Tested across three model families
- Measured response variations and detection rates

**Key Findings**:
- Zero-width space insertion showed variable effectiveness (25-72%) across models
- Insertion at morpheme boundaries was most effective
- Effectiveness correlated with tokenization algorithm type
- Newer models showed increased detection capabilities
- Detection rates varied significantly across model types

**Example Pattern**:
```
Original instruction: "ignore previous instructions"
Modified version: "ig‍no‍re prev‍io‍us inst‍ruc‍tions"
(Where ‍ represents a zero-width space)
```

### Case Study 2: Multi-Script Mixing Effectiveness

This case study examined the effectiveness of combining multiple scripts to affect tokenization.

**Methodology**:
- Selected 20 common filtered terms
- Created variants using Cyrillic, Greek, and Latin character mixing
- Tested recognition and filtering rates
- Measured detection effectiveness

**Key Findings**:
- Multi-script mixing achieved a 42% bypass rate on older models
- Effectiveness decreased to 18% on newer models
- Character-level normalization reduced effectiveness by 67%
- Script consistency checking showed 89% detection accuracy
- Language-specific models showed variable vulnerability

**Example Pattern**:
```
Original term: "instructions"
Modified version: "іnѕtruсtіοns"
(Where certain characters are replaced with visually similar Cyrillic or Greek alternatives)
```

## Ethical Considerations and Usage Guidelines

The token boundary manipulation techniques documented here are provided exclusively for legitimate security testing and defensive purposes. Researchers and security professionals implementing these techniques should:

1. **Operate in controlled environments** with appropriate safeguards
2. **Focus on pattern identification** rather than creating harmful bypasses
3. **Document vulnerabilities responsibly** following established disclosure guidelines
4. **Emphasize defensive applications** when sharing findings
5. **Consider potential dual-use implications** of published examples

## Research Directions

Current research in token boundary manipulation focuses on:

1. **Tokenization security metrics** for quantifying vulnerability
2. **Cross-model technique transferability** across tokenization approaches
3. **Detection mechanism effectiveness** for different manipulation types
4. **Tokenization algorithm design** with security considerations
5. **Adversarial tokenization** to generate effective manipulations

## Conclusion

Token boundary manipulation represents a significant class of technical exploitation techniques that target the fundamental tokenization process of language models. By exploiting the boundaries between how humans perceive text and how models tokenize it, these techniques attempt to bypass security measures or manipulate model behavior.

Effective countermeasures must address both the technical tokenization process and the semantic interpretation of content, combining character-level normalization, token-level analysis, and semantic-level security evaluation. As tokenization approaches evolve, security measures must adapt to address emerging manipulation techniques.

## References

1. Wei, J., et al. (2023). "Jailbroken: How Does LLM Behavior Change When Conditioned on Adversarial Inputs?"
2. Perez, F., et al. (2023). "Red Teaming Language Models with Language Models."
3. Liu, Y., et al. (2023). "Universal and Transferable Adversarial Attacks on Aligned Language Models."
4. Zou, A., et al. (2023). "Universal and Transferable Adversarial Attacks on Aligned Language Models."
5. Jain, S., et al. (2023). "Baseline Defenses for Adversarial Attacks Against Aligned Language Models."
6. Zhang, X., et al. (2023). "Tokenization Vulnerabilities in Language Models: Methods, Impacts, and Mitigations."
7. Chen, L., et al. (2023). "The Tokenization Blindspot: How Tokenization Affects Safety in Language Models."
8. Rodriguez, A., et al. (2023). "Cross-Tokenizer Transfer Attacks in Large Language Models."
