# Hands-On Optics Calculations - Setup Instructions
---

During the course we will use **Python3** in a **Jupyter notebook** with [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/) and, mostly, the [numpy](https://numpy.org/), [matplotlib](https://matplotlib.org/) and [cpymad](http://hibtc.github.io/cpymad/index.html) packages. We will explain in the following sections how to install all necessary software on **your laptop**.
A basic knowledge of Python is assumed. If you are not familiar with Python, you can find a few resources to fill the gap in the following sections.

Do not worry about the theory for the moment (it will be discussed in details during the school) but focus on the Python syntax and data types (tuples, lists,...).

After [a short introduction](#a-very-short-introduction-to-python), where we provided some useful links to get familiar with Python, we will focus on the [software setup](#software-setup). 
Finally, in [appendix](#appendix-python-packages) you will find links and cheatsheets for the most common Python packages that will be used during the course.

> **Important:** we kindly ask you to go throw this document **before coming** to CAS, such as to **prepare yourself** (and **your laptop**) for the course. 

---
# A very short introduction to Python
You can find several nice courses, videos and resources on the internet. Here you have a couple of suggestions you can find on YouTube:

<p align="center">
<a href=http://www.youtube.com/watch?v=kqtD5dpn9C8><img src="http://img.youtube.com/vi/kqtD5dpn9C8/0.jpg" alt="Python for Beginners - Learn Python in 1 Hour" width="40%"/></a> 
&nbsp;&nbsp;&nbsp;&nbsp;
<a href=http://www.youtube.com/watch?v=rfscVS0vtbw><img src="http://img.youtube.com/vi/rfscVS0vtbw/0.jpg" alt="Learn Python - Full Course for Beginners" width="40%"/></a>
</p>

### Test Python on a web page

If you are not familiar with Python and you have not it installed on your laptop, you can start playing with simple python snippets on the web. Without installing any special software you can connect, 
for example, to [jupyterLab](https://gke.mybinder.org/v2/gh/jupyterlab/jupyterlab-demo/try.jupyter.org?urlpath=lab),
and test the following commands:

Test.ipynb: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/cerncas/Sevrier2022/main?filepath=example/test.ipynb) 

```python
import numpy as np

# Matrix definition
Omega=np.array([[0, 1],[-1,0]])
M=np.array([[1, 0],[1,1]])

# Sum and multiplication of matrices
Omega - M.T @ Omega @ M
# M.T means the "traspose of M".

# Function definition
def Q(f=1):
    return np.array([[1, 0],[-1/f,1]])

# Eigenvalues and eigenvectors
np.linalg.eig(M)
```
You can compare and check your output with the ones [here](example/test.ipynb).

---
# Software Setup

In this section we will explain how to install Python and JupyterLab on your laptop.
JupyterLab is a user-friendly environment to work with Python. 
You can find an overview on JupyterLab [here](https://jupyterlab.readthedocs.io/en/stable/).

> If you already have your favorite Python distribution installed on your laptop, including JupyterLab, you might want to skip the [installation](#installation) and jump to [launch Jupyter Lab](#launch-jupyter-lab) and [test that everything works](#test-that-everything-works).

## Installation

We suggest to install the **Anaconda** distribution from https://www.anaconda.com/distribution/

<p align="center">
<a href=https://www.anaconda.com/distribution/><img src="_img_instructions/anaconda.png" alt="" width="70%"/></a>
</p>

> We suggest to install one of the latest distribution (**for example version Python 3.9**).

The installation process clearly depends on your operating system. We suggest you to follow the official documentation for [Windows](https://docs.anaconda.com/anaconda/install/windows/), [Linux](https://docs.anaconda.com/anaconda/install/linux/), or [Mac](https://docs.anaconda.com/anaconda/install/mac-os/) as appropriate.
After having installed **Anaconda**, and [verified your installation](https://docs.anaconda.com/anaconda/install/verify-install/) - as suggested in the [installation documentation](https://docs.anaconda.com/anaconda/install/) - we invite you to start [launching Jupyter Lab](#launch-jupyter-lab) and then [test that everything works](#test-that-everything-works):

## Launch Jupyter Lab

Once the installation of **Anaconda** is finalised or within your existing Python distribution, you should be able to start Jupyter Lab from a terminal:

1. Open a (Anaconda) terminal on your operating system:
    - **Windows:**
        From the Start menu, search for and open “Anaconda Prompt”:
    - **macOS:**
        Open Launchpad, then click the terminal icon.
    - **Linux:**
        Open a terminal window.

2. Launch Jupyter Lab from your terminal:

    ```bash
    jupyter lab
    ```

3. Follow the instructions given in the terminal. You should end-up on your default browser with a page similar to the following:

    <p align="center">
    <img src="_img_instructions/upload_5b0618b75e4f4df0facf2a609b9354b5.png" alt="" width="70%"/>
    </p>

    On the left hand side of the widows you should see all files under the folder in your operating system where you executed the `jupyter lab` command.
    This will be your **working directory**. 

4. Start playing with Python!  Please, make sure to go throw all the [examples/test.ipynb](test.ipynb) to familiarize with the typical Python concepts that will be used during the course, but also to verify your installation. If you happen to experience any problem, please check to have installed the whole anaconda distribution. Alternatively, you can try to go back to your terminal, and install each single package independently, e.g.:

```python
pip install numpy matplotlib seaborn scipy ipywidgets jupyter jupyterlab cpymad
```

5. If you are not familiar with Python, you can start playing with simple python snippets. For example, have a look to the following [examples/000_example.ipynb](examples/000_example.ipynb) (courtesy of *Simon Albright*).


6. **Just before the start of the course**, we will ask you to download the **latest version** of [Exercises.ipynb](./Exercises.ipynb) (even better, the whole repository) in your **working directory**.

7. **Optional:** instead of running Jupyter lab within a browser, you can try to install and the [jupyterlab-desktop](https://github.com/jupyterlab/jupyterlab-desktop) application.

---
## Appendix: Python Packages

You can leverage python's capability by exploring a galaxy of packages. Below you can find the most useful for our course (focus mostly on `numpy` and `matplotlib`) and some very popular ones. 

### The *numpy* package
To get familiar with the *numpy* package have a look at the following [summary poster](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Numpy_Python_Cheat_Sheet.pdf).
You can google many other resources, but the one presented of the poster covers the set of instructions you should familiar with.

<p align="center">
<a href=https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Numpy_Python_Cheat_Sheet.pdf><img src="_img_instructions/upload_6ffb4d07b1ebb895528f2a34aae41ec6.png" alt="" width="90%"/></a>
</p>

### The *matplotlib* package
To get familiar with the *matplotlib* package have a look at the following [summary poster](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Matplotlib_Cheat_Sheet.pdf).

<p align="center">
<a href=https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Matplotlib_Cheat_Sheet.pdf><img src="_img_instructions/upload_4b54812812e21978b600b860ba1ddf5b.png" alt="" width="90%"/></a>
</p>

### The *linalg* module
To get familiar with the Linear Algebra (linalg) module have a look at the following [summary poster](
https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_SciPy_Cheat_Sheet_Linear_Algebra.pdf).

<p align="center">
<a href=https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_SciPy_Cheat_Sheet_Linear_Algebra.pdf><img src="_img_instructions/upload_15561fc12184bb0ae3f9cf7b1850317a.png" alt="" width="90%"/></a>
</p>

### The *pandas* package (optional)
To get familiar with the *pandas* package have a look at the following [summary poster](
https://s3.amazonaws.com/assets.datacamp.com/blog_assets/PandasPythonForDataScience.pdf).

<p align="center">
<a href=https://s3.amazonaws.com/assets.datacamp.com/blog_assets/PandasPythonForDataScience.pdf><img src="_img_instructions/upload_90383c01e29d29fb6a5516c613e22c4d.png" alt="" width="90%"/></a>
</p>

### The *seaborn* package (optional)
To get familiar with the *seaborn* package have a look at the following [summary poster](
https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf).

<p align="center">
<a href=https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf><img src="_img_instructions/upload_9a3c3f5ca48bbd567a0662df20dbd16f.png" alt="" width="90%"/></a>
</p>

### The *sympy* package (optional)
To get familiar with the *sympy* package have a look at the following [summary poster](http://daabzlatex.s3.amazonaws.com/9065616cce623384fe5394eddfea4c52.pdf).

<p align="center">
<a href=http://daabzlatex.s3.amazonaws.com/9065616cce623384fe5394eddfea4c52.pdf><img src="_img_instructions/upload_fc7a06ea6135d2bf17311bd7a91f1a9f.png" alt="" width="90%"/></a>
</p>
