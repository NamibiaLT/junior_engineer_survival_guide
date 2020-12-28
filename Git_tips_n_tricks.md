## git add:

```git add -p``` : the -p stands for patch, it let's you add things in patches and then prints out what you added on your command line so that you can see it.

* there will be options that show up with this git command.
* this is what they mean:
  * **s**: split [do this one first to split up the separate sections that you want to add]
  * **y**: yes
  * **n**: no

## git checkout:

#### This is a destructive command. If you use this, you will lose your work because you've told git to remove it completely.

* ```checkout``` removes changes from your file.
* ```checkout .``` is a command to remove all changes you've made to all files
* ```checkout app``` removes changes from the app directory
* ```checkout [file name]``` removes changes you made to a particular file.



## git rebase:

```git pull --rebase```  or ```git pull -r```  or ```git rebase [branch name]``

* If you have two branches and both have commits, —rebase puts the commits in the order in which they were made and then ammends to the branch in that order.


## revert a commit

#### But save the changes made to a file, just reset the staging:

```git reset --soft HEAD~1```

* reset your git repository to the stage it was in before you added that commit.

#### You made a commit to master, but forgot to pull before hand. What do you do?!
##### Revert to before the commit if it's something that you can easily add back after merging to the right repo:

`git fetch origin
   git reset --hard origin/master
   git pull`

## find lost commits:
Oh no! I know I committed but it got lost in the ether
1. `git fsck --lost-found` to find lost commits and return see all of the lost commit shas
2. `git show <commit sha from the list of shas>` to see what was in that commit
3. `git merge <commit sha>` to merge that commit back into your branch


#### Namibia Torres
