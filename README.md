# Basic
## Questions&Help
type <b>??_functionname_</b>
## Data composition
N X P matriced data; N row and P colum, N observations with P variables
## Char and String and Numerical variable
if you type <b>c("something","Hello")</b> it generates the Char values 
## Subset Function
Just like logical function of MATLAB, it can substract the subset from the dataset and make it into specific(another) dataset
</br><b>subset

## Capital Letters
R specifies the capital letters different from the lower letters
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
## Indexing and modifying the data elements from file
<b>d[10,23]</b> <br> It indexes the date element in 10th colum and 23rd row
</br>colnames(dat1)[1] <- "something_you_want_to_use_it_as_variable_name"
</br>_()_ specifies dataset and _[]_ specifies which column you want to change it to specific variable name
## Various useful functions
<b>summary(dat1)</b> : getting the basic descriptives from data file "dat1"
</br> <b>View(dat1)</b> : it makes able to read data file "dat1" in FANCY data frame on console. ( if you just type _dat1_ in console, it literally will _Print dat1_ on console
</br>colnames(dat1)[1] or dat1$State, you can index the the 1st column of data file _dat1_ or Varialbe named _State_ in data file _dat1_
</br>
## Manipulating Data
If we want to deselect, get rid of certain variables from _dat1_, we can use variable methods. Two are basics.
</br><b>dat1_modified <- cbind(dat1[,1:7], dat1[,11:18])</b>
</br><b>dat1_modified1 <- rbind(dat1[1:7,], dat1[11:18,])</b>
</br>**OR**
</br> Use codes like belows,
</br><b>dat1_modified2 <- dat1[,-8:-10]</b>
  </br><b>dat_modified3 <- dat1[-8:-10,]</b>
  
# Plotting and Test Analysis
## Correlation
corr_matrix$Call :If you type it you can see what you've did to the corr_matrix and track the changes or variables you are using

## Standardization
scale(datafile[

## T-test
<b> t.test(d[,], d[,])</b>, </br> Usually it require datasets to be kind of in line to each other(maybe dimensions?)
**OR**
</br>Other ways to do it with using variables neames </br><b>t.test(d$QualityOfLife[1:25], d$QualityOfLife[26:50])</b>

## ANOVA
<b> anova(X,Y) </b>,</br> you can put even models in X and Y
## Regression
- Simple regression
- Multiple regression
- Hierarchical regression(: Adding new predictors in model to see if "Do XX factors predicting XX beyond XX factor?"/this is a technique to see if a variable adds incremental variance for predicting an outcome)

## Plotting Interaction
<b>interact_plot(model_5, pred=Neuroticism, modx=Extraversion)</b> </br>use the variables from interaction of interest
</br>high E and N is associated with high unemployment; high E and low N is associated with low unemployment
</br>N is not related to unemployment when E is low
</br>we can plot it with Neuroticism as the moderator too. Theory must lead the way here
