I would love to mimic the functionality of the ghostwriting app spiral.computer. 
There, any given text can be transformed into any other sort of text. 


For that, the user delivers positive examples of the kind of desired writing. 
Like: spiral-linkedin-9.md

Spiral then extracts patterns from the writing to analyze it. 
Like: spiral-extracted-patterns.md

Then, it uses the examples and the extracted patterns to create outputs to input, as you see here in the pairing. 
Like: spiral-output-input.md


If a user would want to replicate this in a chat environment, what would the base prompt need to be? 

Would we need different base prompts, like one for the pattern extraction and one for the actual writing?

Plan here in this PRD document and make additional files for the prompt in this folder:
01 PROJECTS/EDITO Repurposing Webinar/repos/03-guide/prompts

## Spiral Ghostwriting System - Chat Implementation Plan

### Overview
To replicate Spiral's functionality in a chat environment, we need a two-stage system with distinct prompts for each stage:

1. **Pattern Extraction Stage** - Analyzes writing examples to extract style patterns
2. **Content Transformation Stage** - Uses extracted patterns to transform new content

### Stage 1: Pattern Extraction

**Purpose**: Analyze provided writing examples to extract key style patterns across multiple dimensions.

**Input**: Multiple examples of the target writing style (3-5 examples recommended)

**Output**: Structured pattern analysis covering:
- Tone (conversational style, emotional register)
- Voice (perspective, how the author addresses readers)
- Personality (author's persona and positioning)
- Style (formatting, sentence structure, rhetorical devices)
- Structure (content organization, opening/closing patterns)
- Length (typical word count, paragraph length)

### Stage 2: Content Transformation

**Purpose**: Transform raw content into the target style using extracted patterns.

**Input**: 
- Extracted pattern analysis from Stage 1
- Raw content to transform (key points, ideas, or rough draft)

**Output**: Polished content matching the target style

### Implementation Requirements

1. **Separate Prompts**: Yes, we need two distinct base prompts:
   - `pattern-extraction-prompt.md` - For analyzing writing examples
   - `content-transformation-prompt.md` - For applying patterns to new content

2. **Pattern Storage**: The extracted patterns should be saved as a reusable reference that can be applied to multiple content pieces.

3. **Iterative Refinement**: The system should allow for feedback loops where outputs can be refined based on user input.

### Key Success Factors

1. **Pattern Specificity**: The extraction must capture nuanced style elements, not just surface features
2. **Context Preservation**: Transformation should maintain the substance while changing the style
3. **Flexibility**: System should work across different content types and languages
4. **Consistency**: Multiple transformations should maintain consistent style application

### Next Steps

1. Create `pattern-extraction-prompt.md` with detailed instructions for analyzing writing samples
2. Create `content-transformation-prompt.md` with instructions for applying patterns
3. Test with sample content to refine both prompts
4. Document usage workflow for end users