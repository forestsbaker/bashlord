#Install and use bashlord in 5 minutes

# Installation #
  1. Download [the latest bashlord revision](http://bashlord.googlecode.com/files/bashlord-0.11.tar.gz)
  1. Extract archive to your home directory
```
tar xzvf bashlord.tar.gz ~/
```
  1. add the following lines at the end of your ~/.bashrc configuration file
```
# Bashlord
if [ -f ~/.bashlord/bashrc ]; then
    . ~/.bashlord/bashrc
fi
```
  1. Reload your bash environment
```
. ~/.bashrc
```

# Using bashlord #
Let's start with a basic example:

I want to create a shell script to backup my web browser bookmarks.

## Step 1: Ask bashlord to create a new script ##
```
bashlord add bkp-bookmarks
```

From here a script and an alias have been created. The name of your script is already a command available from your shell. This command execute your script.

## Step 2: Edit my script ##
The following command will open up my script shell in vim, so I will be able to add the commands that perform my backup.
```
bashlord edit bkp-bookmarks
```

Note: You can configure 'bashlord edit' to open scripts with your favourite editor just replacing 'vim' in the following file: ~∕.bashlord/conf.d/00\_bashlord\_init

## Step 3: Enjoy it ##
Now I can type the following command any time I want to backup my bookmarks
```
bkp-bookmarks
```