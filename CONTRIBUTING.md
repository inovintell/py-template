# Contributing

__This repository uses [gh-flow](https://github.com/inovintell/gh-flow) for
collaboration.__

> Please use it if possible, it automates most of the processes described below.

You can see additional labels for issues/PRs
[here](https://github.com/{{cookiecutter.repository_owner}}/{{cookiecutter.repository}}/labels)

## Commits

### Messages

Commits are required to follow
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
with the exact form:

```bash
<type>[!]: <description>

[optional body]

[footers]
```

Type can be __ONLY__ one of (based on
[Angular guidelines](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#commits):

- `feat` - new feature, corresponds to `MINOR` in [Semantic Versioning](https://semver.org/)
- `fix` - fix code bud, corresonds to `FIX` in [Semantic Versioning](https://semver.org/)

Adding `!` __AFTER `type`__ means `BREAKING CHANGE` and corresponds to `MAJOR`
in [Semantic Versioning](https://semver.org/).

Things to note:

- __`MAJOR` HAS NO SPECIAL MEANING IN CASE OF THIS SOFTWARE (it is treated
simply as an indication of breaking change)__
- __Additional context (e.g. scope) should be specified as a label__

> __For easiest collaboration please consider using
[gh-flow](https://github.com/inovintell/gh-flow) GitHub CLI extension
automating most of the tasks described above!__

### Linting

Each commit (either during `push` or `pull request`) is automatically linted
against the above schema.

## Branches

- __`main` branch is always releasable__
- __Each branch is created from `main`__ - each branch should be responsible
for __small__ semantic unit of work and consist of __up to a few commits__.
- __Each branch is named by a number__ which corresponds to issue ID.
It should be merged with `main` as soon as possible (and as soon as CI runs
successfully).
- __Each branch is squashed before merging__ - changes should have in-depth
description within an issue.

> __For easiest collaboration please consider using
[gh-flow](https://github.com/inovintell/gh-flow) GitHub CLI extension
automating most of the tasks described above!__

## Issues

Please use pre-made `bug` or `feature` forms to file an issue.

Your issue will be picked up by someone, __please don't @ team members!__

## Releases

Releases follow [semantic-release](https://github.com/semantic-release/semantic-release)
guidelines. Due to semantic commits with scope limited
to `feat`/`fix`/`breaking` each merged commit into main
__should entail new release of software__.
