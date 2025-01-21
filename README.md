# Using Devcontainers for AI-assisted agile development

This repo exists to demonstrate how to use devcontainers
to isolated AI written code from your workstation.

It is based on the [playbook here](https://github.com/mikegehard/ai-assisted-agile-development/blob/main/playbooks/ai-generated-code-execution.md).

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
