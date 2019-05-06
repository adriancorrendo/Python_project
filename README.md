# Corn Grain Yield Response to Nitrogen Rates
**Name**: Adrian Correndo

**Semester**: Spring 2019

**Project area**: Agronomy

**Last update**: Apr-15-2019


## Objective

Automating the calculation of grain yield (GY) response to different rates of nitrogen (N) fertilizer, and related fertilizer use efficiencies (NAE) in a database of more than one thousand experiments with different designs. A secondary goal is to explore descriptive statistics of variables of interest grouping experiments by soil texture classes (STx).

## Inputs

*.csv file with 4 columns: TRIAL, STx, N rate, and GY, where:

**-TRIAL**: Experiment ID number;
**-STx**: Soil texture class of typical pedon  (Soil Survey Staff, 2018);
**-Nrate**: Nitrogen rate (kg N / ha);
**-GY**: Grain Yield when Nrate=0  (Mg / ha, 15.5% moisture);

## Outcomes

Two "*.csv" files

1. N0_plots.csv, with the following columns: TRIAL, STx, Y0, Ymax, NRmax, NRmax_r, NAEmax.
2. Nf_plots.csv, with the following columns: TRIAL, STx, Nrate, GY, Y0, Ymax, NR, NRr and NAE, where:

**-Y0**: GY when Nrate=0  (Mg / ha);
**-Ymax**: maximum observed GY (Mg / ha);
**-NR**: absolute nitrogen response corresponding to each fertilizer rate different from 0  (Mg / ha).
**-NRr**: relative nitrogen response corresponding to each fertilizer rate different from 0  (%).
**-NRmax**: maximum absolute nitrogen response (Mg / ha).
**-NRmax_r**: maximum relative nitrogen response (%).
**-NAE**: nitrogen agronomic efficiency as NR divided by its corresponding Nrate (kg NR / kg applied N).

Challenges might be related to: 

i) the # of Nrate levels and the ammount of applied N (kg) vary across trials;
ii) Y0 and Ymax values take place at **Trial** level, while the NR and NAE values, at a sub-level by a given **Trial-Nrate combination**.

## Rationale

Database compund by hundreds of corn nitrogen fertilizer experiments. Automating these calculations will save me a significant amount of time and avoid potential misscalculations when processing the data.

## **Sketch**

![Example](https://github.com/adriancorrendo/project/blob/master/Scatter.JPG)

**Fig. 1**. Scatter plot of Corn Grain Yield (kg/ha) and nitrogen rate (kg N/ha) from two typical corn nitogren experiments from the database (#1: circles, #2: triangles). Y0, Ymax and NR variables are shown for Trial 1. *Fitted functions correspond to quadratic-plateau models (y = a + bx +cx^2, when Nrate < Xc -critical value or threshold-; otherwise y = plateau)*.

![Main steps of the project](https://github.com/adriancorrendo/project/blob/master/Sketch.PNG)
**Fig. 2**. Main steps of the project from data input to expecta data outpouts.