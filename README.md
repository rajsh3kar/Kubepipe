# Kubepipe

## **General Description**
Pipeline creation, management, and orchestration using Kubeflow


## **Architecture**

![https://github.com/rajsh3kar/Kubepipe/blob/main/archi.png](https://github.com/rajsh3kar/Kubepipe/blob/main/archi.png)
## **Component Definition**
Pipeline Components

1. Data Preparation and Collection

The first component fetches and stores the dataset, explicitly separating the training and validation splits. This ensures reproducibility and consistency across subsequent pipeline stages. After this step, this dataset has been given to privacy risk assessment module for 
Assessing the privacy risk of the data being collected. 


2. Privacy Risk Assessment: Anonymization and Minimization of Data


Adhering to GDPR compliance, the anonymization component utilizes spaCy's named entity recognition (NER) and the Faker library to pseudonymize personal identifiable information such as names and organizations within the training dataset. This step mitigates privacy risks, ensuring data security and compliance with regulatory frameworks. The component of the minimized dataset implements GDPR's data minimization principle by selectively removing unnecessary columns (for example, ID and title), retaining only the essential fields (context, question, answers) required to train the model. This practice reduces potential data leakage and storage overhead, enhancing overall data security.
References: https://ieeexplore.ieee.org/document/9839062

4. Model Fine-Tuning
The data collected from the 
This stage incorporates advanced optimization techniques to fine-tune a pre-trained language model. 


5. Benchmarking

After training, the model undergoes benchmarking against the validation dataset subset, evaluating standard performance metrics specific to question-answering tasks, namely Exact Match (EM) and F1 scores. This provides objective measures of the model's ability to generate accurate and contextually relevant answers.

6. Evaluation and Visualization

The evaluation stage performs in-depth analyses by visualizing training dynamics and sustainability metrics. Sustainability metrics, captured during training, are incorporated into an informative markdown document displayed within the Kubeflow Pipelines UI, enabling easy inspection of model performance and ecological impact.

## **Screenshots**
![](https://github.com/DATAPACT/Kubepipe/blob/main/Kubeflow_pipeline.png) "KubePipe Pipeline Definition for Complaint Aware LLM Fine tuning")


## **Commercial Information**

Table with the organisation, license nature (Open Source, Commercial ... ) and the license. Replace with the values of your module.

| Organisation (s) | License Nature | License |
| ---------------  | -------------- | ------- |

## **Top Features**
1. Creates pipeline
2. Deploys
3. Orchastration
4. Monitoring 



### Summary of installation steps
 Write an email to rajashekar.kolichala@uibk.ac.at

### Detailed steps

 under development.


