# Homework 1

## Reading

Select one of the following resources to read in addition to the *material on
grep* and *bash globs and pattern matching* found in D2L.  The UNIX and Linux
System Administration Handbook, 4th Edition  (ULSAH4) is more in-depth and
detailed.  The CentOS Bible is more geared toward beginners.  The free reading
material is, well, free reading material.  Your mileage may vary.

- ULSAH4, Chapter 2, Section 2.2.  If you feel brave, try reading through 2.3
  (Regular Expressions).
- [The Linux Command Line Website: Writing
  Scripts](https://www.google.com/url?q=http://linuxcommand.org/lc3_writing_shell_scripts.php&sa=D&ust=1472368865040000&usg=AFQjCNGhOHOowtCIiUxwiWkEQq2BINRLTw)...
  Stop when you get to #13.

## Exercises and Preparation

- Use your Google powers to find one command not listed on this week’s command
  reference or discussed in class.  Come to class prepared to briefly explain
  what the command does and why it is handy.  Submit this command and a short
  explanation in the D2L dropbox.
- Finish `vimtutor` as described in class. You need to edit the file
  `/etc/sysconfig/network-scripts/ifcfg-enp0s3` and change `ONBOOT=yes`, then
  reboot the virtual machine (or at least *bounce* the interface) to connect
  to the internet. You then can install `vimtutor` (and `man` and any other
  *packages*) with the command:

    # yum install vim-enhanced man

Once installed, `vimtutor` can be launched with the command:

    $ vimtutor

## Submission Requirements

Please submit the following in the *correct* Desire2Learn Dropbox folder. D2L
links these folders under Assesments->Dropbox.

1. Your muddiest point, or one item from the reading/study material that you
   found most confusing. Please submit as plain text in the dropbox itself.

Please submit the following in the Homework 1 discussion form on D2L under
Communication->Discussions.

1. One command not listed in the command reference, an explanation of what it
   does, and example usage.
