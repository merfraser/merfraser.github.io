# merfraser.github.io

This repository contains the building blogs for my personal website, built using quarto, and contains the virtual environments required to render my blog posts which have embedded R and python code. 

To build this website, follow these steps:
(1) Open your terminal, run the following cd command to navigate to the folder (should not already be a github repository) to clone this repository into
    `cd <folder_name>`
(2) Clone this repository into your working directory folder by running the following command in your open terminal:
    `git clone <https or SSH link for this github repo>`
(3) Now make the cloned repo on your local machine your working directory, by running this command in the terminal:
    `cd merfraser.github.io`
(4) Load the required virtual environments for python code by running the following command in the terminal:
    `uv sync`
(5) Similarly, load the required virtual environments for R code by opening the folder in Positron and in the bottom 'Console' panel on the right hand side, click the small + with a down error and select 'Start Another..' from the pop-up in the top pane, select an R session. You now have both a Python and R session running simultaneously. In the R console, run the following commands:
    `renv restore`
(6) Now to build the site locally, return to a terminal window and run the following:
    `uv run quarto render`
The site will land in the ~/docs folder within the repository (once rendered, this folder includes the .html files that make this a website your browser can open and render).

The data required for building the Quarto blog post pages in both python and R are held in the virtual environment detailed in the pyproject.toml and renv.lock files, respectively, and do not require the network to fetch it. 