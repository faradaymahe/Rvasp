Rvasp
=====
Tools for loading, manipulating and plotting VASP files within R

### Important
Many features originated by a need to solve a specific problem and are propably not generalized enough to declare the general problem fully solved.
All functions are implemented in pure R and are mostly easy to understand. Feel free to read the [source](../../tree/master/Rvasp/R), improve and submit changes.

### Install
* download [Rvasp package](../../raw/master/Rvasp_0.1.tar.gz)
* install in R

```R
install.packages(pkgs="Rvasp_0.1.tar.gz")
```

* load in R

```R
library(Rvasp)
```

Contains functions to work with

### [POSCAR](../../wiki/POSCAR)
* [read](../../wiki/Basics-(POSCAR\)) 
* [write](../../wiki/Basics-(POSCAR\)) 
* [manipulate](../../wiki/Manipulation-(POSCAR\))
* [plot](../../wiki/Plotting-(POSCAR\)) [(ex.)](../../wiki/example-Plots#poscar)

### CHGCAR
* [read](../../wiki/CHGCAR)
* calculate and [plot](../../wiki/example-Plots#stm) [stm](../../wiki/STM)

### vasprun.xml 
* read and [plot](../../wiki/example-Plots#dos) (projected) [dosdata](../../wiki/DOS)
* read and [plot](../../wiki/example-Plots#bands) (projected) [bandsdata](../../wiki/BANDS) and fit a dirac cone or a quadratic function to a band

Contains a wrapper for [calculations](../../wiki/CALCULATIONS) organized in the following scheme:   
   
/manyCalculations/Calculation1/Parameter1/VASPfile1   
/manyCalculations/Calculation1/Parameter1/VASPfile2   
..   
/manyCalculations/Calculation1/Parameter2/VASPfile1   
/manyCalculations/Calculation1/Parameter2/VASPfile2   
..   
/manyCalculations/Calculation2/Parameter1/VASPfile1   
/manyCalculations/Calculation2/Parameter1/VASPfile2   
etc.

so there are three levels:
* Calculations
* Calculation
* Parameter

On calculation level there are the following functions:
* get / [plot](../../wiki/example-Plots#eacurve) / fit an e over a curve
* get / [plot](../../wiki/example-Plots#ldos) a local dos curve
* get / [plot](../../wiki/example-Plots#bbands) bulk band data

Furthermore there are some [miscellaneous](../../wiki/miscellaneous) functions like
* [ploting](../../wiki/example-Plots#pt) a periodic table