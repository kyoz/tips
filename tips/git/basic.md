# Set Git Name, Email

### To set
```
$ git config --global user.name "Kyoz"
$ git config --global user.email "banminkyoz@gmail.com"

```

### To view

```
$ git config --global user.name
$ git config --global user.email
> Kyoz
> banminkyoz@gmail.com
```


# Set Git Aliases

```
$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.ci commit
$ git config --global alias.st status
```

# Change Git Remote

The  `git remote set-url`  command changes an existing remote repository URL.

The  `git remote set-url`  command takes two arguments:

> An existing remote name. For example, `origin` or `upstream` are two common choices.

> A new URL for the remote. For example:

* If you're updating to use HTTPS, your URL might look like:
```
https://github.com/USERNAME/REPOSITORY.git
```

* If you're updating to use SSH, your URL might look like:
```
git@github.com:USERNAME/REPOSITORY.git
```



