
# What is git ?

Let's compare our **git** project's lifecycle to a book one (in our case, it will be a dictionnary): it all begins with an idea. 

## A first look: the __editorial process__

So, one or many people want to make a book. Cool thing, and those guys are working hard on it to __publish__ it as fast as they can. 
As they want to get it out faster, they decide to split up the work : each person will be in charge of one or several __chapters__.
Let's say I'm part of the thing, and the chapters A, B, C and D are *under my commandment*. I'm a very focused guy and I plan to work as the following: I'll do A, then B, then C, and finally D. For each of those __chapters__, it's gonna take some time; also I want to be sure to be able to retrieve my work at any time, so I'm gonna make __versions__ of those, that I will save.
The final product will be the results of all of our __chapters__, which we will merge at a given time before our __publishing__.

Basically, I just explained to you the following principles :
> A __publishing__ of the book (or the fact to __publish it__) is a **project's release**    
> A __chapter__ of the book, which can change through the time, is a **branch**    
> A __version__ of the book, at a given time, is a **commit**    

I'm not gonna talk about **remote** right now, as it might make it harder to you but try to think about it like below :
> A **remote** is an __editor__. You migth, in some specific cases, want to __publish__ your work with many of them, but that's not what we're doing here.

So, the thing to remember is, your default __editor__ is called "origin". Yes. That's his name. Deal with it.

## What's next ? The __customer side__ !

Now that we know a bit about the __editorial process__, let's take a look on the __customer side__.
Which steps will have to make a __customer__ before being able to read his book ?
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

[< Previous page](/README.md) | [Next page >](/doc/2-commands.md) 
