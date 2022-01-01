
# Stratified Experience Replay (SER) with Deep Q learning
** PyTorch implementation of our paper titled _Stratified Sampling Based Experience Replay for Efficient Camera Selection Decisions_,  2020 **

_Anil Sharma, Mayank Pal, Saket Anand, Sanjit K. Kaul_

[[Paper](https://www.computer.org/csdl/proceedings-article/bigmm/2020/09232593/1o56ALOzkeA)] [[BibTeX](https://www.computer.org/csdl/api/v1/citation/bibtex/proceedings/1o56xuliEpi/09232593)]

---

## Code

The code is organized as follows:
1. ```scripts``` is the main folder from where training and testing scripts can be found. All codes are in jupyter notebook. It also contains notebook to reproduce the plots from the paper. 
2. ```data``` It contains data files for all datasets (all 4 sets of NLPR MCT, Duke). It also contains scripts to read these data files and also the training testing split as used in our ICAPS [paper](https://github.com/anilsh/scheduleQueries). Original images of the dataset can be downloaded from the dataset website. 

## Downloading the data

### NLPR MCT benchmark dataset

Download the dataset from the [[official website](http://mct.idealtest.org/Datasets.html)] . This dataset contains four sub-datasets and we have used all four in our method. 
We have converted all datasets into trajectory files and only these are used by our method. These are placed in ```data``` folder and necessary scripts are provided to read the files and training/testing split.

---

## Running the tracker

In scripts folder, run ```Q_SER_db4_test.ipynb``` to run with the pretrained models, the script runs for NLPR set-4. To change the dataset, change the variable ```db_no```. The details of the dataset can be checked from ```get_pid_test_train.py``` in data folder.  


### Dependencies

The code requires pytorch 1.1.0 and jupyter notebook (should work well with Python 3.5). Apart from it, you need to install scipy, matplotlib, numpy and hickle for loading and plotting purposes. 

### Pre-trained model

The pre-trained model and results for each specific case of the simulation are provide in 'models' . 

### Tables and Figures
In folder 'plots', you will find notebook to reproduce all analysis figure reported in the paper. 


### Training

To train a model from scratch, use ```Q_SER_db4_train.ipynb``` to train SER based policy for NLPR set-4. To train for a different dataset, change ```db_no``` in the notebook accordingly. 

---

If this code helps your research, please cite the following work which made it possible.

```
@inproceedings{sharmaScheduleCameras,
  title =        {Reinforcement Learning based Querying in Camera Networks for Efficient Target Tracking},
  author =       {Sharma, Anil and Anand, Saket and Kaul, Sanjit},
  booktitle =    {ICAPS},
  year =         {2019}
}

@INPROCEEDINGS {9232593,
author = {A. Sharma and M. K. Pal and S. Anand and S. K. Kaul},
booktitle = {2020 IEEE Sixth International Conference on Multimedia Big Data (BigMM)},
title = {Stratified Sampling Based Experience Replay for Efficient Camera Selection Decisions},
year = {2020},
pages = {144-151},
doi = {10.1109/BigMM50055.2020.00029},
url = {https://doi.ieeecomputersociety.org/10.1109/BigMM50055.2020.00029},
publisher = {IEEE Computer Society}
}



```

## License

This code is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/). Some external dependencies have their own license.

