# Basic
## Data composition
N X P matriced data; N row and P colum, N observations with P variables
## Read and Load
<b>Getwd();</b> get working directory file that we are using
<b>setwd();</b> set the directory addresses
#Intro to practically use the R for analysis
## Assigning variables
"<-" and "=" is little different, "<-" is preferred since the "=" has multiple meanings.(e.g. maybe logical equations?)

## Packages
To use the package, firstly,install it by using command
<b>install.packages(_"psych"_)</b>
</br></br>And load the package into working environment by 
<b>library(psych)</b>
## Load the data file
".csv" files are commonly used. It's short for "comma seperated values" files. 
e.g. spreadsheets, Google Sheets, Microsoft Excel etc....
</br>Give the data frames a useul name </br>e.g. data1, RegDat1 ...
<b>dat1<-read.csv(file="filename.csv", header=T, stringsAsFactors = F)</b>
                       </br> in here, the header means whether you want to take the very first row to the variable names(True, T) or not (False, F)
</br> Also, if you want to treat the categorical variables(e.g. Gender(female, male)) as the binomial, you can set it by </br><b>stringsAsFactors = True(or T)</b>
<br>
## Indexing the data elements from file
<b>d[10,23]</b> <br> It indexes the date element in 10th colum and 23rd row
## Various useful functions
<b>summary(dat1)</b> : getting the basic descriptives from data file "dat1"
</br> <b>View(dat1)</b> : it makes able to read data file "dat1" in FANCY data frame on console. ( if you just type _dat1_ in console, it literally will _Print dat1_ on console
</br>d
