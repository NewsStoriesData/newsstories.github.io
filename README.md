# NewsStories: Illustrating articles with visual summaries

![alt text](motivational_figure.png)

This repository contains a PyTorch implementation of the paper [NewsStories: Illustrating articles with visual summaries](https://arxiv.org/abs/2009.07698) accepted at ECCV 2022. If you find this implementation or the paper helpful, please consider citing:

    @InProceedings{rxtan2022newsstories,
         author={Tan, Reuben and Plummer, Bryan and Saenko, Kate and Lewis, JP and Sud, Avneesh and Leung, Thomas},
         title={NewsStories: Illustrating articles with visual summaries},
         booktitle={Proceedings of the IEEE/CVF European Conference on Computer Vision (ECCV)},
         year={2022} }
    
# Dependencies

1. Python 3.6
2. Pytorch version 1.10.0
3. nltk

# Download NewStories Dataset

![alt text](dataset.png)

You can use this link to download the NewsStories dataset. 

# MIL-SIM code


# Required Arguments

1. pretrained_path: path to pretrained CLIP model
2. num_imgs: maximum number of images in a set
3. num_sentences: maximum number of sentences in an article.
