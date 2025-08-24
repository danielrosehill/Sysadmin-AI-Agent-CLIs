# Sysadmin AI Agent CLIs - Ref

**Date**: August 24, 2025  
**Purpose**: Reference list of CLI tools for local filesystem and remote system operations on Linux machines

## Overview

This repository serves as a personal reference for AI-powered CLI tools that excel at system administration tasks. Traditional AI IDEs often struggle with filesystem operations due to context limitations, while CLI tools offer more focused and efficient approaches to:

- Local filesystem operations
- Remote system management  
- Docker environment optimization
- Code generation for system tasks

## Tool Evaluation Criteria

- **Ubuntu Compatibility**: Native support for Ubuntu/Debian systems
- **Context Efficiency**: Ability to work without full repository context
- **System Operations**: Effectiveness for filesystem and remote operations
- **Standalone Usage**: Can function outside of project repositories

## CLI Tools Reference

| Tool | Ubuntu Compatible | Primary Use Case | Installation Method | Remarks |
|------|:-----------------:|------------------|-------------------|---------|
| **[Gemini CLI](https://github.com/google-gemini/gemini-cli)** | ✅ | Code generation, system scripting | `pip install gemini-cli` | Good for general scripting tasks, handles system operations well |
| **OpenAI Codex** | ✅ | Code completion, refactoring | `pip install openai-codex` | Strong for code optimization, limited system context |
| **[Claude Code](https://www.anthropic.com/claude-code)** | ✅ | Interactive coding, debugging | `npm install -g claude-code` | Excellent conversational interface, good system awareness |
| **[Goose](https://github.com/block/goose)** | ✅ | Automated code generation | See [Goose CLI website](https://goose.ai/cli) for quick launch script | Wide variety of providers, supports OpenRouter for multiple models |
| **[Qwen Code](https://github.com/QwenLM/qwen-code)** | ✅ | Code generation, completion | See GitHub repo for installation | Alibaba's code-focused LLM with CLI interface |
 

## Tool Notes & Observations

### Gemini CLI
- **Advantage**: Large 1 million token context window
- **Observation**: Inference quality often degrades well before reaching the full context limit

### OpenAI Codex
- **Performance**: Strong for code optimization tasks
- **Limitation**: Limited system context awareness

### Claude Code
- **Performance**: Personal favorite for overall performance and conversational interface
- **Drawback**: High API costs make it expensive for extensive use

### Goose CLI
- **Flexibility**: Supports wide variety of providers including OpenRouter
- **Advantage**: Can access multiple models through OpenRouter integration
- **Installation**: Use quick launch script from official website rather than package managers

---

## Methods Of Operation

### Method 1: Local CLI with Remote Access
- Install CLIs locally on your workstation
- Use tools like MCP SSH to access remote systems
- **Advantage**: Centralized tool management
- **Consideration**: Potential confusion about which filesystem context is active

This approach works most effectively when the remote filesystem is constrained by IDE-specific filesystem constraints, sandboxes, dev containers, etc. 

### Method 2: Remote CLI Installation
- Install CLIs directly on remote systems
- SSH into target systems and run tools locally
- **Advantage**: No filesystem context confusion - always working on localhost
- **Advantage**: Clear separation of environments

This approach mitigates against the tendency of agents - even with tools like `MCH-SSH` to get "confused" as to what to do on local vs. remote. Everything is local in this setup. But for generating scripts or code, you may wish to then have the agents push to the repository for proper version control.

**Observation**: Both approaches are viable and work effectively. Choice depends on workflow preferences and security requirements.

---

## Usage Patterns

### Local System Administration
- **Recommended Tool**: Goose CLI works reasonably well for local operations
- **Example Tasks**:
  - Optimizing package management
  - Configuring local management scripts
  - Installing and removing programs
  - Updating package sources
  - System configuration optimization

### Remote System Administration
- **Example Tasks**:
  - Improving server security
  - Security hardening implementations
  - Setting up CI/CD pipelines
  - Streamlining package configurations
  - Remote system optimization

## MCP Pairing

My go-tos for using AI CLIs for "admin":

- **Cloudflare MCP**: Essential for managing Cloudflare services and tunnels
- **Desktop Command**: Local system command execution and management
- **MCP SSH**: Remote system access and command execution
- **Docker MCP**: Container management and Docker environment operations

These MCP tools complement the CLI agents by providing structured access to system resources, enabling more effective automation and management workflows.

