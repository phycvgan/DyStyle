# Preparing materials before training

## 1. Preparing GAN Generator

We suggest training [stylegan2](https://github.com/NVlabs/stylegan2) for high quality image generation. You can also download well pretrained stylegan2 model and put it into "pretrained_model" folder.

## 2. Preparing Attribute Classifier

Our code requires pretrained attribute classifiers. Please refer our pytorch implementation of attribute classifier in "loss/public_loss/multi_class.py" and "loss/public_loss/multi_task.py".

If necessary, you can customize your own attribute classifier file just following the interface of input and output.

## 3. Preparing DyStyle Model Config
