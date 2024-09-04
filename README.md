#1 step — Time to start!
Looking forward to getting started? Let’s do it!

This first exercise is not very complicated; it’s divided into two steps. The Git installation and GitHub account creation.

a. GitHub account creation

To create your account, you need to connect on the main GitHub page and to fill in the registration form.


GitHub main page with registration form
Nothing more! You are officially a new member of GitHub!

b. Git installation

Now you need to install Git tools on your computer. There are different Git software, but it’s better to install the basic one to start. We will use the command line to communicate with GitHub.

Once you are more comfortable with the command line, you can download Git software with a user interface.

For Ubuntu:
First, update your packages:

$ sudo apt update
Next, install Git with apt-get:

$ sudo apt-get install git
Finally, verify that Git is installed correctly:

$ git --version
For MacOSX:
First, download the latest Git for Mac installer.

Next, follow instructions on your screen.

Finally, open a terminal and verify that Git is installed correctly:

$ git --version
For Windows:
First, download the latest Git for Windows installer.

Next, follow instructions on your screen (you can leave the default options).

Finally, open a terminal (example: powershell or git bash) and verify that Git is installed correctly:

$ git --version
For all users:
One last step is needed to complete the installation correctly! You need to run in your terminal the following commands with your information to set a default username and email when you are going to save your work:

$ git config --global user.name "Gaël Thomas"
$ git config --global user.email "example@mail.com"
#2 step — Your first GitHub project!
Now that you’re ready, you can return to the main GitHub page and click on the “+” icon in the menu bar.


GitHub menu bar with “+” icon
Once you click on this button, a new menu appears with a “New repository” entry. Click on it!


Submenu with “New repository” entry
The repository creation page will appear. Choose a cool name for your first repository and put a small description before clicking on the “Create repository” button.

Note: In the context of this article, please don’t tick “Initialize this repository with a README”. We will create a “README” file later!


Repository creation menu
Well done! Your first GitHub repository is created. If you want to see all your repositories, you need to click on your profile picture in the menu bar then on “Your repositories”.


Submenu with “Your repositories” entry
#3 step — A good cover
It’s time to make your first modification to your repository. What do you think about creating a cover for it, a kind of welcome text?

a. A local version of your project

Your first mission is to get a copy of the repository on your computer. To do that, you need to “clone” the repository. On the repository page, you need to get the “HTTPS” address.


Repository page with “HTTPS” address
Once you had the address of the repositories, you need to use your terminal (through shell commands) to move in the place where you want to put the directory copy (for example you can move in your “Documents” folder). When you are ready, you can enter:

$ git clone [HTTPS ADDRESS]
This command will make a local copy of the repository hosted at the given address.


Output message of “git clone” command
Now, your repository is on your computer. You need to move in it with:

$ cd [NAME OF REPOSITORY]
Note: When you clone, Git will create a repository on your computer. If you want, you can access your project with the computer user interface.

b. Repository edition

Now you can create a file named “README.md” in your folder (through the terminal or user interface on your computer). I’m not giving you any more details about this step, nothing in particular. Open your folder and add a file as if it were a standard folder.

If you want to do something cool, copy and paste this template in your “README.md” file. You can replace information between the hooks to personalize the output.


c. Let’s share our work!

Now that you have modified your project, you need to save it. This process is called committing.

To do this, get back to your terminal. If you have closed it, go back in your folder.

When you want to save your work, four steps are required. These steps are called: “status”, “add”, “commit” and “push”. I have prepared a standard procedure for you to perform each time you want to save your work.

Note: All the following steps must be performed within your project.

“status”: The first thing you need to do once your work is to check the files you have modified. To do this, you can type the following command to make a list of changes appear:
$ git status

“git status” output in our project
“add”: With the help of the change list, you can add all files you want to upload with the following command:
$ git add [FILENAME] [FILENAME] [...]
In our case, we are going to add “README.md” because we want to save this file.

$ git add README.md
Note: If you type again “git status”, the “README.md” will appear now in green. This means that we have added the file correctly.

“commit”: Now that we have added the files of our choice, we need to write a message to explain what we have done. This message may be useful later if we want to check the change history. Here is an example of what we can put in our case.
$ git commit -m "Added README.md with good description in it."
“push”: You’re there, you can now put your work online! If you type the following command, all your work will be put online and visible directly on the repository page.
$ git push origin master
You did it! If you come back on your repository page on GitHub, you are going to your “README.md” file with a beautiful preview of it.


Repository page with “README.md” file
Useful commands for Git
You are still missing some essential commands as a beginner with Git. Here is a list that will be useful to you during your project.

Display the history of commits (all modifications made on the project).
$ git log
Revert back all your changes since the last commit.
$ git checkout .
Revert all changes on a specific file since the last commit.
$ git checkout [FILENAME]
Display the last changes on a file since the last commit.
$ git diff [FILENAME]