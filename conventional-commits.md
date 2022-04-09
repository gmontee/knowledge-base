# Conventional Commits
A [specification](https://www.conventionalcommits.org/en/v1.0.0/) for adding human and machine readable meaning to commit messages

The commit message should be structured as follows:

<type>[optional scope]: <description>

[optional body]
  
[optional footer(s)]
  
---
  
The commit contains the following structural elements, to communicate intent to the consumers of your library:

fix: a commit of the type fix patches a bug in your codebase (this correlates with PATCH in Semantic Versioning).
feat: a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.
types other than fix: and feat: are allowed, for example @commitlint/config-conventional (based on the the Angular convention) recommends build:, chore:, ci:, docs:, style:, refactor:, perf:, test:, and others.
footers other than BREAKING CHANGE: <description> may be provided and follow a convention similar to git trailer format.
  
Examples
feat: allow provided config object to extend other configs
feat(api)!: send an email to the customer when a product is shipped
docs: correct spelling of CHANGELOG
feat(lang): add Polish language
