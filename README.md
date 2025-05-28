# Master’s Thesis Repository: Appraisal and Argumentation in the Ukrainian Conflict in UNSC Speeches

## Description

This repository accompanies the master’s thesis:

**“How do diplomats construct the conflict parties in UNSC speeches?  
A study of the Ukrainian conflict through Appraisal Theory, Argumentation Schemes and Natural Language Processing Techniques”**

Authored by **Valentina Tretti-Beckles**, submitted in **June 2025**  
for the **Master’s Degree in Cognitive Systems: Language, Learning and Reasoning** at **Potsdam University**.

The repository includes the dataset, annotation guidelines, and code used for classification experiments.

---

## Dataset Description

The dataset builds upon the **UNSCon** dataset (Zaczynska, Bourgonje, and Stede, 2024), which extends the **UNSC dataset** developed by Schönfeld et al. (2019, 2025). Annotations and experiments are based on a sample of 45 speeches related to the Ukrainian conflict.

---

## Repository Structure

### 1. Code

Scripts for annotation extraction and classification experiments.

#### • Annotation Extraction
- `Argument_Schemes_Annotations_Extraction.ipynb`: Extracts argumentation scheme annotations.
- `Attitude_Annotations_Extraction.ipynb`: Extracts attitude annotations.

#### • Automatic Annotation of Debate SPV.7138

##### Task 1 – Argumentative Sentence Detection
- `Task 1 - Argumentative Sentence Detection.ipynb`: Fine-tunes RoBERTa on the USElecDeb60To16 v.01 dataset (Haddadan et al., 2019) and evaluates the model.
- `Task 1 - Argumentative Sentence Detection on Debate 7138.ipynb`: Applies the model to debate SPV.7138.
- `fine_tuned_roberta.zip`: Contains the fine-tuned model.

##### Task 2 – Argumentative Components Identification
- `Task 2 - Argumentative Components Identification.ipynb`: Fine-tunes RoBERTa for claim/premise classification and applies it to debate SPV.7138.
- `fine_tuned_roberta_claim_premise.zip`: Fine-tuned model for this task.

##### Task 3 – Premise-Claim Relation Extraction and Validation

###### Sentence Transformer Approach:
- `Task3-Premise-Claim Relation Extraction and Validation.ipynb`: Uses the `sentence-transformers/multi-qa-mpnet-base-dot-v1` model.
- `Task3 file evaluations UNSC speeches.csv`: Contains model predictions and evaluations.

###### ChatGPT Validation:
- `Validation_Set_ChatGPT_relations.csv`: File for manual validation via ChatGPT.

##### Task 4 – Argumentation Scheme Classification
- `Task4-Arg Schemes Classification.ipynb`: Fine-tunes RoBERTa using the UNSCUkrArg dataset.
- `validation_set_debate7138.csv`: Manually annotated data.
- `roberta_argumentation_schemes.zip`: Fine-tuned model.

---

### 2. Data

- `argumentation-scheme-in-unsc-speeches.zip`: Annotations from INCEpTION for argumentation schemes.
- `appraisal-annotation-in-unsc-speches.zip`: Attitude annotations from INCEpTION.
- **USElecDeb60To16 v.01 Dataset:**
  - `sentence_db_candidate.csv`: Dataset from Haddadan et al. (2019).
- **UNSCUkr Datasets:**
  - `UNSCUkrAtt.csv`: Contains attitude annotations and metadata (e.g., polarity, targets, conflict party).
  - `UNSCUkrArg.csv`: Argumentation scheme annotations, based on Maria Poiaganova’s repository: [mpoiaganova/political-argument-mining](https://github.com/mpoiaganova/political-argument-mining).
- **SPV.7138 Speeches:**
  - `Debate_7138_Speeches.csv`: Contains all sentences from debate SPV.7138.

---

### 3. Results

Prediction outputs from classification tasks:

#### Task 1 – Argumentative Sentence Detection
- `7138_speches_with_Task1_predictions.csv`

#### Task 2 – Argumentative Components Identification
- `7138_speches_with_Task2_predictions.csv`

#### Task 3 – Premise-Claim Relation Extraction and Validation
- `7138_speeches_with_Task3_predictions.csv`
- `7138_speeches_with_Task3_ChatGPT_validation.csv`

#### Task 4 – Argumentation Scheme Classification
- `7138_speeches_with_Task4_predictions.csv`
- `validation_set_debate7138_predictions.csv`

---

### 4. Annotation Guidelines

- `Annotation_Guidelines.pdf`: Outlines the annotation frameworks, processes, and INCEpTION usage.

---

## References

- **Haddadan, Shohreh**, **Cabrio, Elena**, and **Villata, Serena**.  
  *Yes, we can! Mining Arguments in 50 Years of US Presidential Campaign Debates.*  
  In *Proceedings of the 57th Annual Meeting of the ACL*, 2019, Florence, Italy. [ACL Anthology](https://aclanthology.org/P19-1452/)

- **Zaczynska, Karolina**, **Bourgonje, Peter**, and **Stede, Manfred**.  
  *How Diplomats Dispute: The UN Security Council Conflict Corpus.*  
  In *LREC-COLING 2024*, Torino, Italy.

- **Schönfeld, Mirco**, **Eckhard, Steffen**, **Patz, Ronny**, and **van Meegdenburg, Hilde**.  
  *The UN Security Council debates (Version 5)*. 2019. [Harvard Dataverse](https://doi.org/10.7910/DVN/8RIGNS)

- **Schönfeld, Mirco**, **Eckhard, Steffen**, **Patz, Ronny**, **van Meegdenburg, Hilde**, and **Pires, Antonio**.  
  *The UN Security Council debates 1995–2023.* 2025. [arXiv](https://arxiv.org/abs/1906.10969)

---
This research was conducted under the supervision of **Prof. Dr. Manfred Stede** (University of Potsdam) and **MA.Karolina Zaczynska** (University of Potsdam), whose guidance and expertise were instrumental throughout the development of the thesis.


For any questions, please contact **Valentina Tretti-Beckles**.
