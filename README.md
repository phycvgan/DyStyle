# DyStyle: Dynamic Neural Network for Multi-Attribute-Conditioned Style Editing

<img src='pics/sequential.png' width=750/>

**Figure**: Joint multi-attribute edits using DyStyle model.

Great diversity and photorealism have been achieved by unconditional GAN frameworks such as StyleGAN and its variations. In the meantime, persistent efforts have been made to enhance the semantic controllability of StyleGANs. For example, a dozen of style manipulation methods have been recently proposed to perform attribute-conditioned style editing. Although some of these methods work well in manipulating the style codes along one attribute, the control accuracy when jointly manipulating multiple attributes tends to be problematic. To address these limitations, we propose a Dynamic Style Manipulation Network (DyStyle) whose structure and parameters vary by input samples, to perform nonlinear and adaptive manipulation of latent codes for flexible and precise attribute control. Additionally, a novel easy-to-hard training procedure is introduced for efficient and stable training of the DyStyle network. Extensive experiments have been conducted on faces and other objects. As a result, our approach demonstrates fine-grained disentangled edits along multiple numeric and binary attributes. Qualitative and quantitative comparisons with existing style manipulation methods verify the superiority of our method in terms of the attribute control accuracy and identity preservation without compromising the photorealism. The advantage of our method is even more significant for joint multi-attribute control.

[[paper]()]

## Demo

### Single Attribute edits

examples when editing facial expressions on real face. 
<p>
<img src='pics/13.gif' width=200 /><img src='pics/14.gif' width=200 /><img src='pics/15.gif' width=200 /><img src='pics/16.gif' width=200 />
</p>
examples when editing pupil color, hair color, mouth size and hair length on anime face. 
<p>
<img src='pics/S9.gif' width=200 /><img src='pics/S10.gif' width=200 /><img src='pics/S11.gif' width=200 /><img src='pics/S12.gif' width=200 />
</p>
examples when editing eye, mouth, yaw and age on cat face.
<p>
<img src='pics/C1.gif' width=200 /><img src='pics/C2.gif' width=200 /><img src='pics/C3.gif' width=200 /><img src='pics/C4.gif' width=200 />

<img src='pics/C5.gif' width=200 /><img src='pics/C6.gif' width=200 /><img src='pics/C7.gif' width=200 /><img src='pics/C8.gif' width=200 />

<img src='pics/C9.gif' width=200 /><img src='pics/C10.gif' width=200 /><img src='pics/C11.gif' width=200 /><img src='pics/C12.gif' width=200 />
</p>

### Multiple Attribute Edits

examples when editing both yaw and glass on real face.

images before editing
<p>
<img src='pics/LO1.png' width=200 /><img src='pics/LO2.png' width=200 /><img src='pics/LO3.png' width=200 /><img src='pics/LO4.png' width=200 />
</p>

images after editing
<p>
<img src='pics/L1.gif' width=200 /><img src='pics/L2.gif' width=200 /><img src='pics/L3.gif' width=200 /><img src='pics/L4.gif' width=200 />
</p>

Real photo editing reconstructed with [pSp](https://github.com/eladrich/pixel2style2pixel) and edited with DyStyle. 

<p>
<img src='pics/real/R1.gif' width=150 /><img src='pics/real/R4.gif' width=150 /><img src='pics/real/R3.gif' width=150 /><img src='pics/real/R2.gif' width=150 /><img src='pics/real/R5.gif' width=150 />


<img src='pics/real/A1.gif' width=150 /><img src='pics/real/A4.gif' width=150 /><img src='pics/real/A3.gif' width=150 /><img src='pics/real/A2.gif' width=150 /><img src='pics/real/A5.gif' width=150 />

<img src='pics/real/B1.gif' width=150 /><img src='pics/real/B4.gif' width=150 /><img src='pics/real/B3.gif' width=150 /><img src='pics/real/B2.gif' width=150 /><img src='pics/real/B5.gif' width=150 />
</p>


## Installation

1. Clone this repo.
2. This code require PyTorch, Python 3+. Please install the dependencies by

```sh
conda env create -f environment.yml
```

## Editing Images with Pretrained Model

Before editing images, you need to [prepare](test.md) the **checkpoint**, **GAN generator** and **edit config**.

Then you can just run the following scripts,

```
sh run_test_adult.sh [device_id]
sh run_test_anime.sh [device_id]
sh run_test_cat.sh [device_id]
sh run_test_dog.sh [device_id]
```

## Training DyStyle Model

Before training DyStyle Model, you need to [prepare](train.md) the **GAN generator**, **Attribute Classifier** and **model config**.

Then you can just run the following scripts,

```
sh run_train_adult.sh [device_id]
sh run_train_anime.sh [device_id]
sh run_train_cat.sh [device_id]
sh run_train_dog.sh [device_id]
```

## License

©ByteDance, 2021. For academic and non-commercial use only.


## Citation

To be updated.
