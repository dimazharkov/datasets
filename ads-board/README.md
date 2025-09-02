# Dataset Description

This dataset contains a collection of advertisements classified into categories.  
It was created for experiments with **text classification** tasks using large language models (LLMs).

## Advertisement Object

Each advertisement record contains the following fields:

- `advert_id` *(int)* — unique identifier of the advertisement.  
- `category_id` *(int)* — identifier of the category assigned to the advertisement.  
- `category_title` *(string)* — human-readable name of the category.  
- `advert_title` *(string)* — short title of the advertisement.  
- `advert_text` *(string)* — full advertisement text with detailed description.  
- `advert_summary` *(string, optional)* — compressed representation of the advertisement text, generated with the help of an LLM.  

## Category Object

Each category record contains the following fields:

- `id` *(int)* — unique identifier of the category.  
- `title` *(string)* — name of the category.  
- `bow` *(list of strings, optional)* — bag-of-words representation derived from advertisements within this category.  
- `tf_idf` *(list of strings, optional)* — TF-IDF representation based on the frequency of terms from advertisements in this category.  

## Purpose

The dataset was used as a source of data for classification experiments.  
It provides **ground-truth categories** for evaluating metrics such as *F1-score, Precision, Recall*.  

## Characteristics

- Language: Ukrainian  
- Domain: General advertisements (furniture, rentals, healthcare, cosmetics, etc.)  
- Data format: JSON  
- Records: Each row corresponds to a single advertisement  

## Notes

Real-world advertisements often include spelling mistakes, redundant or irrelevant descriptions, repetitions, commercial details (prices, addresses, conditions), and stylistic variability.  
These features make classification more challenging and justify the use of **LLMs** for robust text understanding.
