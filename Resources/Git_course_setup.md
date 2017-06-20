# Set up BI621 with Git

## Set up Git/GitHub
Be sure you have a [GitHub](https://github.com/) account and be sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) installed on your computer.

After creating your GitHub account, request and Education account [here](https://education.github.com/discount_requests/new).

Test your installation by issuing the command ```git``` on the terminal. You should see something like the following:
```
usage: git [--version] [--help] [-C <path>] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

These are common Git commands used in various situations:
```
Here are some [Git and GitHub learning resources](https://help.github.com/articles/git-and-github-learning-resources/) to help.

Be sure you have provided your GitHub name to Leslie so you can be added to the 2017_Bi621 repository. Look for the invitation link in the email address you provided GitHub.

## Setup 2017_Bi621 on your computer

Before performing the steps in this section, be sure you have:
1. Git installed on your computer.
2. A GitHub account.
3. Accquired an Education discount for unlimited free, private repositories.
4. Accepted your invitation to collaborate on the 2017_Bi621 repository.

You're now ready to clone the repository onto your machine. Navigate to the directory on your computer you'd like to clone the repository into.
1. Clone the repository by issuing the following command (if you're new to using the command line, *note!* the ```$``` is not typed, it's mearly indicating the prompt):
```
$ git clone https://github.com/Leslie-C/2017_Bi621
```
Change to the newly cloned repository:
```
$ cd 2017_Bi621
```
2. By default, the remote called ```origin``` is set to the location you cloned the repository from. You should see the following:
```
$ git remote -v
	origin	https://github.com/Leslie-C/2017_Bi621 (fetch)
	origin	https://github.com/Leslie-C/2017_Bi621 (push)
```
We want to change the origin to be YOUR repository. To do this:
```
$ git remote rename origin upstream
```
And you should see:
```
$ git remote -v
	upstream	https://github.com/Leslie-C/2017_Bi621 (fetch)
	upstream	https://github.com/Leslie-C/2017_Bi621 (push)
```
3. On your GitHub account, click the ```New Repository``` button.
4. Enter a repository name. I suggest ```Bi621``` or similar. Add an optional description, and make the repository ```Private``` for now. Do NOT initialize with a ```README```. Create the repository.
5. On your own computer, issue the following command, but with your GitHub username in place of <username>. If you called your repository something other than ```Bi621```, be sure to change that as well.
```
git remote add origin https://github.com/<username>/Bi621
```
Now you should see:
```
$ git remote -v
	upstream	https://github.com/Leslie-C/2017_Bi621 (fetch)
	upstream	https://github.com/Leslie-C/2017_Bi621 (push)
	origin	https://github.com/<username>/Bi621 (fetch)
	origin	https://github.com/<username>/Bi621 (push)
```
6. Test your setup:
```
$ git push -u origin master
```
You should see something like the following:
```
example
```
7. From now on, you can just issue ```git push``` without the arguments. Try it out!
```
$ git push
	Everything up-to-date
```
8. As new materials are added, be sure to
```
$ git pull upstream master
```
to keep things up-to-date.
