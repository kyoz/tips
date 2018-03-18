# Enable Key Repeating in OSX

Normally, When holding a letter, it'll trigger special characters of that letter.
To Enable key repeating, we have to disabled this feature. 

Open terminal and use this command

```bash
defaults write -g ApplePressAndHoldEnabled -bool false
```

Then you can use key repeating when hold down a letter ( If not, restart to take change effects )

Remember to setting **Key Repeat** ( to **Fast** ) and **Delay Until Repeat** ( to **Short** ) in Keyboard settings to make sure it work as we want.

To re-enable Special Characters feature, open terminal and use:

```bash
defaults write -g ApplePressAndHoldEnabled -bool true
```