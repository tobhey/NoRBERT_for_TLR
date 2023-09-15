![GitHub](https://img.shields.io/github/license/tobhey/NoRBERT)

# NoRBERT for Requirements Classification in Traceability Link Recovery Datasets

This respository contains all code needed to train and evaluate binary classifiers for predicting the functional aspects present in a requirement element.
It is based on [NoRBERT](https://doi.org/10.1109/RE48521.2020.00028) and applies it to a labeled dataset combined of the [relabeled Promise NFR dataset](https://doi.org/10.5281/zenodo.3309669) and a [labeled dataset of requirement elements from five traceability link recovery benchmark datasets](https://doi.org/10.5281/zenodo.7867845).

## Requirements
You need to install [Jupyter](https://jupyter.org/install).
Furthermore, you might have to install further python dependencies than the ones installed in the notebook (first cell) depending on your python installation.
You have to make sure that you installed all python libraries that are imported in the second cell via pip.
It is neccessary to install [PyTorch](https://pytorch.org/get-started/locally/#start-locally).
You will need a machine with a very potent GPU (at least 12GB GPU RAM for the large models) as the pretrained BERT model is very memory hungry.
Also, you have to make sure that your GPU and drivers support CUDA.
We recommend Ubuntu as operating system.

We used Python 3.7 and corresponding dependency versions.
For special requirements see [requirements.txt](./requirements.txt).

## Dataset

The dataset contains a gold standard for classifying parts of requirements in five traceability link recovery benchmark datasets.

### Classification

For aspect classification:
* functional aspects (F)
* quality aspects (Q)

For concerns in functional requirements (c.f. [NoRBERT publication](https://doi.org/10.1109/RE48521.2020.00028)):
* Function: A function that a system shall perform
* Behavior: Behavior, the system displays or reactions that are triggered by one or more stimuli
* Data: A data item or data structure that shall be part of a system's state
UserRelated: Behavior of the user or functionality of the system attributable to the user

## Attribution (of datasets used)
The relabeled Promise dataset can be attributed to Dalpiaz et al.:
F. Dalpiaz, D. Dell’Anna,  F. B. Aydemir, and  S. Çevikol, “explainable-re/re-2019-materials,” Jul.2019. https://doi.org/10.5281/zenodo.3309669

The TLR dataset comprises preprocessed requirements of the eTour, iTrust, SMOS, eAnci and LibEST datasets. As SMOS and eAnci's original requirements were written in Italian, the dataset comprises automatically translated versions of the requirements to English. The datasets were retrieved from the website of the Center of Excellence for Software & Systems Traceability (CoEST). 

Attribution for the datasets:

The original eTour dataset was provided for the TEFSE challenge at 6th International Workshop on Traceability in Emerging Forms of Software Engineering (TEFSE), 2011 and was retrieved from http://coest.org/

The iTrust dataset was retrieved from http://coest.org/

The original SMOS and eAnci datasets can be attributed to Gethers et al., On integrating orthogonal information retrieval methods to improve traceability recovery. In 2011 27th IEEE International Conference on Software Maintenance (ICSM), Sep. 2011 and were retrieved from http://coest.org/ 

The LibEST dataset can be attributed to Moran et al., Improving the Effectiveness of Traceability Link Recovery using Hierarchical Bayesian Networks. In 2020 IEEE/ACM 42nd International Conference on Software Engineering (ICSE), May 2020 and was retrieved from https://gitlab.com/SEMERU-Code-Public/Data/icse20-comet-data-replication-package
