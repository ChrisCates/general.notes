# GIT
## How to use it
### Get started with git

#### (1) How to push up to the server if you've made changes
1. Open up terminal or command line
2. Go to the root directory of your git repository
3. Run the command `git add .` in the root directory to stage ALL files
4. Run the command `git commit -m "your awesome message here"` to commit your code (with a message)
5. Run the command `git push origin master`

#### (2) How to pull from a server if you made changes on another computer or someone else made changes
1. Open up terminal or command line
2. Go to the root directory of your git repository
3. Run the command `git pull origin master`
4. If you have unstaged files. You can follow the steps up to step 4 for (1) How to push up to a server
5. Then you can do `git pull origin master`
6. Then you can do `git push origin master` to push your unstaged files.

#### (3) How to clone a repository
1. Open up terminal or command line
2. Go to the desired folder you want to clone it to
3. Run the command `git clone [the url of the repository]`

#### (4) How to use `.gitignore`
1. You use it to ignore certain files you don't want to stage for commits to github
2. You just put in the file/folder you want to ignore in each new line is a file or folder:

##### Example .gitignore
```
node_modules
npm_debug.log
```

