# Howto use git ?

## A __customer side__ journey !

1) As we want to get the dictionnary, we need to get it from the store.
    There are multiple ways to do it, but let's take a look at `git clone`:
    ```
    # Basic usage:
    # git clone <repository> [<directory-name>]
    git clone https://github.com/team-leoo/CacheCleaner.git
    ```
    Great ! We now got the dictionnary !
    
2) Now, we'd like to check if everything's ok with our new book.
    The first thing to do is to check which __chapter__ is the first one. This is achievable with the command `git status`. 
    > By convention, the default **branch** (__chapter__) is called *master*.
    
    Then, let's quickly throw an eye on the summary with `git log`: 
    ```
    # A very basic usage :
    git log
    # For a full rendered inline graph :
    git log --all --oneline --graph --decorate --color
    # If your project got too many merges and branches :
    git log --all --oneline --graph --decorate --color --simplify-by-decoration
    ```
    > There are a lot of tools which implement a UI ([click here](https://git-scm.com/downloads/guis/)) to help you understand what the fuck is going on ... But I really think mastering the good old `git log` command is necessary.    
    > Why ? Just an example: on an external environment, you might not have access to your favorite tools...
    
**That's it ! You can now read you book (which means, check the files in your project, use it as you want, etc) !**
Oh but ... 2 years have passed now, and you've heard some words meanings have changed ! Also, there are new words in the English language... With `git`, if you already have a dictionnary, you do not have to buy a new one ! You can just __update (1)__ it, then __upgrade (2)__ it !  

*(1) updating is the process which update your index. Basically, it's asking the library store if a new dictionnary has been published. That does'nt chznge yours.*  
*(2) however, by upgrading your project, you change its content. It's like, trading your old dictionnary for a new one*  

3) The command to do the __update__  is `git fetch`.
    > Do not forget that in our example, our __editor__ is called "origin" !
    
    We want to see if there is any new __version__ of our dictionnary... let's use `git fetch` to do so.
    ```
    # Basic usage:
    # git fetch [<remote>]
    git fetch origin
    ```
    Oh. There are a lot of new __versions__ of different __chapters__! Since we want to __upgrade__ it, let's go to __chapter__ A.
    
4) `git checkout` and `git pull` will do the trick.
    The first step is to go to the __chapter__ A, and it's quite simple.
    ```
    # Basic usage:
    # git checkout <branch-name>
    git checkout ChapterA
    ```
    Now, we'd like to __upgrade__ it with the new __version__ of it !
    ```
    # Basic usage:
    # git pull <remote> <branch-name>
    git pull origin ChapterA
    ```
    
    [< Previous page](/doc/2-commands.md)  | [Next page >](/doc/4-contributor-guide.md) 
