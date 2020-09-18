# Prognostoma
A predictive tool that considers the patient demographics,genetic and medical history to predict the prognosis which can help doctor and patient make an informed decision.
#### Context: 
Glioblastoma multiforme (GBM)is the most common and aggressive form of brain tumor in adults. (52 % of all primary brain tumors) with a poor prognosis of 12-15 months.

GBMs are biologically aggressive tumors that present unique treatment challenges due to the following characteristics:

- Localization of tumors in the brain
- Inherent resistance to conventional therapy
- Limited capacity of the brain to repair itself
- Migration of malignant cells into adjacent brain tissue
- The variably disrupted tumor blood supply which inhibits effective drug delivery
- Tumor capillary leakage, resulting in an accumulation of fluid around the tumor; (peritumoral edema) and intracranial hypertension
- A limited response to therapy
- The resultant neurotoxicity of treatments directed at gliomas

The standard treatment option for GBM is 
- Surgery : To remove to remove as much of the tumor as possible without injuring the surrounding normal brain tissue needed for normal neurological function.
- Radiation: Ater the wound from surgery is healed , radiation therapy is done to selectively kill the remaining tumor cells that have infiltrated the surrounding normal brain tissue.
- chemotherapy: Temozolomide is the current standard of treatment for GBM and is given along with radiation to control the tumor growth. However it is effective in only 20% of patients. 

#### Need: 
The 5-year survival rate of patients with brain tumours is among the lowest for all cancer types (35%). GB is the most frequent primary brain tumour; however, its incidence is relatively low compared to other types of cancer, ranging between 0.59 and 3.69 cases per 100 000 person-years. Despite advances in the surgical and oncological treatment of GB, prognosis is still poor, with a 5-year survival rate of between 0.05% and 4.7%.
The standard care are unable to prolong the remission and the investigative treatments introduced over past three decades have only been able to prolong the survival of patients by an average of three months. 
Further, these standard care put impose financial burden on the patient and the caregivers. Healthcare costs associated with GBM are extremely high. With limited resources and rising healthcare costs,it is pertinent to evaluate the not only the cost but also the value of the treatment. 

#### Vison:
A predictive tool that considers the patient demographics,genetic and medical history to evaluate the best treatment option and chances of survival indicating the value of the treatment. 

#### Output for Stakeholders: 
1. Doctors: Helps them to decide the treatment strategy considering multiple factors that affect the success of the treatment and properly advise the patient not simply based on a reasnable guess. Improves doctors efficiency in providing effective treatment and increases the clinical productivity. 
2. Pharma companies: Companies trying to come up with novel treatment strategy need to evaluate within a value based framework as defined by the ASCO. 
3. Insurance company : While approving coverage for these techniques like Novocure's Optune, CMS takes into account the efficacy of the treatment to improve survival of patient while maintaining the quality of life.
4. Patient: To make an informed choice about the treatment based on the survival chances, quality of life and insurance coverage.

## Installation
### Dataset
The dataset used in this project can be downloaded from [cBioportal](https://www.cbioportal.org). This dataset contains data from diffrent cancer studies curated from TGCA. For this project I selected the Glioblastoma - Mayo Clinic, 2019 and TCGA, Firehose Legacy dataset. Other datsets present for glioblastoma used these two studies data primarily. 
Clinical and genomics data was obtained separately by selecting the target genes to evalaute. I focused on PTEN, EGFR, TP53 and IDH1 for my analysis as these are the most commonly mutated genes found in Glioblastoma. 

### Requirements
1. Python 3. 
2. Jupyter notebook (optional)
3. Sci-kit learn
4. Numpy
5. Pandas
6. Pickle

## Steps of Data analysis
While analysing the data, following steps were performed. 
1. Opening and reading the data into a dataframe
2. Data cleaning - Remove outliers, Impute missing values, Evaluate correlation and skewness.
3. Evalaute machine learning models to predict prognosis
4. Storing the best model as pickle file for further prediction in the web app

## Overall conclusion

1. Genetic features play an important role in predicting prognosis.
2. Using Lasso regularization, we got the best Coefficient of determination indicating it is performing better compared to the dummy regression. Using that model, I have built a web app for the doctors to make more accurate prognosis.It can be accessed from here: https://obscure-reef-35666.herokuapp.com/
3. More data will improve the prediction.


### Refrences
While doing this project, I took help from numerous websites but these are the two whose code I have used directly. 
1.  https://github.com/WillKoehrsen/machine-learning-project-walkthrough/blob/master/Machine%20Learning%20Project%20Part%201.ipynb
2. https://github.com/datamadness/Automatic-skewness-transformation-for-Pandas-DataFrame
