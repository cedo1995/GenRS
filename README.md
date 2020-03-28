# GenRS
A generative learning-based Framework for Recommendation Systems algorithms

# Software requirements:
- Python 3.6 or higher
- Tensorflow 1.15 GPU
- Numpy 1.17
- Scipy 1.3
- Pandas 0.25
- Bottleneck 1.3

# Algorithms list available:
- [CFGAN](https://dl.acm.org/doi/pdf/10.1145/3269206.3271743?casa_token=INiS3p2UrDAAAAAA:EQRrS7IBusVt_F8IYiAUtsIGGHHd17ki69QEcNkJwFkq5PuiBvX96OzC8CVcoWEkqhckTg8X7f4)
- [IRGAN](https://arxiv.org/pdf/1705.10513.pdf)
- EASE(https://arxiv.org/pdf/1905.03375.pdf)
- VAE(https://arxiv.org/pdf/1802.05814)
- DAE(https://arxiv.org/pdf/1802.05814)


## TO DO:
### Download datasets you want
- Check which dataset you want to use from Google Drive folder shorturl.at/oqBM4
- Download and extract the preferred into repository project folder

### Set the framework configuration in Data/cfg.JSON
- Check if **path** contains the path to your chosen dataset file 
- Check separator (**sep**) used in selected dataset and update if necessary
- Check **algos** you want to compute respecting the list of string *lowercase* format as predefined
- Define the number of *users* to use as *validation* and *test set* through **heldout_us_val** and **heldout_us_test** param
- Check **metrics** you want to compute from: ["precision@k", "recall@k", "ndcg@k", "ap@k", "auc"]

### Set the algorithms configuration in Data/*alg*_cfg.JSON where *alg* are the name previously set in **algos**

### Run Main/main.py

### Results will be into *console.log.txt* file

