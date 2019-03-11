## Git cheat sheet

[learn enough git to be dangerous | Michael Hartl](https://www.learnenough.com/git-tutorial/getting_started)


![git sequence](git_status_sequence.png)

- commit message -  present tense using the imperative mood. "initialize repository" (not "initializes repository, initialized repository)
- "SHA" - Secure Hash Algorithm


- - -

### Command line

| Command                  | Desc                                                                         | Example                        |
| ------------------------ | ---------------------------------------------------------------------------- | ------------------------------ |
| `git help`               | Get help on a command                                                        | `$ git help push`              |
| `git config`             | Configure Git                                                                | `$ git config --global …`      |
| `source <file>`          | Activate Bash changes                                                        | `$ source ~/.bash_profile`     |
| `mkdir -p`               | Make intermediate directories as necessary                                   | `$ mkdir -p repos/website`     |
| `git status`             | Show the status of the repository                                            | `$ git status`                 |
| `touch <name>`           | Create empty file                                                            | `$ touch foo`                  |
| `git add -A`             | Add all files or directories to staging area                                 | `$ git add -A`                 |
| `git add <name>`         | Add given file or directory to staging area                                  | `$ git add foo`                |
| `git commit -m`          | Commit staged changes with a message                                         | `$ git commit -m "Add thing"`  |
| `git commit -am`         | Stage and commit changes with a message                                      | `$ git commit -am "Add thing"` |
| `git diff`               | Show diffs between commits, branches, etc.                                   | `$ git diff`                   |
| `git commit --amend`     | Amend the last commit                                                        | `$ git commit --amend`         |
| `git show <SHA>`         | Show diff vs. the SHA                                                        | `$ git show fb738e…`           |
| `git remote add`         | Add remote repo                                                              | $ git remote add origin        |
| `git push -u <loc> <br>` | Push branch to remote (-u : set upstream and omit origin master later usage) | `$ git push -u origin master`  |
| `git push`               | Push to default remote                                                       | $ git push                     |
