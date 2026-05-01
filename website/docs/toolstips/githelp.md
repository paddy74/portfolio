---
tags:
  - git
---

# Using Git

This article contains useful tips for working with Git.

## Fix commits with the wrong `user.name`

It is common for upstream repositories to validate a commit's `user.name` before accepting a push. To fix previous commits that have an invalid `user.name`, amend the respective commits by following the below instructions.

1. Set the correct `user.name` value using `git config --global user.name "YOUR_USER_NAME"`. To only apply this change to the active repository, exclude the `--global` flag.

2. To amend a specific commit:[^1]
   1. Checkout the commit you are trying to modify: `git checkout OLD_COMMIT_HASH`
   2. Amend the commit author: `git commit --amend --author "NEW_AUTHOR_NAME <NEW_AUTHOR_EMAIL>"`
   3. Now you have a new commit.
   4. Replace the old commit with the new one (locally): `git replace OLD_COMMIT_HASH NEW_COMMIT_HASH`
   5. Rewrite all subsequent commits: `git filter-branch -- --all`
   6. Remove the old commit (for cleanliness): `git replace -d OLD_COMMIT_HASH`
   7. Push the new history: `git push --force-with-lease`
      1. Only use `--force` instead of `--force-with-lease` if the latter fails &mdash and only after sanity checking with `git log` and/or `git diff`.
   8. If you are comfortable with rebasing, you can replace steps 4 and 5 with `git rebase -i NEW_COMMIT_HASH`.

3. To amend the most recent commit:[^2]
   1. Amend the commit author: `git commit --amend --reset-author --no-edit`
   2. Push the new history: `git push --force-with-lease`

4. To amend the last N commits:[^2] `git rebase --onto HEAD~N --exec "git commit --amend --reset-author --no-edit" HEAD~N`

[^1]: [StackOverflow | How can I change the commit author for a single commit? (28845565)](https://stackoverflow.com/a/28845565/7706917)

[^2]: [StackOverflow | How can I change the commit author for a single commit? (43231587)](https://stackoverflow.com/a/43231587/7706917)
