# Set Git Name, Email

### To set
```sh
$ git config --global user.name "Kyoz"
$ git config --global user.email "banminkyoz@gmail.com"

```

### To view

```sh
$ git config --global user.name
$ git config --global user.email
> Kyoz
> banminkyoz@gmail.com
```


# Set Git Aliases

```sh
$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.ci commit
$ git config --global alias.st status
$ git config --global alias.cf config
...
```

# Set Default Config Editor

```sh
git config --global core.editor "vim"
```

# Change Git Remote

The  `git remote set-url`  command changes an existing remote repository URL.

The  `git remote set-url`  command takes two arguments:

> An existing remote name. For example, `origin` or `upstream` are two common choices.

> A new URL for the remote. For example:

* If you're updating to use HTTPS, your URL might look like:
```sh
https://github.com/USERNAME/REPOSITORY.git
```

* If you're updating to use SSH, your URL might look like:
```sh
git@github.com:USERNAME/REPOSITORY.git
```

# Change Git Remote Name

These examples assume you're cloning using HTTPS, which is recommended.

```sh
$ git remote -v
# View existing remotes
origin  https://github.com/OWNER/REPOSITORY.git (fetch)
origin  https://github.com/OWNER/REPOSITORY.git (push)

$ git remote rename origin destination
# Change remote name from 'origin' to 'destination'

$ git remote -v
# Verify remote's new name
destination  https://github.com/OWNER/REPOSITORY.git (fetch)
destination  https://github.com/OWNER/REPOSITORY.git (push)
```

# Add more to last commit

```
git commit --amend
```

If you dont wanna change message, do use:

```
git commit --amend --no-edit
```


