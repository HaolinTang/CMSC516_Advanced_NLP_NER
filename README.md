# CMSC516_Advanced_NLP_NER
This is a repository includes the information extraction project implementation of CMSC516_Advanced NLP.

## Authors
Akanksha Kosana, Lavanya Thollamadugu and Haolin Tang Group Project at Virginia Commonwealth University.

## Overview
**Named-entity recognition (NER)** is a sub-task of information extraction that seeks to locate and classify named entities in text into pre-defined categories such as the names of persons, organizations, locations, expressions of times, quantities, monetary values, percentages, etc. In this project, we will apply three methods into NER on resumes and ten named entities will be recognized. First, we will download the resumes data with annotations and then implement the necessary data preprocessing steps. Second, the sapCy NER model, conditional random field (CRF) model and BERT model will be built for this task. Third, we will compare the performance of above three models and test them using an unseen rewume of an employee.     

## Data
The resumes with annotations dataset (See [Resume dataset](https://github.com/HaolinTang/CMSC516_Advanced_NLP_NER/tree/main/data)) is used to perform NER on resumes. This dataset has 220 items with manually labeled annotations. The labels are divided into following 10 categories:
<div align="center">
<table>
<tr>
    <td>Name</td>
    <td>College Name</td>
    <td>Degree</td>
    <td>Graduation Year</td>
    <td>Years of Experience</td>
</tr>
<tr>
    <td>Companies worked at</td>
    <td>Designation</td>
    <td>Skills</td>
    <td>Location</td>
    <td>Email Address</td>
</tr>
</table>
</div>
In the data preprocessing, we first convert this dataset into DataFrame and then remove special characters in the resume contents. Second, we extract the annotations into entities. Last, we split this dataset into 90% training and 10% testing.

## Installation & Usage

## Method

## Results

## Discussions

## Future Work
