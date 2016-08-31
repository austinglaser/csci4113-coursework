Lab 0
-----

The main purpose of this lab is to get comfortable with the GNU `bash` shell
found on most Linux distributions, and the filesystem organization. It will
likely be the easiest and most straightforward lab in the course and is meant as
a warm up. Don't get used to things always being this easy!

# Submission Requirements

Copy and past the exercises below into a word document, and then answer each
question in the space below it. If you are already familiary with the basics of
`bash` and the Unix filesystem, push yourself to explore new ways to accomplish
these tasks, or try doing them in a shell you are not normally used to; e.g.
`csh`.

When you get stuck, please ask for help from myself or an SA. Please come to
office hours for help if you can't finish the lab by the end of class. Please
feel free to ask peers for help too, but don't accept any answer without
understanding it.

# Basic Exercises

1.  Once the virtual machine has finished booting, use the command `pwd` to print
    the current (or **p**resent) **w**orking **d**irectory.
2.  How many files does the *home directory* contain? A simple way to find out is
    to use the `ls` command.
3.  How many *hidden* files does the *home directory* contain? With no arguments,
    the `ls` command doesn't show hidden files. Look at the man page for `ls` by
    running `man ls`. You can navigate the man page by using the up and down
    keys.

    **HINT:** *Hidden* files in Unix/Linux have names starting with "`.`". For
    example, `.bash_history` is a *hidden* file.

4.  In what directory would you expect to find the `cp` command?
5.  Where is the command to make a directory (`mkdir`) located on the filesystem?
    What command did you use to find `mkdir`? Give an alternative to the command
    you initially used to find `mkdir`.
6.  Use the `mkdir` command to create a new directory under the root user's home
    directory (i.e. `/root/`). Name it anything you'd like. Use the `touch`
    command to create a file under that directory. What does the new file
    contain?
7.  By default, the `rm` command will not remove directoriess. You can use the
    flag `-r` to tell the `rm` command to remove recursively; i.e., remove all
    files & directories under the target directory (and the target directory
    itself). What happens when you run the command `rm` without `-rf` to remove
    the directory you created in #6? What happens when you run the command `rm
    -rf` to remove the directory you created in #6?
8.  Print the contents of `/etc/passwd`, which contains the list of all users on
    the system in a very specific format. This format is:

        username:password_hash:user_id_number:group_id_number:full_name:home_directory:default_shell

    Write a *command pipeline* to print a list of just usernames here:
9.  Write a *command pipeline* of the `cat`, `cut`, and `tail` commands to print
    only the username of the last user in /etc/passwd here:
10. Combine the `cat`, `cut`, and `sort` commands to print only the usernames,
    sorted alphabetically, in descending order. Write the *command pipeline*
    here:
11. Is the Debian Almquish Shell (`dash`) available on this virtual machine? Is
    the Fish shell (`fish`) available? List two ways below to check the
    availability of a shell.
12. What is the current value of the `$PATH` environment variable? How would you
    append the directory `/usr/local/bin`?
13. Issue this command and explain the result: `>time; date >> time; cat < time`
14. Take a [snapshot of the virtual
    machine](https://www.google.com/url?q=http://www.howtogeek.com/150258/how-to-save-time-by-using-snapshots-in-virtualbox/&sa=D&ust=1472613885947000&usg=AFQjCNHq6m7-kWoYgieicwKKnWxihm_pbQ),
    then run the command `rm / -rf` on your virtual machine. What happened?
    Restart the virtual machine (you may have to click Machine, then Reset).
    Does it boot?
