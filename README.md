# config-ai
Misc AI chat configuration.

This covers the primary per-tool links (system instructions and settings).
Some tools also link additional directories on top of this (for example
Claude's skills and commands directories, and Gemini's policies directory);
those are only tracked in the setup-dotfiles repo's install.sh, not
duplicated here.

# Claude

ln -s ~/dotfiles/config-ai/SYSTEM.md ~/.claude/CLAUDE.md
ln -s ~/dotfiles/config-ai/.claude/settings.json ~/.claude/settings.json

# Codex

ln -s ~/dotfiles/config-ai/SYSTEM.md ~/.codex/AGENTS.md
ln -s ~/dotfiles/config-ai/.codex/config.toml ~/.codex/config.toml

# Copilot

ln -s ~/dotfiles/config-ai/SYSTEM.md ~/.copilot/copilot-instructions.md
ln -s ~/dotfiles/config-ai/.copilot/settings.json ~/.copilot/settings.json
ln -s ~/dotfiles/config-ai/.copilot/mcp-config.json ~/.copilot/mcp-config.json

# Gemini

ln -s ~/dotfiles/config-ai/SYSTEM.md ~/.gemini/GEMINI.md
ln -s ~/dotfiles/config-ai/.gemini/settings.json ~/.gemini/settings.json
