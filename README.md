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
- [EASE](https://arxiv.org/pdf/1905.03375.pdf)
- [VAE](https://arxiv.org/pdf/1802.05814)
- [DAE](https://arxiv.org/pdf/1802.05814)


## TO DO:
- Check which dataset you want to use from [here](https://drive.google.com/drive/u/2/folders/1mX0QMJ8kHTlU-ziK95SWvZb0ehjl5FWb)
- Download and extract the preferred

### Set the framework configuration
- Modify cfg.JSON file from https://github.com/cedo1995/GenRS/tree/master/Cfg

- Check if **path** contains the path to your chosen dataset file
- Check separator (**sep**) used in selected dataset and update it if necessary
- Check **algos** you want to compute respecting the list of string *lowercase* format as predefined
- Define the number of *users* to use as *validation* and *test set* through **heldout_us_val** and **heldout_us_test** param
- Check **metrics** you want to compute from: ["precision@k", "recall@k", "ndcg@k", "ap@k", "auc"]

### Set algorithms configuration
- Download {*alg*}_cfg.JSON where {alg} correspond to name of algos previously set in **algos** parameter in cfg.JSON file.
There must be exactly the same number of {*alg*}_cfg.JSON files and algos set into cfg.JSON file.


### Import RecSys module by:
from GenRS.Main.rec_sys import RecSys

### Define the path to cfg.JSON file and {alg}_cfg.JSON files

### Execute
RecSys(path_frm_cfg, list_algs_cfg_path)

### Results will be into *console.log.txt* file
