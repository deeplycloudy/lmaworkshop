This directory contains materials first developed for an online LMA training workshop on 21 October 2021. The training was developed with the specific aim of supporting the needs of the ESCAPE and TRACER field campaigns in Summer 2022.

## Setup instructions

If you don't already have conda, install Python and conda [according to Unidata's instructions](https://unidata.github.io/python-training/).

You do *not* need to follow the instructions in the *Setup the Environment* section. Just *Installing Conda*. However, there is no harm in going further, and it will have you all set to use Unidata's training, which is great!

Once you have conda,

1. Create a directory where you want this workshop's materials to live.
2. Open a terminal or Anaconda Prompt, and change to that directory
3. From that directory run the following commands:

```
git clone https://github.com/deeplycloudy/lmalib-tracer.git
git clone https://github.com/deeplycloudy/lmaworkshop.git

cd lmalib-tracer
conda env create environment.yml
conda activate lmatracer
pip install -e .

conda install -c conda-forge ipympl matplotlib ipywidgets cartopy jupyter jupyterlab metpy

cd ..
cd lmaworkshop
cd TRACER-2021

jupyter lab
```

This should open jupyter lab in a browser window and you'll see the TRACER-2021 workshop materials. From there open the `test_environment.ipynb` notebook, and run the two cells in that notebook. You should see a plot with axes, but nothing in it. If everything ran without error, you should be all set.