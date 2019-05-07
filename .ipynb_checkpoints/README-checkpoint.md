# Corn Grain Yield Response to Nitrogen Rates
**Name**: Adrian Correndo

**Semester**: Spring 2019

**Project area**: Agronomy

**Last update**: Apr-15-2019


## Objective

Automating the calculation of grain yield (GY) response to different rates of nitrogen (N) fertilizer, and related fertilizer use efficiencies (NAE) in a database of more than one thousand experiments with different designs. A secondary goal is to explore descriptive statistics of variables of interest grouping experiments by soil texture classes (STx).

## Input

*.csv file with 4 columns: TRIAL, STx, N rate, and GY, where:

**-TRIAL**: Experiment ID number;

**-STx**: Soil texture class of typical pedon  (Soil Survey Staff, 2018);

**-Nrate**: Nitrogen rate (kg N ha<sup>-1</sup>);

**-GY**: Grain Yield when Nrate=0  (Mg ha<sup>-1</sup>, 15.5% moisture);

## Outputs

Two "*.csv" files

1. N0_plots.csv, with the following columns: TRIAL, STx, Y0, Ymax, NRmax, NRmax_r, NAEmax.
2. Nf_plots.csv, with the following columns: TRIAL, STx, Nrate, GY, Y0, Ymax, NR, NRr and NAE, where:

**-Y0**: GY when Nrate=0  (Mg ha<sup>-1</sup>);

**-Ymax**: maximum observed GY (Mg ha<sup>-1</sup>);

**-NR**: absolute nitrogen response corresponding to each fertilizer rate different from 0  (Mg ha<sup>-1</sup>).

**-NRr**: relative nitrogen response corresponding to each fertilizer rate different from 0  (%).

**-NRmax**: maximum absolute nitrogen response (Mg ha<sup>-1</sup>).

**-NRmax_r**: maximum relative nitrogen response (%).

**-NAE**: nitrogen agronomic efficiency as NR divided by its corresponding Nrate (kg NR kg<sup>-1</sup> of applied N).


### Main challenges were related to: 

i) the # of Nrate levels and the ammount of applied N (kg) vary across trials;

ii) Y0 and Ymax values take place at **Trial** level, while the NR and NAE values, at a sub-level by a given **Trial-Nrate combination**.

## Rationale

I'm working on a review paper for which I collected more than 1200 experiments. Automating these calculations will save me a significant amount of time and avoid potential misscalculations when processing the data. This code might be potentially useful for other similar databases studying crop responses to fertilizer.

## **Data Example**

![Example](https://github.com/adriancorrendo/project/blob/master/Scatter.png)

**Fig. 1**. Scatter plot of Corn Grain Yield (kg ha<sup>-1</sup>) and nitrogen rate (kg N ha<sup>-1</sup>) from two typical corn nitogren experiments from the database (#1: circles, #2: triangles). Y0, Ymax and NR variables are shown for Trial 1. *Fitted functions correspond to quadratic-plateau models (y = a + bx +cx^2, when Nrate < Xc -critical value or threshold-; otherwise y = plateau)*.

## **Sketch**
![Main steps of the project](https://github.com/adriancorrendo/project/blob/master/Sketch.png)
**Fig. 2**. Main steps of the project from data input to expecta data outpouts.


## **References**
1. Soil Survey Staff, Natural Resources Conservation Service, United States Department of Agriculture. Web Soil Survey. Available online at the following link: https://websoilsurvey.sc.egov.usda.gov/. Accessed [05-06-2019].
2. os - Miscellaneous operating system interfaces. https://docs.python.org/3/library/os.html. Accessed [05-06-2019].
3. glob — Unix style pathname pattern expansion. https://docs.python.org/3/library/glob.html. Accessed [05-06-2019].
4. The pandas project. https://pandas.pydata.org/. Accessed [05-06-2019].
5. Folium 0.1.5. https://pypi.org/project/folium/0.1.5/. Accessed [05-06-2019].