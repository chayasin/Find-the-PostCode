# Project "Find the Postcode"

By Netnito1010 - netnito1010@gmail.com

*Intro*

> Consider a situation that we have gotten a data of addresses of companies. We want to send a mail about our new product to each of the company in the list. However, the addresses we have doesn't contain postcode.

The aim of this project is to teach you how to use basic pandas to extract 'Province', 'District', and 'Tambon' from a giving address and use that information to searching for the postcode in the pre-created database.

---

*Table of Contents*

- [Project "Find the Postcode"](#project-find-the-postcode)
  - [What we have and what we need before we begin this project](#what-we-have-and-what-we-need-before-we-begin-this-project)
  - [Project's Outline](#projects-outline)
  - [Project's Step-by-Step Outline](#projects-step-by-step-outline)
    - [0 Setting up](#0-setting-up)
    - [1 Import data](#1-import-data)
    - [2 Check the addresses data](#2-check-the-addresses-data)
    - [3 Have fun with the postcode data](#3-have-fun-with-the-postcode-data)
    - [4 Have fun with the addresses data](#4-have-fun-with-the-addresses-data)

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

Q3: Display the data that Prov is "กรุงเทพมหานคร"

Hint: Use something like df[df["Prov"=="กรุงเทพมหานคร"]] and display it using *print()* or *display()* to show the dat

Q4: Display the data that Prov is "สมุทรปราการ" *and* Dist is "พระประแดง"

Hint: Use the similar idea as the provious question

Q5: Print the data that Prov is 'กรุงเทพมหานคร', Dist is 'พระนคร', and Tamb = 'วัดสามพระยา'

Hint: Use the similar idea as the provious question

Q6: Show the post code of when Prov is 'กรุงเทพมหานคร', Dist is 'พระนคร', and Tamb = 'วัดสามพระยา'

Hint: Try using *iloc* or *at* funtion to the first row of the table. Then select the PostCode column and print the value.

Hint2: try google 'iloc pandas' and 'print specific cell pandas'

Note: Without using *iloc* or *at* the data we get is *dataFrame* opject which is not the value in the cell. If you want to use just the value in that cell we need to use *iloc* or *at*.

### 4 Have fun with the addresses data

Here wee will deal with the first row of the data first then we use for loop to apply the idea to the whole data.

Q1:
