# gitTutorial

This is a partnered activity to learn and practice basic git commands.

## Setup

There are two roles, A and B. Decide now who will be partner A and who will be parter B.
In this setup, Parter B needs to wait until Parter A has finished their Step1. 

### A (Step 1)
1. Go to github(www.github.com)
1. Create a new empty repository
1. Name it anything, (just remember the name)
1. Open the terminal on your computer.
    1. On Mac, open your Applications folder, then open the Utilities folder and select Terminal.
    1. On Windows, select Start and type Git Bash. Select Git Bash to open the terminal.
1. Use the `cd` command to navigate to the directory that you want the repo to belong.
1. **Clone** your new repo by copying the url in the Clone/Download button using `git clone <url>`
1. **Download** this repository as a .zip.
1. Unzip and drag and drop all files from the downloaded folder into your local repo
1. Enter your repo in terminal using `cd <repo name>`
1. Type the following commands:
    1. `git add *`
    1. `git commit -m "first commit"`
    1. `git push`
    
### B (Step 1) 
1. Open the terminal on your computer.
    1. On Mac, open your Applications folder, then open the Utilities folder and select Terminal.
    1. On Windows, select Start and type Git Bash. Select Git Bash to open the terminal.
1. Use the `cd` command to navigate to the directory that you want the repo to belong.
1. **Clone** your new repo by copying the url in the Clone/Download button using `git clone <url>`

## Part 1 (Branches)
This part can be completed simultaneously. 

### A (Step 2)
1. Make sure you are in the same directory in terminal as before.
1. Use the command `git checkout -b a_branch` to checkout your own branch.
1. Open **test.cpp** and the following line to main after "Git Test" line
1. `cout << "from a_branch" << endl;
1. Add, Commit and Push to b_branch:
    1. `git add test.cpp`
    1. `git commit -m "A added cout"`
    1. `git push origin a_branch`
    
### B (Step 2)
1. Make sure you are in the same directory in terminal as before.
1. Use the command `git checkout -b b_branch` to checkout your own branch.
1. Open **test.cpp** and the following line to main after "Git Test" line
1. `cout << "from b_branch" << endl;
1. Add, Commit and Push to b_branch:
    1. `git add test.cpp`
    1. `git commit -m "B added cout"`
    1. `git push origin b_branch`

Go to your git repo on Github and examine the different branches (master, a_branch, b_branch) and see what everything looks like. 

## Part 2 (Resolving Conflicts)
