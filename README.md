# Reproducing a CNN for Sentence Classification on the Rotten Tomatoes Dataset

**Deep Learning · M.Sc. Applied Data Science and AI · SRH University Munich · Winter semester 2026/27**

**Author(s):** Ashok Rai · **Repository:** [deep-learning-sentiment-analysis](https://github.com/ashok-rai/deep-learning-sentiment-analysis) · **Date:** 22 October 2026

## Abstract

This project investigates binary sentiment classification of movie reviews using a convolutional neural network (CNN). The implementation is based on Yoon Kim's paper, *Convolutional Neural Networks for Sentence Classification* (2014), and uses the Rotten Tomatoes dataset from Hugging Face. A TF-IDF + Logistic Regression model will be established as a baseline, followed by experiments with the CNN using fixed and trainable word embeddings. Model performance will be evaluated using classification metrics such as accuracy and F1-score, with results compared against the published findings where the experimental settings are comparable. Finally, the effect of the selected model variation will be measured and reported after the experiments are completed.

## 1 · The paper and the task

### Paper

Kim, Y. (2014). *Convolutional Neural Networks for Sentence Classification.* Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 1746–1751.

Paper: https://aclanthology.org/D14-1181/

### Task

The model takes a movie-review sentence from the Rotten Tomatoes dataset as input and predicts whether its sentiment is positive or negative. The task is binary sentiment classification, with two output classes: negative (0) and positive (1).

### Their method in our own words

Kim (2014) presents a sentence-classification approach using a convolutional neural network (CNN). First, each word is represented as a dense vector using word embeddings. Convolutional filters process groups of neighbouring word vectors to learn useful local features, such as patterns that may indicate positive or negative sentiment. Max-over-time pooling selects the strongest feature responses, and a fully connected classification layer produces the final sentiment prediction.

The model is trained using labelled sentences and a classification loss. The paper investigates different word-embedding configurations, including static embeddings, which remain fixed during training, and non-static embeddings, which can be updated through backpropagation.

For our project, we will implement the CNN approach and investigate the effect of fixed versus trainable word embeddings using the Rotten Tomatoes dataset hosted on Hugging Face.

### Their main result

Kim (2014) reports experimental results across several sentence-classification datasets in **Table 2** of the paper. For the Rotten Tomatoes dataset, the paper reports **76.1% accuracy** for its CNN with static word vectors and **76.1% accuracy** for its CNN with non-static word vectors.

These published results will serve as reference points when assessing how closely our implementation reproduces the paper's findings. Differences in dataset version, preprocessing, model configuration, and training procedure may affect comparability.

**Our current status:** The paper and dataset have been selected. Implementation, baseline evaluation, and CNN experiments are still planned; our own results will be reported after the experiments have been completed.


## 2 · The data (start this week)

| | |
|---|---|
| Source and version | [where from, which version, download date] |
| Licence | [licence, and what it allows] |
| Size | [number of samples, size of each sample] |
| Classes or targets | [list; class balance as counts or a bar chart] |
| Splits | [training / validation / test sizes; **how** you split: random, grouped (by patient, place, …), by time; why] |
| Preprocessing | [resizing, standardisation (statistics from the training set only), cleaning] |
| Leakage checks | [duplicates between splits? the same patient/place/time in two splits? preprocessing fitted on all data? what you did about it] |
| Shared with Biomedical Image Analysis? | [yes/no; if yes: which preparation was done for BIA, and say that it is not graded again here] |

[Two or three example samples per class, as a figure.]

## 3 · Reproducing the baseline (part of 15 %, and 25 % implementation)

**The recipe:** read the paper (or its code) like a recipe. One row per ingredient; leave nothing empty: if the paper does not say it, write "not stated" and what you chose.

| | The paper says | Where (page, table, code) | What we use |
|---|---|---|---|
| Data: version, split | | | |
| Model: layers, sizes, pretrained? | | | |
| Training: optimiser, learning rate, schedule | | | |
| Training: epochs, batch size | | | |
| Augmentation and preprocessing | | | |
| Metric, and how it was averaged | | | |

- **Setup:** [framework and versions; anything not in the table]
- **What the paper did not say,** and what you chose instead: [list, from the "not stated" rows]

| | Paper | Ours (mean ± spread, n seeds) |
|---|---|---|
| [metric] | [value] | [value] |

[Why the numbers differ, if they do: data version, preprocessing, compute, missing details. A difference that you explain is a result, too.]

## 4 · Your improvement (20 %)

- **Idea:** [what you change]
- **Why it should help:** [the reasoning: a weakness of the baseline you observed, a method from the course or from another paper]
- **Expected effect:** [what you expect to see, and on which metric]

## 5 · Experiments (part of 20 % and 15 %)

- **Design:** one change at a time; the same data splits, the same budget; at least three seeds per setting.

| Setting | [metric] mean | ± spread | seeds |
|---|---|---|---|
| baseline | | | |
| + [change 1] | | | |
| + [change 2] | | | |

- **Statistical comparison:** [test and result, for example a paired test over seeds or folds (Session 31)]
- **Test set:** used **once**, for the final models only.

## 6 · Evaluation and error analysis (15 %)

- [Metrics that fit the task (not only accuracy): confusion matrix, precision, recall, F1, IoU, …]
- [Where does the model fail? Examples of its most confident mistakes; which classes are confused, and why]
- [Limitations: what your results do **not** show]

## 7 · Conclusion

[What you reproduced, what you improved, what you would try next.]

## 8 · Use of AI tools (5 %)

[Which tools you used, for what (code, text, debugging), and how you **checked** their output. Be specific.]

## 9 · Reproducibility (part of 25 %)

- **Run it:** [the commands or notebook order; the environment, for example `requirements.txt`]
- **Seeds and hardware:** [seeds used; GPU or CPU; training time]
- **Where the results come from:** [which notebook/script makes which table and figure]

## References

[All papers, data sets, code and websites you used.]
