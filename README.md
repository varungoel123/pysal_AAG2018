# Open-Source Spatial Statistics workshop at AAG 2018

* Time: Thursday, April 12, 10:00 a.m. – 12:00 p.m.
* Location: Beauregard, Marriott, 5th Floor

### Instructors

- [Dani Arribas-Bel](http://darribas.org/) -  University of Liverpool
- [Levi John Wolf](http://www.bristol.ac.uk/geography/people/levi-j-wolf/overview.html) - University of Bristol
- [Marynia Kolak](https://marynia.me/) - University of Chicago
- [Wei Kang](http://spatial.ucr.edu/peopleKang.html) - Arizona State University


This repository contains the materials and instructions for the Open-Source Spatial Statistics workshop at [AAG 2018](https://annualmeeting.aag.org/AAGAnnualMeeting/Register_To_Attend/Event_Display.aspx?EventKey=AM2018).


## Schedule

* 10:00-12:00

## Obtaining Workshop Materials

If you are familiar with GitHub, you should clone or fork this GitHub repository to a specific directory. Cloning can be done by:

```bash
git clone https://github.com/weikang9009/pysal_AAG2018.git
```

If you are not using git, you can grab the workshop materials as a zip file by pointing your browser to (https://github.com/weikang9009/pysal_AAG2018) and clicking on the green *Clone or download* button in the upper right.

![download](figs/download.png)

Extract the downloaded zip file to a working directory.

## New to Command Line

Are you not sure how to access a working directory or command line? For this workshop, we recommend starting with two minimum points: (1) find your Terminal, and (2) Learn to Changing Your Working Directory. For those who have MacOS operating systems, you can find Terminal in your Utilities. For those using other operating systems, search for multiple options online, depending on your taste. A terminal launched looks like this:

![terminal](figs/terminal.png)

Once in your terminal, type ```ls```. This will list all of the contents in your current directory. You will likely see your Data, Documents, Desktop, Download, and many other folders and files. 

To change working directories, you will type ```cd``` plus the name of the directory you'd like to change to. If you are diving into a subdirectory, or child of the directory you were just in, then that name on its own is sufficient. For example, to access the "Downloads" directory, you type ```cd Downloads```.

![downloads](figs/downloads.png)

If you just downloaded the zip file into Downloads, first make sure you have unzipped the folder. Once unzipped, assuming it is still in the Downloads directory, type ```cd pysal_AAG2018``` to access. Then ```ls``` to list the contents. You have successfully navigated to your working directory to the workshop, and are ready for installations!

![downloads](figs/workingdir.png)


## Installation

### PySAL

We will be using a number of Python packages for geospatial analysis.

An easy way to install all of these packages is to use a Python distribution such as [Anaconda](https://www.anaconda.com/download/#macos). In this workshop we will be using **Python 3.6** so please download that version of Anaconda.

![anaconda](figs/anaconda.png)

Once you have downloaded Anaconda, start a terminal and navigate to the directory of the downloaded/ cloned materials. If you just learned to navigate to your working directory in the tutorial above, you are ready for the next step. For those who need a refresh: if the materials now live in the directory ```/Users/hu/wei/Dropbox (ASU)/python_repos/pysal_AAG2018```, you need to navigate to that directory from the terminal (using command ```cd```):

![directory](figs/directory.png)

Once we have done that, run:

```bash
conda-env create -f gds_stack.yml
```

This will build a conda environment that sandboxes the installation of the required packages for this workshop so we don't break anything in your computer's system Python (if it has one).

This may take 10-15 minutes to complete depending on the speed of your network connection.

Once this completes, you can activate the workshop environment with:

* on Mac, Linux
```bash
source activate gds
```
* on Windows:
```bash
activate gds
```

Next, you will want to test your installation with:
```bash
 jupyter-nbconvert --execute --ExecutePreprocessor.timeout=120 check_workshop.ipynb
```

You should see something like:
```bash
[NbConvertApp] Converting notebook check_py_stack.ipynb to html
[NbConvertApp] Executing notebook with kernel: python3
[NbConvertApp] Writing 393375 bytes to check_py_stack.html
```

Open check_workshop.html in a browser, and scroll all the way down, you should see something like:

![htmlout](figs/htmlout.png)

If you do see the above, you are ready for the workshop.

### GeoDa

We will also have a short and sweet overview of GeoDa, an opensource spatial statistics software. 

You can download the most recent release of GeoDa (version 1.12) by visiting [GeoDaCenter.Github.io](https://geodacenter.github.io/download.html). 

![geoda](figs/geoda.png)

Once installed, open GeoDa on your operating system. 

If you have a Macintosh and run into an error that reads "Can't be opened because it is from an unidentified developer," you will need to implement one additional step. Because you downloaded directly from the GeoDa developler website, the operating system is not certain if the software is safe. To override this feature, because you know the software is safe, you must go to Systems Preferences to click on the "Security & Privacy" option. Here, you click on "Open Anyway" to open GeoDa successfully. 

![systempref](figs/systempref.png)

You have successfully installed and opened GeoDa when you can view the following:

![geodasuccess.png](figs/geodasuccess.png)