# Date match project(finalProject report for Class CS5800)
## Introduciton
In this project, we built an algorithm to help a company “cordiance” map categories between 2 files.
- UNSPSC_English.csv is hierarchical, but the fields are messy and non-uniform.
- Avalara_goods_and_services.xlsx, is a well-structured file of goods and services with somewhat uniform fields!
In the algorithm, we came up with 3 iterations in total. For the first iteration, our code generated 624 matches between the Avalara categories and the UNSPSC file, about 15% of those matches are actually correct (96 matches). For the second iteration, our code also generated 624 matches between the Avalara categories and the UNSPSC file, about 16% of those matches are actually correct (103 matches). For the third iteration, our code generated 2474 matches between the Avalara categories and the UNSPSC file; about 30% of those matches are actually correct. 

## Project Learning Objective
- A simple understanding of how to perform data cleaning and data matching
- How to design and apply algorithms for this purpose.

## Tools Applied
- jupyter notebook (Web-based interactive computing platform)
- python (coding language)
- pandas (Library or read and display data)
- Nltk: (Library used when dealing with natural language processing using Python. We used its text processing libraries to generate keywords from a string.)

## Representation:
The entire project is built on Jupiter Notebook, written in Python. We used read_csv and read_excel methods from Pandas library to read the data from both files. After reading two files, we:
-Created a helper function “genKey” to parse input strings and return a clean set of keywords. After running 2 iterations, we manually added some words to be filtered out.
-Created a Node class to represent segment, family, class, and commodity elements. Each Node has 4 fields, number, keyword, child, and name. Number is used to store segment, family, class, or commodity code of an element. Constructor of a node required a number, keyword, and name. Child has a default value of an empty dictionary.
-Created a dictionary, “segments”, to store all segment nodes from the UNSPSC file. Child field of each segment node includes all the family nodes that are in the same segment. Child field of each family node includes all the class nodes that are in the same family. Child field of each class node includes all the commodity nodes that are in the same class. Child field of each commodity node stores the union of keyword sets generated from its segment, family, class, and commodity.

## Actual operation of three Iterations :
### Processor: 
2.3 GHz 8-Core Intel Core i9
### Iterations 1
### Coding
<img width="722" alt="image" src="https://user-images.githubusercontent.com/105685880/206910459-b1dadc2d-9a9a-4122-8cbf-77a23086f29c.png">
### Matching record
<img width="735" alt="image" src="https://user-images.githubusercontent.com/105685880/206885438-1b155d20-12ef-4038-9d28-724173ecba22.png">
### Iterations 2
### Coding
<img width="723" alt="image" src="https://user-images.githubusercontent.com/105685880/206910426-b54516d3-6c09-4994-8821-45b83d0b0836.png">
### Matching record
<img width="760" alt="image" src="https://user-images.githubusercontent.com/105685880/206910405-4d3a15cd-0c9b-426c-951e-aa6c7ecfc1e2.png">
### Iterations 3
### Coding
<img width="724" alt="image" src="https://user-images.githubusercontent.com/105685880/206910358-939c3c73-1eb0-48c8-9e26-980991ffa090.png">
### Matching record
<img width="772" alt="image" src="https://user-images.githubusercontent.com/105685880/206910339-82861370-e87e-4d4a-afb4-b1c9b58b7449.png">


##references:
https://www.nltk.org/
https://www.w3schools.com/python/pandas/pandas_csv.asp


## Authors
- Chun-Wei Tseng
- Gaoxiang Zhang
- Kuan-Tsa Chen

