# MirDoku


sudo apt-get remove ipython

pip3 install --ignore-installed pyzmq

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
