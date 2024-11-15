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

## 