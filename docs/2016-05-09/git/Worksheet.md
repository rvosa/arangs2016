Local git exercises
-------------------

- Create a ~/.gitconfig file with our [example](https://github.com/rvosa/arangs2016/blob/master/docs/2016-05-09/git/example_gitconfig) _i.e. create an invisible file in your home directory, paste the example into it and enter your name and email address in the appropriate location_
- Clone your personal instance of our repository onto your machine, choose the SSH clone url
- Use git to show information about the commit history for the project _git log ._
- Show information about files changed during the commits _git log --name-only_
- Show information about files changed, with the status of each change for
commit 6aac7ffd516dc18b729a7f2c932633c76a5aeed8 (try 6aac7ff) _git show 4c4ff5ece4_
- Add a file to the repository (use your favorite text editor) _e.g. `touch foo` inside the arangs2016 folder_
- Use `git status` to find out the state of the repository
- Try `git status --porcelain`
- What if you didnt like this file, how could you get rid of it (dont do it)? _unstaged: simply delete it_
- Stage this file change _git add foo_
- What do git status, and `git status --porcelain` show
- How could you get rid of this file now? Go ahead and fully delete the file.  _git reset HEAD foo && rm foo_
- Create a new file, and make sure it gets committed to the repository
- What remote git repositories does your git repository know about? _git remote -v_
- Push your new changes to the file up to your github repository _git push_
- Find the newly committed file in your github repository.  Edit it using
Github and make a change.
- Go back to the commandline and use git to `pull` these changes
- Unix `rm` the file you created.
- What do `git status` and `git status --porcelain` show? _deleted_
- Can you get it back? _git checkout foo_
- `rm` it again, then stage the removal. _rm foo && git rm foo_
- Get it back again _git reset HEAD foo && git checkout foo_
- `git rm` the file.  How is this different than using unix `rm`? _both delete and stage_
- Commit the removal of the file, and push the changes up to Github
- Use the Github Web interface to inspect changes for this file.  Can you
still find the contents of the file in Github?  Do you think it is a
good idea to store usernames and passwords in publicly available GitHub accounts? _It's still there, so don't store sensitive data on github_
- Edit one of the files, but do not add the changes.  Create a branch called 'try_bowtie'.  Use git status to find out the state of the repo.  Add and commit
your changes to the branch.  Use git to find out all the branches you have made (you might see branches pulled in when you forked the repository from someone else).  Change to the master branch.  Use git status to find out the state of the repository.  Can you find your changes?  Switch back to the 'try_bowtie' branch.  Can you find your changes now?  Switch back to the master branch.  Merge try_bowtie in to the master branch.  Use git status to find the status of the master branch. Commit and push these changes to Github.  Use the Github web interface to find out if the branch was pushed. Remove the 'try_bowtie' branch from your repository.
```bash
$ echo "CHANGED" >> changed_file
$ git checkout -b try_bowtie
$ git status
$ git add changed_file
$ git commit changed_file
$ git branch
$ git checkout master
$ git status
$ git checkout try_bowtie
$ git status
$ git checkout master
$ git merge try_bowtie
$ git commit
$ git push
$ git branch -D try_bowtie
```
