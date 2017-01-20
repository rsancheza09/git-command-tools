# git-tools
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
