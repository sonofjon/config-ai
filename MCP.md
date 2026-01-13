# MCP Server Configuration

This document describes MCP (Model Context Protocol) servers that provide AI
agents access to Emacs internals, and how to configure them for various AI
tools.

## MCP Servers

### mcp-server (Pure Elisp MCP Server)

General-purpose MCP server that exposes Emacs functionality to
LLMs. Provides tools for reading and writing buffers, executing Elisp code,
getting diagnostics from flycheck/flymake, running interactive commands, and
managing files and windows. Includes comprehensive security controls with
permission prompts for dangerous operations and sensitive file protection.

### elisp-dev-mcp (MCP Server for Agentic Elisp Development)

Specialized MCP server for Elisp development workflows. Provides tools for
describing functions and variables, retrieving function definitions with
source locations, looking up symbols in Info documentation, and reading
Elisp source files from package directories. Designed to help LLMs
understand and work with Emacs Lisp codebases.

## Configuration

### Claude/Gemini

#### mcp-server

**One-time Setup**

Option 1: Wrapper Script

```bash
{claude | gemini} mcp add -s user mcp-server \
  ~/.emacs.d/elpa/mcp-server/mcp-wrapper.sh \
  ~/.emacs.d/emacs-mcp-server.sock
```

Option 2: Direct socat

Prerequisites: `socat` (install with `sudo apt-get install socat`)

```bash
{claude | gemini} mcp add -s user mcp-server-direct \
  socat - UNIX-CONNECT:$HOME/.emacs.d/emacs-mcp-server.sock
```

**Every Session**

Start the MCP server in Emacs:

```
M-x mcp-server-start-unix
```

Or configure automatic startup via `emacs-startup-hook`.

#### elisp-dev-mcp

**One-time Setup**

1. Get the install script in Emacs:

```
M-x mcp-server-lib-install
```

2. Register with Claude or Gemini:

```bash
{claude | gemini} mcp add -s user -t stdio elisp-dev \
  ~/.emacs.d/emacs-mcp-stdio.sh --init-function=elisp-dev-mcp-enable \
  --stop-function=elisp-dev-mcp-disable --server-id=elisp-dev-mcp
```

**Every Session**

1. Start Emacs server:

```
M-x server-start
```

2. Start MCP server:

```
M-x mcp-server-lib-start
```

Or configure automatic startup via `emacs-startup-hook`.

### Copilot CLI

Edit `~/.copilot/config.json` and add an `mcpServers` section:

```json
{
  "mcpServers": {
    "mcp-server": {
      "command": "/home/joohv/.emacs.d/elpa/mcp-server/mcp-wrapper.sh",
      "args": ["/home/joohv/.emacs.d/emacs-mcp-server.sock"]
    },
    "mcp-server-direct": {
      "command": "socat",
      "args": ["-", "UNIX-CONNECT:/home/joohv/.emacs.d/emacs-mcp-server.sock"]
    },
    "elisp-dev": {
      "command": "/home/joohv/.emacs.d/emacs-mcp-stdio.sh",
      "args": [
        "--init-function=elisp-dev-mcp-enable",
        "--stop-function=elisp-dev-mcp-disable",
        "--server-id=elisp-dev-mcp"
      ]
    }
  }
}
```

**Configuration Format**

Each MCP server entry requires:

- **Server name**: Unique identifier
- **command**: Path to executable or command name
- **args**: Array of command-line arguments
