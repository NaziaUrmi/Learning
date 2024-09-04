

Finally, open a terminal (example: powershell or git bash) and verify that Git is installed correctly:

```

$ git --version 

$ git config --global user.name "Gaël Thomas"
$ git config --global user.email "example@mail.com"

```

##### GitHub project:
Now that you’re ready, you can return to the main GitHub page and click on the “+” icon in the menu bar.


GitHub menu bar with “+” icon
Once you click on this button, a new menu appears with a “New repository” entry. Click on it!


Submenu with “New repository” entry
The repository creation page will appear. Choose a cool name for your first repository and put a small description before clicking on the “Create repository” button.


Your first GitHub repository is created. If you want to see all your repositories, you need to click on your profile picture in the menu bar then on “Your repositories”.


Submenu with “Your repositories” entry

##### A local version of your project:

Your first mission is to get a copy of the repository on your computer. To do that, you need to “clone” the repository. On the repository page, you need to get the “HTTPS” address.


Repository page with “HTTPS” address
Once you had the address of the repositories, you need to use your terminal (through shell commands) to move in the place where you want to put the directory copy (for example you can move in your “Documents” folder). When you are ready, you can enter:
```

$ cd [NAME OF REPOSITORY]

$ git clone [HTTPS ADDRESS]

```

This command will make a local copy of the repository hosted at the given address.


##### Repository edition (Create):

Now you can create a file named “README.md” in your folder (through the terminal or user interface on your computer). I’m not giving you any more details about this step, nothing in particular. Open your folder and add a file as if it were a standard folder.

If you want to do something cool, copy and paste this template in your “README.md” file. You can replace information between the hooks to personalize the output.

1. Open your terminal or command prompt.

2. Navigate to the Git repository where you want to create the `README.md` file. You can use the `cd` command to change directories. For example, if your repository is located on your desktop, you might use:

```
cd ~/Desktop/repository-name

```


3. Create the `README.md` file using any text editor or terminal command. For example, you can use the `touch` command to create an empty file:

```
touch README.md
```

##### Repository edition (modification save):

Now that you have modified your project, you need to save it. This process is called **committing**.

To do this, get back to your terminal. If you have closed it, go back in your folder.

When you want to save your work, four steps are required. These steps are called: “status”, “add”, “commit” and “push”. I have prepared a standard procedure for you to perform each time you want to save your work.

Note: All the following steps must be performed within your project.

1. **status**: The first thing you need to do once your work is to check the files you have modified. To do this, you can type the following command to make a list of changes appear:

```
$ git status

```

2. **add**: With the help of the change list, you can add all files you want to upload with the following command:
```
$ git add [FILENAME] [FILENAME] [...]

```

In our case, we are going to add “README.md” because we want to save this file.
```
$ git add README.md

```

Note: If you type again “git status”, the “README.md” will appear now in green. This means that we have added the file correctly.

3. **commit**: Now that we have added the files of our choice, we need to write a message to explain what we have done. This message may be useful later if we want to check the change history. Here is an example of what we can put in our case.

```
$ git commit -m "Added README.md with good description in it."

```

4. **push**: You’re there, you can now put your work online! If you type the following command, all your work will be put online and visible directly on the repository page.

``` 
$ git branch -M main

$ git push origin master

```


### Useful commands for Git:

1. Display the history of commits (all modifications made on the project).
``` 
$ git log

```
2. Revert back all your changes since the last commit.
```
$ git checkout 

```
3. Revert all changes on a specific file since the last commit.
```
$ git checkout [FILENAME]

```
4. Display the last changes on a file since the last commit.
```
$ git diff [FILENAME]

```