# SMS Spam Classifier

A small machine learning project that uses TF-IDF and logistic regression to classify English SMS messages as spam or ordinary messages (`ham`).

## Data preparation

The [notebook](sms_spam_classifier.ipynb) loads the dataset, removes duplicate messages after normalizing case and whitespace, and summarizes the label distribution. Of the 5,574 original messages, 5,159 are unique. The unique messages include 4,517 ordinary messages and 642 spam messages.

## Run locally


```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

Open `sms_spam_classifier.ipynb` and select **Run → Run All Cells**.

## Dataset

Almeida, T. and Hidalgo, J. (2011). *SMS Spam Collection* [Dataset]. UCI Machine Learning Repository. [DOI: 10.24432/C5CC84](https://doi.org/10.24432/C5CC84).

The [UCI dataset page](https://archive.ics.uci.edu/dataset/228/sms+spam+collection) lists the data under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The bundled data file is unchanged. The original dataset notes are in [data/original-readme.txt](data/original-readme.txt).
