# Document Policy Compliance Checker with Human-in-the-Loop

A beginner-friendly tutorial demonstrating how to build AI workflows with human oversight using LangGraph.

## Overview

This notebook teaches you how to build an automated document compliance checker that reviews files for policy violations while keeping humans in the decision-making loop. You'll learn core LangGraph concepts through a practical, real-world example inspired by policy compliance work in government and enterprise organizations.

## What You'll Build

An AI agent that:
- Scans documents for policy compliance violations
- **Pauses execution** when it finds potential issues
- **Asks for human confirmation** before continuing
- Resumes processing based on your decisions

You'll build this in two stages:
1. **Pattern matching version** - Fast, free, deterministic (no API key needed)
2. **LLM-enhanced version** - Smarter analysis using Claude (requires Anthropic API key)

## Why Human-in-the-Loop?

Even smart AI systems need human oversight, especially for:
- Compliance and policy enforcement
- Ambiguous cases requiring context or judgment
- Situations where mistakes have real consequences
- Building trust in automated systems

This tutorial shows you how to build workflows where AI handles the tedious scanning work while humans make the final decisions.

## What You'll Learn

- **LangGraph fundamentals**: State management, nodes, edges, and checkpointers
- **Human-in-the-loop patterns**: Using `interrupt()` and `Command(resume=...)` to pause and resume workflows
- **Iterative development**: Starting simple, then adding sophistication
- **Trade-offs**: When to use pattern matching vs. LLM analysis
- **Real-world application**: Why human oversight matters even with advanced AI

## Prerequisites

- Basic Python knowledge
- Familiarity with Jupyter notebooks
- A conda environment (recommended) or pip

**Optional**: Anthropic API key for Part 2 (LLM-enhanced version)
- Get one at https://console.anthropic.com

## Installation using conda 

```bash
conda create -n langgraph-tutorial python=3.13
conda activate langgraph-tutorial
conda install -c conda-forge langgraph langchain-anthropic -y
```

## Quick Start

1. Clone or download this repository
2. Open `policy_compliance_checker.ipynb` in Jupyter
3. Run the cells in order
4. **Part 1 requires no API key** - start here to learn the basics!
5. When ready for Part 2, add your Anthropic API key

## Example Use Cases

This pattern works for many scenarios beyond document compliance:

- **Legal/Compliance**: Reviewing contracts, policies, or regulatory documents
- **Content Moderation**: Flagging content that needs expert review
- **Quality Assurance**: Checking code, documentation, or data quality
- **Medical/Healthcare**: Identifying cases requiring specialist attention
- **Financial**: Reviewing transactions or documents for approval

## Repository Contents

- `policy_compliance_checker.ipynb` - Main tutorial notebook
- `README.md` - This file
- `sample_documents/` - Example files that are created automatically when you run the notebook

## Learn More

- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [Anthropic API Documentation](https://docs.anthropic.com)
- [Explore LangGraph on anaconda.org](https://anaconda.org/search?q=langgraph)

## Extending This Project

Ideas for building on this tutorial:

- Add support for .docx, .pdf, or other file formats
- Implement batch processing for directories
- Generate compliance reports (PDF/HTML)
- Use persistent storage (databases) for checkpoints
- Add multi-user support with role-based review
- Create custom policy templates
- Integrate with document management systems or Slack

## Acknowledgments

- Built with LangGraph 
- Tutorial developed for the Anaconda community