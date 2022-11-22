## Cherry Picking
<p align="center">
    <img src="../assets/cherry.png" alt="cherry" width="200" height="200"/>
</p>

This is the act of picking a commit from a branch and applying it to another.

For example, 2 devs are working on separate feature branches. One implements a system wide bug fix on their branch. The other dev can add the bug fix commit to their branch by picking it by reference and appending it to their current working branch(HEAD).

### When to use it
- Team collaboration
- Bug hotfixes
- Undoing changes and restoring lost commits.

### How to use it
```bash
# make sure you've fetched all remotes
$ git fetch --all
# get back to the branch you want to cherry pick to
$ git checkout <my-feature-branch>
# then grab the commit SHA and run the cherry pick.
# the flag -x adds the dev1's commit message to your history.
$ git cherry-pick -x <commit-SHA>
```

A successful cherry pick should display a change log.
e.g
```bash
[<my-feature-branch> <commit-hash>] Commit message
 Author: Dev 1 details
 Date: Mon Nov 21 21:46:39 2022 -0500
 2 files changed, 40 insertions(+), 1 deletion(-)
```

#### Additional reading
- [Atlassian Git tutorial](https://www.atlassian.com/git/tutorials/cherry-pick)
