# Hadolinl

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/faa25d16-f230-4ec7-aca6-75cebe3e7f9b">
</p>

Hadolint is a Dockerfile filter that can detect common problems for you. It uses an Abstract Syntax Tree (AST) to parse your Dockerfile against predefined rule sets. Hadolint also incorporates ShellCheck so you can filter shell scripts in your Dockerfile. RUN instructions as well.
Hadolint has dozens of built-in rules that check for common configuration and security issues. The linter aims to make your Dockerfiles comply with Docker's suggested image creation best practices.

The checks included cover using non-root end users, referencing a relative path in a WORKDIR statement, adding multiple HEALTHCHECK statements, and not using explicitly set labels and versions. Since Hadolint also inherits the ShellCheck rule set, common Bash scripting problems will arise that that tool also identifies.

Rules are identified as numbers with the prefix HL or SC. HL rules are part of Hadolint while SC entries come from ShellCheck. Each check is assigned a severity from Error to Information. If you get errors in your analysis results, those should be the first problems you solve.

## References
- https://alexandre-vazquez.com/hadolint-best-practices-for-your-dockerfiles/
- https://diarioinforme.com/como-usar-hadolint-para-filtrar-sus-dockerfiles/#google_vignette​
