# Lesson 1

## Learn your environment
In order to effectively learn how to work you need to know what tools you have
available to work with. I have setup your computer with the tools you need like
`git`, `python3`, VSCode, and a Linux environment using Windows 10 WSL 2. If
you want to get help on the internet or from other people you'll need to know
what version of each piece of software you are using.

To start out with open up your Ubuntu WSL instance and find out what version of
Ubuntu you are using. You can use the internet and Google as much as you would
like. This is what you'll be doing on a daily basis to find out things you
don't know. Trust me, there will be new things to learn every day.

Now that you know what version of Ubuntu you're using lets look into what other
versions of software you have. Let's start with Python. Look up how to find out
what version of Python you have. Run the command and write down what version it
is.

Now that you know the Python version and Ubuntu version it will be important to
know what Git version you're running. Find out the Git version and write it
down.

## The Linux command line
While all the modern web pages have nice colors, buttons, tabs, frames, images,
etc. many of the most productive tools you will use are call CLI or Command
Line Interface. Being able to navigate the CLI is going to be important for
many years to come regardless of what new tools come. It's much easier to put
together several small commands, process their output, and create an automated
pipeline of work using the CLI than it is using a GUI (Graphical User Interface).

Some commands that you will need just to get started:
- `ls` List the files and subdirectories in a directory
- `cd` Change directory to either a relative or absolute directory name
- `mkdir` Make a new directory with either a relative or absolute path
- `cp` Copy one or more files or directories to a new location
- `rm` Remove (delete) one or more files or directories
- `man` Look at the manual page for a Linux command

To start let's use the `man` command to start learning more about each command.
Type `man` and hit enter. It should ask you what manual page you want to see.
In order to let it know what you really want to see you give it another parameter
so now let's type `man ls`. You now see a lot of text that starts to tell you
about the `ls` command. You are also in a navigation page similar to `vi` which
we will get to later. While you are in a `man` page you can use the keyboard to
navigate around the page. The `j` key will go up one line at a time, the `k` 
key will go down one line at a time. The `b` key will go back a while page at a
time. The `f` key will go forward one page at a time. Move around the man page
for `ls` and find the parameter that will list files sorted by modification
time. Next find the parameter that will sort them in reverse order. Write down
the parameters you found and try them out.
