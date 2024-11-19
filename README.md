# Finscope Survey Response Analysis on Bank Access

Financial Inclusion remains one of the main obstacles to economic and human development in Africa. For example, across Kenya, Rwanda, Tanzania, and Uganda only 9.1 million adults (or 13.9% of the adult population) have access to or use a commercial bank account.

Traditionally, access to bank accounts has been regarded as an indicator of financial inclusion. Despite the proliferation of mobile money in Africa and the growth of innovative fintech solutions, banks still play a pivotal role in facilitating access to financial services. Access to bank accounts enables households to save and facilitate payments while also helping businesses build up their credit-worthiness and improve their access to other financial services. Therefore, access to bank accounts is an essential contributor to long-term economic growth.

Inorder to figure out how we can predict which individuals are most likely to have or use a bank account, an understanding of the state of financial inclusion in Kenya, Rwanda, Tanzania, and Uganda is required,as well as an identification some of the key demographic factors that might drive individuals’ financial outcomes.

## Objectives
- Determine the state of financial inclusion in selected countries based on number of individuals with bank accounts
- Identify key demographic factors that influence whether an individual has a bank account or not.
- Build a classification model that predicts if an individual has a bank account or not using identified demographic factors.

Access the colab notebook with the complete analysis [here.](https://colab.research.google.com/drive/1GHrMC5d34JFLPn0U3UcYHCPl5tSSjNg1?usp=sharing)
## Data Description
The data used for analysis contains demographic information and what financial services are used by individuals across East Africa. This data was extracted from various Finscope surveys ranging from 2016 to 2018 and is relevant for analysis.

## Summary of Findings
A staggering 85% of respondents lack a bank account, indicating a considerable barrier to financial inclusion. This is a stark contrast to the proportion of individuals with bank accounts, underscoring the challenges in expanding banking services. Kenya has the highest penetration of banking services, while Rwanda has the lowest, followed by Tanzania.
### Demographic Factors Analysis
- The categorical demographic factors such as *gender*, *job type*, *location* as well as *accesss to a cellphone* having a significant impact on whether an individual has an account or not.
- 63% of respondents without bank accounts live in rural areas. Banks should focus their expansion plans on these regions to boost adoption.
![rural vs urban](https://github.com/user-attachments/assets/f86b3a50-38f0-4a77-9537-8b07cf50a9f3)

- 82% of respondents with access to a cell phone did not have a bank account. Banks should target this market through mobile banking initiatives.
![cell phone access](https://github.com/user-attachments/assets/f167364e-bdc2-44df-9e66-bdc6af9c1311)
- 61% of respondents without a bank account were women. Women-led initiatives and affirmative action programs by financial institutions could help tap into this market.
![gender distribution](https://github.com/user-attachments/assets/853eb2d7-a0af-4334-9a92-269a2367b413)

### Model Development
- Model performance was highly affected by the imbalance in the target variable. Upsampling the minority class drastically improved performance of the tree based methods.
- The best performing model was a tuned random forest model with an accuracy of 93% and an roc_auc score of 96%
- The random forest cited the most important features in separating classes as respondent age, level of education, household size, type of job and cell phone access.
![important features](https://github.com/user-attachments/assets/a19f323d-a2c2-4fc2-81ca-9cfc66a4deda)

In conclusion, the Finscope survey highlights the need for financial institutions to adopt inclusive, targeted strategies to improve bank access, particularly for women, rural populations, and mobile users, to enhance financial inclusion across the region.
