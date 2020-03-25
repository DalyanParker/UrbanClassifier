# UrbanClassifier

UrbanClassifier is a program which gives detailed information regarding population density, for a given pair of latitude and longitude coordinate points.

Its main functionality includes:

1. Calculating total population density for a user specified approximate r x r area in Km squared, for a user specified pair of coordinates
2. Calculating average population density for a user specified approximate r x r area in Km squared, for a user specified pair of coordinates
3. Classification of whether a calcuated total population density, with a given threshold, is Urban.
4. Classification of whether a calcuated average population density, with a given threshold, is Urban.
5. Extracting population density data at resolution of approximatley 1 Km squared (30 secs) for a given pair of coordinates
6. Conversion of coordinate points to meaningful Raster cells

## UrbanClassifierToolkit

The Toolkit contains clearly written code, along with clear commenting and documenting, which comprises the sub process and tasks of the higher level functions.

### urbanByAverage(bound, arr, x, y, r)

The function urbanByAverage, return a boolen, where true indicates that the program has classified the given r x r area's population density average as Urban, based on given parameters.

The function expects as parameters:

1. _bound_ : numeric value, the threshold average which, if the returned calculated population density average is greater than or equal to, will be used to classify this average as Urban
2. _arr_ : the Raster Data encocoded as a multidimensional array - a matrix handled by the program
3. _x_ : longitude
4. _y_ : latitude
5. _r_ : numeric value, will determine the r x r area covered in approximately r x r Km squared

### urbanByTotal(bound, arr, x, y, r)

The function urbanByTotal, return a boolen, where true indicates that the program has classified the given r x r area's population density total as Urban, based on given parameters.

The function expects as parameters:

1. _bound_ : numeric value, the threshold average which, if the returned calculated population density average is greater than or equal to, will be used to classify this average as Urban
2. _arr_ : the Raster Data encocoded as a multidimensional array - a matrix handled by the program
3. _x_ : longitude
4. _y_ : latitude
5. _r_ : numeric value, will determine the r x r area covered in approximately r x r Km squared

## Data

The data used for this program is retrived from https://sedac.ciesin.columbia.edu/data/set/gpw-v4-population-density-rev11.
The toolkit specifically uses the 2020 data, with resolution of approximately 1 Km, specifically:

1. _gpw_v4_population_count_rev11_2020_30_sec.tif_

### Citation

Center for International Earth Science Information Network - CIESIN - Columbia University. 2018. Gridded Population of the World, Version 4 (GPWv4): Population Density, Revision 11. Palisades, NY: NASA Socioeconomic Data and Applications Center (SEDAC). https://doi.org/10.7927/H49C6VHW. Accessed 25 03 2020.
