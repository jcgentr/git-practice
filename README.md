A repo to practice git commands with.

# git-practice

# Examples

```
git add .
```

# Notes

```
git pull -> git fetch && git merge
```

```
git checkout -b new-branch -> git branch new-branch && git checkout new-branch
```

```
git checkout -
// switches to previous checked out branch
```

```
// make new feature on branch
// when finished merge into master
git checkout master
git merge new-feature

// Fast-forward merge result: no additional commit
// Three-way merge result: an additional commit
```

```
// delete local branch
git branch -d branch_name
```

```
// merge conflict
git pull
git status
// fix merge conflict and push
git add .
git commit -m "fix merge conflict"
git push
```

```
// stage ALL changes
git add -A
// stage new files and modifications, w/o deletions
git add .
// stage modifications and deletions, w/o new files
git add -u
```

```
// save uncommitted changes for later
// prevent them from carrying over to new branch
git stash
// pull change back out of .git folder
git stash pop
git stash pop -> git stash apply && git stash drop
```

```
// navigate git command pager
git log
/search-term
J, K to move up and down lines
q to quit
uses Unix less commands
```

```
// git log formatting options
// single line commit
git log --oneline
// ASCII art graph
git log --graph
// stats on insertions and deletions
git log --stat
// can combine
git log --stat --oneline
```

```
// 3 most recent commits
git log -3
// commits since yesterday
git log --after="yesterday"
// more advanced filter (can also use 'since' and 'until')
git log --after="3/15/21" --before="yesterday"
// find by author (add -i to ignore case)
git log --author="Jared"
// grep to find certain commit messages
git log --grep="copyright"
// filter on specific file(s)
git log README.md .gitignore

// can commbine these options for powerful filtering
```

```
// compare changes from previous and current working dir(2 references)
git diff
// stats condensed
git diff --stat
// compare branches
git diff origin/master
// specific files
git diff filename.js
```

