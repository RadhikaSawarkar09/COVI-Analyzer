# COVI-Analyzer

"COVI-Analyzer" is based on domain Big Data and Python, In this project  i worked with the COVID-19 datasets which consists of total confirmed cases, Positive cases, Negative cases, etc. And visualized the analysis result using Seaborn.

# Data Science-

This report has been prepared on the project of topic Covi-Analyser by using Data-Science(Python)in Jupyter Notebook.
Initially we collected raw data through official website WWW.Kaggle.com Afterwards we analyzed the collected data, We have refined, and analyzed those data in different aspects and displayed it in a systematic form

Finally, we carried out comparison of the States based data using different way of
Representation like-relplot,catplot,heapmap,distmap,boxplot,regplot,barplot,lineplot..etc,

# Data Analysis-

After collecting the data, as per our planning we prepared and analyse dataset. We sorted the collected data and represent those using different visualisation methods like-relplot,catplot,heapmap,distmap,boxplot,regplot,barplot,lineplot..etc,and analyzed them making comparative study of the COVID -19 situations.
Libraries used-
•	Pandas
•	Numpy
•	Matplotlib
•	Seaborn
We have also used voila which turns into a standalone web applications.


# Software Used-

Jupyter Notebook was used to collect the data in a systematic way and to visualize them.It makes us easier to provide some better visualization of the data. We have used different bars and graphs to represent the data.
They are great for exploration. Jupyter Notebooks are an amazing tool for exploration purposes. It allows you to create some visualizations, and calculate results all in one go.
The architecture of Jupyter is language independent. The decoupling between the client and kernel makes it possible to write kernels in any language.

# Outcomes & Analysis-
 
 	  Lineplot-
       This lineplot will gives you statewise positive cases out of Total Samples.
       This lineplot will gives you Datewise positive cases out of Total Samples
       It is on  the world’s data representing the no of people fully vaccinated on specific dates.	

	  Boxplot-	  
       Here boxplot is representing Total Samples according to states   	 

   	Heatmap-
       This heatmap contains representing various shades of the same colour foreach value to be plotted.
	
	 	Catplot-
        These plot are basically used for visualizing the relationship between variables .It gives  Total sample counts in various states.
	 
   	Barplot-
        A barplot shows categorical data as rectangular bars with the height of bars proportional to the value they represent.   
        
    Relplot-
        This visualizes statistical realtionsip using two common approaches.It shows the no.of positive cases from the Total samples.
        This graph represents the world’s data on the basis of people fully vaccinated according to the country
        
        
# Algorithm-
   Step1:- Start
   Step2:-  Import numpy,matplotlib.pyplot,pandas,seaborn.
   Step3:- Import Plotly.express as px
   Step4:- Install Plotly
   Step5:- Take input pd.read_csv file
   Step6:- Print input
   Step7:- Take input from dataset
               Plot1:- Coordinates(Total Sample, Positive)
                             Hue(States)
               Plot2:- Coordinates(Positive, Total Samples)
               Plot3:- Coordinates(Negative, Total Samples)
               Plot4:- Coordinates(State, Total Samples)
               Plot5:- Coordinates(State, Total Samples)
               Plot6:- Coordinates(State, Total Samples)
               Plot7:- Cooridinates(x=Total Samples,color= purple)
               Plot8:- Coordinates(TotalSamples,State,palette(Wistia_r))
               Plot9:- Coordinates(Total Sample, Positive)
               Plot10:- Coordinates(Total Sample, State)
                              ( legend="full",palette="nipy_spectral_r")
               Plot11:- Coordinates(Total Sample, Positive)
                           (hue=State,legend=full,palette="gist_ncar_r")
               Plot12:- PC read
               Plot13:- Coordinates(Total Sample, Positive) hue=Date,legend=full,palette="gnuplot2_r

    
    Step8:- End

	
# COVI - Analyzer Implementation :-

# In[1]:


import numpy as np
import matplotlib.pyplot as plt
import pandas as pd 
import seaborn as sns

read=pd.read_csv(r"C:\Users\RADHIKA\Downloads\StatewiseTestingDetails.csv")
print(read)


# In[2]:


plt.figure(figsize=(12,4))
ax=sns.lineplot(x="TotalSamples",y="Positive",data=read, hue="State")


# In[3]:


ax=sns.relplot(x="Positive",y="TotalSamples",data=read)


# In[4]:



ax=sns.relplot(x="Negative",y="TotalSamples",data=read)


# In[5]:


plt.figure(figsize=(12,6))
ax=sns.boxplot(x="State",y="TotalSamples",data=read)


# In[6]:


plt.figure(figsize=(13,6))
ax=sns.barplot(x="State",y="TotalSamples",data=read)


# In[7]:


plt.figure(figsize=(12,6))
x=read["TotalSamples"].values
sns.distplot(x,color="Purple")


# In[8]:


plt.figure(figsize=(12,6))
ax=sns.barplot(x="TotalSamples",y="State",data=read,palette="Wistia_r")


# In[9]:


plt.figure(figsize=(12,6))
ax=sns.scatterplot(x="TotalSamples",y="Positive",data=read,legend="full")



# In[10]:


plt.figure(figsize=(12,6))
ax=sns.catplot(x="TotalSamples",y="State",data=read,legend="full",palette="nipy_spectral_r")


# In[11]:


plt.figure(figsize=(12,6))
ax=sns.regplot(x="TotalSamples",y="Positive",data=read)


# In[12]:


plt.figure(figsize=(12,6))
ax=sns.relplot(x="TotalSamples",y="Positive",data=read,hue="State",legend="full",palette="gist_ncar_r")


# In[13]:


pc=read[["TotalSamples","Date","State","Positive","Negative"]]
pc


# In[14]:


plt.figure(figsize=(12,5))
ax=sns.lineplot(x="TotalSamples",y="Positive",data=read,hue="Date",legend="full",palette="gnuplot2_r”


# In[15]:


import plotly.express as px


# In[16]:


pip install plotly










	

