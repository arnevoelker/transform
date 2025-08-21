# /transform · AI-Powered Content Promotion System

/transform helps you transform your long-form content into platform-optimized promotional materials using a professional AI workflow. Based on the methodology presented in "Promoting Content with AI", this repository provides a complete implementation of the Extract-Chunk-Guide framework.

Here's how NotebookLM wraps it up: [» Play the video](https://www.youtube.com/watch?v=LyVitMpLzqE)
[![Promoting Content with AI](https://img.youtube.com/vi/LyVitMpLzqE/maxresdefault.jpg)](https://www.youtube.com/watch?v=LyVitMpLzqE)

## Problem Statement

Creating content is hard. Getting people to see it is even harder. In today's "zero-click world", success means delivering complete value directly within social media feeds - not just posting links. This system helps you transform any piece of content into multiple platform-specific promotional pieces that work.

## The Solution: Extract-Chunk-Guide Framework

A three-step professional AI workflow that transforms your content into high-quality promotional materials:

### 1. **Extract** (`01-extract/`)
Clean and prepare your raw content by removing formatting artifacts, HTML, and other distractions. Creates pure, AI-ready text.

### 2. **Chunk** (`02-chunk/`)
Break down content into "golden nuggets" - self-contained packages of value, each containing:
- Core message (one sentence)
- Context (why it matters)
- Application (what the audience can do)
- Original quote (powerful excerpt)

### 3. **Guide** (`03-guide/`)
Transform golden nuggets into platform-specific posts using pattern analysis and style matching. Includes:
- Pattern extraction from writing examples
- Style-consistent content transformation
- Platform-specific adaptations

## Repository Structure

```
transform/
├── 01-extract/          # Content extraction and cleaning
│   ├── input/
│   │   └── prompts/     # Extraction prompts for different content types
│   └── output/          # Cleaned, markdown-formatted content
│
├── 02-chunk/            # Golden nugget extraction
│   ├── input/
│   │   ├── context/     # Source content to process
│   │   └── prompts/     # Nugget extraction prompts
│   └── output/          # Extracted golden nuggets
│
├── 03-guide/            # Style transformation and ghostwriting
│   ├── context/         # Writing examples and patterns
│   ├── prompts/         # Transformation prompts with README
│   └── output/          # Final promotional content
│
├── 98-background/       # Documentation and methodology
│   └── Promoting Content with AI (Overview).md
│
└── 99-engineering/      # Technical documentation
    └── engineering/     # System design and implementation notes
```

## Key Features

### Spiral-Style Ghostwriting
The system includes a sophisticated ghostwriting capability that can:
- Analyze any author's writing style across 6 dimensions
- Extract patterns from 3-5 writing examples
- Transform raw content to match the target style perfectly
- Maintain consistency across multiple pieces

### Multi-Platform Support
Generate content optimized for:
- LinkedIn posts
- Twitter/X threads
- Newsletter blurbs
- Instagram carousels
- Blog summaries

### Language Flexibility
Works with content in multiple languages (examples include English and German).

## How to Use

### Quick Start with Ghostwriting

1. **Navigate to prompts**: Go to `03-guide/prompts/`
2. **Read the guide**: Start with `README.md` for detailed instructions
3. **Copy the prompt**: Use `content-transformation-prompt.md` in your AI chat
4. **Provide examples**: Supply 3-5 writing samples from your target style
5. **Transform content**: Input your raw content and receive styled output

### Complete Workflow

1. **Extract**: Clean your raw content using prompts in `01-extract/input/prompts/`
2. **Chunk**: Extract golden nuggets using `02-chunk/input/prompts/golden-nuggets-extraction-prompt.md`
3. **Guide**: Transform nuggets into posts using the ghostwriting system in `03-guide/prompts/`

## Core Concepts

### Zero-Click Content
Content designed to deliver complete value within the platform where it's discovered, without requiring users to click through to external sites.

### Golden Nuggets
Structured content blocks that can be repurposed across platforms while maintaining their core value proposition.

### Pattern-Based Transformation
Using AI to extract and apply writing patterns ensures authentic, consistent voice across all promotional materials.

## Background & Philosophy

This system is based on the principle that "the worst AI you'll ever use is the one you're using today" - meaning AI capabilities are constantly improving, so our workflows should be flexible and evolutionary.

The goal isn't to master one perfect prompt, but to build an intelligent, flexible workflow that evolves with the technology.

For a complete overview of the methodology, see [`98-background/Promoting Content with AI (Overview).md`](98-background/Promoting%20Content%20with%20AI%20(Overview).md).

## Technical Notes

- **AI Models**: Tested with Claude (Sonnet, Opus), GPT-4, and GPT-5
- **Input Formats**: Markdown, plain text, interview transcripts
- **Output Formats**: Platform-optimized markdown with appropriate formatting

## Best Practices

1. **Better Context = Better Results**: Always provide clean, well-structured input
2. **Build Your Example Library**: Collect great examples of your target style
3. **Iterate and Improve**: Each use should refine your prompts and patterns
4. **Platform Awareness**: Understand each platform's unique requirements

## Attribution

The Extract-Chunk-Guide methodology was first presented at a webinar with [Edito Magazine](https://edito.ch) on August 19, 2025.

Sample content used for demonstration purposes is courtesy of Edito Magazine and contains the original work of writers **Matthias Zehnder**, **Reto Vogt**, and interview guest **Sabine Meyer**.

## Contributing

This repository represents a working implementation of content transformation workflows. Contributions that improve prompts, add new platform support, or enhance the extraction process are welcome.

## License

This repository contains methodologies and prompts for content transformation. Please use responsibly and maintain attribution when sharing or adapting these workflows.

---

*"Clicks are so 2015"* - Embrace the zero-click world with intelligent content transformation.
