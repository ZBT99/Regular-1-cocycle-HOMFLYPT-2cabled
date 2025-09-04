# Regular-1-cocycle-HOMFLYPT-2cabled

This repository contains a Jupyter Notebook project.
The notebook (demo.ipynb) aims to use the quantum equations from pushing a twist and another tangle T2 to distinguish different knots. 

If you do not know how to run Jupyter notebook in your own computer 
you can run it in Colab online. The link is below:

https://colab.research.google.com/drive/1ypdBw-02Bs2sUFuF893tQ_WGDgO18Z8D?usp=sharing


The notebook begins with the definitions of a lot of functions (in the code part). 
Then there are several examples such as 6_1 and 6_2. 

There are several packages to be installed listed in requirements.txt
If you have not yet install these packages, you can insert a cell in the notebook
and write the following: !pip install -r requirements.txt


## Files
- `demo.ipynb`: Main Jupyter Notebook file
- `README.md`: Project documentation
- `LICENSE`: Open-source license (MIT)
- `.gitignore`: Git ignore configuration
- `requirements.txt`: Python dependencies

## Usage

Open demo.ipynb in Jupyter Notebook or Colab online.
Run the cells sequentially from top to bottom to reproduce the examples.

For your own calculations:

A long knot of n crossings is represented by a matrix of 2n rows and 3 columns. Actually it represents the Gauss diagram of the long knots.
The first column of the matrix is the names of the arrows. 
The second column of the matrix represent the overcrossing (+1) or the undercrossing (-1). 
The third column of the matrix represents the sign of the arrow. 
The matrix going from top to bottom is as in the order of the Gauss diagram from the base point going counterclockwise. 

Let G be such a matrix (e.g. G = four_1)
you can use `writhe(G)` and `whitney(G)` to see its writhe and the Whitney index of G. 

To modify the writhe and the Whitney index of G, 
two functions are useful:

`addcurl(G, i, j)` where i is 0,1,2 or 3, and j is a natural number

`infty_avancer(G, k)` where k is an integer. 


`addcurl(G, i, j)` add j times curls of type i at the end of the matrix G (there are 4 kinds of curls)

`infty_avancer(G, k)` moves the base point of the Gauss diagram of G k times counterclockwise. 

One could consult the usages in the given examples. 

Convention: The regular homflypt relation we use here are: 

H_{+} - H_{-} = ZH_{0};

H_{+} = A H;

H_{-} = A^{-1} H

