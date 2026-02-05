---
name: analyze-project
description: Analyze a project's features, architecture, and implementation details without modifying any files.
---

# Project Analysis

## Overview

Perform comprehensive project analysis across three dimensions: **Features**, **Architecture**, and **Implementation**. Provide actionable insights with specific file paths and line references.

**Core principle:** Read and understand, never modify. Always provide concrete code references.

**Announce at start:** "I'm analyzing this project's features, architecture, and implementation."

${languageInstruction}

## Critical Constraints

- **READ-ONLY** - Do not edit or create any files
- **NO CODE GENERATION** - Only reference existing code
- **ALWAYS CITE SOURCES** - Include `file:line` references for all code mentions

## Analysis Process

### Phase 1: Feature Discovery

**Goal:** Identify what the project does.

**Steps:**

1. Find entry points (main files, CLI commands, API routes)
2. Identify feature modules and their responsibilities
3. List public APIs and interfaces
4. Document configuration options

### Phase 2: Architecture Analysis

**Goal:** Understand how the project is organized.

**Steps:**

1. Identify tech stack (language, runtime, framework, build tools)
2. Analyze third-party dependencies and their purposes
3. Map source directory structure with file purposes
4. Identify core components and their relationships
5. Trace data flow (input → processing → output)
6. Identify design patterns used

### Phase 3: Implementation Deep Dive

**Goal:** Understand how key features are implemented.

**Steps:**

1. Trace code paths for core features
2. Document key algorithms and logic
3. Identify important classes/functions and their roles
4. Find extension points and customization options

## Output Format

```markdown
# Project Analysis: [Project Name]

## Overview

[One paragraph describing what the project does]

## Features

| Feature | Description | Entry Point |
|---------|-------------|-------------|
| [name] | [what it does] | [file:line] |

## Architecture

### Tech Stack

| Category | Technology |
|----------|------------|
| Language | [e.g., TypeScript 5.x] |
| Runtime | [e.g., Node.js 20] |
| Framework | [e.g., Express, React] |
| Build Tool | [e.g., Vite, Webpack] |

### Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| [name] | [version] | [what it does] |

### Source Structure

project/
├── src/                # Source code
│   ├── core/           # Core business logic
│   │   ├── index.ts    # Module entry
│   │   └── types.ts    # Type definitions
│   ├── utils/          # Utility functions
│   └── index.ts        # Main entry point
├── tests/              # Test files
├── package.json        # Project configuration
└── tsconfig.json       # TypeScript configuration

**Key Files:**

| Path | Purpose |
|------|---------|
| `src/index.ts` | Main entry, exports public API |
| `src/core/` | Core business logic |
| `src/utils/` | Shared utility functions |

### Core Components

| Component | Location | Responsibility |
|-----------|----------|----------------|
| [name] | [file:line] | [what it does] |

### Data Flow

[Input] → [Processing Stage 1] → [Processing Stage 2] → [Output]

### Design Patterns

| Pattern | Location | Purpose |
|---------|----------|---------|
| [pattern name] | [file:line] | [why it's used] |

## Implementation Details

### [Feature Name]

- **Entry:** `file.ts:line`
- **Code Path:** file1.ts:10 → file2.ts:25 → file3.ts:100
- **Key Logic:** [explanation of algorithm/approach]
- **Extension Points:** [how to customize/extend]
```

## Guidelines

- Use tables for structured data (features, dependencies, components)
- Use tree diagrams for directory structure
- Use flow notation (→) for data flow and code paths
- Always include file:line references
- Focus on the three dimensions: features, architecture, implementation
- Identify patterns and design decisions

Arguments: ${args}
