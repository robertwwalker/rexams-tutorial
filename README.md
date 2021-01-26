# rexams-tutorial

**Summary**: (enough to start)

This Github page is intended to be a simple tutorial for using the "exams" package in R to generate files, typically testbanks, for use in Canvas.

These .Rmd (Rmarkdown) files are to be used with the "exams" R package:\
https://r-forge.r-project.org/R/?group_id=1337

While it is certainly possible to install this package on CRAN as would typically be done with other R packages,
 I recommend using the latest version from the R-forge page above because it always contains the latest (pre-CRAN upload) changes.
 These changes can be particularly important for Canvas.

These .Rmd files are intended to be used (learned) in sequence.  This helps with understanding how these files are created--from simple to complex.

In general, these files are intended to be used in the Canvas LMS.  Use in other LMSs, or as .html. or .pdf files, is quite possible as well.

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

6. Generate your Canvas Quiz/Testbank file (i.e., 'exams2canvas( file = "01-mult-num-static.Rmd", n = 1, name = "01-mult-num-static.Rmd" )')
    * This generates a .zip file.

7. Import the resulting Quiz/Testbank file into Canvas (i.e., from a Canvas course main page):
    * "Import Existing Content"
    * "Content Type: QTI .zip file"
    * "Source: <select your Quiz/Testbank file on your local computer>"
    * "Default Question Bank: -- Create new question bank --" and then enter <the name of your testbank file>
    * "Import" (wait a few moments for the file to be uploaded, queued, and completed)

8. Canvas makes both a "Quiz" and a "Testbank".  You most likely only want the "Testbank"; you can then go to "Quizzes" and delete the new "Quiz".

9. Add a new Quiz or Select an existing Quiz.

10. Select "Edit".

11. Select "Questions".

12. Select "New Question Group".

13. Select "Link to a Question Bank".

14. Select the desired question bank (e.g., "01-mult-num-static.Rmd" ) and click "Select Bank'.

15. Select the desired question bank (e.g., "01-mult-num-static.Rmd" ) and click "Select Bank'.

16. Select "Create Group".  This creates a Quiz Question that--for each student--will pull one question randomly from the testbank.
    * If 1), the range of the variables in Quiz .Rmd file is high, and 2), the number of versions in the generated testbank is higher enough, it is possible that each student could, in fact, get a unique Quiz Question in Canvas.


**Details**: (regarding each .Rmd file)

1. ***01-mult-num-static.Rmd***
    * genre: multiplicaton, type: numeric, versioning: static

I welcome your feedback.


Enjoy,

Wayne Smith, Ph.D.\
<mailto:wayne.smith@csun.edu>

