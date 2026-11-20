# SMS Spam Classifier

A small machine learning project that uses TF-IDF and logistic regression to classify English SMS messages as spam or ordinary messages (`ham`).

The [Jupyter notebook](sms_spam_classifier.ipynb) includes class counts, a majority-class baseline, a confusion matrix, examples of model errors, and a cell for trying your own messages. The dataset is bundled, so the notebook runs offline after you install the dependencies.

## Run locally

Use Python 3.11 or newer. Open a terminal in the project folder. If you use Anaconda on Windows, open Anaconda Prompt.

```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

Open `sms_spam_classifier.ipynb` and select **Run → Run All Cells**.

## Results

After removing duplicates, 5,159 of the 5,574 messages remained. The test split used 20% of the unique messages, with stratification by label and random seed 42. The vectorizer and classifier were fitted on the training split.

| Model | Accuracy | Spam precision | Spam recall | Spam F1 |
| --- | ---: | ---: | ---: | ---: |
| Majority baseline | 87.6% | 0.0% | 0.0% | 0.0% |
| TF-IDF + logistic regression | 98.3% | 91.7% | 94.5% | 93.1% |

The model caught 121 of 128 spam messages and incorrectly flagged 11 of 904 ordinary messages. These scores describe one held-out split of a historical English-language corpus. Performance on current SMS and other languages is unmeasured.

## Dataset

Almeida, T. and Hidalgo, J. (2011). *SMS Spam Collection* [Dataset]. UCI Machine Learning Repository. [DOI: 10.24432/C5CC84](https://doi.org/10.24432/C5CC84).

The [UCI dataset page](https://archive.ics.uci.edu/dataset/228/sms+spam+collection) lists the data under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The bundled data file is unchanged. The original dataset notes are in [data/original-readme.txt](data/original-readme.txt).
