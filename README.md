# GIT Useful Commands
It contains not common git commands that are very helpfull

# Multiple pushurl
Let's create a new remote called 'all'
```
$ git remote add all [Original Repository URL]
$ git config -l | grep '^remote\.all'
$ git remote set-url --add --push all [Another Repository URL]
$ git config -l | grep '^remote\.all'
$ git remote set-url --add --push all [Original Repository URL]
$ git config -l | grep '^remote\.all'
```
Now you can use ```git push all master``` and ```git pull all master```

Reference: http://stackoverflow.com/questions/14290113/git-pushing-code-to-two-remotes

# Pretty Log
![Pretty Log](https://coderwall-assets-0.s3.amazonaws.com/uploads/picture/file/91/1._git_lg__git_.jpg)


Run the following command:

1. `$ git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"`

Now, just run this:

`$ git lg`
