# datafun-04-notebooks Assignment

# _Jupyter Notebooks and DataFrames_

In this assignment, you'll explore the Jupyter environment and notebooks - a web-based approach that combines code with formatted text and automatic display of results. We'll look at tools for working with one-dimensional and two-dimensional data. We'll explore the string class and let you know that regular expressions exist to help us identify and parse elements of text (e.g. a phone number or web address).

# Chapters

- Read and work through the Jupyter intro in Ch 1.10.3.
- Read and work through the book and examples from Chapters 7 and 8.
- Focus especially on 7.14.2 pandas DataFrames.

# Additional Reading

- [Markdown](https://nwmissouri.instructure.com/courses/50814/pages/markdown?wrap=1)
- [Project Jupyter (Official Website)Links to an external site.](https://jupyter.org/)
- [TryLinks to an external site.](https://jupyter.org/try)
- [DocumentationLinks to an external site.](https://docs.jupyter.org/)

# Installations

The Python standard library is no longer enough - now we need to download and install some powerful, industry-standard modules for data analytics.

Jupyter especially takes a bit of extra setup.

1. Follow (or confirm you already have followed) the instructions here: [https://github.com/denisecase/datafun-01-textbook/blob/main/UPDATED\_SETUP.mdLinks to an external site.](https://github.com/denisecase/datafun-01-textbook/blob/main/UPDATED_SETUP.md)
2. Read and follow these instructions next: [https://github.com/denisecase/datafun-01-textbook/blob/main/RUN\_ALL.mdLinks to an external site.](https://github.com/denisecase/datafun-01-textbook/blob/main/RUN_ALL.md)
3. You won't need ALL of those modules installed - once you know how to install them, you can get them as needed.
4. Being able to install packages/modules into your standard environment is a critical skill.
5. If using conda, try to install from the conda-forge channel.
6. If the module you need isn't available from conda-forge install it _using the pip in your conda module._

# Notebooks in VS Code - or Just the Browser?

- Browser: Some analysts work with Jupyter right in their browser. There's more space and we get some benefits of an IDE.
- VS Code: Some analysts work with Jupyter notebooks from within VS Code. On a smaller laptop screen, it can be a bit crowded, but it has benefits.
- Try them both - maybe discuss in the forum which is generally preferred.

# Start Jupyter

- Once Jupyter has been installed into your active environment, start it up by following the instructions in the book Ch 1.10.3:
- In Terminal (Mac) or Anaconda Prompt (Windows), run jupyter lab.

For more instructions, see:

- [https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.htmlLinks to an external site.](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.html)

Get it running both inside VS Code - and without VS Code - so you can make an informed choice on your preference.

Sometimes, getting it started is the hardest part. Once you get Jupyter up and running celebrate a bit - this a great environment for exploring and presenting analytics.

# Task 0 - get started

1. Log in to your GitHub account.
2. Create a new GitHub repo named datafun-04-notebooks.
3. Git clone your new repo into your Documents folder.
4. Ensure your repo has the 3 basic files all our repos need:
 1. A good README.md,
 2. .gitignore, and
 3. about.py.
5. Copy these from previous repos as needed.
6. Update README.md to reflect the focus of this module.
7. Add new files to your repo as described below.
8. Git add, git commit, and git push (commit/sync in VS Code) your updated content to GitHub.

Authors examples: You're encouraged to use the authors examples for practice. Use these right from your local IntroToPython directory - don't commit the author's work into your repo.

# Task 1 - yourname\_1.ipynb

1. Start the Jupyter environment on your machine from your Documents folder.
2. Use the navigation window to get to your repo for this module.
3. In your repo, create a new notebook in Jupyter (name the file yourname\_1.ipynb ), so mine might be denisecase\_1.ipynb.
4. Research how to add Markdown to a Jupyter notebook.
5. At the top of your new notebook, change the first cell from Python to Markdown.
6. Add your name as a top-level heading in Markdown at the top of the file (hint: # Denise Case's Module 4 Project)
7. In the next cell of your notebook, change back to Python code.

Use the text, do a search, find a video, and/or use the forum to share resources for getting acquainted with notebooks. We won't duplicate those resources here.

Add a Markdown cell for each section heading.

## Task 1 - Series

1. We'll look at using a one-dimensional pandas Series to hold and process simple exam data.
2. Follow the instructions in 7.14 to import the pandas module (as pd).
3. Create a pandas Series named grades from a list of integers (exam scores).
4. Get the value of the first grade with grades[0].
5. Call the built in Series functions: count(), mean(), min(), max(), std(), and describe().

## Task 2 - Series from Dictionary

1. Follow the instructions in the "Dictionary Initializers' subsection to modify your code to initialize grades with a dictionary (a set of key-value pairs instead) - we'll use the student name as the key and their exam score as the value.
2. Get Eva's score by calling grades['Eva']
3. Get Wally's score using the easier dot notation: grades.Wally. This is much more common and can be used as long as there are NO spaces in the key text. If there are spaces, you'll have to use the approach we used for Eva above - wrapping the key in single quotes.
4. Use the Series values attribute to display the array of values.
5. Complete the self-check on Page 266.
6. We can use a Series whenever our values are a simple one-dimensional array.
7. Make sure the notebook is nicely formatted with a heading and sections in Markdown clearly dividing the work.

Run the entire file and export the results to yourname\_1.html. This will display your calculated results.

# Task 2 - yourname\_2.ipynb

1. See the text Ch 7.14.2.
2. For more complex data, we can use a DataFrame. In a DataFrame, each value is a Series of numbers.
3. We can use a two-dimensional DataFrame to handle many exam scores for each key/student.
4. Create a new notebook to practice using DataFrames.
5. Name the notebook yourname\_2.ipynb.
6. Use your Markdown skills to add a customized title to your notebook.
7. Use Markdown heading for each section below.

## Task 1. Create DataFrame

1. Follow the instructions in 7.14.2 to import pandas as pd and create a pandas DataFrame from a dictionary (a set of key-value pairs) holding multiple exam scores for each key/student. In this example, we have 5 students, each with 3 exam scores, but the scores aren't labeled.

## Task 2. Custom Index

1. Follow the instructions to apply a custom index (instead of 0,1,2), let's call them 'Test1', Test2', and 'Test3'. See 'Customizing a DataFrame's Indices with the index Attribute subsection.
2. As we did in Part 1, we can request grades by key using the text attribute (square brackets with single quoted text strings). Find Eva's grades with grades['Eva']
3. If no spaces in the key, we can use the simpler dot attribute approach. Find Sam's grades with grades.Sam as shown in 'Accessing a DataFrame's columns' subsection.

## Task 3. Accessing Rows (loc, iloc)

1. Like spreadsheets, we can access specific rows or columns.
2. We use loc ['ColA'] and iloc [i] to access rows by name and index, respectively.
3. Execute the examples using loc['Test1'] to get scores for the first exam, or iLoc[0] to get scores for the first exam and iLoc[1] to get scores for the second exam. Which do you prefer?
4. We can also get slices of rows, e.g., from ['Test1':'Test3'], inclusive, or, using index values, from [0:2], inclusive.

## Task 3. Accessing Subsets (at, iat)

1. We can use similar notation to get a single cell in the DataFrame (much like getting a single cell in a spreadsheet).
2. Use [grades.at](http://grades.at/)['Test2', 'Eva'} to find her score on the second exam using labels.
3. Use grades.iat[2,0] to get the score on the third exam for the first student (Wally), using indices.

## Task 4. Describe (By Column)

1. Use grades.describe() to get descriptive statistics for our gradebook columns.
2. See why learning Python and DataFrames can be so powerful?
3. Try to set the precision using the pd.set\_option('precision',2) provided.
4. Does it work? Libraries are evolving. If you get an error, copy the error text and do a web search.
5. Can you find something about a newer option using "_display.precision"?_
6. If so, try pd.set\_option("display.precision",2).
7. Being able to debug evolving features on your own is important for success.
8. Our field, languages, and libraries are constantly evolving.

## Task 5. Transpose (rows \<--\> columns)

1. Get the average for each column by calling grades.mean()
2. Transpose the DataFrame using the T attribute.
3. Get the mean by the new columns with .T.describe()

## Task 6. Sort

1. Sort the gradebook rows in reverse order so the most recent exam row appears at the top with grades.sort\_index(ascending=False)
2. Sort the gradebook columns so the names appear in order using grades.sort\_index(axis=1).
3. We can sort our data pretty much however we like.

Make sure the notebook is nicely formatted with a heading and sections in Markdown clearly dividing the work.

Run the entire file and export the results to yourname\_2.html. This will display your calculated results.

Minimal submissions earn minimal credit. Repos clearly demonstrating practice, in an organized fashion, with custom notes and remarks are eligible for maximum credit.

# Task 3. Push Repo to GitHub

Your repo should at least the 3 basic files. 2 notebooks, and 2 exported html files.

Use VS Code to commit and sync (push) your repo to GitHub - or in Git Bash or terminal, do the following.

git add .
 git commit -m "added code"
 git push origin main

# Task 4. Read about String Methods

1. String methods are helpful for processing text.
2. For now, in 8.9, read "Joining Strings" on page 295 carefully.
 1. string.join() is an important and widely used method when working with text.
 2. The string holds the separator and we pass one argument to the join() method - a list, or a list comprehension.
3. Get an idea of what's possible with strings and string methods.
4. In 8.11, read about raw strings (with an r instead of an f in front).
5. In 8.12, read about regular expressions - a powerful way to locate specific elements of text (e.g. a phone number).
6. We'll do more with strings and text in Web Mining and NLP.
7. If you want some practice now, try the bonus.

# Optional Task 5 (Bonus).

1. Raw data is rarely ready for use.
2. Data preparation can be about 75% (or more) of our work.
3. Work through Ch 8.13 to get an idea of wrangling (cleaning & transforming) data.
4. On your machine, in your repo, create an additional notebook named xtra\_p4.ipynb.
5. Start by creating the list of contacts in "Reformatting your Data" on page 310.
6. Create a DataFrame.
7. The phone numbers are not formatted.
8. Follow the text to create a function that uses regular expressions (usually abbreviated regex or re) to create a function to get a formatted version of the unformatted phone number.
9. Use map() and your function to improve the DataFrame
10. Verify phone numbers now appear with two dashes (e.g., 555-555-5555).
11. Prepare your notebook with a nice header (include a title, your name, and date)
12. Clearly label your steps and result.
13. Execute the entire notebook, export it to xtra\_p4.html.
14. Commit and push both files into your GitHub repo.

# Reflection (on your own)

Notebooks and scripts are both important.

- Scripts for automated, unattended processes (e.g. fetch a file with daily sales).
- Scripts for reusable functions so the module can be imported.
- Notebooks for initial data exploration - it makes it easy to add visualizations and remarks to your analysis.

DataFrames and Series are widely used.

Can you think of something in your domain (or at work or in a personal project) that would be good for either a DataFrame or a Series? Would it be better as a script/module or as a notebook?

# Submission Instructions

1. [Project Submission Instructions](https://nwmissouri.instructure.com/courses/50814/pages/project-submission-instructions?wrap=1)

# Submit

# Part 1 - Project

1. Paste a clickable link to your public GitHub repo:
2. Your domain:
3. About how long did you spend on class this module:
4. In general, how did it go:
5. What was the most difficult part:
6. What was most interesting:
7. Did you do the optional bonus (y/n). How did it go - or why not?

Part 2 - Self Assessment

From the Module Overview, paste the numbered list of objectives and assess your ability on each as "Highly proficient", "Proficient", or "Not Proficient":

# Reference

1. Remember to explore the code examples and check our FAQ (in Module 0).
2. Read and use the text.
3. Try to resolve issues independently (using the text and a web search).
4. Share technical questions and suggestions in this module's discussion forum.
5. Emails should be for personal things rather than technical questions.
6. If you have a personal issue, be sure to use the correct email subject line (see the syllabus for details).

# Checklist

- [x] Chapters
- [x] Additional Reading
- [x] Installations
- [x] Notebooks in VS Code - or Just the Browser?
- [x] Start Jupyter
- [x] Task 0 - get started
- [x] Task 1 - yourname\_1.ipynb
- [x]   Task 1 - Series
- [x]   Task 2 - Series from Dictionary
- [x] Task 2 - yourname\_2.ipynb
- [x]   Task 1. Create DataFrame
- [x]   Task 2. Custom Index
- [x]   Task 3. Accessing Rows (loc, iloc)
- [x]   Task 3. Accessing Subsets (at, iat)
- [x]   Task 4. Describe (By Column)
- [x]   Task 5. Transpose (rows \<--\> columns)
- [x]   Task 6. Sort
- [x] Task 3. Push Repo to GitHub
- [x] Task 4. Read about String Methods
- [x] Optional Task 5 (Bonus)
- [x] Reflection (on your own)
- [x] Submission Instructions
- [x] Submit
- [x] Part 1 - Project
- [x] Part 2 - Self Assessment
- [x] Reference