# start-to-use-GitHub
This is an exercise about how to use GitHub.

This project updating ever I get free time.

##1. Get a GitHub Account

First things first, create a free account on www.Github.com(http://www.Github.com). If you're under 13, you'll need a parent's email and help to set up the account.

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

Visit git-scm.com(http://git-scm.com) and download the latest version for your operating system.
In Mac, you won't notice anything or see the application installed, but it will install on your computer.
In Windows, hit Ok or Next for all options, then finish (you don't have to review notes).

##5. Use Bash

![terminal and git bash](http://diy-visualpedia.s3.amazonaws.com/terminal-bash-01.png)

In Mac you've already got Bash. If you go to your Launchpad and search for Terminal, this is the application you'll use.

In Windows you got Bash when you installed Git. Go to Programs > Git and select Git Bash.

We'll refer to both Mac's Terminal and Window's Git Bash as just Bash.

Let's check our Git. In the Bash window type:
command:

#A. version:
```
git --version
```

#B. Configure Git
We need to tell Git who we are so that when we move files around it knows who is moving them. Type the following lines one at a time into Bash and inside of the quotations add the email you signed up to GitHub with and your GitHub username.

```
git config --global user.email "yourGitHub@email.com"
git config --global user.name "yourGitHubusername"
```

#C. Cloning

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

#. Clone the Repo
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