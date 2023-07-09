**WARNING**
You're about to read a bunch of things that won't always make sense. Now, there are going to be many times in your journey where understanding simply that something works will be enough, even if you don't know HOW it works.

**This is not one of those times.** You need to have a basic understanding of Git.

# Getting Started On Your Journey

Welcome to the first part of learning how to program! We will be starting off by looking at Git. Before we get started, you should familiarize yourself with the layout of [the glossary](GLOSSARY.md) found in this repository. When you come across crazy new words, I want you to plan to read the glossary definition before you continue. The glossary will give you a reference point to look back at as you move through the course, and complicated terms will often be linked back to the glossary multiple times, so you can re-read the definition if you need to. There is no shame in needing to look at a definition more than once, that is how we as humans learn things, it is expected.

With that out of the way, let's actually get started.

Maybe you've heard of [git](GLOSSARY.md#git) before, or maybe it sounds like something an angry southern belle would yell at you if you tried to eat her freshly baked peach cobbler.
Git is a source management software, or you can think of it as a library system for code. The git [repository](GLOSSARY.md#repository) is the central storage place for information about an application or group of applications, and you "checkout" versions of that application or group of applications and make changes to individual files. Git keeps track of all the changes and provides sane ways of bringing things back together into a single version of the entire thing.

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
