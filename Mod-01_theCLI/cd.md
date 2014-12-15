# Moving from A to B to A to C with CD

Thanks to `pwd` we can now turn on the CLI's GPS and find out where we are. And, thanks to `ls`, we can see what files and directories are in the directory we're currently in.

But now, how do we get from Point A to Point B? What other points can we get to?

The next command we're going to learn is `cd`, "change directories."

# More than just a CD

Unlike `pwd`, `cd` has to be followed by "arguments" which you can think of as "inputs." Think of it as inputting info into a form.

If I type `pwd` right now, I'm going to get:

    $ pwd
    /c/Users/[me]

So now I know where I am. Now I want to go to my Documents folder.

I'm going to type in `cd` followed by an argument telling it where I want to go. If `pwd` is GPS, this is like programming your self-driving car to take you somewhere on your computer.

    $ pwd
    /c/Users/[me]
    $ ls
    [lots of stuff, including 'Documents']
    $ cd Documents
    $ pwd
    /c/Users/[me]/Documents

I told it to move me down into the Documents folder and then used `pwd` to make sure I was in the right place.

`cd` can take a really long location too. For example, if I know that in *Documents* I have a directory called *ProfDev* which has a folder called *webinars*. Instead of typing `cd` each time, I could type this long string:

    $ pwd
    /c/Users/[me]
    $ cd Documents/ProfDev/webinars
    $ pwd
    /c/Users/[me]/Documents/ProfDev/webinars

As long as you know the filepath, you can move as far down it as you want. You'll learn in a bit what you can do when you get there. At first, you may have to use `ls` a lot to figure out what the next place you're going is called. But eventually you'll get to know your filepath structure and be able to do it from memory. And if not, `pwd` and `ls` are always there with you.

# Backing It Up!

Ok, so now we can move forward, but what about going back? Suppose I'm done in my *webinars* directory and want to go back to *ProfDev*?

The command for backing up one directory is `cd ..`

Those are two periods in a row: `..`

If you want to, you can back it all the way up by putting it a `..` for each level, with slashes in between.

    $ pwd
    /c/Users/[me]/Documents/ProfDev/webinars
    $ cd ../../..
    $ pwd
    /c/Users/[me]/

You can also go back up a tree with `..` and then go down it. Suppose you want to move from `ProfDev/webinars` to `ProfDev/conferences`?

    $ pwd
    /c/Users/[me]/Documents/ProfDev/webinars
    $ cd ../conferences
    $ pwd
    /c/Users/[me]/Documents/ProfDev/conferences

You can use as many `..` as possible to go as far back as you want, but...

# Absolute Filepaths Do Not Corrupt Absolutely

At some point, you might say "wait, ok, how can I keep track of all the `../../../../../../`?" And after a while, you may decide that it's just a bit ridiculous to do all those `../../../` and just want to go from one place to another.

To do this, you have to use the absolute filepath. **"Absolute"** in this case means "full." The kinds of filepaths we were using before were "relative." **"Relative"** in this case means "path as related to our starting place."

Fortunately, `pwd` is a great way for us to know the absolute filepath. That's what it's printing.

So, if we want to go from `/c/Users/[me]/Documents/ProfDev/webinars` to `/c/Users/[me]/Documents/RPGs/13thAge/Adventure` we can just do this:

    $ cd /c/Users/[me]/Documents/RPGs/13thAge/Adventure
    $ pwd
    /c/Users/[me]/Documents/RPGs/13thAge/Adventure

You don't need to know where you are when you're using the absolute filepath! You just need to know where you're going and cd + the absolute filepath will get you there.

# The Weird Stuff

Sometimes you run into weird stuff in using `cd`. Here are two simple ways to make your directory changing work and your life simpler.

First, unless you're already really aware of this stuff, you'll probably have folders on your computer with spaces in the name. I have a folder named *Collections Committee*. But if I try typing:

    $ cd Documents/Collections Committee

I get the error message *sh.exe": cd: Collections: No such file or directory* (gitbash's error message). That's because it doesn't realize that *Collections Committee* is all one directory name.

But, we can fix that without renaming the folder. Instead, I type

    $ cd Documents/Collections\ Committee

See what's different? There's a \\ in front of the space. That \\ is called an escape and it tells the CLI "Hey, she didn't make a mistake here. She wants you to look for something called 'Collections Committee.'"

    $ cd Documents/Collections\ Committee
    $ pwd
    /c/users/[me]/Documents/Collections Committee

Phew! I can still access my directory.

Then there's \*, which is a wildcard in programming just like it is in database searching.

What if I can't remember whether I called a directory "Colloquia" or "Colloquium"? That's where the wildcard comes in. What if I type this?

    $ cd Documents/Collo*
    $ pwd
    /c/users/[me]/Documents/Colloquia

Ok, now I know the name! I'm also where I wanted to be. You can use more than one \* in your path, like `/c/users/[me]/Documents/Collo*/Engine*`. The only thing is, you have to use enough of the directory name for the system to know which directory you mean, so:

    $ cd Documents/Co*
    sh.exe": cd: Co*: No such file or directory

It sees directories called "Code," "Collections Committee," and "Colloquia" and gives me an error because I have too many possible right answers. A lot of the time, if you have a basic idea of where you're going, you can use \* vs. using `ls`. But `ls` is there for when you end up in a situation where you need the specific name of the directory.

# Review

So, we've learned that you can use `cd` to get all over your filesystem.

    $ cd foldername

Will take you into that folder name.

We learned you can move backward using `..` and combine it with forward travel to go back and forward down another branch of your filesystem.

We learned that you can use an absolute filepath to go somewhere completely different.

And then we learned a few tricks to deal with weird cases like spaces in the directory name or not being entirely sure what it's called.

# What's Next?