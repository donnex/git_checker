git_checker
===========

Check git repos for changes, with the ability to auto commit. Written in Python and requires the [sh](https://github.com/amoffat/sh) module.
Auto commit and push can be enabled if used together with a [ssh keychain](http://www.funtoo.org/wiki/Keychain) file. I'm using this to make sure that my config files that are put into a git repo always get commited and pushed to my remote for backup and version control. Also handy as a notification when stuff changes in your code repo or to remind you to commit or push changes. Just setup a crontab and git_checker does the rest.

    Usage: git_checker [-a] [-k keychainfile] [-q] gitdir
    
    Options:
      -h, --help            show this help message and exit
      -a, --autocommit      auto commit the git repo
      -k KEYCHAIN_FILE, --keychainfile=KEYCHAIN_FILE
                            SSH keychain file for auto commits
      -q, --quiet           Don't output anything. Only exit with 0 if everything
                            is clean and 1 otherwise. Can't be used together with
                            auto commit.
