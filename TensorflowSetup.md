# Tensorflow Setup for all your Jupyter Notebook Needs

(Get Python 3.8 if you don't have it already)\
jupyter jupyter why must i do this

**Jupyter Notebooks:**
* Server-client application used to run code in your browser
* Super convenient for data science and ML
* Easy to collaborate

<hr/>

## Anaconda Installation
**Why Anaconda?**
* Supports Jupyter Notebook
* Contains many libraries
* Auto installs the SciPy stack: numpy, pandas, matplotlib

Download page: https://www.anaconda.com/products/individual

Click on `Download` \
Select the appropriate Anaconda Installer\
hf tbh

<hr/>

## Your Conda Virtual Environment
Why use one?
* jupyter notebook lets you select your kernel (well essentially your conda venv. we'll get to this in `Kernel Config`)
* we will be managing our packages by installing them to our conda virtual environment so that we can access them through jupyter notebook

Setup

1. Go to your terminal
2. Create your conda venv
```
$ conda create -name <venv_name> python=3
```
Agree to the installation

View all your conda environments:
```
$ conda info --envs
```

3. Activate your conda venv
```
$ conda activate <venv_name>
```
While your conda venv is activated:
* you will be able to use packages installed to your conda venv
* all your `install` commands will install packages to the conda venv

Some more conda commands:\
Deactivate conda venv
```
conda deactivate
```
Remove an environment
```
conda env remove -n <venv_name>
```
<hr/>

Note: your conda venv should be activated for the following steps

<hr/>

## Kernel Config
I have never heard of a kernel:
* an ipython kernel executes python code in jupyter notebook cells (as if it were your terminal)

What's ipykernel then?
* it's preinstalled with jupyter notebook but needs to be manually added for virtual environments


Install ipykernel and add your conda env to jupyter
```
$ pip install ipykernel
$ python -m ipykernel install --name <venv_name>
```

You will now be able to run jupyter notebook cells with the packages installed to your conda venv\
Read more about this here: https://janakiev.com/blog/jupyter-virtual-envs/ 
## Tensorflow Installation
```
$ conda install tensorflow
$ pip install --upgrade tensorflow
```

## sklearn Installation
```
$ pip install scikit-learn
```

# Jupyter Notebook finally
```
$ conda activate <venv_name>
$ jupyter notebook
```
This should launch jupyter notebook in your browser at `localhost:8888/tree`

Navigate to the folder where you want to get create your notebook

1. Click on `New`\
2. Select `<venv_name>` option. This will link our kernel to the conda environment, so that when the kernel executes your notebook cells, it will be using the selected conda venv

Start coding


