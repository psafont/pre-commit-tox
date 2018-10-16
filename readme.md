
tox for pre-commit
==================

For pre-commit: see https://github.com/pre-commit/pre-commit
For mypy: see https://github.com/tox-dev/tox

### Using tox with pre-commit:

Add this to your `.pre-commit-config.yaml`

```yaml
-   repo: https://github.com/psanfont/tox
    rev: ''  # Use the sha / tag you want to point at
    hooks:
    -   id: tox
```


By default tox will run all environments.
It's recommended to change the behaviour so it runs only the checks
that are fast to run.
To change the arguments, override the `args` as follows:

```yaml
    hooks:
    -   id: mypy
        args: ["-e py27-mypy,py27-lint"]
```
