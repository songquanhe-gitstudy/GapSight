# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**GapSight** ("缺口之眼") is a project focused on identifying and visualizing gaps between requirements and current state. The name translates to "The Eye of the Gap" - a tool designed to see and analyze discrepancies.

**Current State**: Early stage project with minimal implementation. The repository is in its initial phase with only basic structure in place.

## Development Setup

Since this is a Python-based project (indicated by the `.py` file in the youtube directory), the following setup is recommended:

### Python Environment
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies (when requirements.txt exists)
pip install -r requirements.txt
```

### Essential Dependencies to Consider
Based on the project name and YouTube directory, the project will likely need:
- `requests` or `httpx` - for HTTP requests
- `pydantic` - for data validation
- `click` or `argparse` - for CLI interface
- `pytest` - for testing
- `black` - for code formatting
- `ruff` - for linting

## Architecture

The project structure suggests a modular approach:

```
GapSight/
├── src/                 # Main source code
│   ├── core/           # Core gap analysis logic
│   ├── adapters/       # External system integrations
│   └── utils/          # Shared utilities
├── youtube/            # YouTube-specific functionality
├── tests/              # Test suite
├── docs/               # Documentation
└── scripts/            # Utility scripts
```

### Core Concepts (To Be Implemented)

1. **Gap Analysis Engine**: Core logic for identifying discrepancies
2. **Data Collection**: Modules for gathering current state data
3. **Requirements Parser**: Tools for processing requirement definitions
4. **Visualization**: Components for presenting gap analysis results
5. **Integrations**: Adapters for external systems (starting with YouTube)

## Development Workflow

### Code Style
- Use **Black** for code formatting: `black .`
- Use **Ruff** for linting: `ruff check .`
- Follow PEP 8 style guidelines
- Use type hints throughout the codebase

### Testing
```bash
# Run all tests
pytest

# Run tests with coverage
pytest --cov=src

# Run specific test file
pytest tests/test_specific.py
```

### Git Workflow
- Create feature branches from `main`
- Use descriptive commit messages
- Ensure all tests pass before creating PR
- Include documentation updates with code changes

## Key Principles

1. **Modularity**: Build components that can work independently
2. **Extensibility**: Design for easy addition of new data sources
3. **Clarity**: Make gap analysis results clear and actionable
4. **Reliability**: Handle errors gracefully and provide meaningful feedback

## Getting Started for New Developers

1. Clone the repository
2. Set up Python virtual environment
3. Install dependencies (requirements.txt to be created)
4. Run existing tests to verify setup
5. Check existing issues for good starter tasks
6. Read through the core modules to understand the architecture

## Notes

- This project is in its initial phase, many architectural decisions are yet to be made
- The YouTube directory suggests video content analysis as a primary use case
- Contributions to defining the project's architecture and tech stack are welcome
- Focus should be on creating a robust gap analysis framework that can work across domains