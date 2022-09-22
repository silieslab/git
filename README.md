# git
Repository to teach basic git commands for collaborative projects

## Warm-Up
- how to start a repo from scratch?
    - `git init` local method for new projects
    -  on GitHub `git clone` for existing collaborative projects 
    (make sure to first fork the repository from the main repo account to your GitHub account)
    
- how to create a branch and start working on it.
    - `git branch <new_branch_name>`
    - `git switch <new_branch_name>`
    - Create new files or mofidy existing ones
    
- how to add your changes from your working directory to your local machine?
    - `git add <modified_file>`
    - `git commit -m "your_message_describing_changes"`

- how to update the main brach with new files from your branch?
    - `git switch main` (important to be in the main branch)
    - `git merge <another_branch>`
    
- how to revert mistakes?
    - before commit:
      - `git restore <file>` [discard changes in the working directory] __changes files__
      - `git restore --staged <file>` [unstage changes ➔ opposite of `git add <file>`, does not modify the working directory]
    - after commit:
      - `git revert <commit>` [creates a new commit, modifies the working directory]
      - `git reset <commit>` [only reset the HEAD pointer, does not modify the working directory] __rewrites history__ 
      - `git reset --hard <commit>` [reset HEAD and modify working directory] __rewrites history__ and __changes files__
      
- how to *move* the whole working directory to a specific point in history?
    - `git checkout <commit>` ➔ `DETACHED HEAD` problem, __changes__ __files__
    - interaction with branches: `git branch <branch_name>` + `git switch <branch_name>` 
- `git gui`: building commits along the way interactively (for the *mess around* type of workflows)


## Interacting with remotes
- `git remote -v`: checks which remote repositories are linked to your local machine.
- `git remote add <repository_name> <URL>`: adds a new remote, for example an "upstream" repository. Here repository_name = upstream.
-  Update from/to remote:
  - `git pull <from_where> <what>`, `git push <where> <what>`, `git fetch <from_where> <what>`

## Scenarios
1. lone scientist working alone in the cellar without Internet (local git)
2. lone scientist uploading their software to the Internet in the hope it can be useful for other people (local git + one personal GitHub repo)
3. lone scientist sharing one software project with some other befriended lone scientist working in a different place (local git + o.p.G.r + permissions)
4. research group sharing software among members (local git + several GitHub repos + permissions + branches + [optional] PRs)
(Check pictures in git_scenarios)

## Extra resources
1. Version control with git tutorial with exercises: https://swcarpentry.github.io/git-novice/
2. A more thorough and detailed explanation can be found on the [Numpy Contributor's Guide](https://docs.scipy.org/doc/numpy/dev/gitwash/index.html).
 This guide can be adapted to your own needs, see [gitwash](https://github.com/matthew-brett/gitwash).
