# Assignment: Questionnaire Design and Sample Evaluation

## Requirements

The goal of this assignment is to practice developing and evaluating sampling materials.

### Part A - Survey Design:

Select one of the scenarios below and design a survey to meet the need(s) outlined in the prompt.

1.	In two to three sentences, describe the purpose of your survey
2.	Describe your target population, sampling frame, sampling units, and overall sampling strategy.
3.	Write a 5-10 question survey to address your chosen scenario below.

##### Scenarios
1.	You work in the Human Resources Department at a large tech company. Over the past few months, the company has been experiencing a high turnover rate across many of its departments, specifically within the entry- and lower-level positions. The company wishes to understand why this turnover is happening, and what changes need to occur to improve employee satisfaction.
2.	You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
3.	You are a student researcher in the sociology department at the University of Toronto. You are working on a research project that concerns the relationship between music taste and age. This involves both comparisons between different people of different ages and comparisons of the same individual at different ages during their lifetime. You wish to understand to what extent age influences music taste, specifically as it relates to perceptions of popular music. Your results will be written into an academic paper that you hope to publish.

### Part B - Survey Evaluation:

For the **Canadian General Social Survey on Giving, Volunteering, and Participating, 2018 (cycle 33)**, conducted by Statistics Canada find any and all available documentation for the data gathered and identify and describe the survey features indicated below.

1. Sample type
2. Sample size
3. Target population
4. Sampling frame
5. Survey mode(s) 
6. Timeline
7. Response rate
8. Weights
9. Data processing
10. Cleaning, imputation, etc
11. Sources of error
12. Limitations, known biases, etc
13. Link to documentation and any additional sources used


# Your Changes

## Part A - Survey Design: 

The number of your chosen topic: `#`

Describe the purpose of your survey:
```
The purpose of the survey is to identify areas of early employee dissatisfcation. Key
areas of potential dissatisfcation which are being probed are commute times, training, 
workloads, and overall workplace culture.  
```

Describe your target population, sampling frame, sampling units, and observational units:
```
Target population: All current employees at the company.
Sampling frame: Registry of current employees.
Sampling units: Current employees.
Observational units: All current employees.

Sampling strategy: From the registry of all current employees, stratify the population by 
number of years worked at the company with blocks of 
- less than 1 year
- between 1 and 2 years
- between 2 and 5 years
- more than 5 years
We then take a random sample from each stratum via proportional allocation. The selected employees
will then be sent an email via a third party so that they can fill out the survey anonymously.

```

Your 5-10 question survey:
```
For each of the 10 questions listed below, please answer each question as best you can.
Your responses will be kept anonymous and your employer will not know if you filled out
the survey. You can decline to answer any question.

1. Estimate the number of months you have worked for the company

        [NUMERIC ENTRY BOX]


2. On a scale from 1 to 10, how satisfied are you working for the company overall?
 A score of 1 indicates you are very dissatisfied and a score of 10 indicates you 
 are completely satisfied. Select only one answer.

    (1)   (2)   (3)   (4)   (5)   (6)   (7)   (8)   (9)   (10)
 

3. Do you work remotely?

    YES         NO


4. If your answer to Question 3 was NO, estimate the number of hours you commute
each work day

        [NUMERIC ENTRY BOX]


5. Estimate the number of hours you work each week.

        [NUMERIC ENTRY BOX]


For Questions 6 - 10, circle the level of agreement you have with each statement. 

6. "I have been adequately prepared for the tasks the company asks me to complete"

(COMPLETELY DISAGREE)   (SOMEWHAT DISAGREE)     (NEUTRAL)   (SOMEWHAT AGREE)    (COMPLETELY AGREE)


7. "I can easily communicate with my coworkers,"

(COMPLETELY DISAGREE)   (SOMEWHAT DISAGREE)     (NEUTRAL)   (SOMEWHAT AGREE)    (COMPLETELY AGREE)


8. "My coworkers treat me respectfully."

(COMPLETELY DISAGREE)   (SOMEWHAT DISAGREE)     (NEUTRAL)   (SOMEWHAT AGREE)    (COMPLETELY AGREE)


9. "My supervisor has clear expectations for me."

(COMPLETELY DISAGREE)   (SOMEWHAT DISAGREE)     (NEUTRAL)   (SOMEWHAT AGREE)    (COMPLETELY AGREE)


10. "I think management values me as an employee."

(COMPLETELY DISAGREE)   (SOMEWHAT DISAGREE)     (NEUTRAL)   (SOMEWHAT AGREE)    (COMPLETELY AGREE)


```

## Part B - Survey Evaluation:

Identify and describe survey features:

```
1. Sample type: Stratified probability sampling. 


2. Sample size: 16,149 respondents


3. Target population: All persons 15 years of age or older living in the 10 provinces of Canada, excluding full-time residents of institutions.


4. Sampling frame: Combined list of landline and cellular numbers from the census and from administrative sources from Statistics Canada.


5. Survey mode(s): Each respondent was sent a voluntary electronic questionnaire.

6. Timeline: Data was collected between September 4, 2018 and December 28, 2018. Respondents were told the survey would take approximately 44 mintues to complete.

7. Response rate: 41.9%

8. Weights: The initial weighting per respondent was given by
```
$$
\frac{\text{Number of records sampled in the stratum}}{\text{Total number of records in the stratum from the survey frame}}
$$
```
This number was then adjusted to take into account the following factors:
- Only one person from each household was surveyed.
- The useage of rejective sampling to screen volunteers.
- Differing populations in the strata
- Differing incomes within strata
- Skewed provincial, age, and sex data


9. Data processing:
- Responses were manually entered into computers by respondents.
- Write-in responses matched together to create new categories.


10. Cleaning, imputation, etc:
- Out-of-scope respondents were removed from the raw data file
- Incomplete surveys were classified into two categories. 
    - Complete non-response. This is where the respondent did not answer the minimum number of questions. These responses were removed from the data file. 
    - Item non-response. This is when only a few items were not answered. Their responses to these questions were categorized as "Not stated"
- Missing information was estimated by comparing incomplete surveys to completed "donor" surveys or by replacing the missing values with the mean value.

11. Sources of error:
- Coverage errors
- Non-response errors
- Random sampling error

12. Limitations, known biases, etc: There is a bias in the data due to persons from some demographics being more likely to not respond. This introduces a non-response bias which was taken into account in the imputation step. Furthermore, the survey was biased towards persons with working phone numbers.

13. Link to documentation and any additional sources used:

https://www150.statcan.gc.ca/n1/pub/45-25-0001/cat5/c33_2018.zip

```



## Rubric

-	All required components are present and complete **Complete / Incomplete**
-	Choice of sampling strategy for Part A is justified and related to survey purpose **Complete / Incomplete**
-	Information for Part B is complete and correct **Complete / Incomplete**

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 18/04/2025`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (a2_survey_design_and_evaluation.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
