# Nexus_Wicked-Problems-UNU
A Python and SQL implementation to find patterns in 7000 publication metadata from SCOPUS

This is a part of Wicked Science project from United Nations University - FLORES, Dresden.

We were curious about how the different problem sructure keywords (Wicked, Complex, Uncertain and Conflict) trends with Social Science Dimension (Policy and Governance) in Resource Nexus (Water,Soil, Food, Waste and Energy) around different regions in the world.

We first downloaded the csv data from Scopus using the following keyword combination:

( AUTHKEY ( wicked* )  OR  AUTHKEY ( uncertain* )  OR  AUTHKEY ( complex* )  OR  AUTHKEY ( conflict* )  AND  AUTHKEY ( "Water" )  OR  AUTHKEY ( "Soil" )  OR  AUTHKEY ( "Waste" )  OR  AUTHKEY ( "Energy" )  OR  AUTHKEY ( "Food" )  AND  AUTHKEY ( "Governance" )  OR  AUTHKEY ( "Policy" ) )  OR  ( TITLE ( wicked* )  OR  TITLE ( uncertain* )  OR  TITLE ( complex* )  OR  TITLE ( conflict* )  AND  TITLE ( "Water" )  OR  TITLE ( "Soil" )  OR  TITLE ( "Waste" )  OR  TITLE ( "Energy" )  OR  TITLE ( "Food" )  AND  TITLE ( "Governance" )  OR  TITLE ( "Policy" ) )  OR  ( ABS ( wicked* )  OR  ABS ( uncertain* )  OR  ABS ( complex* )  OR  ABS ( conflict* )  AND  ABS ( "Water" )  OR  ABS ( "Soil" )  OR  ABS ( "Waste" )  OR  ABS ( "Energy" )  OR  ABS ( "Food" )  AND  ABS ( "Governance" )  OR  ABS ( "Policy" ) )  AND  ( LIMIT-TO ( SUBJAREA ,  "SOCI" ) )  AND  ( EXCLUDE ( PUBYEAR ,  2021 ) )  AND  ( LIMIT-TO ( LANGUAGE ,  "English" ) ) 

This Generated a 7041 results!
[image](https://user-images.githubusercontent.com/65511509/118087132-62a76980-b3c5-11eb-8601-adb801c1c70a.png)

We download the following data
![image](https://user-images.githubusercontent.com/65511509/118087317-a7330500-b3c5-11eb-9bdb-ec40128d8d5e.png)

However we mostly need the author name, author keywords, title, abstract and their affiliation. Scopus allows only data of 2000 at a time thus the data was downloaded in 4 year wise chunks
1. 1953-2010.csv
2. 2011-2014.csv
3. 2015-2017.csv
4. 2018-2010.csv
A python joiner was built using pandas framework to join the files
The joined file is named as:
1953-2020.csv
1953-2020.xlsx

assign an index and outputting a csv file for pattern matching in SQL

**SQL Pattern Matching**
![Structure](https://user-images.githubusercontent.com/65511509/118099074-08160980-b3d5-11eb-8e43-9286d8b67291.jpg)

the pattern matching in intended to find cooccurance or the intersections of the keywords of Problem Structure, Social Science Dimensions and Resource Nexus.
Problem Structure:
1. Wicked
2. Conflict
3. Complex
4. Uncertain

Social Science Dimensions: 

1. Governance
2. Policy


Resource Nexus

1.Water
2.Soil
3.Food
4.Energy
5.Waste

The details of column creation, pattern matching codes, formulas are listed in this [file](https://drive.google.com/file/d/1IsdevgmWRnhcy74gdfrgNDUMmVd-oWtR/view?usp=sharing "Google_sheet")

