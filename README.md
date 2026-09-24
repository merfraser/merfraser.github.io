# merfraser.github.io

This repository contains the building blogs for my personal website, built using quarto, and contains the virtual environments required to render my blog posts which have embedded R and python code. 

To build this website, follow these steps:

(1) Open your terminal, run the following cd command to navigate to the folder (should not already be a github repository) to clone this repository into:
    > `cd <folder_name>`

(2) Clone this repository into your working directory folder by running the following command in your open terminal:
    > `git clone <https or SSH link for this github repo>`

(3) Now make the cloned repo on your local machine your working directory, by running this command in the terminal:
    > `cd merfraser.github.io`

(4) Load the required virtual environments for python code by running the following command in the terminal:
    > `uv sync`

(5) Similarly, load the required virtual environments for R code by running the following two commands in the same terminal (still in same working directory). First, open an R session by running: 
    > `R`

Next, within that R session, load the R virtual environment by running this code within the R session:
    > `renv::restore`

Once loaded, quit the R session by running `q()`, to return to your terminal.

(6) Now to build the site locally, return to a terminal window and run the following:
    > `uv run quarto render`


The site will land in the ~/docs folder within the repository (once rendered, this folder includes the .html files that make this a website your browser can open and render).

Once rendered, to open the local render of the site, run the following in the same terminal window:
    > `open docs/index.html`

The data required for building the Quarto blog post pages in both python and R are held in the virtual environment detailed in the pyproject.toml and renv.lock files, respectively, and do not require the network to fetch it. 