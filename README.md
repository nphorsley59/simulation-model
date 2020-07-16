# <div align="center">Modeling Population Growth</div>

### <div align="center">Project Overview</div>
As part of my Master's thesis, I built a partial life-cycle matrix model<sup>1</sup> and used it to predict the survival rate of Common Grackles<sup>2</sup> during the non-breeding season. The model simulates realistic population growth and has several additional features that extend beyond the scope of my research. I am in the process of publishing the results produced by this model. I am also using this model to do predictive modeling for another publication investigating Micronesian Starling demography on the island of Guam.

### <div align="center">Model Structure</div>

#### Stage 1
The first modeling stage simulates population growth over a pre-defined trial period to transform a single population variable into an array representing stable age distribution. 

#### Stage 2
The second modeling stage proportionally adjusts the stable age distribution array to represent the desired initial population size. From here, population growth is simulated over the length of time defined by the user.

#### Stage 3
The third and final modeling stage averages annual population size and growth over the number of simulations defined by the user. It then plots mean population size with confidence intervals and calculates an annual trend estimate.

#### Additional Features
The three stages outlined above describe the most simplistic modeling approach. More details can be found in the PLC_MatrixModel_AddFeat.txt file included in my Portfolio repository.

### <div align="center">Results</div>

Matrix models use matrices to track population growth across age classes (Table 1). This model structure allowed me to input age-specific survival and fecundity for more accurate modeling results. 

**Table 1.** A sample of the age matrix dataframe that shows population distribution across age classes.<br />

![alt text](https://github.com/nphorsley59/Portfolio/blob/master/PLC_MatrixModel_Figures/Pop_Matrix_Table1.png "Age Matrix")<br />

In order to account for environmental stochasticity, I built natural variation into each rate based on real data collected in the field. As a result, each simulation produces slightly different results (Table 2, Figure 2). 

**Table 2.** A sample of the population growth dataframe that show population growth across simulations.<br />

![alt text](https://github.com/nphorsley59/Portfolio/blob/master/PLC_MatrixModel_Figures/Pop_Growth_Table1.png "Population Growth")<br />

For my thesis, we used established demographic rates from the literature and estimated demographic rates from our own research (Table 3) to predict non-breeding season survival in three distinct populations: a stable population, the current global population, and the current Illinois population (Table 4, Figure 1). 

**Table 3.** The model parameters used to predict non-breeding season survival.<br />

![alt text](https://github.com/nphorsley59/Portfolio/blob/master/PLC_MatrixModel_Figures/Model_Parameters_Table1.png "Model Parameters")<br />

**Table 4.** The predicted rates of non-breeding season survival for each population.<br />

![alt text](https://github.com/nphorsley59/Portfolio/blob/master/PLC_MatrixModel_Figures/NBS_Survival_Predictions_Table1.png "Model Predictions")<br />

**Figure 1.** Population growth projections using predictions of non-breeding survival for three distinct populations.<br />
&nbsp;  

![alt text](https://github.com/nphorsley59/Portfolio/blob/master/PLC_MatrixModel_Figures/Proj_Pop_Growth_Figure1.png "Predicted Population Growth")<br />

**Figure 2.** A sample of simulations produced by the model, replicating projected decline in Illinois.<br />
![alt text](https://github.com/nphorsley59/Portfolio/blob/master/PLC_MatrixModel_Figures/livesim_plot_24sims.gif "Simulation Animation")
### <div align="center">Summary</div>

The partial life-cycle matrix model I built for my Master's thesis was used to project population decline in my study species, the Common Grackle, and to predict rates of non-breeding season survival for three distinct populations: a stable population, the current global population, and the current Illinois population. The modeling approach I chose allowed me to use many demographic parameters and account for realistic environmental variation. I learned a lot about model design, custom functions, and advanced visualization techniques from this project and am excited to reuse the model to answer other research questions in the future.

### <div align="center">Resources</div>
<sup>1</sup> https://onlinelibrary.wiley.com/doi/abs/10.1034/j.1600-0706.2001.930303.x<br />
<sup>2</sup> https://birdsoftheworld.org/bow/species/comgra/cur/introduction<br />
