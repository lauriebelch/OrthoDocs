# Beginner tutorial for using OrthoFinder

This tutorial will cover;
1) [Downloading OrthoFinder](#downloading-orthofinder)
2) Downloading input files for OrthoFinder
3) Running OrthoFinder
4) Exploring the results of OrthoFinder

All these steps will be done on the command line so that you can just copy and
paste the commands yourself. If you are not familiar with the command line there
are many online tutorials and reference pages, [here](https://www.techspot.com/guides/835-linux-command-line-basics/) is a nice short one that covers
the basics.

## Downloading OrthoFinder

There are two main ways of getting OrthoFinder. You can either use conda, or you can
install it directly from github. Installing directly from github will always give you the latest
version, but you might have to manually install other software that OrthoFinder is
dependent on, and it can be trickier to troubleshoot if you aren’t familiar with the
command line. Conda automates the installation process and handles all dependencies,
making it very beginner-friendly.
To install via conda, we first need to install miniconda. Follow the instructions [here](https://docs.anaconda.com/miniconda/)

We then need to run these commands

```
conda config --add channels defaults conda config --add channels bioconda conda config
--add channels conda-forge
conda create -n orthofinder
conda activate orthofinder
conda install orthofinder
```

If you are on one of the newer Macs with the new chips (M1/M2/M3), you might need to
follow a few extra steps to use conda. Check out the guide [here](https://towardsdatascience.com/how-to-manage-conda-environments-on-an-applesilicon-
m 1-mac-1e29cb3bad12).

To install directly from github, we need to run these commands
```
python3 -m venv of3_env
. of3_env/bin/activate
pip install git+https://github.com/OrthoFinder/OrthoFinder.git
```

You can test that OrthoFinder has been installed by printing its help file
```orthofinder -h```, which will print all of the command line options.

You can test that OrthoFinder is working correctly by running it on the example
dataset, which you can download from our [github](https://github.com/OrthoFinder/OrthoFinder/)

```orthofinder -f ExampleData/ ```

OrthoFinder will print lots of information to the command line as it runs. If you get an
error message, the best way to troubleshoot is to just google the error message. You
can also ask a question on our [github](https://github.com/OrthoFinder/OrthoFinder/issues) 

When OrthoFinder has finished running, it will generate a folder containing the output,
with the folder named according to today’s date.
‘ExampleData/OrthoFinder/Results_Jul12’ The folder looks like this:

*Beginner_img1*

We’ll discuss how to interpret and analyse these files and folders later on, in the
‘Exploring the results’ section of the tutorial.

## Downloading input files for OrthoFinder


