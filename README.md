# Basic Git Course

### Index

### What is a Version Control Software?

Version control software allows you to have “versions” of a project, which show the changes that were made to the code
over time, and allows you to backtrack if necessary and undo those changes.

We also have the idea of centralized version control server, where multiple developer could pull the latest changes and
then push to the server the changes made. But what happens if the server is down. There's where Git comes in.

### What is Git?

With Git, the develipers don’t just check out the current version of the files and work from them, they actually mirror
the entire version history. Each developer always has a complete copy of everything.

A central server is still used, but should the worst happen, then everything can still be restored from any of the
developers who have the latest versions.

Git takes “snapshots” of files, if files remain unchanged in a particular version, it simply links to the previous
files.

### What is GitHub?

Github is both a remote server, a community of developers, and a graphical web interface for managing your Git project.
It’s free to use for public repositories and low cost plans for private projects. Other two good examples for Git remote
servers are BitBucket and Stash.

### First steps

To start working on a project using git we have three choices, the first one is to create our own repository in one of
the previous server, forking a repository or pushing up one after initializing it from a local folder.

For this example we will cover the two first ones and we will choose GitHub as remote server.

Supposing that we already have a GitHub account, we need to go the the main page of the remote server and create the
repository. This is accomplished by clicking the `+` Icon and then selecting the right option of the dropdown menu.

![GitHub new repository image](./img/new-repo-image-1.png)

After filling the needed information we will finally have our repository created. Once there we will be able to get a
local clone of it and start working.

To fork a repository that already exists on GitHub we should go to the repository's homepage and click the Fork
button provided to us.

![GitHub fork repository image](./img/fork-repo-image-1.png)

After this you will have a perfect copy of the original repository but into your own repositories of GitHub.

To end up with the first steps to work with Git we will clone a repository into our local sandbox so we can start
working on a project. Go to the homepage of the repository and click the copy to clipboard button and then write the
following command into the command line.

`git clone https://github.com/troianoandres/git-course.git`

![GitHub fork repository image](./img/clone-repo-image-1.png)

The only difference you must have is the URL of the repository to be cloned. After you run this command you should have
locally cloned the entire project.

### Working with git

We will cover 3 of the most important commands you must know to work with Git. Those are `git pull`, `git commit`,
`git push`

#### git pull

Is a command used to get all the latest changes made to the repository, this will update all git history, files and
branches. To run this command just type `git pull` into the command line.

#### git commit

Is a command used to make a snapshot of the current changes, to make the changes be saved into the snapshot you must
stage them into the commit files. To add the `README.md` file to the commit files you should run `git add README.md`
into the command line.

To check the status of the staging process you could run `git status` and it will show you the changes to be committed.

Then when you are ready to commit the changes you should run `git commit -m "(...)"` where `(...)` is the commit message.
We must use a representative message for each commit, allowing us to know which is the purpose of the commit. We should
also have in mind to make each commit as atomic as possible, allowing us to revert the changes if needed.

#### git push

When you have made all the changes you want, and they are all committed you must push all to the server. To
accomplish this you should run `git push origin (branch)`, where `(branch)` is the branch where you want the
changes to be pushed. What is a branch will be covered in the next section.

### Collaborating into a project with git

