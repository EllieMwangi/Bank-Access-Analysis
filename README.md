# Finscope Survey Response Analysis on Bank Access

## Executive Summary
Financial inclusion remains a major obstacle to economic and human development in East Africa, with only 13.9% of adults in Kenya, Rwanda, Tanzania, and Uganda having access to or using a commercial bank account. Despite the rise of mobile money and innovative fintech solutions, banks continue to play a key role in facilitating access to financial services. Access to a bank account is crucial for long-term economic growth, enabling savings, facilitating payments, and improving access to credit.

In this analysis, we examined the state of financial inclusion and identified key demographic factors influencing access to banking. The findings reveal that 85% of respondents do not have a bank account, with rural populations, mobile phone access, and gender disparities being significant drivers. Our classification model, using demographic factors such as age, education, and job type, achieved a high accuracy of 93%, identifying key opportunities for banks to target women, rural areas, and mobile phone users with tailored solutions.

Recommendations include focusing expansion efforts in rural areas, targeting mobile banking services, and implementing women-centered initiatives to boost financial inclusion in the region. Financial institutions should consider adopting these strategies to effectively bridge the gap in access to banking services and contribute to economic development.

Access the colab notebook with the complete analysis [here.](https://colab.research.google.com/drive/1GHrMC5d34JFLPn0U3UcYHCPl5tSSjNg1?usp=sharing)
## Data Description
The data used for analysis contains demographic information and what financial services are used by individuals across East Africa. This data was extracted from various Finscope surveys ranging from 2016 to 2018 and is relevant for analysis.
![Entity Relationship Diagram](https://github.com/user-attachments/assets/e2714af5-03f0-411a-8865-f1da932ac102)

### Demographic Factors Analysis
- The categorical demographic factors such as *gender*, *job type*, *location* as well as *accesss to a cellphone* having a significant impact on whether an individual has an account or not.
- 63% of respondents without bank accounts live in rural areas. Banks should focus their expansion plans on these regions to boost adoption.
![rural vs urban](https://github.com/user-attachments/assets/f86b3a50-38f0-4a77-9537-8b07cf50a9f3)

- 82% of respondents with access to a cell phone did not have a bank account. Banks should target this market through mobile banking initiatives.
![cell phone access](https://github.com/user-attachments/assets/f167364e-bdc2-44df-9e66-bdc6af9c1311)
- 61% of respondents without a bank account were women. Women-led initiatives and affirmative action programs by financial institutions could help tap into this market.
![gender distribution](https://github.com/user-attachments/assets/853eb2d7-a0af-4334-9a92-269a2367b413)
- Kenya leads the region with the highest banking service penetration, while Rwanda has the lowest, followed closely by Tanzania. These variations suggest a need for tailored banking strategies to address the diverse challenges in each country.

### Model Development
- Model performance was highly affected by the imbalance in the target variable. Upsampling the minority class drastically improved performance of the tree based methods.
- The best performing model was a tuned random forest model with an accuracy of 93% and an roc_auc score of 96%
- The random forest cited the most important features in separating classes as respondent age, level of education, household size, type of job and cell phone access.
![important features](https://github.com/user-attachments/assets/a19f323d-a2c2-4fc2-81ca-9cfc66a4deda)

In conclusion, the Finscope survey highlights the need for financial institutions to adopt inclusive, targeted strategies to improve bank access, particularly for women, rural populations, and mobile users, to enhance financial inclusion across the region.
