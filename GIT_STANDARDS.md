# Git Standards

### Workflow

In order to facilitate the simplest, most effective and asynchronous workflow, I will follow the GitHub flow for version control (in a simplified form). This is because it allows the highest degree of flexibility and is the simplest to onboard into. 

> Create a branch > Make changes > PR into master > Merge into master

### Branches

In order to sort through branches effectively (as humans and machines) it's important that there be a naming convention for branches (other than master). The naming convention I will use is as follows.

- `feature/<pithy-feature-description>` - for any branch which contains code that will introduce a new feature for the end consumer.
- `bugfix/<pithy-description-of-bug>` - for any branch which contains code that does not introduce new functionality, but remediates unintended side-effects of previously introduced functionality to the end consumer
- `hotfix/<pithy-fix-description>` - for any branch which contains time-sensitive code fixes that need to move into production as soon as humanly possible. This branch prefix is a special case that can (when appropriate) skip continuous integration steps and should be prioritized for review above all others.

### Commits

Commit messages are the living history of code and as such should be concise, readable and communicate precisely the changes that are held within that commit. Here I will stand on the shoulders of giants and rely on the community-backed [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) for guidance on how to write commit messages with a standard formatting, with a small change however, that commit messages NOT include a body and footer and keep themselves to a single line (of at minimum a type and 25 characters). While the official specification relies on only 2 main types of commits, I will rely on the following list of commit types.

- `feat: <at least 25 characters>` - for commits that introduce new functionality to the code.
- `fix: <at least 25 characters>` - for commits that mediate unintended issues with previously added functionality in the code.
- `docs: <at least 25 characters>` - for commits that document existing code or functionality of the code.
- `style: <at least 25 characters> `- for commits that do not change the operation of the code but merely the styling of that code or of the interfaces that code exposes.
- `refactor: <at least 25 characters>` - for commits that make no change in the operation of the code, but simply make the code more human readable.
- `perf: <at least 25 characters>`  - for commits that do not change the end consumer interface but do contain performance improvements for the end consumer of the code.
- `test: <at least 25 characters>` - for commits that contain testing of existing code and its functionality for the end consumer.
- `ci: <at least 25 characters>` - for commits that do not change the functionality of the code or functionality for the end consumer but that make changes to the continuous integration or deployment of the code to the end consumer.
- `chore: <at least 25 characters>` - for commits that contain small, non-functional changes that maintain the codebase. For example, updating dependencies, adding tags etc.
- `revert: <at least 25 characters>` - for commits that revert previously implemented code to a previous version but that do not contain any new functionality that did not exist in previous versions. This commit type is added to allow for a linear history of the codebase, while still allowing for the possibility of rollbacks within the codebase.
