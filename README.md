## Object detection from High-Resolution Aerial Imagery

## Annotated Aerial Imagery Dataset

The hihg-resolution imageries are collected from [Land Board of Republic of Estonia](https://geoportaal.maaamet.ee/). We use [CVAT](https://github.com/opencv/cvat) to annotate the objects of interest. In this dataset the objects of interest are Car, Airplane, Bus, Watercraft, Building and Truck. These imageries are high-resolution with 1:2000 scale. Moreover, the images were captured from 1250m altitude, with focal length of 120mm by using Leica ADS100-SH100 . The imagery dimension is 10000x10000 pixels. The Ground Sample Distance for these orthophotos is 10cm (quite high).

The training dataset contains overall 236 images. Every object of interest in those images are annotated. Totally making ~18k object instances.
In the following table we can see the distribution of the objects of interest in both test and training datasets.

![Image](/data/dataset_distr.png)

Additionally there are 2 more test datasets where we have downsampled the original test images by a factor of 2 and 4 respectively. By this way we increase the GSD by a factor 2 and 4 respectively. As a result we get the new datasets of images where the GSD is 20cm and 40cm respectively. This produces the images as if they are taken from 2/4 times higher altitude. As we can see from the following table the to differ the datasets we concatenate their respective GSD values to end of the dataset. E.g Dataset10

![Image](/data/test_datasets.png)

## Data Processing

Furthermore, if you would like to downsample the images further you can use the script that is in [data_processing](/data_processing)

## Usage of the dataset

If you wish use this dataset in your works please refer please use the following BibTeX entry.

@misc{wu2019detectron2,
author = {Majnun Abdurahmanov},
title = {High-resolution aerial imagery dataset},
howpublished = {\url{https://github.com/MajnunMan/High-resolution-aerial-imagery-dataset}},
year = {2020}
}
