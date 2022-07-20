# Detecting Cross-Modal Inconsistency to Defend Against Neural Fake News

![alt text](motivational.png)

This repository contains a PyTorch implementation of the paper [Detecting Cross-Modal Inconsistency to Defend Against Neural Fake News](https://arxiv.org/abs/2009.07698) accepted at EMNLP 2020. If you find this implementation or the paper helpful, please consider citing:

    @InProceedings{tanDIDAN2020,
         author={Reuben Tan and Bryan A. Plummer and Kate Saenko},
         title={Detecting Cross-Modal Inconsistency to Defend Against Neural Fake News},
         booktitle={Empirical Methods in Natural Language Processing (EMNLP)},
         year={2020} }
    
# Dependencies

1. Python 3.6
2. Pytorch version 1.2.0

# Download NeuralNews Dataset

Please follow the instructions here (https://cs-people.bu.edu/rxtan/projects/didan/) to download the NeuralNews dataset. In particular, download this file (https://drive.google.com/file/d/1rswGdNNfl4HoP9trslP0RUrcmSbg1_RD/view?usp=sharing) and place it into the data folder.

# Preprocess Data

### Image Features
For each image, we extract 36 region features using a Faster-RCNN model (https://github.com/peteanderson80/bottom-up-attention) that is pretrained on Visual Genome. The region features for each image is stored separately as a .npy file.

### Language Features
To convert the articles and captions into the required input format, please go to https://github.com/nlpyang/PreSumm/blob/master/README.md and carry out steps 3 to 5 of data preparation.

### Named Entities
We use the SpaCY python library to parse the articles and captions to detect named entities. We store this information as dictionary where the keys are the article names and the values are sets of detected name entities.

# Required Arguments

1. captioning_dataset_path: Path to GoodNews captioning dataset json file
2. fake_articles: Path to generated articles
3. image_representations_dir: Directory which contains the object representations of images
4. real_articles_dir: Directory which contains the preprocessed Torch text files for real articles
5. fake_articles_dir: Directory which contains the preprocessed Torch text files for generated articles
6. real_captions_dir: Directory which contains the preprocessed Torch text files for real captions
7. ner_dir: Directory which contains a dictionary of named entities for each article and caption
