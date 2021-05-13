# Nexus_Wicked-Problems-UNU
A Python and SQL implementation to find patterns in 7000 publication metadata from SCOPUS

This is a part of Wicked Science project from United Nations University - FLORES, Dresden.

We were curious about how the different problem sructure keywords (Wicked, Complex, Uncertain and Conflict) trends with Social Science Dimension (Policy and Governance) in Resource Nexus (Water,Soil, Food, Waste and Energy) around different regions in the world.

We first downloaded the csv data from Scopus using the following keyword combination:

( AUTHKEY ( wicked* )  OR  AUTHKEY ( uncertain* )  OR  AUTHKEY ( complex* )  OR  AUTHKEY ( conflict* )  AND  AUTHKEY ( "Water" )  OR  AUTHKEY ( "Soil" )  OR  AUTHKEY ( "Waste" )  OR  AUTHKEY ( "Energy" )  OR  AUTHKEY ( "Food" )  AND  AUTHKEY ( "Governance" )  OR  AUTHKEY ( "Policy" ) )  OR  ( TITLE ( wicked* )  OR  TITLE ( uncertain* )  OR  TITLE ( complex* )  OR  TITLE ( conflict* )  AND  TITLE ( "Water" )  OR  TITLE ( "Soil" )  OR  TITLE ( "Waste" )  OR  TITLE ( "Energy" )  OR  TITLE ( "Food" )  AND  TITLE ( "Governance" )  OR  TITLE ( "Policy" ) )  OR  ( ABS ( wicked* )  OR  ABS ( uncertain* )  OR  ABS ( complex* )  OR  ABS ( conflict* )  AND  ABS ( "Water" )  OR  ABS ( "Soil" )  OR  ABS ( "Waste" )  OR  ABS ( "Energy" )  OR  ABS ( "Food" )  AND  ABS ( "Governance" )  OR  ABS ( "Policy" ) )  AND  ( LIMIT-TO ( SUBJAREA ,  "SOCI" ) )  AND  ( EXCLUDE ( PUBYEAR ,  2021 ) )  AND  ( LIMIT-TO ( LANGUAGE ,  "English" ) ) 

This Generated a 7041 results!
[image](https://user-images.githubusercontent.com/65511509/118087132-62a76980-b3c5-11eb-8601-adb801c1c70a.png)
