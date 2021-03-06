#Git Workshop

##Goals:
- Create new Github account
- Quick overview of Github
- Clone code from Github 
- Change code around a bit
- Learn how to add files to staging area
- Learn how to commit the changes
- Push code back to gihub

- Learn how to create own repository on Github
- Initialize repository on computer
- Set remote repository to Github repo URL
- Create / Change new branch
- Commit on new branch
- Merge branch back to master
- Add contents of new repository to commit
- Push up to master branch of Github repository

##First Steps:
Open terminal and follow instructions:

    cd ~/Desktop
    mkdir git-todo
    cd git-todo

    touch README.md
    git init
    git add README.md
    git commit -m "initial commit"
    git remote add origin <paste http:// link here from Github>
    git push origin master
    
###What Happened?
- `cd ~/Desktop` will change directory into our 'Users/<username>/desktop' directory
- `mkdir git-todo` will create a new folder called 'git-todo' on your Desktop
- `git init` creates a new repository in our `git-todo` directory. `cd git-todo` changes the directory into the `git-todo` directory. Think of it as going down one level.
- `touch README.md` generates a markdown file that is called README. 
- `git init` initializes, or generates, a new `.git` file. Think of a `.git` file as the memory store at the root of a directory. The logic that stores your repository data as well as the synchronization between your remote repositories is encapsulated in this `.git` file.
- Before you can commit new files, you have to "stage" them by adding them to a staging directory. You do this by `git add README.md`. You can also add all new/updated files in current directory by doing `git add .`, and if you also need to remove files that were deleted, you do `git add -A`
- Once all the previous steps are finished, you commit the staging file via `git commit -m "initial commit".
- Finally, push up to your remote via `git push origin master`.

##Cloning:
`cd` into a the directory you want your project to live in.

On Github, go to the repository you want to contribute to and copy the link on the right hand side of the page.

Back in terminal, and type: `git clone <paste http:// link here from Github>`

(Note, if this project is something sustantial, say an open source project that you would like to contribute to, it's best practices to `Fork` the repo to your page and then clone that fork. A `fork` is basically copying and pasting the repo.)

Once you've cloned the repo, make the changes you want and then, just like when you initialized a new repo above, stage, commit, and push your changes:

    git add <file you've changed>
    git commit -m "these are the changes I've made"
    git push origin master

##Branching:
Another best practice technique is to make every body of work a separate branch. So far, we've been pushing to the `master` branch. You can create your own branching off of the `master` branch and do you work on that, and then `merge` those changes into `master` when you're done.

While on master, before you begin working, type:
`git checkout -b <your-branch-name>`

Do your work on this branch, and while on this branch, be sure, like above to stage, commit, and, if you want your teammates to see your work, push your changes up to Github on your new branch:

    git add <file you've changed>
    git commit -m "these are the changes I've made"
    git push origin <your-branch-name>

Note the last command is pushing the changes up to your new branch, not master. 

##Merging
When you're done with your work on your new branch, you may want to merge it into master. There are two ways to do this, either locally (through git on your computer) or remotely (on Github).