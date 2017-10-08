

Oct 8, 2017
===========
Set up a git repo on Caliper.

1. Log in as user "git" and add the ssh public key.
$ sudo su - git

$ cat xx.pub >> ~/ssh/authorized_keys


2. Set up the repo.
$ cd git
$ mkdir foursquare.git
$ cd foursquare.git
$ git init --bare


3. Set up user name and email.
In .git/config, add

[user]
        name = William Wong
        email = william.s.wong@gmail.com

Check by running
$ git config --list


4.  As "williamw",
$ git init
$ git add README.txt
$ git commit

// Check that the correct credentials are used.
$ gitk

$ git remote add origin git@10.0.1.13:/home/git/git/foursquare.git
$ git push origin master


5. To clone the repo.

  $ git clone git@localhost:/home/git/git/foursquare.git

