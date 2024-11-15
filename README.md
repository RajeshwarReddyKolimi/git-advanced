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
- Made some changes to file2.md.
- Didn't stage it.
- Ran `git stash`, and tested stash list using `git stash list`.
- Ran `git clean`, it cleared the recent changes.
- Ran `git stash pop` to apply the stashed files and remove the current stash from stash list.
- Tried to stash the files which aren't tracked and got the response as "No local changes to save".
- Tried again using `git stash -u` and this time the changes are saved and repeated the above process which worked as expected.

## Interactive staging

- Made changes to file2.md and file3.md.
- Entered into interactive staging using `git add -i`.
- First saw the status using `1` which shown the 2 unstage files.
- Then selected `2` which is update to stage the files.
- Tried reverting using `3` and unstaged the files.
- Againg staged them using `2`.

## Undoing changes using `git revert`

- Changed text in file3.md and committed 3 times.
- Using `git log` copied the previous commit hash.
- Using `git revert {commit-hash}` reverted back to previous commit.
- This created a new commit with the previous state.

## Git Reset

- Added a new file file4.md and added some text.
- Stage it and committed
- Tested the 3 options of reset: --soft, --mixed, --hard and checked the status using `git status`.
- The simple `git reset HEAD^` or `git reset --mixed HEAD^` did unstaged the file.
- The `git reset --soft HEAD^` did reverse the commit. i.e file4 moved from committed state to staged state.
- The `git reset --hard HEAD^` did complete removal of changes from working directory, staging and committed states.
- They all does the same thing of moving the pointer back to specified location.

## Git Show

- Tested various uses of `git show`.
- `git show {commit-hash}`: Displayed the detailed info of the commit including commit hash, author, date, commit message, diff.
- `git show {branch-name}`: Displayed the info about the specified branch including commit hash, author, date, commit message, diff.
- `git show {commit-hash}:{filename}`: Displayed the changes of the specified file from the specified commit.
- `git show {commit-hash-1}...{commit-hash-2}`: Displayed the changes between the 2 specified commits.

## Git Interactive rebase

- Currently, we have feature-a, feature-b, main branches.
- Entered interactive rebase mode by `git rebase -i {branch/commit}`.
- Reordered the commits by reordering them in the editor.
- Renamed them by using `r` command.
- combined multiple commits or squashed using `squash` and entered the new commit message when prompted.

## Git reflog

- Ran `git reflog` and understood that it shows not just commit history but also merge, rebase history, branching history.
- It provides above additional details unlike `git log` which only shows commit history.