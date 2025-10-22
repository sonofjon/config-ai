# Programming instructions

## General

1. Ensure lines do not exceed 79 characters.

2. Don't include the data type in variable names, for example a string
   variable containing an address should be named 'address', not
   'addess_str'; a class containing animal types should be named 'Animals',
   not 'AnimalsClass'.

3. Always add docstrings when new functions, classes and modules (and other
   constructs) are introduced.

4. The first line of a docstring (the summary line) should be a single
   sentence less than 80 characters long, using imperative mood (e.g.,
   'Return the user's full name.'). Following sentences should use
   third-person present (indicative) (e.g., 'Returns the user's full
   name.').

5. When you rewrite or move code, never remove code comments that were
   present in the original code.

6. Code Consistency: Maintain strict consistency with existing code patterns
   by: (a) using search tools to find similar functions before
   implementation, (b) analyzing their naming conventions, documentation
   style, error handling, and formatting patterns, and (c) verifying that
   new code adhere to the same rules.

## Documentation

1. If a README.md or other documentation file exists for the current
   project, always keep it up-to-date with any code changes applied.

## Tests

1. If a test suite exist for the current code project, always keep it
   up-to-date with any code changes applied.

   project, always keep it up-to-date with any code changes applied.

## Languages

### Python

1. Use the "Google Python Style Guide" for programming style.

2. Import statements should always be placed at the top of a module, never
  inline in the code.

3. Don't use type annotations in function definitions.

### Emacs Lisp (elisp)

1. All function arguments should be documented in the docstring.
