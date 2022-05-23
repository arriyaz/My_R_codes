## 1. Install necessary dependencies:

```bash
sudo apt-get install libzmq3-dev libcurl4-openssl-dev libssl-dev jupyter-core jupyter-client
````

When you have run this command once. If you create a new conda environment and want to install **IRkernel** for a new R version inside that environment you don’t have to run this command again.


## 2. Install R within a `conda` environment
Create a new R environment and install `r-base` with other necessary & important packages all together

```bash
conda create -y -n r-env r-base r-repr r-irdisplay r-irkernel r-essentials
```

**If your conda contains `mamba` package, install your packages with this command. It is quite faster than native `conda` command.**

```bash
mamba create -y -n r-env r-base r-essentials r-repr r-irdisplay r-irkernel
```

After installing R you may want to run your R codes in jupyter notebooks. In that case, you have to install the R kernel. This kernel will make your R available for jupyter notebook or lab.

Let’s say you install **R version 4.1.2** in the **r-env** environment. So, to make this version of R accessible for jupyter notebook/lab you have to install `IRkernel` in this environment.

You should add `r-essentials` along with `r-base` as it will not only install all the important r packages but also help during **IRkernel** installation.


>> To install a specific R version, let’s say R 4.1.2  
>> `conda create -n r-env3.6 r-essentials r-base==4.1.2`

To know more about installing specific versions of a tool you can see [conda cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf).

## 3. Make kernel available to Jupyter:
Here is the trick. If we install kernelspecs with default names, every time it will replace the previous kernel from a different conda environment.

The aim of creating a conda environment is to manage different versions of tools (in this case different R versions) simultaneously.

So, you have to install different kernels with different names for every version of R. In that case we will be able to run r codes in a different version of R from the jupyter lab/notebook.

**Even we don’t have to activate that particular conda environment to run R inside that environment. We can just run jupyter lab/notebook from conda base and select a particular R kernel.**

**Here, we have installed `R 4.1.0` inside the `r-env` environment**, so for simplicity, we will give the kernel name according to the environment name and displayname of the kernel according to the R version (it is not a specific rule, I am doing this for my ease of use)

### Now, run R in the terminal:
```bash
R
```
You will see a typical R console in the terminal. Now we will install our kernel in this console.

```R
IRkernel::installspec(name = 'ir-env', displayname = 'R 4.1.0')
```
> **NB**: Obviously run this command in the R console, not in bash terminal.

After installing the kernel in this way you can access this kernel from the jupyter lab/notebook launcher display. Example of typical launcher display:

![R_kernel_in_jupyterlab](./graph_images/Kernel_image.png)

>> **NB**: If you install another R version in another conda environment, don’t forget to change the `name` and `displayname` option in the above code.


