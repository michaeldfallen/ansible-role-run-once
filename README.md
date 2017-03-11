Run once role
=========

Role to run adhoc shell scripts on hosts. Useful for migrations and quick fixes.

For example:

```
scripts:
  - 'ln -s ~/Projects/git-radar/git-radar /usr/local/bin/git-radar'
  - cmd: 'git config --global user.email michaeldfallen@gmail.com'
    when_false: 'test `git config --global user.email` == *"michaeldfallen"*'
```
