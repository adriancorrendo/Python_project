# Calculate Corn Response to Nitrogen Rates
---

**Name**: Adrian Correndo

**Semester**: Spring 2019

**Project area**: Agronomy

---

## **Objective**

Write a python function to automate, for more than one experiment with different nitrogen fertilizer rates, the calculation of grain yield (GY) response to different rates of nitrogen fertilizer, the estimation of related fertilizer use efficiencies (NUE), and then analyze these variables by subgroups of interest, for example soil texture (STx). I also want to identify for each experiment, the grain yield when nitrogen rate is equal to 0 (Y0) and the maximum observed yield (Ymax).

## **Outcomes**

I want the function to produce a *.csv file with up to 8 columns: Trial, STx, Nrate, GY, Y0, Ymax, NR, and NUE. Where Y0 is the grain yield corresponding to the Nrate equal to 0; Ymax is the maximum observed grain yield; NR is the raw nitrogen response corresponding to each fertilizer rate different from 0. The challenge could be related to the following aspects: i) while Y0 and Ymax values are only one per Trial, the NR and NUE values correspond to a sub-level identified by a given Trial-Nrate combination; ii) Nrate levels (in number and applied N) could vary among trials. 

## **Rationale**

My research project will be related to managing a database of hundreds of corn nitrogen fertilization experiments. For this reason, automating the calculations will save me a significant amount of time when processing the data of nitrogen response, nitrogen use efficiency, and analyzing the database following a classification criterion to create subgroups of soil texture. Creating a criterion like the latter might be useful to reduce the number of potential groups of soil texture (12 main classes from clay to sand) and cluster them into, for example, three main subgroups (fine, medium, coarse).

## **Sketch**

![Main steps of the project](https://github.com/adriancorrendo/project/blob/master/sketch.jpg)
