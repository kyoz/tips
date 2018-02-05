# How to Prevent Permissions Errors

&&Notes**: Not apply with window

To minimize the chance of permissions errors, you can configure npm to use a different directory. In this example, it will be a hidden directory on your home folder.

1. Back-up your computer before you start.

2. Make a directory for global installations:

```sh
 mkdir ~/.npm-global

```

3. Configure npm to use the new directory path:

```sh
 npm config set prefix '~/.npm-global'

```

4. Open or create a **~/.profile** file and add this line:


```sh
 export PATH=~/.npm-global/bin:$PATH

```

5. Back on the command line, update your system variables:


```sh
 source ~/.profile
```

Done. Now retry to download a packages globally without using sudo

```sh
npm install -g tslint
```

