This directory contains materials developed for an online LMA 
training workshop on 3 January 2022. The training was modified from the 
2021 TRACER training  with the aim of supporting the needs of the Lake 
Effect Electrification field campaign that took place from Nov 2022-Jan 
2023.

## Setup instructions

If you don't already have Python and conda, install them [according to Unidata's instructions](https://unidata.github.io/python-training/). You do *not* need to follow the instructions in the *Setup the Environment* section, except for the part that mentions how to install git. Just *Installing Conda*. However, there is no harm in going further, and it will have you all set to use Unidata's training, which is great for lots of other meteorological map-making!

If you already have Python and conda, just reuse that installation starting with the instructions below. We will create an entirely separate conda environment for this workshop, so it shouldn't conflict with things you've already installed. You will also need to install git, which can also be done with `conda install git`, as in the Unidata instructions.

Once you have conda,

1. Create a directory where you want this workshop's materials to live.
2. Open a terminal or Anaconda Prompt, and change to that directory
3. From that directory run the following commands:

```
git clone https://github.com/deeplycloudy/lmaworkshop.git

cd lmaworkshop
cd LEE-2023
conda env create environment.yml
```

These steps create a conda environment called `leelma`. Every time you 
return to use these workshop notebooks (running from a new terminal window), you'll need 
to activate the conda environment again before opening the notebooks.

```
conda activate leelma

jupyter lab
```

This should open jupyter lab in a browser window and you'll see the 
LEE-2023 workshop materials. From there open the `test_environment.ipynb` notebook, and run the cells in that notebook. You should see a plot with axes, but nothing in it. If everything ran without error, you should be all set.
