# Recipe_Generation
Machine translation models for Recipe_Generation



In this repo, we provide some models to do the task of recipe generation. 

The baseline model is Seq2Seq model. Then we add attention mechanism and copy mechanism to improve the performance of the basic model. After that, pre-training idea is used to further improve the performance. Pre-trained embedding is tried (which is stored in the Google Drive, this link is shown below). Also, pre-trained encoder and pre-trained decoder model based on copy model has been built and trained.

The above models are trained based in the dataset (total_data.csv).

Finally, we introduce phrasal level method to explore the effect of  the introduction of phrasal level idea. There are two directions here. The first is that we use phrasal level in pre-training step and use the normal copy model in the formal training step (dataset: total_data_part_phrasal_1.csv). The second direction is that we use phrasal level in  formal training step without pre-training step (dataset: total_data_withcommainput.csv,).

The all datasets and the pre-trained embedding template we use are stored in the Google Drive, the link is 



Enviroment:

Tensorflow 2, Python 3



Note:

- All codes are in the format of .ipynb, which can be run in Colab or Kaggle. The only modification you should do is change the directory of the location of data in codes.
- There are some of evaluation metrics we use in this task, most of them are written in the main codes. However, NLTK version of Colab and Kaggle doesn't support METEOR funciton. We provide the codes of calculating METEOR score independently, which is provided in the directory of evaluation.
- The loss plotting codes is located in the directory of plotting.