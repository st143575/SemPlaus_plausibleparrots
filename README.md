# Enhancing Semantic Plausibility Modeling using Entity and Event Knowledge [[Paper]](https://arxiv.org/abs/2408.16937)

---

<div  align="center">    
<img src="./system_architecture.png" width="70%">
</div>

## Usage

### Virtual Environment
Create and activate a conda environment.
```bash
conda create -n MSPPlausibleParrots python=3.11
conda activate MSPPlausibleParrots
git clone https://github.com/st143575/SemPlaus-plausibleparrots.git
cd SemPlaus-plausibleparrots
```

Install pip in the conda env (if it's not installed by default).
```bash
conda install pip
```

### Installation
Make sure you have the following dependencies installed.
- cuda 12.3

Install packages in requirements.txt by running
  ```bash
  pip install -r requirements.txt --no-cache-dir
  ```

### Path Configuration
PATH is the root path of this repository.
CACHE_DIR = PATH + "cache/"

### Data Analysis
Please follow the instructions in `./0-preliminary_study/` for data analysis.

### Data Preprocessing and Data Augmentation
Please follow the instructions in `./1-data_preprocessing/` for data preprocessing and augmentation.

### Baselines
We evaluate two baseline systems on our task: (1) zero-shot inference; and (2) fine-tuning on the sentences preprocessed and augmented from the original (s,v,o)-event triples.
To run the baselines, please follow the instructions in `./2-baselines/`.

### Event Detection (ED)
Please follow the instructions in `./3-ed/`.

Note: To avoid potential package version conflict, please create and activate a new environment, install packages in `requirements_ed.txt` and run ED there. See the instructions in `./3-ed/` for details.

### Ultra Fine-grained Entity Typing (UFET)
Please follow the instructions in `./4-ufet/`.

Note: To avoid potential package version conflict, please create and activate a new environment, install packages in `requirements_et.txt` and run UFET there. See the instructions in `./4-ufet/` for details.

### Dataset Construction
We construct the datasets for our system using the templates specifically designed for (1) injecting both event and entity type knowledge (evt+ent), (2) injecting only event type knowledge (evt), and (3) injecting only entity types knowledge (ent), respectively. Please follow the instructions in `./5-dataset_construction/`.

### System Fine-tuning and Evaluation
We fine-tune and evaluate our system with the knowledge-enhanced datasets.
Please follow the instructions in `./6-finetune_and_eval/`.

## Evaluation Results
<div  align="left">    
<img src="./msp_eval_results.png" width="90%"/>
</div>
