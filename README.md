# Using Devcontainers for AI-assisted agile development

This repo exists to demonstrate how to use devcontainers
to isolate AI written code from your workstation.

It is based on the [playbook here](https://github.com/mikegehard/ai-assisted-agile-development/blob/main/playbooks/ai-generated-code-execution.md).

This is the starting point for all of my development environments for
AI-assisted agile development.

## What are devcontainers?
See the [devconatiners website](https://containers.dev/).

## Why devcontainers?

To isolate our system from security breaches that could possibly be introduced
by LLM generated code.

To standardize the setup of the development environment for our projects.

To easy onboarding for new developers of our project.

## Why isolation?

To allow AI assistants to autonomously iterate on code via command line
tools like running tests, linting, etc that provide context/feedback
to the LLM.

## Tool Installation Approaches

### Dev Containers Features
- **Modular** - Install tools through reusable components from the Dev Container ecosystem
- **Curated** - Community-maintained installers with best practices
- **Portable** - Consistent across different environments (local/CI/cloud)
- **Secure** - Verified installation methods reduce risk of misconfiguration
- **VS Code Integrated** - Automatic configuration with editor extensions

### Raw Dockerfiles
- **Full Control** - Exact control over layer construction and image optimization
- **Minimal Images** - Exclude Dev Container-specific tooling when not needed
- **Build Performance** - Fine-grained cache control for faster builds
- **Production Parity** - Closer match to deployment environments
- **Complex Workflows** - Better support for multi-stage builds and custom networks

**Recommendation**: Use Dev Container features for development environments and Dockerfiles for production images - they can co-exist in the same project!

## Running

1. First, copy example.env to .env and fill in your API keys:
```bash
cp example.env .env
# Edit .env to add your API keys
```

2. Then build and run the devcontainer:
```bash
devcontainer build --workspace-folder .
devcontainer up --workspace-folder .
```

3. You can then either:
- Open a shell in the container:
```bash
devcontainer exec --workspace-folder . /bin/bash
```
- Or run aider directly:
```bash
devcontainer exec --workspace-folder . aider
```
