# spatial-analysis-datasets
Data sets from the book Spatial Analysis by J T Kent and K V Mardia

1. The data sets have been stored as standard ascii text files.  They in two forms:

geo = geodata = the format used by the R package geoR.  The data can be read into R as an n by 3 data frame.  When plotting the data, the first column represents the first coordinate of a site, going left to right, and the second column represents the second coordinate of a site, going bottom to top.  The third column represents the value of the random field at this site.

mat = matrix.  The data take the form of an n1 by n2 matrix, where the rows and columns label the sites. When plotting the data, the row label runs from top to bottom and the column label runs from left to right.  The entry in the matrix gives the value of the random field at the corresponding site.

2. Here are the data sets and their dimensions:

Data set                          dimensions              Page in book

bauxite-geo.txt                   33 by 3 data frame          8

elevation-geo.txt                 52 by 3 data frame          5

fingerprint-section-mat.txt       356 by 218 matrix          17 

gravimetric-mat.txt               10 by 10 matrix            20    

landsat-mat.txt                   200 by 200 matrix           9

laslett-mat.txt                   11 by 11 matrix            21

mercer-hall-mat.txt               20 by 25 matrix            25

synthetic-mat.txt                 200 by 200 matrix          10

webster-mat.txt                   10 by 10 matrix            28

3. Reading the data into R.  Use the read.table command to read in the data as a data frame; convert it to a matrix if desired.  For example, if the data sets are located in the working directory of R, the following commands can be used:

baux=read.table("bauxite-geo.txt",header=FALSE)

gravi=read.table("gravimetric-mat.txt",header=FALSE); gravi.mat=as.matrix(gravi)

Note: webster-mat.txt contains some missing values indicated by NA. The read.table command in R treats these missing values correctly.


