# Introducing Git
## What is Version Control?
Version control allows you to track the history of a file. Imagine you were working on a document, finished and saved the file, but you’ve realized you’ve made a terrible mistake.  What if you could go back to a previous version of the file — wouldn’t that make your life easier? 

That’s what **version control** does. Version control acts like a database that takes snapshots[^1] of your document or complete project anytime you like. The version control system records the changes to your project’s files. 

Version control also stores metadata about your project, such as the author name, any comments you might add to note modifications to your project.

Version control allows you to work with any kind of document you like; plain text files, spreadsheets, images, sound files — whatever the tool, you can use version control to save previous versions of your work. 

As projects progress, you might find it hard to keep variants of your project in sync. Version control allows you to save versions properly, restore previous versions in case something goes wrong, and collaborate with your teammates without overwriting each others’ changes. 

And even though it isn’t the primary focus of the system, version control also provides a local backup of your project. 

### Distributed Version Control
Some version control systems are *centralized*, which means there is one single master copy of your project, and you check in/check out files from this master copy. Git is not like that. 

Git is a *distributed* version control system. A full copy of your project can exist in many different locations, such as on your workstation, your personal laptop, or on a web server that serves your library’s website. 

The best thing about distributed systems is you don’t have to check them out from a centralized location. You can keep a copy of your entire project on as many computers as you need and work on those files for as long as you want. 

[^1]:	an image of a previous version of your file