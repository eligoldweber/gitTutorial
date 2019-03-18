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
This part should be completed simultaneously. 

### A (Step 2)
1. Make sure you are in the same directory in terminal as before.
1. Use the command `git checkout -b a_branch` to checkout your own branch.
1. Open **test.cpp** and the following line to main after "Git Test" line
1. `cout << "from a_branch" << endl;`
1. Add, Commit and Push to b_branch:
    1. `git add test.cpp`
    1. `git commit -m "A added cout"`
    1. `git push origin a_branch`
    
### B (Step 2)
1. Make sure you are in the same directory in terminal as before.
1. Use the command `git checkout -b b_branch` to checkout your own branch.
1. Open **test.cpp** and the following line to main after "Git Test" line
1. `cout << "from b_branch" << endl;`
1. Add, Commit and Push to b_branch:
    1. `git add test.cpp`
    1. `git commit -m "B added cout"`
    1. `git push origin b_branch`

Go to your git repo on Github and examine the different branches (master, a_branch, b_branch) and see what everything looks like. 

## Part 2 (Resolving Conflicts)

This part needs to be completed sequentially. 

### A (Step 3)
1. Click Pull Request -> New Pull Request -> `a_branch` -> Create Pull Request 
1. Then **Merge** your pull request to master (there should not be any conflicts)
1. Navigate back to master branch and observe your changes in test.cpp
1. **WAIT FOR B TO FINISH THEIR PART**
1. update your code by calling `git pull origin master`

### B (Step 3)
1. **WAIT FOR A TO FINISH #3 in Step 3**
1. Go to terminal and type: `git branch` to make sure that you are on `b_branch`
    1. If not, type `git checkout b_branch`
1. Type `git pull origin master`
    1. You should see: 
    ```Auto-merging test.cpp CONFLICT (content): 
    Merge conflict in test.cpp Automatic merge failed; fix conflicts and then commit the result.```
1. Open test.cpp, you should see something like:
```
int main(int argc, const char * argv[]) {

    cout << "Git Test\n";
<<<<<<< HEAD
    cout << "from b branch" << endl;
=======
    cout << "from a branch" << endl;
>>>>>>> 90e7d8c67a14f6894e3199c8e71d633b3c68e4e2
    return 0;
}
```
1. Go ahead and modify the file to return it to correct c++ syntax by deleting the added lines
    1. make sure that `B added cout` is above `A added cout`
1. Save the file
1. Add, Commit and Push to b_branch:
    1. `git add test.cpp`
    1. `git commit -m "fixed conflict"`
    1. `git push origin b_branch`

1. Go back to github.com and refresh the repo page.
1. You should see a yellow header with your branch name on it. Click **Compare & pull request**
1. Click create merge request, and merge the branch to master by clicking merge-> confirm. 
1. Go back to master branch and observe your changes

