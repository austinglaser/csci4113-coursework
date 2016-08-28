# Lab 1

The only Linux system administrator at Dunder Mifflin recently quit on very
short notice. 'Management' has chosen you to temporarily fill the role because
you are the only one (of our *valued* employess) with any Linux experience.

You've been informed that your new position starts on Tuesday, and that there
is no funding for additional training prior to assuming the role. A few buddies
have suggested starting out by writing two basic `bash` scripts to gain
experience with the command line.

These scripts are easy to describe and harder to implement. Essentially, you'll
create two different `bash` scripts to do the following:

1. Monitor the space utilization of the `/` directory as indicated by the `df`
   command, and send an e-mail to the root account using the `mail` program
   when it exceeds a specified threshold (80% is reasonable.)
2. Display a *system dashboard* to give a brief overview of the current state
   of the system from three different perspectives: CPU/RAM, network, and user
   accounts

Programs that you'll find useful are: `free`, `uptime`, (load average indicates
CPU utilization), `cat /proc/net/dev`, `cat /etc/passwd`, and `ping`.

Please note that the 1-byte return status, or code, of a command usually
indicates success or failure of that command. `bash` makes that available in
`$?`. A sample output of the dashboard appears below.

You must at a minimum implement the features shown in the sample output, but
graduate students are always expected to go beyond the minimum expectations. If
you need ideas about how to go beyond, then please ask.

    [root@localhost: ~]# ./dashboard.sh
    CPU AND MEMORY RESOURCES --------------------------------
    CPU Load Average: 0.01, 0.01, 0.00             Free RAM: 412 MB

    NETWORK CONNECTIONS -------------------------------------
    io Bytes Received: 0           Bytes Transmitted: 0
    enp0s3 Bytes Received: 21632         Bytes Transmitted: 10674
    Internet Connectivity: Yes

    ACCOUNT INFORMATION -------------------------------------
    Total Users:        19        Number Active: 1
    Most Frequently Used Shell:        /sbin/nologin

Do your best to write these scripts with as little Googling as possible. The
more you rely on Google, the harder it is to develop effective `bash` CLI
skills.

A few helpful hints are:

- Sometimes you must 'escape' characters that have special meaning to `bash`
    (e.g. `|`)
- Some commands have very helpful formatting flags (e.g. `-e` or `-n` with
    `echo`)
- If you are sure that you sent mail to the local root account but it never
    arrives in `/var/mail/root`, make sure that the postfix daemon is running.

These scripts can be implemented entirely with the commands in the command
reference for this week plus those listed in this document above.

# Prerequisites

Please finish the first two homework assignments before starting the lab. You
will also need to install some software on your machine. Run the following
command to ensure that you have the necessary *packages* before proceeding:

    # yum install man mail

# Submission Requirements

1. Please submit both scripts in the Desire2Learn Dropbox for this lab as `.sh`
   files.
2. The dashboard script, at a minimum, should have all the items in the output
   listed above. The formatting need not be exactly the same. You must extract
   and display the required portions of text from the commands, not simply
   display the output of the commands.
3. The disk utilization monitoring script should send an e-mail when the disk
   space of the root partition exceeds a percentage defined by a variable in the
   script (parametrize!)
4. Scripts must work with the version of `bash` included in CentOS 7.x
