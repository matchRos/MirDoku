# MirDoku

Based on: https://www.digitalocean.com/community/tutorials/how-to-set-up-a-jupyter-notebook-to-run-ipython-on-ubuntu-16-04


Step 1 — Installing Python 2.7 and Pip

In this section we will install Python 2.7 and Pip.

First, update the system's package index. This will ensure that old or outdated packages do not interfere with the installation.

    sudo apt-get update

Next, install Python 2.7, Python Pip, and Python Development:

    sudo apt-get -y install python2.7 python-pip python-dev

Installing python2.7 will update to the latest version of Python 2.7, and python-pip will install Pip which allows us to manage Python packages we would like to use. Some of Jupyter’s dependencies may require compilation, in which case you would need the ability to compile Python C-extensions, so we are installing python-dev as well.

To verify that you have python installed:

    python --version

This will output:

Output
Python 2.7.11+

Depending on the latest version of Python 2.7, the output might be different.

You can also check if pip is installed using the following command:

    pip --version

You should something similar to the following:

Output
pip 8.1.1 from /usr/lib/python2.7/dist-packages (python 2.7)

Similarly depending on your version of pip, the output might be slightly different. 


Step 2 — Installing Ipython and Jupyter Notebook

In this section we will install Ipython and Jupyter Notebook.

First, install Ipython:

    sudo apt-get -y install ipython ipython-notebook

Now we can move on to installing Jupyter Notebook:

    sudo -H pip install jupyter

Depending on what version of pip is in the Ubuntu apt-get repository, you might get the following error when trying to install Jupyter:

Output
You are using pip version 8.1.1, however version 8.1.2 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.

If so, you can use pip to upgrade pip to the latest version:

    sudo -H pip install --upgrade pip

Upgrade pip, and then try installing Jupyter again:

    sudo -H pip install jupyter
    
If that does not work try:

    sudo apt-get remove ipython
    pip install --ignore-installed pyzmq


Step 3 — Running Jupyter Notebook

You now have everything you need to run Jupyter Notebook! To run it, execute the following command:

    jupyter notebook



