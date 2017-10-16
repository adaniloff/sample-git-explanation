
# Most useful commands

#### Quick vocabulary resume

- the __dictionnary__ is our --> **git project**
- a __chapter__ is a --> **git branch**
- a __version__ is a --> **git commit**
- a __publishing__ is a --> **project release**

## git clone

Cloning a project is basically downloading it.

> Getting the latest* __publishing__ of the __dictionnary__    
>     
> (* Actually, that depends on the **git project**'s configuration)

```
# Simple usage : 
# git clone [-b <branch-name>] <repository> [<target-dir>]
#
# Examples :
# git clone https://github.com/adaniloff/sample-git-explanation.git # will get you the project on the default branch, in a directory named "sample-git-explanation"
# git clone https://github.com/adaniloff/sample-git-explanation.git my-directory # will get you the project on the default branch, in a directory named "my-directory"
# git clone -b dev https://github.com/adaniloff/sample-git-explanation.git my-directory # will get you the project on the "dev" branch, in a directory named "my-directory"
```

[< Previous page](/doc/1-git.md) | [Next page >](/doc/3-user-guide.md) 
