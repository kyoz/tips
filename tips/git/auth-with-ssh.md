# Generate SSH keys for Git authorization

## Window

Just follow these 5 steps:

1. Go to this address, and download msysgit, after the download install it with default settings

2. Open Git Bash that you just installed (Start->All Programs->Git->Git Bash)

3. Type in the following: ssh-keygen -t rsa (when prompted, enter password, key name can stay the same)

4. Open file your_home_directory/.ssh/id_rsa.pub with your favorite text editor, and copy contents to your Git repository’s keys field (GitHub, beanstalk, or any other repository provider), under your account.

5 Be sure that you **don’t copy** any whitespace while copying public key’s content (id_rsa.pub)

**Note**: your_home_directory is either C:\Users\your_username (on Windows Vista / 7), or C:\Documents and Settings\your_username (on Windows XP)

## Mac

Follow these 5 steps:

1. Start the terminal

2. Navigate to your home directory by typing: cd ~/

3. Execute the following command: ssh-keygen -t rsa (when prompted, enter password, key name can stay the same)

4. open file you’ve just created ~/.ssh/id_rsa.pub with your favorite text editor, and copy contents to your Git repository’s keys field (GitHub, beanstalk, or any other repository provider), under your account.

5. Be sure that you don’t copy any whitespace while copying public key’s content (id_rsa.pub)

## Ubuntu (Linux)

Follow these 5 steps:

1. Open console

2. cd ~

3. ssh-keygen -t rsa (when prompted, enter password, key name can stay the same)

4. open file /home/your_username/.ssh/id_rsa.pub with your favorite text editor, and copy contents to your Git repository’s keys field (GitHub, beanstalk, or any other repository provider), under your account.

5. Be sure that you don’t copy any whitespace while copying public key’s content (id_rsa.pub)

## Additional Info

When you create private / public SSH keys on your machine (that’s what you did in above steps), it’s not enough. You need to give your public key to the repository in order to pair the Git server with your local machine (that’d be steps 4. and 5. above).

Most of the popular repositories will give you web interface access to the application

After added, you are good to go with using ssh to authorize git :D