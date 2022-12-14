# Project "Find the Postcode"

By Netnito1010 - netnito1010@gmail.com

**Intro**

> Consider a situation that we have gotten a data of addresses of companies. We want to send a mail about our new product to each of the company in the list. However, the addresses we have doesn't contain postcode.

The aim of this project is to teach you how to use basic pandas to extract 'Province', 'District', and 'Tambon' from a giving address and use that information to searching for the postcode in the pre-created database.

---

**Table of Contents**

- [Project "Find the Postcode"](#project-find-the-postcode)
  - [What we have and what we need before we begin this project](#what-we-have-and-what-we-need-before-we-begin-this-project)
  - [Project's Outline](#projects-outline)
  - [Project's Step-by-Step Outline](#projects-step-by-step-outline)
    - [0 Setting up](#0-setting-up)
    - [1 Import data](#1-import-data)
    - [2 Check the addresses data](#2-check-the-addresses-data)
    - [3 Have fun with the postcode data](#3-have-fun-with-the-postcode-data)
    - [4 Have fun with the addresses data](#4-have-fun-with-the-addresses-data)
      - [4.1 Clean the address](#41-clean-the-address)

---

## What we have and what we need before we begin this project

nothing. JK. I have provided you the Adresses data which is called *SET_DATA.csv* and the pre-created database of the postcode called *ProCheck.csv*.

## Project's Outline

This is the pseudo code of the project

## Project's Step-by-Step Outline

This is different from the main outline since we will explore the deeper detail of each step and might take some detours to see how each function works

Let's begin

### 0 Setting up

First check that your terminal is in the correct path (the path which you have your main python file and the data)

And don't for get that we are going to use the package **pandas** (as pd)

### 1 Import data

Q1: Import the data

Hint1: Now you should be able to import the data. Let's use the function **pd.read_csv()** (from pandas) to import the data into a variable call **df** and **df_postcode** for SET_Data.csv and ProCheck.csv respectively.

Hint2: Don't forget to specific the path of the data

Q2: Display the header useing head()

Hint2: google "head pandas"

### 2 Check the addresses data

Q1: Count the number of rows in the **df** data.

Hint: google "count row pandas"

Hint2: Don't for get to print it to see the results

Note: There many ways to count the rows and with some specific way it can slightly improve your performance.

### 3 Have fun with the postcode data

Q1: Count the number of rows in the **df_postcode** data

Q2: Count the number of *unique province* in the **df_postcode** data

Hint: First, you need to select the province column which called "Prov". Next, we count the unique value in that column - try google "count unique values pandas"

Q3: Display the data that Prov is "???????????????????????????????????????"

Hint: Use something like df[df["Prov"=="???????????????????????????????????????"]] and display it using *print()* or *display()* to show the dat

Q4: Display the data that Prov is "?????????????????????????????????" *and* Dist is "???????????????????????????"

Hint: Use the similar idea as the provious question

Q5: Print the data that Prov is '???????????????????????????????????????', Dist is '??????????????????', and Tamb = '?????????????????????????????????'

Hint: Use the similar idea as the provious question

Q6: Show the post code of when Prov is '???????????????????????????????????????', Dist is '??????????????????', and Tamb = '?????????????????????????????????'

Hint: Try using *iloc* or *at* funtion to the first row of the table. Then select the PostCode column and print the value.

Hint2: try google 'iloc pandas' and 'print specific cell pandas'

Note: Without using *iloc* or *at* the data we get is *dataFrame* opject which is not the value in the cell. If you want to use just the value in that cell we need to use *iloc* or *at*.

### 4 Have fun with the addresses data

Here we will deal with the first few rows of the data then we use for loop to apply the idea to the whole data.

Q1: Store the column 'Location' of the data in

Q2: Store the first few row of data in **df_location_head**

Hint: You might need to use something like *df.head()*

Q3: Display the data and check the pattern

One might notice that the Province is always the last word in the address. The seccond last is District and the third last is Tambon. Therefore, we will use this information to extract the data we need.

#### 4.1 Clean the address

Before we split the data we need to clean it first.

Task1: Replace '?????????.' with '???????????????????????????????????????'

Later, we will compare the province to the database and in the database Bangkok is refered as '???????????????????????????????????????'.

Task2: Remove '???????????????', '????????????', '???.', and '???.'

Again, in the database we don't have the word '???????????????', '????????????', '???.', and '???.', therefore we don't need it.

Task3: Split the data and store the province, district, and tambon in a new database called **df2**
