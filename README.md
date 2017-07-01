#My GIT Tutorial

Not everyone will need to do the entire process outlined here, feel free to skip to the section you need.
I use Linux for my GIT client. Beanstalk has [instructions](http://guides.beanstalkapp.com/version-control/git-on-windows.html) for Windows.

## SSH Keys


### Check if you already have an SSH Key
`ls -a ~/.ssh`

if you do, you will see output like:
`.  ..  id_rsa  id_rsa.pub  known_hosts`

You can choose to use your existing ID or create a new one.

### Creating a New SSH Key
`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

This creates a new ssh key, using the provided email as a label.
Accept the default location (`/home/you/.ssh/id_rsa`)

###  Adding your SSH key to the ssh-agent
Start the ssh-agent in the background.
`eval "$(ssh-agent -s)"`

Add your SSH private key to the ssh-agent.
`ssh-add ~/.ssh/id_rsa`

Use the ssh-add command to list the keys that the agent is managing.
`ssh-add -l`

This will list all your SSH Keys.

### Adding a new SSH key to your GitHub account
Install xclip
`sudo apt-get install xclip`

Copy your key to clipboard
```xclip -sel clip < ~/.ssh/id_rsa.pub```

In the upper-right corner of any page, click your profile photo, then click `Settings`.
In the user settings sidebar, click `SSH and GPG keys`.
Click `New SSH key` or `Add SSH` key.
Enter a name to identify which computer or account this is for. I use multiple computers so I use my computer name on each key.
Paste in the key that you copied earlier
Click `Add SSH key`.
If prompted, confirm your GitHub password.

### Testing your SSH connection
In your teminal run the following:
```ssh -T git@github.com```

At the next prompt type `yes` and press `Enter`, you should get output like this:
```Hi username! You've successfully authenticated, but GitHub does not
provide shell access.```

## Start working
From this point you should be able to start working. Here are some good tutorials on using GIT if you need them.
[Git Basics](https://youtu.be/8oRjP8yj2Wo?list=PLg7s6cbtAD165JTRsXh8ofwRw0PqUnkVH)
