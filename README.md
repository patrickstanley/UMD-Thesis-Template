# UMD-Thesis-Template
An unofficial, updated template for a University of Maryland Ph.D. Thesis.
Based on the work of Dorothea F. Brosius at IREAP.
Origional documentation and files are located at <https://ireap.umd.edu/resources/thesis-templates>.
This template assumes you are using pdflatex and bibtex.
There is no guarntee that this template matches the Graduate School's guidelines as the rewrite them, but it aims to.

## Glossaries Package for List of Abbreviations
In this template I chose to use the glossaries package to keep track and automatically generate a list of abbreviations and symbols.
I have tried to include a few examples in the writing of various formats.
If this is not desired, one can go back to the supertabular method in IREAP's template.

## Lipsum
The Lipsum package is used to generate filler text, allowing one to see what the style looks like without having to insert actual text.
At the end of your work, once you have completed everything, you should remove the lipsum package from the preamble.
If it then gives you an error, you know you accidentally left some Lipsum somewhere in your document.
Be sure it is all gone before you submit it to anyone.

## Other Packages
The origional template form IREAP at UMD included a large number of packages, many of which I don't know why were included.
I removed some to resolve errors or when I know I removed their purpose, but many are left.
You may find that you need to re-add a package or eliminate one due to overlapping calls as you work on your project.

## Updates to the Template
Please feel free to adapt the template as you see fit. Remember that it must conform to the Graduate School's [Style Guide](https://www.gradschool.umd.edu/students/academic-progress/thesis-and-dissertation-filing).

If you make changes that you think would benifit others, feel free to suggest changes to this template.
The easiest thing to make your change happen is to submit a pull request on GitHub, but you can also file an issue with the changes.
If you do, please be sure to be as specific as possible with where the change should go (file name and line).
If the change is a matter of pesonal preference (serif vs sans serif fonts, etc), it will probably be rejected.
Also, if it changes the style of the document, please reference the section in the style guide so it can be checked to ensure the template still conforms to it.


## A Beginner's Guide to Using Git
As you may have noticed, this template is hosted on GitHub, an online repository for git.
Git is a nice way to keep track of revisions of a document, create multiple versions as you give it to people to edit, and share.
I highly suggest using git when working on your project.
I have been a bit verbose here to give you an idea of what is happening.
Don't be intimidated.
You are already using LaTeX, so go ahead and learn another skill.
I know you can do it.

### Installing Git
If you are running a Linux or Mac computer you already have git installed, just open your Terminal (//Applications/Utilities/ on a mac).
Windows users can download git from <https://git-scm.com/downloads>.

#### If you are starting fresh...
If you haven't downloaded the template yet and made any edits, congrats, this is pretty straight forwards.
Adapt these commands to fit your needs.

1.  Using the terminal, use the command 'cd' to change to your desired location, such as:

        cd ~/Documents/

2.  Next clone the template from GitHub to your computer:

        git clone <https://github.com/patrickstanley/UMD-Thesis-Template.git>

    Feel free to rename this folder to something that makes sense to you.

        mv UMD-Thesis-Template NewName

3.  Now you can cd into it:

        git clone <https://github.com/patrickstanley/UMD-Thesis-Template.git>

    Feel free to rename this folder to something that makes sense to you.

        mv UMD-Thesis-Template NewName

3.  Now you can cd into it:

        cd 'NewName'/

4.  Congrats, your project is now set up.
    It is generally a good idea not to make edits to your master brach (which you are currently in).
    Make a new branch by:

        git checkout -b writing

5.  Now you are free to start making what ever changes you want to the document.

6.  Once you have enough changes that you want to commit and back everything up you will want to add everything to the staging area then commit it.
    Do so with:

        git add .
        git commit -m "Add commit notes here"

7.  At this point, all changes will be committed to the brach "writing" if you want to put everything into the master brach, first switch to the master then merge.

        git checkout master
        git merge writing

And you are done.
You can make more braches as needed, such as when you give copies to your advisor or committee for review, or you can go back to writing as you want.

If changes occur to this template, you can update your copy by running:

    git pull origin master

#### If you started writing before git...
This is a little more complicated.

*   Start off as before following steps 1 though 3. Do not use the same folder for cloning that you have done work in so far. Start something new.
*   Before making your writing brach (step 4), you need to backtrack the master brach to the point where you downloaded the files.
Go to the template's [GitHub commits page](https://github.com/patrickstanley/UMD-Thesis-Template/commits/master) and find the commit which occured most recently before you downloaded the files.
    - If that commit is the most recent one then skip the next step.
    - If other commits have happened since, copy the hash for that commit.
        It will be something like 7b5b34595c82848d0b6dd44dd5d7259944383ebe.
*   Move the master brach back to that commit by running:

        git checkout 7b5b34595c82848d0b6dd44dd5d7259944383ebe

*   Continue with steps 4 through 6. If you have your edited files somewhere else, feel free to copy them over. Before step 7, update your master brach by running:

        git pull origin master

*   Go ahead and finish out the rest of the earlier instructions by merging your writing branch to the master.

    This will attempt to automatically resolve any differences between your edited files and the template. Depending on the changes you may have to go though and manually fix differences.

#### Making Your Own Online Repo
If you would like to keep a backup of your thesis (which is always a good idea), online such as on GitHub you can create your own repository.
UMD students can get access to private repositories by signing up with their university email at <https://education.github.com/pack>.
You can also use other services than GitHub.

Once you have the private repository set up on GitHub, the following changes 'origin' to it, and creates 'template' to link to origional:

    git remote set-url origin <https://github.com/yourusername/yourrepo>
    git remote add template https://github.com/patrickstanley/UMD-Thesis-Template.git

Push everything to the remote repository with:

    git push origin master
    git push origin brachname

If you need to update the template you can do so by running:

    git pull template master
