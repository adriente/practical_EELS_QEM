# practical_EELS_QEM

Repository to share the content of the EELS data analysis practical of QEM2025. This practical is divided in two main parts : 

- The first part describes how to use Digital Micrograph to analyse core-loss STEM-EELS data. If you want to use Digital Micrograph, please contact Gatan.
- The second part describes how to use Hyperspy to analyse core-loss STEM-EELS data as well as low-loss STEM-EELS data. It is an open-source python based software. We describe the installation steps to run the ipython notebooks just below.

Authors : Hugo Lourenço-Martins, Adrien Teurtrie, Maya Marinova

# Installation

In the first part of the installation process, you will need to install Git to clone this repository (Optional). If you don't want to install git you can download the archive (.zip) if this repository. 

In the second part, you will go through the installation of the python environment required for the hyperspy part.

## Install Git

The version control software Git can be installed from here: https://git-scm.com/downloads . The default options should work nicely.

### Clone the repository

You need to have git installed. On this page click on the green button "clone" and copy the suggested text (option https). Then run the command :
`git clone the/line/you/copied`

## Install Hyperspy with anaconda

This section is intended to help you to install hyperspy on your own computer in your own lab. **You can skip this part for the practical.**

Anaconda is python package manager dedicated to science. Using Anaconda it is possible to create virtual environments. You can then manage different virtual environments to isolate different distributions of python packages. This way you can keep stable python distributions safe from unstable ones.

We describe here the few steps required to create an environment with Hyperspy.

### Install Anaconda

Depending on your operating system install anaconda : https://www.anaconda.com/products/individual

Then, launch the Anaconda Prompt, a console should appear.

### Create a virtual environment

Run the command : ```conda create --name myenv python=3.12``` (change "myenv" by any name you like.)

Your virtual environment is created but you're still in the default one called "base". You need to activate it by typing: ```conda activate myenv```

### Installing packages (in general)

When installing a package there are three solutions: 
1. Either it is part of the already available libraries 
2. Either you can access it from anaconda forge
3. If (1) or (2) didn't work you can try with pip

(1). Run the command : ```conda install package-name``` with for example: ```conda install scikit-learn```

(2). The available python packages are listed on : https://anaconda.org/ . After searching for the library you want, you can click on its name in bold. There will be a list of commands to type and execute to install the selected package. For Hyperspy it is: ```conda install -c conda-forge hyperspy``` or ```conda install conda-forge::hyperspy```

(3). The available python packages are listed on : https://pypi.org/ . Once you have the name of the package you want to install, you can type: ```pip install packagename```. The interaction between pip and conda is tricky, it is better to stick with conda only. 

## Install the conda environment of this practical

Install anaconda on your computer: https://www.anaconda.com/products/individual

Run the "Anaconda prompt". A terminal should pop-up. 

Then run the following commands (replacing "qem" by whatever you want): 

```
conda create --name qem python=3.12

conda activate qem

conda install -c conda-forge hyperspy

conda install -c conda-forge exspy

conda install jupyterlab

conda install -c conda-forge jupyter_contrib_nbextensions

python -m ipykernel install --user --name qem
```

# Running the notebooks

Open the "Anaconda prompt" and go to the folder where the git repository is : `cd /the/path/you/chose` (either from the clone command or from the unzipped archive). Then, run the following command : `jupyter lab`
