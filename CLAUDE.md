# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an AI development setup repository that configures multiple Model Context Protocol (MCP) servers for enhanced AI capabilities. The repository serves as a centralized configuration hub for various AI tools and services.

## MCP Server Configuration

The project uses `.mcp.json` to configure the following MCP servers:
- **databricks**: For Databricks SQL warehouse operations
- **github**: For GitHub API interactions (requires GITHUB_PERSONAL_ACCESS_TOKEN in .env)
- **context7**: For retrieving up-to-date library documentation
- **sequential-thinking**: For complex problem-solving workflows
- **puppeteer**: For browser automation
- **fetch**: For web content retrieval
- **magic**: For UI component generation (requires 21ST_DEV_API_KEY)
- **playwright**: For browser testing and automation
- **serena**: For semantic code analysis and editing

## Environment Setup

1. Copy `.env.example` to `.env`
2. Add required API keys:
   - `GITHUB_PERSONAL_ACCESS_TOKEN`: For GitHub operations
   - `DATABRICKS_HOST`, `DATABRICKS_TOKEN`, `DATABRICKS_HTTP_PATH`: For Databricks access
   - `21ST_DEV_API_KEY`: For magic UI component generation (configured in ~/repos/ai_setup/.env)
   - Other optional API keys as needed

## Project Structure

- `.mcp.json`: MCP server configurations
- `.serena.yaml`: Serena project configuration for code analysis
- `.serena/project.yml`: Detailed Serena project settings
- `.env.example`: Template for environment variables
- `.gitignore`: Comprehensive ignore patterns for various development environments

## Serena Configuration

The project is configured for Python and SQL development with:
- Full editing, search, and symbol capabilities enabled
- Language server support for Python and SQL
- Project-specific memory storage in `.serena/memories/`

## Development Notes

- The repository uses LF line endings (Unix-style) by default, with CRLF for Windows batch/cmd files
- Git tracking is active on the main branch
- Environment files (.env) are gitignored for security
- Claude-specific files (CLAUDE.md, logs, backups) are tracked or ignored as configured