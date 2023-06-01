<img src="https://colmap.github.io/_images/sparse.png">
***
# dl_reconstruction

Collection of colmap and deep learning featuring/matching integrations 

## Intro
COLMAP is a general-purpose Structure-from-Motion (SfM) and Multi-View Stereo (MVS) pipeline with a graphical and command-line interface. It offers a wide range of features for reconstruction of ordered and unordered image collections. [More at official docs.](https://colmap.github.io/)

## Problem
It is difficult to train a large reconstruction model because it requires both powerful resources and a large amount of data. 
This data must be preprocessed before training the model.

## Solution
This implementation aims to simplify the data filtering process.

### Setup and run
#### Setup
```bash
git clone https://github.com/RolfAdolf/dl_reconstruction.git
cd dl_reconstruction
```

#### Run with Docker
```bash
docker build . -t test_script
docker run -it --rm -d --shm-size 2G --gpus 'all,"capabilities=compute,utility"' -v $(pwd):/app/ --name try_script test_script
```
