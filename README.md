# Python-Quantum-Mechanics-Intro   
This repository houses Python code (predominantly, if not only, Jupyter Notebooks) that I am writing as I learn to use `QuTip` for simulating quantum mechanical systems. I will probably focus on photon polarization systems (eventually). To begin with, I will be using the following resources:
1. Andrew M.C. Dawes' preprint [Undergratuate Quantum Mechanics: a Numerical Approach using QuTip](https://arxiv.org/abs/1909.13651)
2. QuTiP's [tutorials](https://qutip.org/qutip-tutorials/) and [Read the docs](https://qutip.readthedocs.io/en/)
3. Online course notes found here: [Open Quantum Sensing and Measurement Notes](https://qsm.quantumtinkerer.tudelft.nl/)

---
## Installation, Requirements, etc. 
I recommend using `conda` to create and manage your environments. This ensures that Python packages with dependencies have the correct versions of those dependencies. I recommend using the `miniconda` version of `conda`, which has a smaller disk space requirement.   
To install `miniconda`, follow the instructions given here: [conda installation guide](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)

I also recommend using the JupyterLab IDE to work with Jupyter Notebooks because I find it to be user-friendly and its extensions easy to install. To avoid installing JupyterLab and its extensions in each conda environment, I install it in the base environment and allow it to access other enviroments using `nb_conda_kernels`. 
### If you want to use the same JupyterLab installation with multiple environments
Enter the following command into the terminal:
```
conda install -n base jupyterlab nodejs nb_conda_kernels pip
```
and type 'y' when prompted by the terminal. To enable extension support (not necessary if you don't want to use extensions), type the following command in the terminal:
```
pip install npm
```
Now that you've created the base enviroment for JupyterLab, create a new environment named "quantum" for QuTiP:
```
conda create -n quantum qutip numpy pandas matplotlib scipy pip ipykernel
```
You can update all packages in an enviroment with the command:
```
conda -n <ENV_NAME> update --all
```
### If you're only using one environment
Enter the following command into the terminal:
```
conda install -n base jupyterlab nodejs pip qutip numpy pandas matplotlib scipy
```
and type 'y' when prompted by the terminal. To enable extension support (not necessary if you don't want to use extensions), type the following command in the terminal:
```
pip install npm
```
----
