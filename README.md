# Solution for gitleaks pre-commit check of sensitive information

## 1. Install pre-commit from [https://pre-commit.com/#install](https://pre-commit.com/#install)

```bash
pip install pre-commit
```
Run this command in your repository for initiate pre-commit

```bash
$ pre-commit install
pre-commit installed at .git/hooks/pre-commit
```
Copy **.pre-commit-config.yaml** and **install-gitleaks.py** in your repository.

## 2. Enabling and disabling of the Gitleaks pre-commit hook

Enebling hook

```bash
git config hooks.gitleaks true
```

After that manipulation pre-commit check of sensitive information will be activated.

If you want to desable Gitleaks pre-commit hook, you should run next command

```bash
git config hooks.gitleaks false
```

## Additional information:
### Usage of GitLeaks [https://github.com/gitleaks/gitleaks](https://github.com/gitleaks/gitleaks)

```bash
Usage:
  gitleaks [command]

Available Commands:
  completion  generate the autocompletion script for the specified shell
  detect      detect secrets in code
  help        Help about any command
  protect     protect secrets in code
  version     display gitleaks version

Flags:
  -b, --baseline-path string       path to baseline with issues that can be ignored
  -c, --config string              config file path
                                   order of precedence:
                                   1. --config/-c
                                   2. env var GITLEAKS_CONFIG
                                   3. (--source/-s)/.gitleaks.toml
                                   If none of the three options are used, then gitleaks will use the default config
      --exit-code int              exit code when leaks have been encountered (default 1)
  -h, --help                       help for gitleaks
  -l, --log-level string           log level (trace, debug, info, warn, error, fatal) (default "info")
      --max-target-megabytes int   files larger than this will be skipped
      --no-color                   turn off color for verbose output
      --no-banner                  suppress banner
      --redact                     redact secrets from logs and stdout
  -f, --report-format string       output format (json, csv, junit, sarif) (default "json")
  -r, --report-path string         report file
  -s, --source string              path to source (default ".")
  -v, --verbose                    show verbose output from scan

Use "gitleaks [command] --help" for more information about a command.
```
