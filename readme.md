# Project Name

## Branches

This repository currently has two main branches:

1. **master (origin)**: The main branch containing the stable version of the project.
2. **ML/sentiment**: A dedicated branch for developing sentiment analysis models.

## ML/sentiment Branch

The `ML/sentiment` branch is focused on implementing sentiment analysis using deep learning techniques. In this branch, we are using **PyTorch** with **CUDA 12.4** for GPU acceleration.

### Requirements

I am using pytorch with CUDA 12.4. You may consider to change requirements.txt in "sentiment" folder.

Word embbedings from: https://nlp.stanford.edu/projects/glove/
I am using Wikipedia 2014+ version with 400k vocab size and 100d vectors. 

## Sentiment analysis

Dockerignore excludes "glove.6B*". It can affect working on container itself.