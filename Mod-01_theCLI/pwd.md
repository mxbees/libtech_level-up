# Finding Where We Are &mdash; Directories, Folders, and Paths

First thing, we have to figure out where they are. You're probably familiar with the idea of folders. And you may have seen things like C:\Users\Me\Documents or /Users/Me/Documents and recognize that as the path to a folder. You probably won't see the slashes when you're looking at the file in Explorer or Finder, just the names of each level of folder.

A folder is the same as a directory and we're going to use that term for it from now on. But it'll be the same thing, so when you see "directory," think "folder."

So...when you open the CLI, how do you know where you are in the directory structure?

# PWD - Print Working Directory

Let's learn our first CLI command, the "where am I right now?" of CLI.

The phrase is very simple: `pwd`

Yes, it looks like shorthand for "password.""

`pwd` means "print working directory." Since all three of those words will come up throughout working with the CLI, and in other documentation you might read, let's define them quickly here.

Print &mdash; doesn't mean a printer like you might think. It generally means making something display on your screen. In this case, it means that by executing the command (pressing Enter/Return) you will be making the computer output information onto your screen, in the interface.

Working &mdash; means current or the one that we're in right now. Like when you have an Explorer or Finder window open, you're in one directory and can move up or down. Working is that directory you're in at the moment.

Directory &mdash; as we said above, means the same as "folder."

# Let's Use PWD

Open up your CLI terminal and type in: `pwd`

You should see something that looks like:

    $ pwd

Now press Enter.

You should get the filepath to your current working directory. It'll look something like:

    $ pwd
    /c/Users/Me/

or
    $ pwd
    /Users/Me

# Why Do We Care About PWD?

You might be looking at this and thinking "ok, I won't break my computer but seriously this is the most boring thing ever."

And yeah, this is probably the least interesting CLI command you're going to learn. But here's how it's useful. Next, we're going to talk about navigating in your file structure, between directories. How do you navigate if you don't know where you're starting?

If I'm giving people from North of me directions to my house, I say "Go South on 95," but if they're South of me, I say "Go North on 95." You've gotta know where you are before you start moving.

Sometimes, you'll totally know where you are and you won't worry about `pwd`. But when you don't, `pwd` is always there, like a GPS when you're not sure which street you're on.

# Practice

Did you try it in the "Let's Use PWD" section above? If not, open up your terminal and do it now!

How can you keep practicing this? Well, in the next section, which involves traveling between directories, I'll remind you to `pwd` just to confirm where you are. It's a great command because it doesn't mess up whatever you're working on. It just tells you where you are.

Next, let's learn about **CD &mdash; Moving from A to B to A to C!**