---
title: CS50 Final Project Review
date: 2025-06-09
---

Though I've worked on some Python projects in the past, I went through Harvard's CS50 Introduction for Python to get a good foundational understanding and learn some best practices.  I have made it to the final project, to create a Python program with specifications found [here](https://cs50.harvard.edu/python/2022/project/).

The goal for my project was to create a program that gives a user a random Magic the Gathering Commander based on the colors that the user provides.  I was able to create a mostly working product found below in my initial commit to my repo:  https://github.com/thenatepierce/cs50final/commit/fe75ce08e77717068fb7b539da900ede7dcf88d5

That being said, there's a lot of work that I think can be done to improve it (not just including fulfilling the requirements of the assignment).  My current thoughts are the following:

1.  The code needs many more comments to explain what things do.
2.  There is currently a bug in the case that some commanders do not have an EDHRec Rank in Scryfall, so some logic needs to be built in to work with those cases.  Perhaps rather than creating try/excepts for each unique case where errors occur, there's a reasonable way to create a loop for each field I expect, and create a "n/a" or other placeholder string for fields that don't exist in Scryfall or EDHRec.
3.  I currently have the outputs printing in the get_commander_info functions.  I believe for best practices, I should be returning that information to main and have main print that out.  In addition, I think these would better serve as defined classes rather than being large blocks within the function.
4.  I would like to also let the user specify the number of colors that they would like their commander to be, but I think I should be improving the current code rather than adding new.

I hope to have some of these improvements done this week, stay tuned!
