# Intro

Let's get a couple things out of the way to start with. Unix was originally
created in the 1970's as an experiment to see what a few people could do with
an older piece of hardware. It was a pretty good idea and a lot of companies
made their own Unix. IBM made AIX, HP make HP-UX, Sun made Solaris, etc.

Today there is raelly only one Unix left and that's Linux. Ubuntu (what you're
using now) is just a distribution of Linux. That means that they made a
company and starting gluing parts of software together into an operating system
and all the software that comes with it. So, when I say Unix it will generally
mean Linux and for your case specifically it will mean Ubuntu.

# Setup

Unix has some built in functionality that we will use to demonstrate some neat
features that just come with Unix. Some of those things are `sudo`, `words`,
`grep`,`cat`,`head`,`tail`, and `wc`.

To start with lets check to see if your Unix has the `words` file. It is
commonly found in either the `/usr/share/dict/words` or `/usr/dict/words` file.
Check those locations using your `ls` command and see what you come up with.

You probably didn't find anything because it didn't come installed by default
when we setup your Ubuntu instance. Ubuntu uses a package manager called `apt`
to install and manage prebuilt software. There are lots of ways to get software
onto your computer but using a package is generally the easiest way to to do it.
I have done a little bit of research and I know that the package
`wamerican-huge` contains a large list of dictionary words. Use the command
`apt-get install wamerican-huge` to install your dictionary.

You probably got a message that looks like this:
```
E: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
```
The error message asks a good question, "are you root?".

Being `root` means that you are THE admin in Unix. The `root` ID bypasses most
security and has rights to do everything. In order to be safe and not do things
by accident that would destroy the system or delete things that should not be
deleted we generally will use our own IDs and only use the `root` privileges as
necessary. In this case it's necessary so we're going to use something called
`sudo` which is short for "switch user and do". When you invoke sudo and then
give it a command it will run the command as `root` so it has extra power.

Check out [this XKCD comic](https://xkcd.com/149/) to see what I mean.

Now run `sudo apt-get install wamerican-huge` and it will prompt you for your
password and execute the command to install the dictionary. Now look in
`/usr/share/dict` and see what shows up. You have a couple of new files now
right? If not we can look at it and see what went wrong.

# Looking in Files

Let's check out the file and see what we can find out about it. One of the first
things you'll probably want to do is look at the file so let's run the `cat`
command on it. `cat` is short for `concatenate` but in this case we're going
to abuse the command and just `concatenate` the file with what is called
"standard out" or "stdout" (your terminal output). Run `cat /usr/share/dict/words`
and see what that does.

Ok, that was a lot of output. How many lines do you think that was? There's an
easy way to tell. Unix has a built in command called `wc` that can count words.
Check out the man page and then we can continue. We can see that the file has
one word per line. How can we use `wc` to tell us how many words are in the
file? Is there another way to tell us how many words are in the file? How many
total characters are in the file?

Sometimes you just want to see the first few lines of a text file like a startup
log or the last few lines of a file like an application log (so you would know
what it just got done doing). Unix has some built in commands for that too.
`head` will show you the first lines of a file and `tail` will show you the
last lines of a file. Using your `man` pages how would you look at only the
first 20 lines of our new words file? How would you look at only the last line
of the words file?
