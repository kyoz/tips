# How to Prevent Permissions Errors

Use [Node Version Manager](https://github.com/creationix/nvm)

## Installation

### Install script

With cURL:

```sh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
```

With Wget:

```sh
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
```

**Note:** On Linux, after running the install script, if you get `nvm: command not found` or see no feedback from your terminal after you type:

```sh
command -v nvm
```
simply close your current terminal, open a new terminal, and try verifying again.

**Note:** On OS X, if you get `nvm: command not found` after running the install script, one of the following might be the reason:-
  - your system may not have a [`.bash_profile file`] where the command is set up. Simply create one with `touch ~/.bash_profile` and run the install script again
  - you might need to restart your terminal instance. Try opening a new tab/window in your terminal and retry.

If the above doesn't fix the problem, open your `.bash_profile` and add the following line of code:

`source ~/.bashrc`

- For more information about this issue and possible workarounds, please [refer here](https://github.com/creationix/nvm/issues/576)

### Verify installation

To verify that nvm has been installed, do:

```sh
command -v nvm

## Usage

To download, compile, and install the latest release of node, do this:

```sh
nvm install node
```

And then in any new shell just use the installed version:

```sh
nvm use node
```

Or you can just run it:

```sh
nvm run node --version
```
Or, you can run any arbitrary command in a subshell with the desired version of node:

```sh
nvm exec 4.2 node --version
```

You can also get the path to the executable to where it was installed:

```sh
nvm which 5.0
```

In place of a version pointer like "0.10" or "5.0" or "4.2.1", you can use the following special default aliases with `nvm install`, `nvm use`, `nvm run`, `nvm exec`, `nvm which`, etc:

  - `node`: this installs the latest version of [`node`](https://nodejs.org/en/)
  - `iojs`: this installs the latest version of [`io.js`](https://iojs.org/en/)
  - `stable`: this alias is deprecated, and only truly applies to `node` `v0.12` and earlier. Currently, this is an alias for `node`.
  - `unstable`: this alias points to `node` `v0.11` - the last "unstable" node release, since post-1.0, all node versions are stable. (in SemVer, versions communicate breakage, not stability).

  ### System version of node
If you want to use the system-installed version of node, you can use the special default alias "system":

```sh
nvm use system
nvm run system --version
```

### Listing versions
If you want to see what versions are installed:

```sh
nvm ls
```

If you want to see what versions are available to install:

```sh
nvm ls-remote
```

To restore your PATH, you can deactivate it:

```sh
nvm deactivate
```

To set a default Node version to be used in any new shell, use the alias 'default':

```sh
nvm alias default node
```