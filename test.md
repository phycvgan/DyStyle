# Preparing materials before testing

## 1. Preparing GAN Generator

We suggest training [stylegan2](https://github.com/NVlabs/stylegan2) for high quality image generation. You can also download well pretrained stylegan2 model and put it into "pretrained_model" folder.

## 2. Preparing Checkpoint

The checkpoint file is suffixed with ".pth", which is saved during training. 

## 3. Preparing Edit Config

Edit config file describes the way to generate edited images based on user specified preference. 
The core of this config file consists of "sampler" and "configer". 
In which, the "sampler" specifies the way to sample latent code, e.g., randomly sample from normal distribution, sample from given file and sample from real face using e4e encoder. 
The "configer" describes how to generate a sequential of target attributes to edit the original image. 

We have provided some examples. 
Please refer the "edit_config/adult/basic.yaml" for more details. 

You can also customize your own "sampler" and "configer" in "./hooks". 