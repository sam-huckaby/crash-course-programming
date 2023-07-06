**WARNING**
You're about to read a bunch of things that won't always make sense. Now, there are going to be many times in your journey where understanding simply that something works will be enough, even if you don't know HOW it works. **This is not one of those times.** You need to have a basic understanding of Git.

# Getting Started On Your Journey

Welcome to the first part of the crash course programming program! We will be starting off by looking at Git. I also regret we will be starting with a glossary, but I promise that defining our terms up-front will prove invaluable in the long term.

| Term | Definition |
| --- | --- |
| Git | Git is a software program. It's not a website and it's not a **repository**. It is a software that is used to create **repositories** which can be hosted on a website like GitHub (which is where this course lives). |
| Repository | A **repository** is a collection of code. You might be more familiar with a folder or directory on your computer. A repository is like a folder on your computer, it stores other files and folders. Now, maybe you're wondering: "Why not just call it a folder then?" and that would be a super good question. It turns out the reason is simple: time travel. You read that right. Git is a folder that allows you to time travel by creating **commits** that you can warp back to. It also creates a "multiverse" of sorts, because that one folder actually exists in alternate dimensions (called **branches**) where the things inside the folder are slightly different. |
| Commit | No, this is not the thing we were all afraid of doing in high school (unless you were super nerdy like me). A **commit** is a collection of changes that you want to make to one of the alternate realities (**branches**) in a repository. When you open a file in a normal folder and make a change, you will see the last updated date change to the current time. A **commit** is a change like that, but possibly multiple files that are all being changed at the exact same time (in git's eyes, you make them normally). You make the changes individually, and then you create a **commit** to bundle all the changes together before submitting that change (**pushing**) to the **repository**. |
| Branch | Every **repository** starts with a single **branch**, or a single version of reality, usually called either "main" or "master". Additional **branches** are like alternate realities where one or two things were done differently and things ran their course. Imagine you have a **repository** that stores the files for your personal website (hey, that's what this **repository** does...). Now imagine that in your "main" **branch** you have a banner that goes across the top with a green background. Now imagine that you've heard from some of your friends that green is _boring_, and you're considering changing the color to something more lively, like orange. You could create a **branch** and call it "pizzaz_renovation" (**branch** names can't have spaces) and in that **branch**, you add a **commit** (a set of changes) that changes every banner on your website to make them orange. Now you still have your main **branch** with green banners, but you ALSO have another reality where the banners are orange. Down the road, you may decide that you agree with your friends and you can **merge** that **branch** into the main **branch**, and then the banners in the main **branch** will be orange. You could also decide that you don't really care what your friends think, and delete that **branch**, keeping your banners green in your main branch. |
| Merge | **Merging** is taking the code from one **branch** (alternate reality), and combining it with the code from another **branch**. **Merges** can take place between two **branches** in a single **repository**, or between two **branches** in separate **repositories**. When a merge takes place, git (the software program) will look at each line in each file that is being changed, and will keep the line that has changed from the original. This can lead to problems, because potentially someone else has changed the line you are trying to change without telling you, in which case you have a **conflict** which is where git is unsure which change is supposed to be kept. In the case of a **conflict**, git will ask you to tell it which things to keep and which things to get rid of. |

[ EDITING POINT - LINES BELOW HAVE NOT BEEN UPDATED ]

Maybe you've heard of git before, or maybe it sounds like something an angry southern belle would yell at you if you tried to eat her freshly baked peach cobbler.
Git is a source management tool, or you can think of it as a library system for code. The git repository is the central storage place for information about an application or group of applications, and you "checkout" versions of that application or group of applications and make changes to individual files. Git keeps track of all the changes and provides sane ways of bringing things back together into a single version of the entire thing.

To get started, we're going to go through a simple workflow that won't entirely make sense but will at least make things a little less scary because you will have "done them" already.

We'll start with a high-level overview of what we'll be doing:

1. **Forking** a repository - this creates a copy of a repository in your own GitHub account.
2. **Cloning** the repository - this downloads the repository to your local machine so you can make changes.
3. **Editing** a file - you'll add your name to the `I_WAS_HERE.md` file in your fork of this repository.
4. **Committing** your changes - this saves your changes to your local copy of the repository.
5. **Pushing** your changes - this uploads your changes to your forked version of the repository in Github.
6. **Creating a Pull Request** - this proposes your changes in the forked repository to the original repository.

Did your eyes glaze over? There were a lot of big words in there, and some of it could be a little confusing. Let's break it down just a tiny bit before we move on.

Before you start, there is only the one repository and it is the one that you are reading right now (not counting other people's copies).

When you fork this repository, there will now be TWO repositories: this one and a new one that you own (in Github).

When you clone your fork, there will now be THREE repositories: this one, the one that you own (in Github), and one on your local computer.

Any time you propose a change to another person's repository, you will make the changes in your local repository, you will commit and push that change to the repository that you own in Github, and then you will open a "Pull Request" in the other person's repository which is just a polite way of asking them to include your changes in their version of whatever it's a repository for.

Hopefully that made things a little clearer, but if not, just follow along with the tutorial and you will start to understand as we go.

Alright, let's dive into it!

## Step 1: Forking the Repository

1. Navigate to the repository you want to fork: [https://github.com/sam-huckaby/crash-course-programming](https://github.com/sam-huckaby/crash-course-programming)
2. Click on the "Fork" button in the top right corner of the page.
3. You'll be redirected to your personal copy of the repository. You can tell it's your fork because the repository name will now start with your GitHub username (at the top left of the page).

## Step 2: Cloning the Repository

1. Now you want to get this code onto your local machine. Click on the green "Code" button on your repository page.
2. Copy the URL that shows up. (in a perfect world, [you should already have an SSH key setup](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account))
3. Open a terminal window on your local machine. (If you're using Windows, I'm sorry. I will write something up for you soon)
4. Navigate to the directory where you want to clone the repository using the `cd` (change directory) command. For example: `cd /path/to/your/directory/`.
5. Once you're in the right place, type `git clone [the URL you copied]`. For example: `git clone https://github.com/[your_username]/crash-course-programming.git`.
6. This will create a new directory in your current location with the cloned repository.

## Step 3: Editing a File

1. Go to the new directory that was created when you cloned the repository: `cd crash-course-programming`.
2. Open the `I_WAS_HERE.md` file in your favorite text editor. It might look something like this: `nvim I_WAS_HERE.md` or `code I_WAS_HERE.md` (NeoVim is my preference, but it can be daunting for beginning developers. I may create a simple walkthrough for that in this course as well later)
3. Add your name to the file, save and close it.

## Step 4: Committing Your Changes

1. Go back to your terminal window.
2. Type `git add I_WAS_HERE.md`. This stages your changes for committing.
3. Now commit your changes with a message. Type `git commit -m "Added my name to I_WAS_HERE.md"`. This saves your changes with a description of what you did.

## Step 5: Pushing Your Changes

1. Still in your terminal window, type `git push origin main`. This pushes your committed changes up to your forked repository on GitHub.

## Step 6: Creating a Pull Request

1. Go back to your forked repository on GitHub.
2. Click on the "Pull requests" tab, then click the "New pull request" button.
3. You'll be redirected to the "Comparing changes" page. Here, you're comparing the original repository (base repository) and your forked one (head repository).
4. Make sure you're proposing to make changes to the correct branch (`main` in the base repository).
5. Click "Create pull request".
6. Add a title and description for your changes.
7. Finally, click "Create pull request" again.

And voila! You've successfully forked a repository, made a change, and opened a pull request. You're now participating in the open-source world, contributing your bit to the ocean of collective knowledge. Well done!

Remember, the magic of Git and GitHub lies in collaboration. You can now wait for the maintainer of the original repository to review and possibly merge your changes. If they have any suggestions or require some changes, they'll let you know, and you'll learn from it.

Keep exploring, keep coding, and keep contributing!
