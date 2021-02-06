# rexams-tutorial

**Introduction**: (overall idea)

This Github repository is intended to be a simple tutorial for using the "exams" package (https://cran.r-project.org/web/packages/exams/) in R to generate files, typically Quiz testbanks, for use in an Learning Management System (LMS) such as Canvas.
 The "exams" package uses .Rmd files to generate the Quiz questions.  The R "exams" package is extensively documented, including examples of many other .Rmd ("Rmarkdown") files or "templates" (http://www.r-exams.org/).

The "exams" package can be installed in R with the usual command:\
```r
install.packages( "exams" )
```

While it is certainly possible to install this package on CRAN as would typically be done with other R packages,
 I recommend using the latest version from the R-forge page (https://r-forge.r-project.org/R/?group_id=1337
) because it always contains the latest (pre-CRAN upload) changes.
 These changes can be particularly important for Canvas.  The development version of the "exams" package is at:\
```r
 install.packages( "exams", repos = "http://R-Forge.R-project.org" )
```

Novices with R, the "exams" package, or Canvas Quizzes can use (learn) these .Rmd files in sequence.
 Advanced users can quickly review the simpler .Rmd files and go directly to the more complex .Rmd files.
 Having many examples helps all users with understanding how these files are created--from simple to complex.

These files are intended to be used in the Canvas LMS.  Use in other LMSs, or as .html. or .pdf files, is possible as well.
 The purpose of using a single LMS is to demonstrate a complete quiz workflow from creating a .Rmd file to "previewing" an exact student view.


**Summary**: (enough to start for power R users)

1. In R, install the "exams" package at:\
https://r-forge.r-project.org/R/?group_id=1337

2. Either create a new .Rmd file or download one of the example .Rmd files on this web site (either copy-and-paste or use the "Raw" button and Save)

3. In R, load the "exams" library and run the following command (make sure you are in the directory with the .Rmd file in it):\
exams2canvas( file = "t01-mult-num-static.Rmd", n = 10, name = "t01-mult-num-static.Rmd" )

4. Import the resulting 't01-mult-num-static.Rmd.zip' file into Canvas as a testbank as you would from a publisher's software tool or Respondus.
 Delete the 't01-mult-num-static' Quiz (you only want the testbank).
 Finally, create a new Question Group in a Quiz and link to this testbank.


**Details**: (step-by-step)

The process for generating a Canvas quiz or testbank is as follows:

1. Have a .Rmd with your Quiz question in it.
    * Either download one of the examples on this web page, or
    * make your own from scratch following an example on this web page.

2. Start "R" on your computer (e.g., usually an "R" icon on your desktop).
    * "R" can be installed from:\
https://cloud.r-project.org/

3. Install the "exams" package (the instructions are at:\
https://r-forge.r-project.org/R/?group_id=1337)
    * This needs to be done just once; however, please know that the "exams" package is updated frequently.

4. Switch to the directory containing your .Rmd quiz file (e.g., 'setwd( "c:\\\exams" )')

5. Load the "exams" library (i.e., 'library( exams )' )

6. Generate your Canvas Quiz/Testbank file (i.e., 'exams2canvas( file = "t01-mult-num-static.Rmd", n = 10, name = "t01-mult-num-static.Rmd" )')
    * This generates a 't01-mult-num-static.zip' file.

7. Import the resulting Quiz/Testbank file into Canvas (i.e., from a Canvas course main page):
    * "Import Existing Content"
    * "Content Type: QTI .zip file"
    * "Source: <select the 't01-mult-num-static.zip' file on your local computer>"
    * "Default Question Bank: -- Create new question bank -- and then enter 't01-mult-num-static.zip' (or any other name you like)"
    * "Import" (wait a few moments for the 't01-mult-num-static.zip' file to be "Uploaded", "Queued", and "Completed")

8. Upon Import completion, Canvas makes both a "Quiz" and a "Testbank".
 You most likely only want the "Testbank"; you can then go to "Quizzes" and delete the new "Quiz" ('t01-mult-num-static.zip').

9. Add a new Quiz or Select an existing Quiz.

10. Select "Edit".

11. Select "Questions".

12. Select "New Question Group".

13. Select "Link to a Question Bank".

14. Select the desired question bank (e.g., 't01-mult-num-static.zip' ) and click "Select Bank'.

15. Select "Save" (or "Save and Publish" if desired).

16. Select "Preview" to see what a student would see (of course, you'll only see one version of the question in the testbank).

17. Select "Create Group".  This creates a Quiz Question that--for each student--will pull one question randomly from the testbank.
    * If 1), the range of the variables in Quiz .Rmd file is high, and 2), the number of versions (the "n" variable in the "exams2canvas" function) in the generated testbank is high enough, it is possible that each student could, in fact, get a unique Quiz Question in Canvas.
    * In general, R users would use the "sample" function to generate continuous or discrete samples or perhaps the "runif" function to generate random variates from a "uniform" distribution.


**.Rmd documentation**: (regarding each .Rmd file)

1. ***t01-mult-num-static.Rmd***
    * genre: multiplicaton, type: numeric, r-code: manually entered numbers, versioning: static

2. ***t02-mult-num-constants-static.Rmd***
    * genre: multiplicaton, type: numeric, r-code: constants, versioning: static

I welcome your feedback.


Enjoy,

Wayne Smith, Ph.D.\
<mailto:wayne.smith@csun.edu>

