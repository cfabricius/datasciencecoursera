<html>
<head>
<link rel="stylesheet" type="text/css" href="screen.css">
</head>


Basic Git Commands
========

**Initialisation**

* git config --global user.name <UserName> 
* git config --global user.email <email> 


**Tweaks**

* git config --global color.ui "auto" 
* git config --global pack.threads "0" 

**Working with Repos**

* git init (Create an empty Git repository or reinitialize an existing one) 
* git remote add origin https://github.com/<UserName>/<repoName>.git (add new remote repo) 
* git add  <filename> (add file to repo) 
* git commit -m "<comment>" (Record changes to the repository,post given comment) 
* git push -u origin master (Update remote refs along with associated objects) 
* git clone https://github.com/<UserName>/<remoteRepo>.git (Clone a repository into a new directory) 
* git pull (Fetch from and integrate with another repository or a local branch)

Advanced
========

* git remote [-v | --verbose]
* git remote add [-t <branch>] [-m <master>] [-f] [--[no-]tags] [--mirror=<fetch|push>] <name> <url>
* git remote rename <old> <new>
* git remote remove <name>
* git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
* git remote set-branches [--add] <name> <branch>…​
* git remote get-url [--push] [--all] <name>
* git remote set-url [--push] <name> <newurl> [<oldurl>]
* git remote set-url --add [--push] <name> <newurl>
* git remote set-url --delete [--push] <name> <url>
* git remote [-v | --verbose] show [-n] <name>…​
* git remote prune [-n | --dry-run] <name>…​
* git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)…​]

</html>
