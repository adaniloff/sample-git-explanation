
# Most useful commands

#### Quick vocabulary resume

- the __dictionnary__ is our --> **git project**
- a __chapter__ is a --> **git branch**
- a __version__ is a --> **git commit**
- a __publishing__ is a --> **project release**

## Summary

- [git clone](#git-clone)
- [git fetch](#git-fetch)

## <a name="git-clone"></a>git clone

Cloning a project is basically downloading it.

> Getting the latest* __publishing__ of the __dictionnary__      
> (* Actually, that depends on the **git project**'s configuration and the parameters you pass to the command)    
> From a mobile user point of view, it's like downloading a new app    
   
```
# Simple usage : 
# git clone [-b <branch-name>] <repository> [<target-dir>]
#
# Examples :
# git clone https://github.com/adaniloff/sample-git-explanation.git # will get you the project on the default branch, in a directory named "sample-git-explanation"
# git clone https://github.com/adaniloff/sample-git-explanation.git my-directory # will get you the project on the default branch, in a directory named "my-directory"
# git clone -b dev https://github.com/adaniloff/sample-git-explanation.git my-directory # will get you the project on the "dev" branch, in a directory named "my-directory"
```

## <a name="git-fetch"></a>git fetch

This command updates your local repository with the new things that happened on one/many remotes.

> Asking the store to know if there is a new __publishing__ of the __dictionnary__    
> From a mobile user point of view, it's like checking if your downloaded app has any new update, without downloading anything. You just want to know if you can update your app.

```
# Simple usage : 
# git fetch [-p][--all] [<repository>]
#
# Examples :
# git fetch # will fetch the default remote, aka "origin"
# git fetch --all # will fetch all remotes
# git fetch -p my-remote # will fetch the "my-remote" remote ; the "-p" argument will remove any remote-tracking references that no longer exist on the remote 
```
[< Previous page](/doc/1-git.md) | [Next page >](/doc/3-user-guide.md) 
