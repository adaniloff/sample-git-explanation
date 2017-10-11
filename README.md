# A sample git explanation

So, today I was trying to explain how **git** works to an intern, and had some troubles to do so.
The problematics about this person were :
- almost no knowledges in this tool
- not quite a "computer person"
- not fluent in english

After a while, I figured out a metaphoric speech would be more appropriate to explain it. 
Then I thought : "Why not to publish that online, as it may help non tech. people to understand how git works ?".

By the way... please understand that this article is made for *very beginners* and some things will be over simplified (they might even seems wrong to you !) for them to understand what **git** is.

#### A few words about the tool

**Git** is a versioning tool, which is usefull for collaborative work, but also for keeping trace of what we do in time, and **much more** things.
I won't spend a lot of time talking about those concepts, as it is not the topic of this post and it has been done a lot of time and by many people ; to learn more you can read the [https://www.atlassian.com/git/tutorials/what-is-version-control](Atlassian documentation about it) which is very well done in my opinion.

#### A first look: the __editorial process__

Let's compare our **git** project's lifecycle to a book one (in our case, it will be a dictionnary): it all begins with an idea. 

So, one or many people want to make a book. Cool thing, and those guys are working hard on it to __publish__ it as fast as they can. 
As they want to get it out faster, they decide to split up the work : each person will be in charge of one or several __chapters__.
Let's say I'm part of the thing, and the chapters A, B, C and D are *under my commandment*. I'm a very focussed guy and I plan to work as the following: I'll do A, then B, then C, and finally D. For each of those __chapters__, it's gonna take some time; also I want to be sure to be able to retrieve my work at any time, so I'm gonna make __versions__ of those, that I will save.
The final product will be the results of all of our __chapters__, which we will merge at a given time before our __publishing__.

Basically, I just explained to you the following principles :
> A __publishing__ of the book (or the fact to __publish it__) is a **project's release**
> A __chapter__ of the book, which can change through the time, is a **branch**
> A __version__ of the book, at a given time, is a **commit**

I'm not gonna talk about **remote** right now, as it might make it harder to you but try to think about it like below :
> A **remote** is an __editor__. You migth, in some specific cases, want to __publish__ your work with many of them, but that's not what we're doing here.

So, the thing to remember is, your default __editor__ is called "origin". Yes. That's his name. Deal with it.

#### What's next ? The __customer side__ !

Now that we know a bit about the __editorial process__, let's take a look on the __customer side__.
Which steps will have to make a man before being able to read his book ?
- get the book
- read it

Simple right ?
Keep in mind though, that our **git project** (__the book__) is opensource, and free to people to get it and contribute to its development.
That means, a __contributor__ will be able to suggest some modifications to our book. Awesome, is'nt it ?

In short :
> A __customer__ of the book is someone who wants to use our **project**, without working on it
> The __contributor__ is basically a __customer__ which wants to get involved in the project
> The __customer side__ is the usage of our **project** through :
> -- the different __versions__ (**commits**) for __contributors__
> -- the different __publishings__ (**releases**) for __customers__

#### Now, let's practice a lil'bit :)

###### A __customer side__ journey !

1) As we want to get the dictionnary, we need to get it from the store.
    There are multiple ways to do it, but let's take a look on `git clone`:
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
Oh but ... 2 years have passed now, and you've heard some words meanings have changed ! Also, there are new words in the English language... With `git`, if you already have a dictionnary, you do not have to buy a new one ! You can just __update__ it, then __upgrade__ it !
    
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
    
    
