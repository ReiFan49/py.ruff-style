# Python Style Guide

## About the Rules

- Guide heading may be renamed, as there's no way to standardize them in two-way resolution.
- These rules will adapt based on how much project personal I have linted on.

## Guides

### line-length

Each line are recommended to have at most **128 characters** long.

### docstring-convention / flake8-quotes.docstring-quotes / pydocstyle.convention

Docstrings are **single quoted**, with **newlines surrounding the contents**.

```py
def fun():
  '''
  This is a function.
  '''
  ...
```

Docstrings on public module/package **do not need to be documented**.

Docstrings content need to be clear about it's purpose, but there are no imperative enforcement applied.

Enabled Linters: `D`, `D213`.
Disabled Linters: `D100`, `D104`, `D200`, `D203`, `D204`, `D212`, `D300`, `D401`, `D415`.

### isort.section-order

Import order are grouped into `future`, `standard library`, `third party`, `first party`, `local folder`.

### isort.split-on-trailing-comma

Multiline imports **requires trailing comma** at the end of a set of import statement line.

### ruff.default-linters

Currently there are no plans from fully freezing the linting rule.

### flake8-logging

The use of `logging` module is recommended and understanding a good practice to use it is needed.

Enabled Linters: `LOG`.

### flake8-no-pep420

Avoid the use of *namespace package* when possible, it is not recommended in general.

Enabled Linters: `INP`.

### flake8-pie

Pie linter has decent style enforcement to follow.

Enabled Linters: `PIE`.

### flake8-print

Following the use of `logging`, explicit `print`-related functions are not recommended instead.
`logging` allows much more granular in terms of output related control, especially it allows to find out the source
and when does it happens in the first place.

Enabled Linters: `T20`.

### flake8-return

Branch cutting efficiency in general are good.

However there's an exception, `if`/`else` that has explicit `return` on either ends are fine to be written.

Enabled Linters: `RET`.
Disabled Linters: `RET505`.

### flake8-slots

`__slots__` definition are required when subclassing an immutable built-in class such as `str`, `tuple` or `namedtuple`.

Enabled Linters: `SLOT`.

### flake8-simplify

Simplification linter provides good set amount of linting rules to follow.

Enabled Linters: `SIM`.

### pycodestyle.multiple-imports-on-one-line

Multiple imports are fine within the same line.

Disabled Linter: `E401`.

### Pyflakes.star-import

The use of star imports are to copy the variables (reference) into the module's variable.
This can be improved further by a clever metaprogramming.

Disabled Linter: `F403`, `F405`.

### flake8-commas.missing-trailing-comma

Parameters, Lists or Dictionary Entries that spans over multiple lines are required to have **trailing comma**.

Enabled Linters: `COM812`.

### flake8-pie.unnecessary-placeholder

A placeholder function with a docstring should have it's placeholder statement left behind rather than leaving it just
with the docstring alone.

Disabled Linters: `PIE790`.

### flake8-simplify.open-file-with-context-handler

File handing through context manager only applies if the file can be solved directly.
Advanced file handling cannot make use of context-based file handler.

Disabled Linters: `SIM115`.

### format.quote-style

Project string quotation prefers the use of **single quotes** whenever possible.

### format.indent-style

Project indentation uses **2-width spaces**.
