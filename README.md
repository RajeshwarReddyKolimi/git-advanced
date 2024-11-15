# git-advanced

## Cherry-pick

- Created a remote repository in github.
- Cloned the repo to local.
- Added file1.md with a sample text.
- Added to staging and committed.
- Created a new branch feature-a here and checked.
- Updated the file1.md by adding some text.
- Added to staging and committed.
- Checked back to main and created a new branch feature-b and checked.
- Here added a new file file2.md and added some text.
- Added to staging and committed.
- Using git log, copied a commit hash for cherry-pick.
- Checked to feature-a and executed the command `git cherry-pick {commitHash}`.
- The changes in feature-b are copied to feature-a.

## Stashing and Cleaning

- Merged feature-a and main.
- 