# Sentence Level Quality Estimation Task

This Github repository was made for the challenge Sentence Level Quality Estimation Task 2020 for the NLP course of Imperial College MSc Computing(ML/AI) 2019/2020

## Getting Started


Create a virtual environment and activate it with the following command lines (you need to create your
  environment with Python3.7):

```
python -m venv ./venv/
source venv/bin/activate
```

Install all the requirements with:

```
pip install -r requirements.txt
```

You need to run the following additional lines for some libraries

```
python -m laserembeddings download-models
python -m spacy download en_core_web_md
python -m spacy download de_core_news_md
```

Open a jupyter notebook from your venv:

```
venv/bin/jupyter notebook
```

The final step is to download the MUSE embeddings German and English vectors (which are so heavy it
  is impossible to git them) and put them in a folder called 'muse/' in 'data/'. They corresponds word embeddings aligned in the same vector space.

  English: https://dl.fbaipublicfiles.com/arrival/vectors/wiki.multi.en.vec <br/>
  German: https://dl.fbaipublicfiles.com/arrival/vectors/wiki.multi.de.vec

If the link is broken, they probably still can be found in the MUSE Github, in the section "Multilingual word Embeddings": https://dl.fbaipublicfiles.com/arrival/vectors/wiki.multi.de.vec
## How to use the repository

The repository contains two notebooks:

* feature_engineering_pipeline.ipynb which contains all the feature_engineering_pipeline which leads to the creation of a pickle dataset_with_features.pickle. This notebook takes approximately 30 minutes to run
so the dataset created has been stored and is available to test the models in the other notebook.
* model_testing.ipynb which permits to run models we have tried and used to compute our best performance. The end of the notebook can be run to get a model prediction to be tested on Codalab.

All the data necessary to run the notebooks has also been added in the folder /data.
