# Data for Data Science 
# Class 1: Data entry and creating spreadsheets

At the end of this course,
you should be able to apply some best practices in data management to your current research projects,
and plan ahead to improve your future projects. 

A bigger picture of the data lifecycle
Data is valuable, and often includes the interest of many stakeholders.
It may not be possible to incorporate best practices for long-running projects that are nearing completion. 
Understanding best practices will help you identify which areas you can improve, and how to plan better for the future.

> Note about many choices around data management may have been already decided by your lab or manager,
> and how to use the information here to improve processes when you can and understand the limitations when you can't change them

## What is data management?

organize, manage, and track scientific data

Key terms:
- data
- scientific data
- metadata

## Why learn about data management?

- scientific research is increasingly data-driven
- few researchers are adequately trained 
- an understand of best practices in data management can help you save time, energy, and frustration later

image: books of human genome


By the end of this class, you should be able to:
- implement best practices in data table formatting
- identify and address common formatting mistakes
- understand approaches for handling dates in spreadsheets
- effectively export data from spreadsheet programs

Understanding best practices for data entry and formatting is foundational to other issues in data management

## Why spreadsheets?

Biological data is often represented as text

image: DNA sequences

Data as text can be interpreted by both humans and computers, although not always as easily for both

Spreadsheets provide a useful, familiar structure for working with tabular data (organized in rows and columns).
Spreadsheet programs (like Microsoft Excel and LibreOffice/OpenOffice) allow us to view these data in a comprehensible way.

> #### Challenge-Spreadsheet issues 
> What are some limitations of spreadsheets? 
> Have you ever had a frustrating experience with a spreadsheet program?

## Organizing data in spreadsheets

Spreadsheets are a great way to enter and organize data, 
because it allows us to see and understand how data have been formatted,
with information appearing in rows and columns,
often with column headers including important descriptive information.

| experiment | sex | weight_g | treatment |
| --- | --- | --- | --- |
| 4 | F | 41 | control |
| 3 | F | 37 | control |
| 4 | F | 117 | insulin |
| 3 | F | 121 | insulin |
| 2 | M | 115 | insulin |

Spreadsheets (e.g., MS Excel files) are not an acceptable way of formatting data for many computer programs, 
so it is necessary to convert them to a different format.

some of their features and the habits we develop through using them can make it difficult to perform data science tasks with these same data later.

Our goal is to have data entered in a way that we can easily export in a plain-text format that is straightforward for other programs to interpret

```text
experiment,sex,weight_g,treatment
4,F,41,control
3,F,37,control
4,F,117,insulin
3,F,121,insulin
2,M,115,insulin
```

Tidy data
Each cell should represent a single value (piece of data)
Rows represent individual observations (samples, patients, etc)
Columns represent variables (information about each observation)
variables
observation
value

If you have data that need to be organized, keep the following guidelines in mind:
- Keep the original data unaltered 
- Create a new spreadsheet to hold the reformatted data
- List the steps taken while reformatting in another spreadsheet
- Export the final (reformatted) spreadsheet as a text file

> #### Challenge-Spreadsheet organization
> Using experimental_data.xlsx, put the data from the 2013 and 2014 tabs into the same table.

## Common spreadsheet errors  

- Multiple tables appearing in the same sheet

- Related data split among multiple sheets/tabs

- Inconsistent use of zeros versus missing data (null/blank values)
    - Zero (0) can represent observed data
    - Does a blank cell indicate no data was collected, or an error in data entry?
    - If all cells must have data, what symbol represents missing values?

- Using formatting to convey information

- Formatting the spreadsheet to make the table easier to read
    - Merging and splitting cells 
    - Including empty rows or columns

- Including comments or units in cells

- Including more than one piece of data in a single cell

- Using special characters in data tables, as these can have unintended consequences during data analysis later 
- 
```text
! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ ` { | } ~
```
New lines, spaces, tabs, and vertical tabs 

- Problematic field names (row and column labels): Avoid spaces: use underscores (or dashes, or capitalization)

- Including metadata in a data file: Metadata (data about data, e.g., descriptions of what variables represent) should go in a separate file

- Unclear formatting of dates as data
  - Spreadsheet programs include features that allow manipulation of dates, 
which can accidentally introduce ambiguity or conversion errors
  - Recommendation: store year, month, and day as separate columns
  - The International Organization for Standardization (ISO) also has a format (ISO 8601) for dates and time

- Including calculations and/or figures in data file

## Exporting data as a text file

Spreadsheet programs do a lot more than help us organize data, and those things may interfere with long-term data stability and interpretation.
Export your data from a spreadsheet program to plain text file, which is universal, open, and static (meaning more stable and accessible)

```text
experiment,sex,weight_g,treatment
4,F,41,control
3,F,37,control
4,F,117,insulin
3,F,121,insulin
2,M,115,insulin
```

You can save your data as a text file using the “Save as” command in a spreadsheet program.
Common formats are .tsv (tab separated values) and .csv (comma separated values); 
they are differentiated by the character that separates the columns on each line 
(there are other options as well, but these are most common)

An example of `csv` format:

```text
experiment,sex,weight_g,treatment
4,F,41,control
3,F,37,control
4,F,117,insulin
3,F,121,insulin
2,M,115,insulin
```

The same data as above in `tsv` format:

```text
experiment	sex	weight_g	treatment
4	F	41	control
3	F	37	control
4	F	117	insulin
3	F	121	insulin
2	M	115	insulin
```

These files can still be opened by spreadsheet programs!

A bigger picture of the data lifecycle:
- Data is valuable, and often includes the interest of many stakeholders.
- It may not be possible to incorporate best practices for long-running projects that are nearing completion. 
- Understanding best practices will help you identify which areas you can improve, and how to plan better for the future.

## Wrapping up

Spreadsheets are a great way to enter and organize data, and can be used to apply tidy data principles.
Take care to avoid common errors associated with data organization and formatting in spreadsheets to make your life easier when it’s time to analyze data.
Saving your data files as `.csv` or `.tsv` makes your data more stable and accessible.



Next time: organizing data files 

- These materials are adapted from content originally appearing in [Data Organization in Spreadsheets for Ecologists](https://datacarpentry.org/spreadsheet-ecology-lesson/) Copyright (c) Data Carpentry.
- [Tidy Data](https://vita.had.co.nz/papers/tidy-data.pdf) by Hadley Wickham
- [Spreadsheet Help](http://cdluc3.github.io/spreadsheet-help/) from California Digital Libraries
