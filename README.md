# Pattern Functional Dependencies

Patterns (or regex-like rules) are widely used to discover meta-knowledge in a given domain, e.g. a {Year} column should contain only four digits, and thus a value like "1980-" would be erroneous. In addition, data dependencies across columns, e.g. {Postal Code}  uniquely determines {City}،is an important type of integrity constraints (ICs), which have been extensively studied. A promising, but not explored, direction is to leverage patterns to model the dependencies  (or meta-knowledge)  between partial values  across columns. For instance, in an employee ID "{F-9-107}", "{F}" determines the financial department.

We propose a novel class of ICs, called pattern functional dependencies (PFDs), to model fine-grained data dependencies gleaned from partial attribute values. These dependencies cannot be modeled using traditional ICs, such as (conditional) functional dependencies, which work on entire attribute values. 



## What is inside the main folder?

### There are two subfolders:
#### 1- data: which include data from two open source repositories used in our paper so it has three folders 
        a. DGOV that include the csv files for the data extracted from data.gov
        b. CHE which include the csv extracted from the ChEMBL database so we stored those tables in csv 
        for ease of use while our system supports postgres databases.

#### 1- src: which include the source code of our system. The system can be executed using the pfd.ipynb. We use jupyter notebook as the main interface for now.


## How to run the code?

Download both data and src folders and put them in the same folder in your machine. Open a terminal and cd to the "src" folder. On the terminal type "$ jupyter-notebook pfd.ipynb". Initially, you will the results that were obtained when I run the code. 

The presented experiment 1 correspond to the CFD vs PFD Discovery in Section 5.1 in the paper and experiment 2 correspond to the PFD Validation experiment in Section 5.2. Also, experiment 1 in pfd.ipynb reports the run time for processing the data sets which correspond to the experiment in Section 5.4.
