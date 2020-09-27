# Positive-Unlabeled Learning with Arbitrarily Non-Representative Labeled Data

[![docs](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/ZaydH/udl_arbitrary_pu/blob/master/LICENSE)

**Venue**: [ICML 2020 Workshop on Uncertainty & Robustness in Deep Learning (UDL)](https://sites.google.com/view/udlworkshop2020/home)  
**Author**: [Zayd Hammoudeh](https://ZaydH.github.io/) and [Daniel Lowd](https://ix.cs.uoregon.edu/~lowd/)

This repository contains the source code associated for the UDL'20 paper entitled "Positive-Unlabeled Learning with Arbitrarily Non-Representative Labeled Data"

## Latest Version

Official version of the paper published at NeurIPS'20.  See the official and latest version of the [aPU learner repository](https://github.com/ZaydH/arbitrary_pu).  Please open issues in that repository.

## Running the Program

To run the program, enter the `src` directory and call:

`python driver.py ConfigFile`

where `ConfigFile` is one of the `yaml` configuration files in folder `src/configs`. If CUDA is installed on your system, the program enables CUDA execution automatically.

### First Time Running the Program

The first time the program is run, it will download any necessary dataset and create any transfer learning representations automatically.  Please note that this process can be time consuming --- in particular for 20 Newsgroups where creating the ELMo-based embeddings can take several hours.

These downloaded files are stored in a folder `.data` that is in the same directory as `driver.py`.

### Results

Results are printed to the console. The tool also creates a folder named `res` in the same directory as `driver.py` where it exports results in CSV (comma separated value) format.

### Requirements

Our implementation was tested in Python 3.6.5.  Minimum testing was performed with 3.7.1 but `requirements.txt` may need to change depending on your local Python configuration.  It uses the [PyTorch](https://pytorch.org/) neural network framework, version 1.3.1 and 1.4.  For the full requirements, see `requirements.txt` in the `src` directory.

We recommend running our program in a [virtual environment](https://docs.python.org/3/tutorial/venv.html).  Once your virtual environment is created and *active*, run the following in the `src` directory:

```
pip install --user --upgrade pip
pip install -r requirements.txt
```

### License

[MIT](https://github.com/ZaydH/udl_arbitrary_pu/blob/master/LICENSE).

### Acknowledgements

This repository includes an implementation of PUc [1] that was provided by the tool's author [Tomoya Sakai](https://t-sakai-kure.github.io/).

## References

[1] Tomoya Sakai and Nobuyuki Shimizu. Covariate shift adaptation on learning from positive and unlabeled data. In Proceedings of the AAAI Conference on Artificial Intelligence, volume 33, pp. 4838-4845, July 2019.
