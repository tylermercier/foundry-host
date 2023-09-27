Add a user for your application

`adduser foundry`

You’ll be prompted to enter a password and a bunch of rubbish info. Add a password and just spam enter through the junk.

Now we give this user a way to do admin things - aka sudo.

`usermod -aG sudo foundry`

Now we need to set it such that our new user can login to the server.

`rsync --archive --chown=foundry:foundry ~/.ssh /home/foundry`

Now log out (just close the terminal), and log back in, using your new username instead of root.

Test this user is working with this command, entering this new user’s password when prompted:

`sudo ls -la /root`

If you see some random files listed, nice!

Update the server:

`sudo apt update`
`sudo apt upgrade`

Accept the default on anything that pops up.
