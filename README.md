# DeepTrading

DeepTrading is a collection of Jupyter notebooks. The objective is to organize in a systematic but flexible way all the necessary steps to calculate and conceive trading systems based on the Tensorflow software.

For more info see: [TodoTrader DeepTrading Tensorflow serie](https://todotrader.com/deeptrading-with-tensorflow/)

## Installation

If you are Black Belt (BB) then &quot;Quick Way&quot; is your way of installation, else use &quot;Detailed Way&quot;.

What!, wait...Am I a Black Belt?

Well, if you can use these Jupyter notebooks with &quot;Quick Way&quot; instructions then sure, you are a BB.

## Quick Way (Black Belt)

It is highly recommended to run DeepTrading in designated Conda virtual environment. To install Conda you can be guided by any of the many tutorials that are disseminated throughout the Web.

git clone https://github.com/parrondo/deeptrading.git

cd deeptrading

conda env create --file environment.yml

conda activate deeptrading

It&#39;s likely you want to have a .env file. It is a configuration text file that is used to define some variables you want to pass into your application&#39;s environment.

Example of .env file:

PROJ\_DIR=.

DATA\_DIR=../data/

RAW\_DIR=../data/raw/

INTERIM\_DIR=../data/interim/

PROCESSED\_DIR=../data/processed/

FIGURES\_DIR=../reports/figures/

MODEL\_DIR=../models/

EXTERNAL\_DIR=../data/external/

PRODUCTION\_DIR=/home/PRODUCTION/

## Detailed Way (Brown Belt)

### Set Up Your Anaconda Python Environment

Here, you will learn how to install a conda environment designed specifically for deeptrading posts called DeepTrading with Tensorflow from a .yaml file.

### Objectives

At the end of these instructions, you should be able to:

- Install a new environment in Anaconda
- View a list of the available environments in Anaconda

### What You Need

You should have Bash, Git (Git Bash for Windows users) and the Anaconda distribution of Python 3.x setup on your computer and an deeptrading working directory. Installation of Git Bash (Windows users) and Anaconda is out of the scope of these instructions. Here you can find the hyperlink and below, how to test your set-up.
So, Be sure you have:

- Completed the setup for Bash and Git, or [Git Bash for Windows users](https://gitforwindows.org/)
- Completed the setup for [Anaconda](https://www.anaconda.com/)
- Created a deeptrading directory on your computer

Information below is adapted from materials developed by the Conda documentation for [installing conda](https://conda.io/docs/user-guide/install/index.html) and [managing packages](https://conda.io/docs/user-guide/tasks/manage-pkgs.html).

### Test your set-up of Bash, Git and Anaconda

#### Windows

1. Search for and open the Git Bash program. In this Terminal window, type bash and hit enter. If you do not get a message back, then Bash is available for use.
2. Next, type git and hit enter. If you see a list of commands that you can execute, then Git has been installed correctly.
3. Next, type conda and hit enter. Again, if you see a list of commands that you can execute, then Anaconda Python has been installed correctly.
4. Close the Terminal by typing exit.

#### Mac

1. Search for and open the Terminal program (found in /Applications/Utilities). In this Terminal window, type bash and hit enter. If you do not get a message back, then Bash is available for use.
2. Next, type git and hit enter. If you see a list of commands that you can execute, then Git has been installed correctly.
3. Next, type conda and hit enter. Again, if you see a list of commands that you can execute, then Anaconda Python has been installed correctly.
4. Close the Terminal by typing exit.

#### Linux

1. Search for and open the Terminal program. In this Terminal window, type bash and hit enter. If you do not get a message back, then Bash is available for use.
2. Next, type git and hit enter. If you see a list of commands that you can execute, then Git has been installed correctly.
3. Next, type conda and hit enter. Again, if you see a list of commands that you can execute, then Anaconda Python has been installed correctly.
4. Close the Terminal by typing exit.

### Set up a Conda Python Environment

#### Install the deeptrading Conda Environment

Anaconda allows you to have different environments installed on your computer to access different versions of Python and different libraries. Sometimes libraries conflict which causes errors and packages not to work.

To avoid conflicts, we created an environment specifically for deeptrading posts that contains all of the python libraries that you will need.

**Tip:** For more information about conda environments check out the [conda documentation](https://conda.io/docs/user-guide/tasks/index.html).

To install the deeptrading environment, you will need to follow these steps:

1. Fork and clone a Github repository from [https://github.com/parrondo/deeptrading](https://github.com/parrondo/deeptrading) to your deeptrading directory. This repository contains a file called yaml that is needed for the installation. (For instructions on forking/cloning repositories, see the section below on **Fork and Clone Github Repository** ).
2. Be sure you have the yaml file into your deeptrading parent directory using your file manager.
3. Open the Terminal on your computer (e.g. Git Bash for Windows or Terminal on a Mac/Linux).
4. In the Terminal, navigate to the deeptrading directory (e.g. cd ~, then cd deeptrading).
5. Then, type in the Terminal: conda env create -f environment.yml

Note that it takes a bit of time to run this setup, as it needs to download and install each library, and that you need to have internet access for this to run!

**Tip:** The instructions above will only work if you run them in the directory where you placed the environment.yml file.

Once the environment is installed, **always make sure that the deeptrading environment is activated** before doing work for this class.

See the instructions further down on this page to **Activate a Conda Environment**. Once the environment is activated, the name of the activated environment will appear in parentheses on the left side of your terminal.

### Fork and Clone Github Repository

This section provides the basic steps for forking a Github repository (i.e. copying an existing repository to your Github account) and for cloning a forked repository (i.e. downloading your forked repository locally to your computer).

Also you could see my post:

https://todotrader.com/robust-git-workflow-for-research-projects/

#### Fork a Repository on Github.com

You can fork an existing Github repository from the main Github.com page of the repository that you want to copy (example: [https://github.com/parrondo/deeptrading](https://github.com/parrondo/deeptrading)).

On the main Github.com page of the repository, you will see a button on the top right that says Fork.

Click on the Fork button and select your Github.com account as the home of the forked repository.

####

![](data:image/*;base64,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)

#### Clone a Repository to Local Computer

To download your forked copy of the deeptrading repository to your computer, open the Terminal and change directories to your deeptrading directory (e.g. cd ~, then cd deeptrading).

Then, run the command git clone followed by the URL to your fork on Github (e.g. https://github.com/your-username/deeptrading). Be sure to change your-username to your Github account username.

cd ~

cd deeptrading

git clone https://github.com/your-username/deeptrading

### About the Conda Environment

#### The .yaml File

When you work with Anaconda, you can create custom lists that tell Anaconda where to install libraries from, and in what order. You can even specify a particular version. You write this list using [yaml](http://yaml.org/)(Yet Another Markup Language). This is an alternative to using pip to install Python packages.

In previous steps, you used a custom .yaml list to install all of the Python libraries that you will need to complete the lessons in this course. This .yaml list is customized to install libraries from the repositories and in an order that minimizes conflicts.


The .yaml file looks like:

| # run: conda env create --file environment.yml |
| --- |
| name: deeptrading |
| |
| dependencies: |
| - python=3.5 |
| - pip: |
| - tensorflow==1.5.0 |
| - numpy==1.15.0 |
| - scipy==1.1.0 |
| - scikit-learn==0.19.2 |
| - jupyter==1.0.0 |
| - matplotlib==2.2.2 |
| - requests==2.18.4 |
| - Pillow==5.1.0 |
| - GitPython==2.1.11 |
| - backtrader==1.9.65.122 |
| - pandas==0.23.4 |
| - python-dotenv==0.9.1 |
| - seaborn==0.9.0 |

Notice at the top of the file there is the environment name. This file has a few key parts:

1. NAME: the name of the environment that you will call when you wish to activate the environment. The name deeptrading is defined in the environment.yml file.
2. Channels (optional): this lists where packages will be installed from. There are many options including conda, conda-forge and pip. You will be predominately using conda-forge.
3. Dependencies: Dependencies are all of the things that you need installed in order for the environment to be complete. In the example, python version 3.5 is specified . The order in which the libraries should be installed is also specified.

### Manage Your Conda Environment

You can have different Python environments on your computer. Anaconda allows you to easily jump between environments using a set of commands that you run in your terminal.

#### View a List of All Installed Conda Environments

You can see a list of all installed conda environments by typing:

conda info --envs

If you want to Jupyter Notebook to use a particular environment that you have setup on your computer, you need to activate it.

For example, if a Python package such as tensorflow is only installed in the deeptrading environment, and not the default anaconda environment, you will not be able to import it to Jupyter Notebook, unless you have the deeptrading environment activated.

#### Activate a Conda Environment

**To activate an environment** , use the Terminal to navigate to your deeptrading directory (e.g. cd to the directory). Then, type the following command to activate the environment (e.g. deeptrading):

conda activate deeptrading

[For older installations of Anaconda (versions prior to 4.6)](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) on Mac, Linux, and Git Bash for Windows, type:

source activate deeptrading

**Windows Users:** We assume that Windows users are using Git Bash as their primary terminal. If you need to activate a conda environment using the Command Prompt, you will need to use the following command: activate deeptrading

Once the environment is activated, the name of the activated environment will appear in parentheses on the left side of your terminal.

**Tip:** Note that after you restart the Terminal, the deeptrading environment is no longer active. You will need to activate the deeptrading environment each time you start the Terminal by running the appropriate command provided above for your operating system.

#### Deactivate a Conda Environment

If needed, you can deactivate a conda environment. Deactivating the environment switches you back to the default environment in your computer.

#### Mac and Linux Instructions:

Source deactivate deeptrading

#### Windows Instructions

deactivate deeptrading

#### Delete a Conda Environment

If you ever want to delete an environment, you must first deactivate that environment and then type:

conda env remove --name myenv

and replace myenv with the name of the environment that you want to remove.

**Remember to never delete your working environment.**
