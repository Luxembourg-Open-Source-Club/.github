# Club General Conventions
This document presents the general conventions that our club shall follow in order to
be consistent across all the organization repositories.

## Table of Contents
<!--toc:start-->
- [Commits Conventions](#commits-conventions)
    - [Some examples](#some-examples)
- [Branch Conventions](#branch-conventions)
- [Code Formatting](#code-formatting)
<!--toc:end-->


## Commits Conventions

Commits are an essential part for contributing and letting others and know what has been 
done or changed. For this reason, our commits will need to have some meaning.

In order to clearly indicate what the commit addresses, we will be using labels, where they are enclosed with `[]`
Each commit will have one label at the beginning. The possible labels are:

- `[feature]`: Use this label in case the commit represents the implementation of a new feature;

- `[fix]`: Use this label in case the commit fixes a bug;

- `[refactor]`: Use this label in case you have modified the codebase, where it does not affect 
the integrity of the code. This can be for example the addition of a docstring;

- `[docs]`: Use this label in case you have modified documentation files, such as
the README;

- `[chore]`: Use this label in case the commit does not affect the source code,
but things like dependencies;

- `[test]`: Use this label in case the commit affects only test files/cases;

- `[style]`: Use this label in case the commit only contains changes when 
formatting has been applied;

- `[perf]`: Use this label in case the commit improves performance;

- `[build]`: Use this label in case the commit affects the build system. 
This should be the case in compiled languages such as C/C++. An example would be a CMakelists.txt;

- `[revert]`: Use this label in case the commit reverts to a previous commit.

When writing the actual commit message, ensure it is clear, concise, and descriptive, 
summarizing the purpose of the commit. Use the present tense and a brief sentence format. 
If necessary, provide extra details in the commit body.

Additionally, you can reference an issue if the commit is based on one. 
For example, if there is an issue addressing a bug, the commit that fixes that bug can be referenced. 
To reference an issue, use #issue_number.

Finally, commits should contain as small and focused changes as possible. 
Each commit should address a single logical change.

### Some examples

- `[fix] Fix bug X (#12)`

- `[feature] Implement feature Y (#32)`

- `[misc] Rename file to Z`

## Branch Conventions

Consistent branch naming and usage are important for effective collaboration and project management.


To maintain consistency across branch names, we also have some naming conventions. These follow closely to the issues.
Once working on an issue, the branch name should be named according to the issue label. For example, if you have an issued labeled as bug,
the branch should be named starting with the prefix `bugfix/.`

1. **Branch Naming:** Use descriptive and meaningful names for branches. Include a prefix that indicates the type of branch (the prefix should be related to the issued label). Here are some common prefixes and examples:

    - `feature/`: Use this prefix for branches related to adding new features. For example, `feature/my-feature`.
    - `bugfix/`: Use this prefix for branches addressing specific bugs or issues. For example, `bugfix/fix-issue`.
    - `refactor/`: Use this prefix for branches focused on code refactoring. For example, `refactor/code-refactor`.
    - `docs/`: Use this prefix for branches involving documentation updates. For example, `docs/update-docs`.

1. **Main Branches:** Keep the repository's main branches stable and production-ready. The following branches are commonly used:

    - `main`: The main branch containing the production-ready code.
    - `dev`: The branch where ongoing development and integration take place.

Whenever everything has been accomplished related to the branch, perform a pull-request to the `dev` branch. 
If everything is fine, the changes made will be reviewed by the repository responsible and then merged into the `dev` branch.

## Code Formatting

When coding, it is important to maintain a consistent stucture throughout the entire code base of any repository. For this matter, we enforce the use of formatting tools which will ensure that everyone will use the same format. Different formatters are available for each programming language and thus there is no formatter that will work for every programming language. 

Since we will be mostly coding in Python, the formatter that we have chosen is `black`. If using Vs Code, you can activate this in your settings. You can then format the code by hitting the keys combination (Ctrl + Shift + i in linux/windows) in order to perform the formatting. In addition, you can also toggle in Vs Code settings `Format On Save`, which will format the file every time you save it.
