# Python Style Guide in Ruff

Personal style preference when developing with Python using Ruff.

## Adoption with Ruff

1. Import the config into your project by doing  `git submodule add <this repository link> <your project top folder>/.ruff_config`. **Make sure to not directly copy these as you need to replace both URL and the folder you were on.**
  a. In any case the target repository is on local as well, make sure to put `--reference <path to local copy>` during the addition/update.
2. Create a ruff configuration either through any of `.ruff.toml`, `ruff.toml`, `pyproject.toml`, and declare `extend = ".ruff_config/baseline.toml"`. Feel free to replace `baseline.toml` with any other file that exists within this repository.
  a. If you are using `.ruff.toml` or `ruff.toml`, put it on the top of the file.
  b. If you are using `pyproject.toml`, make sure to declare `[tool.ruff]` and put it directly after the said section declaration line.
3. Start extending your own or project-specific rules by tinkering the ruff configuration further. It's strongly advised to not define `select` or `ignore` on the ruff configuration as it'll override any previously configured linting rules.

Note:

- I may host this on several repositories, so I did not put the repository link explicitly. Thank you.

### `ruff.toml` snippet example

```toml
extend = ".ruff_config/baseline.toml"
...
```

### `pyproject.toml` snippet example

```toml
...
[tool.ruff]
extend = ".ruff_config/baseline.toml"
...
```

## Rules

What does each rules do? Check RULES.md instead.

## Licnese

zlib
