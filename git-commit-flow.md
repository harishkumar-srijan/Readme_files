> [!IMPORTANT]
> first time send the changes on branch

#### first time send the changes on branch

```
- git checkout -b <feature-branch>;
- git add files;
- git commit -m “ commit msg”;
- git push origin <feature-branch>;
- PR raise against blt-dev
```

#### rebase the branch and resolve merge conflict issue.

```
- git checkout <branch>; —> update branch (from which branch you want to rebase you feature branch like dev)
- git pull --rebase origin develop;
- resolve conflicts;
- git status
- git add <files>
- git rebase --continue
- git push origin <branch name> -f
```

#### if commit the changes and working on same commit and history / merge issues on branch

```
- git pull --rebase origin blt-dev;
- git checkout -b <feature-branch>; do your changes
- git add files;
- git commit -amend ----------> enter
- New window will open change the commit msg (first line ) if you want change —> then —> press : (colon only)
  :wq command (write wq for save and exit that terminal)
- git push harishkumar-srijan (branch name EZ-894-referenced-cards-component-themimg) -f

```

#### if you working on other's branch and thats not merged on dev

```
1. git checkout blt-dev;
2. git pull --rebase origin blt-dev;
3. git checkout -b <your-feature-branch-name>
4. git pull --rebase indrajith <indrajiths-branch-name>
5. Do your changes
6. git add
7. git commit
8. git push harishkumar <your-feature-branch-name>
9. Raise PR against blt-dev
```

> [!TIP]
> useful cammand

```
- git pull --rebase origin branch_name;
- git cherry-pick <commit-hash>;
- git checkout --<file-name>;
- git stash;
- git commit --amend;

```

> [!NOTE]
> git remote check and add

```
- git remote -v
- git remote add harishkumar-srijan git@github.com:harishkumar-srijan/ezcontent_theme.git
- git remote
```

> [!NOTE]
> Permission to file and folder

```
- cmd —> chmod 755 folder_name or file_name
```
