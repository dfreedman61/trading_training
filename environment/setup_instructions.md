

\# Trading Environment Setup



This document explains how to recreate the Python environment used for this project on a new machine (Mac or Windows).



\---



\## ✅ Step 1 — Install Anaconda or Miniconda



Download and install:



\- https://www.anaconda.com/download



\---



\## ✅ Step 2 — Create the environment



Open terminal (Mac) or Anaconda Prompt (Windows):



```bash

conda create -n trading\_env python=3.11 -y



\## ✅ Step 3 — Activate environment



conda activate trading\_env





\## ✅ Step 4 - Install core packages (using conda)



conda install pandas numpy matplotlib seaborn scipy jupyter ipykernel -y





\## ✅ Step 5 - Install additional packages (using pip)



pip install yfinance





\## ✅ Step 6 - Register environment with Jupyter





python -m ipykernel install --user --name trading\_env --display-name "Python (trading\_env)"



\## ✅ Step 7 - start Jupyter



jupyter notebook



Select the kernel:

&#x09;Kernel → Change Kernel → Python (trading\_env)



\## ✅ Step 8 - Verify environment





import pandas as pd

import numpy as np

import matplotlib.pyplot as plt

import yfinance as yf



data = yf.download("SPY", start="2020-01-01")

data\['Close'].plot()

plt.show()



