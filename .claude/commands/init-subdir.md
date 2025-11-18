Initialize a new CLAUDE.md file with subdirectory documentation

Please analyze the subdirectory specified in $ARGUMENTS and create a
CLAUDE.md file for it, following the same principles as the built-in /init
command.

What to add:
1. Commands that will be commonly used for this subdirectory, such as how to
   build, run, and test. Include the necessary commands to work with this
   part of the codebase.
2. High-level code architecture and structure of this module so that future
   instances can be productive more quickly. Focus on the "big picture"
   architecture that requires reading multiple files to understand.

Usage notes:
- If there's already a CLAUDE.md in this subdirectory, suggest improvements
  to it.
- When you make the initial CLAUDE.md, do not repeat yourself and do not
  include obvious instructions like "Provide helpful error messages to
  users", "Write unit tests for all new utilities", "Never include sensitive
  information (API keys, tokens) in code or commits".
- Avoid listing every component or file structure that can be easily
  discovered.
- Don't include generic development practices.
- If there are Cursor rules (in .cursor/rules/ or .cursorrules) or Copilot
  rules (in .github/copilot-instructions.md) in this subdirectory, make sure
  to include the important parts.
- If there is a README.md in this subdirectory, make sure to include the
  important parts.
- Do not make up information such as "Common Development Tasks", "Tips for
  Development", "Support and Documentation" unless this is expressly
  included in other files that you read.
- Do not repeat instructions from the root CLAUDE.md - only add
  module-specific context.
- Be sure to prefix the file with the following text:

```
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working
with code in this subdirectory.

All general project guidelines from /CLAUDE.md in the project root still
apply.
```
