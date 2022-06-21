# Useful Git Commands 

#### To push contents to a new repo 

Note: if the existing folder was one used with github, 
	delete .git folder before starting 

    $ git init
    $ git add . // to add all contents
    $ git commit -m 'first commit'
    $ git remote add origin <git@github...>
    $ git push -u origin master

#### To delete a bad commit ie pushed to main accidently

    $ git revert <bad commit>
    $:wq //if vim
    $ git push

#### Change global git email
	$ git config --global user.email "<insert email here>"
	$ git config --global user.email

#### Commit history
	$ git clone https://....
	$ git log

#### Find out when a change was made and who are the authors of an individual file
	$ git blame README.MD // displays username
	$ //or
	$ git blame -e README.MD // display email instead 

#### Look at the changes from a single commit
	$ git show <enter hashcode for commmit> // can locate at github
	$ //or 
	$ git log --graph --oneline --decorate // display branch graphics

#### Find latest git commit hash
	$ git log -1 --format=format:"%H"
	$ //or
	$ git rev-parse HEAD

#### See changes to branch
	$ git status

#### Save work and reverse those changes so you can move between branches
	$ git stash

#### Apply stashed changes to branch
	$ git stash apply

#### Undo git add 
IMPORTANT: Do not forget the flag --staged or else it will
undo local changes too!
	
	$ git restore --staged index.html 
