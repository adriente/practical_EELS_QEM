# practical_EELS_QEM

Repository to share the content of the EELS data analysis practical of QEM2022.

Authors : Laura Bocher, Hugo Lourenço-Martins, Cécile Marcelot, Sophie Meuret, Adrien Teurtrie, Bénédicte Warot-Fonrose

# Installation

## Clone the repository
You need to have git installed. On this page click on the green button "clone" and copy the suggested text (option https). Then run the command :
`git clone the/line/you/copied`

## Install the conda environnement

Install anaconda on your computer: https://www.anaconda.com/products/individual

Run the "Anaconda prompt". A terminal should pop-up. 

Then run the following commands (replacing "myenv" by whatever you want): 

**For now the practical only works for hyperspy = 1.6.5, I'll try to fix it later**

```
conda create --name myenv

conda activate myenv

conda install -c conda-forge hyperspy = 1.6.5 

conda install jupyter

conda install jupyterlab

conda install -c conda-forge nodejs

conda install ipykernel

conda install -c conda-forge jupyter_contrib_nbextensions

python -m ipykernel install --user --name myenv
```

# Running the notebooks

Open the "Anaconda prompt" and go to the folder where the git repository is : `cd /the/path/you/chose`. Then, run the following command : `jupyter lab`
