# Bug description

This repository describes a bug in git `v2.13.0`.

If you have a merge commit (maybe any commit) that contains `\r\n` the command
`git branch -v` (and `git branch -vv` as well as `git branch -avv`) will show weird behaviour.

Parts from the body of the message will appear at the start of the line (were the branch name usually is).

In this repository the merge commit (`de3de0555fec83496b83d8dc279da0a6e9223d58`) shows the mentioned behaviour.

Older versions of git don't have this problem.

To see for yourself: Check out the branch `bad-commit` and run `git branch -v`
