## A Novel Deep Learning Method for Identifying Antigen-Antibody Interactions (DeepAAI)

DeepAAI is an advanced deep learning-based tool for identifying antigen-antibody interactions.

For making DeepAAI available at no cost to the community, we have set a **[web service](https://aai-test.github.io/)** predicting antigen-antibody interactions. 
[https://aai-test.github.io/]( https://aai-test.github.io/)




### Architecture   
![](/doc/img/model_architecture.png)

### Installation
```bash
pip install -r requirements.txt
```


      

### Descriptions  
The most important files in this projects are as follow:
- dataset: 
  - `abs_dataset_cls.py`: The object for load the HIV classification data set. 
  - `k_mer_utils.py`: Create K-mer feature. 
- baseline_trainer: Train scrips for DeepAAI and some baselines. 
- models: Implementation of DeepAAI and all baselines.


### Training
Execute the following scripts to train antigen-antibody binding model.
```bash
python model_trainer/deep_aai_kmer_embedding_cls_trainer.py --mode train
```
Hyper-parameter in DeepAAI: 
| Parameter | Value | 
| ----  | ----  |
| Dropout| 0.4 | 
| Adj L1 loss | 5e-4 | 
| Param L2 loss | 5e-4 |
| Amino embedding size | 7 |
| Hidden size | 512 |
| Learning rate | 5e-5 |




