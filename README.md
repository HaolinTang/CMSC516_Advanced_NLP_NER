# CMSC516_Advanced_NLP_NER
This is a repository includes the information extraction project implementation of CMSC516_Advanced NLP.

## Authors
Akanksha Kosana, Lavanya Thollamadugu and Haolin Tang Group Project at Virginia Commonwealth University.

## Overview
**Named-entity recognition (NER)** is a sub-task of information extraction that seeks to locate and classify named entities in text into pre-defined categories such as the names of persons, organizations, locations, expressions of times, quantities, monetary values, percentages, etc. In this project, we will apply three methods into NER on resumes and ten named entities will be recognized. First, we will download the resumes data with annotations and then implement the necessary data preprocessing steps. Second, the sapCy NER model, conditional random field (CRF) model and BERT model will be built for this task. Third, we will compare the performance of above three models and test them using an unseen rewume of an employee. 

![image](https://user-images.githubusercontent.com/102632570/201744684-a0170a7a-11c8-4e4a-bb6b-7694a85ee3db.png)

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
We recommend to run the code in Google Colab while we provide two options to run our codes. 
* **Run in Google Colab:**\
Before running our codes, you have to first download the dataset and load it to your Google Colab.
- NER on resumes using CRF. (Run [NER_CRF.ipynb](https://colab.research.google.com/drive/1huV8wZWO0Q0rBGShqyF0s8EXOyxcbMf4?usp=sharing))
- NER on resumes using spaCy. (Run [NER_spaCy.ipynb](https://colab.research.google.com/drive/1wqWmfWSQORNZqOFFTDh21WHZWozPxV68?usp=sharing))
- NER on resumes using BERT.\
 (Run [NER_BERT.ipynb](https://colab.research.google.com/drive/1cKNmrIcJarsLUdWhXLhTr_VMDyn16gDY?usp=sharing), **NOTE** Please change the Colab runtime type to GPU) 

* **Run in Local System:**
    - Install Andconda (See [Installation Guide](https://docs.continuum.io/anaconda/install/))
    - Create a new conda environment named `cmsc516` with the command: `conda env create -f environment.yml`
    - Activate the environment: `conda activate cmsc516`  
    - Install jupyter notebook: `conda install jupyter`
    - Run jupyter from system: `jupyter notebook`. Now, you can run the notebooks in your local system.   

## Method
* **Conditional Random Filed:**\
The CRF formula is defined as:\
![image](https://user-images.githubusercontent.com/102632570/201798050-3488e30e-26fd-4072-aca9-e196c210ba2f.png)\
Here, *p(y|x)* refers to the probability of calculating a label sequence given a word sequence.

* **spaCy NER Model:**\
spaCy provides an exceptionally efficient statistical system for named entity recognition in python. It provides a default model which can recognize a wide range of named or numerical entities, which include company-name, location, organization, product-name, etc to name a few. Apart from these default entities, spaCy enables the addition of arbitrary classes to the entity-recognition model, by training the model to update it with newer trained examples. 

* **BERT:** `model = BertForTokenClassification.from_pretrained("bert-base-uncased")`\
The BERT model was proposed in BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding by Jacob Devlin, Ming-Wei Chang, Kenton Lee and Kristina Toutanova. It’s a bidirectional transformer pretrained using a combination of masked language modeling objective and next sentence prediction on a large corpus comprising the Toronto Book Corpus and Wikipedia.
## Results

## Discussions

## Future Work
