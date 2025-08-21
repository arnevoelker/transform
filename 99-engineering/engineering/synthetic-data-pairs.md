# Engineering Synthetic Data Pairs for Spiral Ghostwriting

## Overview

This document describes the process for creating synthetic input-output data pairs that replicate Spiral's ghostwriting functionality. These pairs are essential for training or demonstrating how to transform raw content ideas into polished posts matching a specific writing style.

## Process for Generating Synthetic Data

### Step 1: Analyze Target Writing Examples

First, collect and analyze the target writing samples (e.g., LinkedIn posts) to understand:
- Core themes and messages
- Writing patterns and style
- Structure and formatting
- Key quotes and phrases

### Step 2: Extract Pattern Dimensions

Using the pattern extraction framework, identify:
- **Tone**: Emotional register, formality level, reader relationship
- **Voice**: Perspective (I/you/we), authority positioning
- **Personality**: Author traits, values, attitudes
- **Style**: Sentence structure, rhetorical devices, formatting
- **Structure**: Opening hooks, content flow, closing techniques
- **Length**: Word count, paragraph size

### Step 3: Reverse-Engineer Inputs

For each output (published post), create a synthetic input containing:

#### Required Components:
1. **Title**: Brief topic summary (5-10 words)
2. **Kernaussage** (Core Message): The main point in one sentence
3. **Kontext** (Context): Background and relevance for the target audience
4. **Anwendung** (Application): Practical takeaway or action item
5. **Originalzitat** (Original Quote): Key phrase to include verbatim (optional)

#### Guidelines for Input Creation:

**Kernaussage should:**
- Capture the essential thesis
- Be factual and neutral in tone
- Summarize without stylistic flourishes

**Kontext should:**
- Explain why this matters now
- Identify the target audience
- Connect to broader trends or issues

**Anwendung should:**
- Provide concrete next steps
- Suggest how to apply the insight
- Focus on practical value

**Originalzitat should:**
- Select the most memorable line
- Choose quotes that anchor the piece
- Include if there's a signature phrase

### Step 4: Structure the Data Pairs

Format each pair as:

```markdown
## Beispiel [Number]

### Input
[Title]

**Kernaussage**: [Core message]

**Kontext**: [Context and relevance]

**Anwendung**: [Practical application]

**Originalzitat**: «[Key quote]» (optional)

### Output
[Full formatted post text]
```

### Step 5: Quality Validation

Verify each synthetic pair by checking:
- Does the input contain enough information to generate the output?
- Are all key themes from the output represented in the input?
- Is the input neutral enough to be transformed into any style?
- Would different writers produce similar content from this input?

## Example Transformation

### From Analysis to Input

**Original Post Theme**: AI-generated content lacks authenticity, humans needed for curation

**Synthetic Input Components**:
- Title: "KI-Content und Authentizität"
- Kernaussage: Question whether AI content can be made "with love"
- Kontext: Many publish raw AI outputs, lowering content quality
- Anwendung: Use AI as tool, not replacement for human creativity
- Originalzitat: «Hello, is There any Value Out There?»

### From Input to Output

The transformation applies the extracted style patterns:
- Opens with provocative question (Structure)
- Uses "ich" perspective (Voice)
- Includes em-dashes for lists (Style)
- Maintains conversational tone (Tone)
- Ends with engagement prompt (Structure)

## Key Insights

1. **Abstraction Level**: Inputs should be abstract enough to allow style variation but specific enough to guide content

2. **Information Density**: Each input component serves a distinct purpose - don't duplicate information

3. **Cultural Context**: Preserve language-specific elements (e.g., German phrases) where they're essential to meaning

4. **Iterative Refinement**: Creating good synthetic pairs requires multiple passes to balance information and abstraction

## Usage in Chat Environments

To replicate Spiral's functionality in chat:

1. **First Message**: Provide writing examples and request pattern extraction
2. **Second Message**: Share the synthetic input for transformation
3. **Third Message**: Receive the styled output

Or combine into a single prompt with both examples and new content to transform.

## Files Generated

- `/prompts/pattern-extraction-prompt.md` - Base prompt for analyzing writing styles
- `/prompts/content-transformation-prompt.md` - Base prompt for applying patterns
- `/prompts/spiral-linkedin-9-synthetic-data-pairs.md` - Complete set of 9 example pairs
- `/prompts/PRD.md` - Product requirements and implementation plan

## Next Steps

1. Test the prompts with new content types
2. Refine the input structure based on results
3. Create templates for common content formats
4. Build a library of extracted patterns for different authors