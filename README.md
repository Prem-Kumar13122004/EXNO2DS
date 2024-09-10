# -*- coding: utf-8 -*-
"""EXNO2DS.ipynb

Automatically generated by Colaboratory.

Original file is located at
    https://colab.research.google.com/drive/1ymCTA1j5RI-UKnnpBC6gOUJWzDfOtFCs
"""

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

dt=pd.read_csv("#COPY CSV FILE PATH")

dt

dt.info()

#DISPLAY NO OF ROWS AND COLUMNS

#SET PASSENGER ID AS INDEX COLUMN

dt.describe()

"""**CATEGORICAL DATA ANALYSIS**"""

# USE VALUE COUNT FUNCTION AND PERFROM CATEGORICAL ANALYSIS

"""**UNIVARIATE ANALYSIS**"""

# USE COUNTPLOT AND PERFORM UNIVARIATE ANALYSIS FOR THE "SURVIVED" COLUMN IN TITANIC DATASET

# IDENTIFY UNIQUE VALUES IN "PASSENGER CLASS" COLUMN

# RENAMING COLUMN
dt.rename(columns = {'Sex':'Gender'}, inplace = True)
dt

"""**BIVARIATE ANALYSIS**"""

# USE CATPLOT METHOD FOR BIVARIATE ANALYSIS

fig, ax1 = plt.subplots(figsize=(8,5))
graph = sns.countplot(#USE THE NECESSARY PARAMETERS HERE)
graph.set_xticklabels(graph.get_xticklabels())
for p in graph.patches:
    height = p.get_height()
    graph.text(p.get_x()+p.get_width()/2, height + 20.8,height ,ha="left")

# USE BOXPLOT METHOD TO ANALYZE AGE AND SURVIVED COLUMN

"""**MULTIVARIATE ANALYSIS**"""

# USE BOXPLOT METHOD AND ANALYZE THREE COLUMNS(PCLASS,AGE,GENDER)

# USE CATPLOT METHOD AND ANALYZE THREE COLUMNS(PCLASS,SURVIVED,GENDER)

# IMPLEMENT HEATMAP AND PAIRPLOT FOR THE DATASET
