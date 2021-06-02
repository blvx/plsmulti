# plsmulti
Test differences of SEM-PLS coefficients between two groups, with the results of the SmartPLS 2 data  

Estimate the boostrap model with group A  
Copy the data from "Path coefficients" in an Excel file (or .csv)  
Idem with group B  

library(plsmulti)  

setwd(folder data)  
boot.A = read.csv2("boot.A.csv",header=TRUE)  
boot.B = read.csv2("boot.B.csv",header=TRUE)  

plsmulti(boot.A,n.A=200,boot.B,n.B=250)  

Results:  
              Diff      t   Sign.  
Var1....Var2  -0.018 -0.158 0.563  
Var3....Var2  -0.305 -2.639 0.996  
