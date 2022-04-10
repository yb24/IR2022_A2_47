# IR2022_A2_47

## Assignment Info
Course: Information Retrieval [CSE508]  
Semester: Winter 2022  
Group: 47  
Assignment 2

## Repository Description
Q1a.ipynb & Q1b.ipynb: Complete code with comments for Question 1  
Q2.ipynb: Complete code with comments for Question 2
Q3.ipynb: Complete code with comments for Question 3

## .gitignore Description
All the data files are stored in the Dataset folder which is present in the root folder. Link to pkl files: [link](https://drive.google.com/drive/folders/1SpfnfR0R3EFE1fTViYQm-DGLVLNGaC5h?usp=sharing)

- Question 1
  - Methodology (Q1a)
    - Relevant libraries are imported
    - List of path of all the files in the dataset is determined
    - Each document is preprocessed as done in Assignment 1
    - Query is input and sanitized with the same preprocessing steps
    - Jaccard Coefficient for doc,query pairs is found
    - Top 5 relevant documents based on jaccard coefficient are displayed
  - Methodology (Q1b)
    - Relevant libraries are imported
    - List of path of all the files in the dataset is determined and a file_dictionary is constructed
    - Each document is preprocessed as done in Assignment 1
    - Global vocabulary is created
    - matrix of size no. of document x vocab size is constructed
    - above matrix is filled with TF-IDF values
    - Query is input and sanitized with the same preprocessing steps
    - The query vector is made of size of vocabulary
    - TF-IDF score of query is computed using TF-IDF matrix
    - Top 5 documents based on above score are displayed
    - Same is repeated for all 5 weighing schemes
  - Jaccard Coefficient
     - Pros: Faster and requires less space as we don’t need to make the size of query vector equal to that of document vector
     - Cons: Does not take into account important metrics like term frequency and ordering of words
  - TF-IDF Matrix
     - Pros: Takes into account term frequency of document and query. Terms occurring highly in a small number of documents are given more weightage and less weightage to terms occurring in almost all documents.
     - Cons: Slower and requires more space as we have to make the size of query equal to length of document. Doesn’t take into account position of term in document, semantics and co-occurrences in different documents.

- Question 2
  - Methodology
    - Relevant libraries are imported
    - List of path of all the file in the dataset is determined
    - Qid:4 is extracted and stored in a separate list and rest all the rows are stored in another list
    - The list is sorted in descending order
    - Total number of files is calculated
    - nDCG at 50 and whole dataset is calculated
    - Precision-Recall graph is plotted on feature 75

- Question 3
  - Methodology
    - Relevant libraries are imported
    - List of path of all the files in the dataset is determined
    - Each document is preprocessed
    - The dataset is split into 3 train:test ratios; 50:50, 70:30, 80:20. For each case the following steps are performed
    - TC-ICF scoring technique is applied
    - Top k features of each class is selected
    - Global vocabulary is the union of top k features of all classes
    - Priors and likelihoods for each class on training set are evaluated
    - For each document in test set, its class is predicted and confusion matrix is updated
    - Accuracy is evaluated and reported
