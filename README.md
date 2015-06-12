# start-to-use-GitHub
This is an exercise about how to use GitHub.

This project updating ever I get free time.

##1. Get a GitHub Account

First things first, create a free account on [www.Github.com](http://www.Github.com). If you're under 13, you'll need a parent's email and help to set up the account.

##2. Create a Repo

. Click the new repo button near the top left of your menu
. Give your repo a name and short description
. Keep 'Public' selected
. Check to initialize with a README
. Click Create Repository

Awesome! Now you've created your very own repo.

##3. Edit a File

You can actually edit files right in GitHub.com! Click the linked blue filename, README.md. Next, click Edit.

You've now got a text box that you can type directly into. Once you've made changes, add a short commit summary. This is your commit message that summarizes the changes you've made. Then click commit changes!


##4. Install Git

A few of the steps may require your computer's password if one is set

Visit [git-scm.com](http://git-scm.com) and download the latest version for your operating system.
In Mac, you won't notice anything or see the application installed, but it will install on your computer.
In Windows, hit Ok or Next for all options, then finish (you don't have to review notes).

##5. Use Bash

![terminal and git bash](http://diy-visualpedia.s3.amazonaws.com/terminal-bash-01.png)

In Mac you've already got Bash. If you go to your Launchpad and search for Terminal, this is the application you'll use.

In Windows you got Bash when you installed Git. Go to Programs > Git and select Git Bash.

We'll refer to both Mac's Terminal and Window's Git Bash as just Bash.

Let's check our Git. In the Bash window type:
command:

###A. version:
```
git --version
```

###B. Configure Git
We need to tell Git who we are so that when we move files around it knows who is moving them. Type the following lines one at a time into Bash and inside of the quotations add the email you signed up to GitHub with and your GitHub username.

```
git config --global user.email "yourGitHub@email.com"
git config --global user.name "yourGitHubusername"
```

###C. Cloning

. Navigate to Folder:

In Macs type:
```
cd Documents
```

In Windows type:
```
cd My\ Documents/
```
The slashes let Bash know that there is a space between 'My' and 'Documents'
Now we're inside the Documents folder, let's put the DIY open-sourcerer repo in it!

###. Clone the Repo
Each repo on GitHub.com has an address for its location. You'll see it following the HTTP and SSH buttons near the top middle of the page. Click on HTTP, this is the address you'll use.

![HTTP Address](http://diy-visualpedia.s3.amazonaws.com/http-addie.png)

```
git clone https://github.com/YOURUSERNAME/open-sourcerer.git
```

Watch as it copies the files! It will also create a folder for you with the name of the repo. When it's done cloning, move into the repo's folder:

```
cd open-sourcerer
```

Now we're inside our very own copy of the files. Let's use ls to list the contents of this folder to see what we've got!

```
ls
```
You should see a list of filenames that look exactly like the files you see on the website for both DIY and your account page.

![cloned files](http://diy-visualpedia.s3.amazonaws.com/cloned-files.png)

###. Connect to Original and Pull Changes

We have one last thing to do. Because this is an open project, we can expect that may others will be doing the same as us: forking, cloning and making changes to the files. We want to make sure we're always working with the most up to date files. To ensure this, we'll connect our local copy to the DIY original so that we can pull in the most recent changes before we work on ours.

Go back to the DIY page for [Open-Sourcerer](http://www.github.com/diy/open-sourcerer), just like our fork had an address, this repo has an address too. We're going to name this connection upstream (because this is where updates will come from).

Type

```
git remote add upstream https://github.com/diy/open-sourcerer.git 
```

###. Pull Changes

Before we make any additions, we want to make sure we have the latest files by pulling in any changes from the master branch upstream.

Type

```
git pull upstream master
```

If it says 'Already up to date' then no changes have been made since you started setting up! If there were changes, it updated your files. In both cases, your files will match the files on DIY's GitHub.com repo.

##6. Edit Story

Bash is awesome - we can even open files with it.

Macs Type:

```
open collaborative-story.txt
```

PCs Type:

```
start notepad "collaborative-story.txt"
```

It should open up the file in your computer's text editor. Add your own portion of the story after the last sentence.

![add to story](http://diy-visualpedia.s3.amazonaws.com/story-addition.png)

When you're done, save the file. Make sure you keep it saved as a .txt file.

##7. Push Changes

Now we'll push (aka add) our changes to our forked copy and then submit them to be added to the DIY original file.

Return to Bash and let's check what changes we've made. Type:

```
git status
```

![git status](http://diy-visualpedia.s3.amazonaws.com/git-status.png)

This shows you what files you've made changes to - it should say collaborative-story.txt. Let's see the difference before and after our changes with diff.

```
git diff
```

![git diff](http://diy-visualpedia.s3.amazonaws.com/git-diff.png)

You'll see a plus and minus sign showing the before and after. Press Q to exit the diff.

##8. Add Changes

Let's tell Git what files we want to add, what our message about our changes is, and push those changes to our fork.

![git status add commit push](http://diy-visualpedia.s3.amazonaws.com/git-status-add-commit-push.png)

Start by adding your changed file:

```
git add collaborative-story.txt
```

##9. Commit Changes

Now we'll add a message describing our changes and attach that to our addition.

```
git commit -m "your description of changes"
```

##10. Push Changes to our Fork

Now, finally, we'll actually push the file and message to our fork on GitHub.com. Remember our fork's name is origin (it's our original file) and the branch is master.

```
git push origin master
```