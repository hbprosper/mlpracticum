# mlpracticum
An introduction to the basics of machine learning including the mathematical underpinnings. This practicum comprises several __jupyter__ notebooks (see below) that work with Python 3. 

### Dependencies and Installation
The jupyter notebooks in this package depend on a few well-known Python packages:

| __modules__   | __description__     |
| :---          | :---        |
| pandas        | data table manipulation, often with data loaded from csv files |
| numpy         | array manipulation and numerical analysis      |
| matplotlib    | a widely used plotting module for producing high quality plots |
| scikit-learn  | easy to use machine learning toolkit |
| pytorch       | a powerful, flexible, machine learning toolkit |

Also recommended are

| __modules__   | __description__     |
| :---          | :--- |
| scipy         | scientific computing    |
| sympy         | an excellent symbolic algebra module |

The simplest way to install these packages is first to install miniconda (a slim version of Anaconda) on your laptop by following the instructions at:

https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html

I recommend installing miniconda3, which comes pre-packaged with Python 3.

Software release systems such as Anaconda (__conda__ for short) make it possible to have several separate self-consistent named *environments* on a single machine, say your laptop. For example, you may need to use Python 2.7.14 sometimes and Python 3.6.7 at other times. If you install software without using *environments* there is the very real danger that the software on your laptop will become inconsistent. Anaconda (and its lightweight companion miniconda) provide a way, for example, to create a software *environment* consistent with Python 2.7.14 and another that is consistent with Python 3.6.7. Note, however, that Python's standard installer *pip* and miniconda are *blind* to each other. Consequently, using *pip* within a conda environment can disrupt that environment. So, be careful!

After installing miniconda3, It is a good idea to update conda using the command
```bash
conda update conda
```
Assuming conda is properly installed and initialized on your laptop, you can create an environment, here we call it *python3*, containing the __root__ package from CERN, plus a large subset of the packages in the conda system, using the command>
```bash
conda create -c conda-forge --name python3 root
```
Before pressing __y__ to continue with the installation, scan through the list of packages and identify which of the above are in the list. That way, you will know which ones are missing and need to be installed using the conda install command. For example, as of this writing __pytorch__ is not available by default. In order to install a missing packages, first be sure to choose the conda environment into which the package is to be installed. First activate the desired environment, by doing, for example,
```bash
conda activate python3
```
Later, in order to update root together with a consistent set of packages do
```bash
conda update root
```
taking care to do so in the desired conda environment, here __python3__.

### Other Packages

To install pytorch do
```bash
conda install pytorch torchvision -c pytorch
```
You may also wish to install the rather impressive 3D animation package __vpython__,
```bash
conda install vpython -c vpython
```

If all goes well, you will have installed a rather complete set of amazing high quality *absolutely free* software packages on your system that are consistent with Python 3.

For some quick help on conda see 

https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/


If you still prefer to do everything by hand, follow the instructions at

https://www.scipy.org/install.html

and 

https://jupyter.org/install


### 1. Download
It is a good idea to organize your computer-based projects in a systematic way. For example, in your home directory (usually the area identified by the environment variable $HOME), you may wish to create a directory (i.e., folder) called __Projects__ and create within it a sub-directory called __Tutorials__ as follows
```bash
cd
mkdir -p Projects/Tutorials
```
In a terminal window dedicated to running the jupyter notebook, do
```bash
cd
cd Projects
jupyter notebook
```
This will run the notebook in your browser and block the terminal window, which you can iconize.

In another terminal window, go to your Tutorials sub-directory
```bash
cd
cd Projects/Tutorials
```
and execute the command
```bash
git clone https://github.com/hbprosper/mlpracticum
```
This should download the package *mlpracticum* to your current directory.

### 2. Notebooks

The notebooks provide detailed background information and explanations and are well-commented.

| __notebooks__                   | __description__     |
| :---          | :--- |
00_generate_data.ipynb     | Create files data\_01.db and data\_02.db |
01_classification_sklearn.ipynb           | use __scikit-learn__ to classify data i data\_01.db|
01_classification.ipynb | use __PyTorch__ to classify data i data\_01.db | 
02_regression.ipynb | use __PyTorch__ to fit data in data\_02.db |


