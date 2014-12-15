# What's in the Box? Using LS

So, we've turned on our GPS with `pwd` and we know where we are. But if we want to move around between directories or work with files, we have to know what files and directories are located inside this directory. So how do we know what's in the directory?

This brings us to the world's best CLI command (personal opinion), `ls`.

It's as simple as that. You're in a directory and used `pwd` to find out where you are (you don't have to, but I'm showing you this is a place you can use it). Once you get the result, you type `ls`:

    $ pwd
    /c/Users/[me]/Documents/Code
    $ ls

press Enter, and you'll get something like:

    $ pwd
    /c/Users/[me]/Documents/Code
    $ ls
    Wordpress        Outline.docx      GitHub
    HTML file dump   libtech_level-up  test.html

Those items without any extension like .html or .docx are the directories (again, folders) that are inside Code. The order the the things listed doesn't always make sense. If you have a lot of files in a directory, this can become a really long list.

And that's really it. Later on, you'll learn some fun arguments, which are controls to handle how the list of files display.

Next, let's learn about **CD &mdash; Moving from A to B to A to C!**