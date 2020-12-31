# Contributing to the project

## Issues
`ISSUE_TEMPALTE.md` will be used to pre-fill any issues created. Logs and detailed
descriptions are extremely helpful and may be required. **DO NOT** report any
issues relating to browser compatibility.

## Pull requests
Please use an open issue and reference that issue in the pull request, as suggested
in `PULL_REQUEST_TEMPLATE.md` (will be pre-filled when opening a pull request).
When you open a pull request, it **MUST** pass test/linting or it cannot be merged.

It is also suggested that you label your branches according to the issue and label,
so a bug reported in issue 14 becomes a branch named `bug/14` and a feature requested
in issue 42 becomes `feature/42`. Do not work directly on master branch, as your
pull request may not end up being accepted, causing your fork to divert.

## Testing
All Pull Requests must pass linting rules set in [`.yaml-lint.yml`](https://github.com/kernvalley/places/blob/master/.github/linters/.yaml-lint.yml). All entries should also validate
on [Google's Rich Results Test](https://search.google.com/test/rich-results) where
possible (*`image` is not currently required here although it is required by Google*).
