# Lab 10: Statistical inference

💪🏻 Under development

<!--
- [ ] add the transformed ENNTT data to the data directory
-->

## Preparation

- Read/ annotate: [Recipe \#10](https://qtalr.github.io/qtalrkit/articles/recipe-10.html). You can refer back to this document to help you at any point during this lab activity.

## Objectives

- Review skills and knowledge on performing diagnostic checks on data
- Learn to convert research questions to hypotheses
- Apply skills and knowledge to identify, inspect, interrogate, and interpret the results of inferential analysis

## Instructions

### Getting started

In this lab, you will be using Git and Github to fork, clone, commit, and push changes to a repository. The repository you will select to use as the repository to fork to your own Github account can be one of the following:

- [Lab 10 repository](https://github.com/qtalr/lab-10)
- [Minimal template](https://github.com/qtalr/project)
- [Web-based project template](https://github.com/qtalr/project_web)
- Other (consult your instructor)

If you are starting with a new repository, fork and clone the repository you selected to your local machine. Then orient yourself to the repository by opening the README file and reviewing the template configuration.

If you are using an existing reproducible research project repository, open that project on your local machine, and `pull` the latest changes from the remote repository to ensure that your local and remote repositories are in sync.

Open a Quarto document in the process directory and name it accordingly (e.g., `4_analysis.qmd`, `analysis.qmd`, *etc.*).

The data you select to explore should be in a format conducive for performing statistical inference for a specific hypothesis. The options include the following:

- Europarl Corpus of Native, Non-native, and Translated Texts (see [below for details](#europarl-corpus-of-native-non-native-and-translated-texts))
- The dataset you transformed in Lab 07
- Other (consult your instructor)

### Inferential analysis

In your analysis process file,

1. add a section which provides a brief description of the dataset you will be using and the analysis setup and hypothesis. Include:

  - the name and/ or source of the data
  - the nature of the data
  - the response variable and the explanatory variable(s)

2. add a section which provides a description of the explanatory variables you will use and how they are operationalized. Include:

  - a description of the response variable and the explanatory variable(s)
    - including the unit of observation and the key variables of interest in the dataset
  - a description of the process you will use to inspect the data and perform diagnostic checks

3. add a section which provides a description of the modeling process you will be using to conduct the analysis. Include:

  - a description of the high-level modeling process you will be using to conduct the analysis (e.g. chi-square test, *t*-test, or logistic or linear regression)
  - for the modeling process, how will you operationalize the model (e.g. chi-square test of independence, *t*-test for difference in means, or logistic or linear regression fit)
  - a description of the process you will use to derive the $p$-value and and confidence intervals

4. Implement and make sure to organize your analysis process in a way that is reproducible. This means that you should be able to run the code in your process file and reproduce the process (use `set.seed()` for any sampling process, for example). Use the `data/analysis` (or similar) directory to store any derived datasets used in the analysis.

5. Make sure that your code is well documented with code comments and that you have included prose to describe the process of analyzing the dataset.

6. Include a section to describe the results of your analysis. This will minimally contain the model estimates, $p$-values, and confidence intervals and may contain effect size and/ or variance explained measures.

7. Confirm that your code runs without errors and that the code, visualizations, and/ or tables are displayed as expected.

8. Finally, commit and push your changes to your Github repository. *Make sure to include files or directories that you do not have permission to share in your `.gitignore` file.*

### Assessing your progress

1. In your repository on Github, open an issue to provide feedback on your experience with this lab (Click on the 'Issues' tab and then click the 'New issue' button). Title the issue "Lab 09 feedback" and provide your feedback in the body of the issue.

Some questions to consider:

  - What did you learn?
  - What did you find most/ least challenging?
  - What resources did you consult?
    - Instructor? R or Quarto documentation, Websites (provide links)?
  - What more would you like to know about inferential analysis?
    - Find potential resources you might consult to continue your learning. Provide links and a brief description of the resource.

## Submission for feedback

- Provide a link to your GitHub repository

## Europarl Corpus of Native, Non-native, and Translated Texts

Transform the ENNTT data so that the dataset is in the following format.

| doc_id | doc_type | syntactic_complexity_1 | syntactic_complexity_2 | ... |
|--------|----------|------------------------|------------------------|-----|
| 1      | native   | 0.1                    | 0.2                    | ... |
| 2      | native   | 0.3                    | 0.4                    | ... |
| 3      | translation   | 0.5                    | 0.6                    | ... |
| 4      | translation   | 0.7                    | 0.8                    | ... |

: Table 1: Example of the transformed ENNTT data
