If you're on a Mac, you need to install Apple's developer tools (XCode). Make sure to install the command line tools component from XCode's Downloads preference pane
https://developer.apple.com/xcode/
If you're still on Mac OS X 10.6.8, then you'll need to locate and install XCode 3.

Also check to see if you have git, and if not download and install it from git-scm.com.

You probably have to log out and log back in if you're on a Mac at this point - it helps the path info propagate.

Install Anaconda (free download):
https://store.continuum.io/cshop/anaconda/
Installation Instructions:
http://docs.continuum.io/anaconda/index.html#installation-instructions

If you're on Linux and download the anaconda.sh script, you will need to chmod u+x anaconda.sh

From a Terminal, update to latest packages:
conda update conda
conda update anaconda

Check to make sure the Anaconda is on your path:
which pip
Result is something like
/Users/ebruning/anaconda/bin/pip


Install stuff needed for LMA analysis
-------------------------------------
```
pip install pyproj
pip install pupynere
```

Create a working directory for source code:
```
cd ~
mkdir code
```

Add the directory you created above to your PYTHONPATH
Edit `.bash_profile` in your home directory:

```export PYTHONPATH=/Users/ebruning/code/:$PYTHONPATH```

Install lmatools:
From within the code directory:

```git clone https://github.com/deeplycloudy/lmatools.git```

Try starting iPython

`ipython`

and then import lmatools:

`import lmatools`

If that import works,
```
cd code
git clone https://github.com/deeplycloudy/stormdrain.git
git clone https://github.com/deeplycloudy/brawl4d.git
```

Process and view sample data included with lmatools
```
python ~/code/lmatools/testing/test_sklearn.py /path/to/output/files/
cd brawl4d/notebooks
ipython notebook
```
Click on LMAGui3D. Edit the data_path in the second cell to include /path/to/output/files/ as defined above. Run all the cells prior to the "Charge Analysis" and try interacting with the plot.
