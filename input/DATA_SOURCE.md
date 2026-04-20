---
editor: visual
---

# Data Source Description

We are using from the [High School Longitudinal Study of 2009](<https://nces.ed.gov/surveys/hsls09/>) which surveyed high school freshmen in 2009 and has subsequently followed these students over time with additional follow-up surveys in 2012 and 2016.

From the full data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.qmd quarto document. The name of the dataset in R is `NAME`.

-   **drop_out**: This variable is based on information collected from respondents in the 2016 and prior waves. Students who were ever reported as having dropped out of high school are coded as TRUE on his variable and students who did not drop out are coded as FALSE. Some students who dropped out later returned to complete high school or earned a GED. This is the key dependent variable. You can enter this variable directly into your models as the outcome variable and it will be coded as a 1 or 0 for TRUE or FALSE, respectively. This model is called the "linear probability model" and you can interpret changes in y from the slope to indicate changes in the probability of dropping out.
-   **educ_parent_high**: This variable measures the highest degree earned among both parents (or caregivers when parents are not present) and was measured in the initial 2009 survey. This is the key independent variable.
-   **school_type**: This variable indicates the type of school the student attended in 9th grade which was coded as either public or private. The private school category includes Catholic and other parochial schools. This is the key contextual variable.
-   **school_loc**: This variable indicates the location of the school as either urban, suburban, town, or rural.
-   **family_structure**: This variable indicates the type of family the respondent was living in at the time of the 2009 survey. No distinctions are made between biological and adoptive parents, but step-parent households are distinguished from two-parent households where both parents are biological or adoptive parents.
-   **sex**: The reported sex of the respondent in the baseline 2009 survey.
-   **poverty**: A categorical measure of whether the respondent's household income fell below the official poverty line or not in 2009.
-   **math_score**: A standardized math score from a math test all respondents completed. Higher scores indicate more math proficiency. This variable can proxy for academic performance overall.
