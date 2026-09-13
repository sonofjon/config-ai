- [ ] Use settings.json instead of config.json for copilot, add:

"allowedUrls": [
  "https://docs.github.com"
],

- [ ] Shorten SYSTEM.md? Considering LLM's have evolved rapidly lately also
      the harnessing , perhaps some of our detailed instructions are not
      helpful and potentially even confusing.

- [ ] Should some of our instructions be converted into skills, for example
      instructions for git committing?

- [ ] Quote code identifiers with backticks in the Markdown files, following
      the convention applied in the `tdm.anonymization.python` project
      (commit b6eb225, "TODO.md: Quote code identifiers with backticks",
      with its `TODO.md` as the worked example). Filenames, paths,
      functions, classes, variables and constants are quoted; field and
      column names stay unquoted in any case style. `README.md` carries most
      of the unquoted identifiers.
