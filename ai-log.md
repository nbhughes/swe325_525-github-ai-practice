## AI interaction 1

Date: 9/28/2026

Assistant: U-M GPT

Prompt: Explain the difference between a repository, branch, commit, pull request, and issue.

Response:

These are core concepts in Git and platforms such as GitHub or GitLab:

- Repository (repo): The project’s main container. It holds files, folders, code, and the complete history of changes.Think: the entire project and its filing cabinet.

- Branch: An independent line of development within a repository. You can change files on a branch without immediately affecting the main version, often called main.Think: a working copy for a particular feature or fix.

- Commit: A saved snapshot of changes on a branch. Each commit has a unique identifier and usually a message explaining what changed.Think: a checkpoint in the project’s history.

- Pull request (PR): A proposal to merge changes from one branch into another. It provides a place to review the differences, discuss the work, run automated checks, and approve or reject the changes.Think: “Please review and incorporate my branch.”

- Issue: A tracked task, bug report, feature request, or discussion. An issue describes work that may need to happen but does not itself contain code changes.Think: an item on the project’s to-do list.


Typical workflow

1. An issue is created for a bug.
2. A developer creates a branch in the repository.
3. They make changes and save them as one or more commits.
4. They open a pull request to merge the branch into main.
5. After review and testing, the pull request is merged, often closing the issue.

In short: repository = project, branch = workspace, commit = saved checkpoint, pull request = merge proposal, issue = tracked work.

## AI interaction 2

Date: 9/28/2026

Assistant: U-M GPT

Prompt: Suggest a checklist for a complete pull-request description.

Response:

Pull-request description checklist
Summary

 Explain what changed in one or two sentences.
 State why the change is needed.
 Identify the user, system, or workflow affected.

Related work

 Link the relevant issue, ticket, or design document.
 Use an automatic-closing keyword when appropriate, such as Closes #123.
 Mention related or dependent pull requests.

Scope

- List the major changes included.
- Clearly state what is not included.
- Call out unrelated cleanup or refactoring.
- Keep the pull request focused enough to review effectively.

Implementation

- Summarize the technical approach.
- Explain important design decisions and tradeoffs.
- Identify new dependencies, configuration, migrations, feature flags, or infrastructure changes.
- Note any departures from established project patterns.

Testing and validation

- List automated tests added or updated.
- Provide exact commands used to test.
- Describe manual testing steps.
- State the expected results.
- Cover important edge cases and failure paths.
- Explain any tests that were skipped or could not be completed.

Evidence

- Include screenshots or recordings for visual changes.
- Include before-and-after examples when helpful.
- Provide relevant logs, benchmark results, or API examples.
- Add accessible text descriptions for important images.

Impact and risk

- Identify breaking or backward-incompatible changes.
- Describe performance, security, privacy, accessibility, and data impacts.
- Note affected services, APIs, users, or platforms.
- Describe known limitations or unresolved concerns.
- Assign a risk level if your team uses one.

Deployment and rollback

- Explain the deployment sequence.
- Include database migration or data-backfill steps.
- Mention required environment variables or configuration changes without including secrets.
- Describe monitoring or post-deployment verification.
- Provide a rollback or recovery plan.

Reviewer guidance

- Highlight the files or decisions that need the closest review.
- Call out generated files or code that can be reviewed lightly.
- List specific questions for reviewers.
- Identify appropriate reviewers or code owners.

Final checks

- The branch is up to date and merge conflicts are resolved.
- Continuous integration checks pass.
- Documentation and release notes are updated if needed.
- Temporary debugging code and commented-out code are removed.
- No credentials, secrets, or sensitive data are included.
- Commit history meets the project’s conventions.
- The pull request is marked Draft if it is not ready to merge.

## AI interaction 3

Date: 9/28/2026

Assistant: U-M GPT

Prompt: Explain what a GitHub history view shows.

Response:

A GitHub history view shows how a repository, branch, or individual file has changed over time. Depending on where you open History, it typically includes:

- Commit list: Each saved checkpoint, usually newest first.
- Commit message: The author’s summary of the change.
- Author and date: Who created the commit and when.
- Commit identifier: A unique SHA hash, often displayed in abbreviated form.
- Changed files: Opening a commit shows files added, modified, renamed, or deleted.
- Diffs: Line-by-line changes, with additions and deletions clearly marked.
- Parent relationships: How commits connect, including merges between branches.
- Pull-request or issue links: Commits may reference the pull request or issue associated with the work.
- Status information: Some views show whether automated checks passed and whether a commit is verified.

Common history views

Repository or branch history

Shows commits reachable from the selected branch. This helps answer:

- What changed recently?
- Who made each change?
- When was a feature or fix introduced?
- Was a commit merged from another branch?

Changing the selected branch may produce a different history.

File history

Shows only commits that affected a particular file. This helps trace when and why that file changed.
A file’s history can become harder to follow after a rename or move, depending on how the change was committed and displayed.

Line history with Blame

GitHub’s Blame view shows the most recent commit responsible for each line or block of a file. Despite the name, it is primarily a diagnostic tool for finding context—not assigning fault.

Important distinction

History records committed changes. It does not normally show:

- Unsaved edits
- Uncommitted local changes
- Commits that exist only on someone’s computer
- Deleted branches whose commits are no longer reachable
- Every discussion or decision behind a change

In short, the history view is the project’s timeline of committed changes, while pull requests and issues usually provide more context about why those changes were made.
