---
layout: post
author: Sandra Sawchuk
description: A tutorial that matches a shelf list with Library of Congress classifications to understand a subject-specific library collection.
category: tutorials
keywords: |
    Library of Congress classification, Excel, tutorial, libraries, digital humanities, shelf list
title: Collection Mapping with Excel -- Determining LOC classification based on call number
permalink: /collection-mapping/
---

This tutorial matches call number data from a shelf list to the respective Library of Congress subject classifications in order to calculate the number of books in each LOC subclass.

[![L subclass general numbers](/assets/images/lc-l-subclass-general.png "General L subclass counts")](/assets/images/lc-l-subclass-general.png)	|[![L subclass detailed numbers](/assets/images/lc-l-subclass-detail.png "Detailed L subclass counts")](/assets/images/lc-l-subclass-detail.png)
:--------------------------:|:--------------------------:
*general L subclass counts*	| *detailed L subclass counts*

This information may help in making decisions about acquisitions or weeding. Right now, the only data available in this tutorial is for [Class L: Education](https://www.loc.gov/catdir/cpso/lcco/), but with the Excel tips in this tutorial, the other classes can be done with a bit of extra work. And as I branch out, I will post templates with other classes.

<p class="lead">This tutorial assumes that you have access to a shelf list.</p> This shelf list is preferably in a `.txt, .csv, or .xlsx` format. Depending on how things work at your institution, you may be able to obtain this list from your collections librarian, your systems librarian, or your library/institution IT people. Depending on the discovery layer you use, you may have to contact the vendor. Keep asking!

Aside from the shelf list file, you will require the following files, which can be downloaded from the [GitHub repository](https://github.com/mediagestalt/collection-mapping):

- Library of Congress Class L: Education excel file
	- other classes will be available as I create them, for now this can be a template if you need something other than L
- Shelf list template file
	- the exact information contained in your shelf list is impossible for me to predict. This file is meant only to be a template for the Excel formulas you will need to complete this project.

-----

<p class="larger">TASKS</p>

* TOC
{:toc}

-----

## Step 1: Preparing the shelf list

__Save a master copy!__ Before you make any changes to your shelf list, save a copy with the word 'master' in the filename and put it somewhere safe. If something goes wrong with the working copy of the file, whether it's a mistake or something gets corrupted, you can always make another copy of the master file and start again. This is just good practice for any data manipulation projects. I called my files `master-shelflist-november-2017` and `working-shelflist-november-2017`.

Much like any other project that involves external data, you'll need to do a bit of cleanup to your shelf list to prepare it for analysis. Delete any unnecessary columns, such as ones that list due dates, or information that you won't require for your analysis.

## Step 2: Using the Excel formulas

## Step 3: Cleaning the data

After you pull down the formulas to split the call numbers apart, you'll need to check the `callNumberAlpha` column for outliers. For example, in my shelf list, some of the original call numbers did not have a space between the first letters and the numbers. The formula we used assumes a space, so any call number without a space won't be parsed correctly. Your shelf list may also have some catalogued items that aren't reading material. My list had several instances like `CARREL #44 XF1121`, which were codes for library carrel keys for students to reserve or check out.

The easiest way to do this is to use the `filter` function in Excel.

[![Call number outliers](/assets/images/call-number-filter-outlier.png "Call number outliers")](/assets/images/call-number-filter-outlier.png)| [![Call number outliers](/assets/images/call-number-filter-outlier-1.png "Call number outliers")](/assets/images/call-number-filter-outlier-1.png)
:---------------------:|:--:
*filtering outliers* | *these aren't books!*
