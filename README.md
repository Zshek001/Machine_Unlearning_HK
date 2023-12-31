# Machine Unlearning HK 
A shared learning space for [2023 Kaggle competition "Machine unlearning"](https://www.kaggle.com/competitions/neurips-2023-machine-unlearning). Just some undergrad friends in HKU & CUHK & UST interested in DL advances. 

## The machine unlearning introduction from Kaggle

> machine unlearning is an emergent subfield of machine learning that aims to remove the influence of a specific subset of training examples — the "forget set" — from a trained model. Furthermore, an ideal unlearning algorithm would remove the influence of certain examples while maintaining other beneficial properties, such as the accuracy on the rest of the train set and generalization to held-out examples.
> 
> A straightforward way to produce this unlearned model is to retrain the model on an adjusted training set that excludes the samples from the forget set. However, this is not always a viable option, as retraining deep models can be computationally expensive. An ideal unlearning algorithm would instead use the already-trained model as a starting point and efficiently make adjustments to remove the influence of the requested data.

## Problem statement by kaggle

The competition considers a realistic scenario in which an **age predictor** has been trained on face images, and, after training, a **certain subset of the training images must be forgotten to protect the privacy or rights of the individuals concerned**.

Your goal is to submit code that **takes as input _the trained predictor, the forget and retain sets_, and outputs _the weights of a predictor_ that has unlearned the designated forget set**. We will evaluate submissions based on both the strength of the forgetting algorithm and model utility. We also enforce a hard cut-off that rejects unlearning algorithms that run slower than a fraction of the time it takes to retrain. A valuable outcome of this competition will be to characterize the trade-offs of different unlearning algorithms.

![alt text](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiRnut8P03hlk5tKJPEEsqUl1DSlqN2ScdJeiaRfC3mWbQ_PBBwf7wBU9xgxuzr1GoqgkB6MwCa6Zrdo6LQxSOIPXIUrl1Yug73k2Q2zFI61VDAi9K21JOPox0Hc1CIh6ShKxW9Tgy45TYV3p3r5IiI7yxzzzOpzvbJ-5o3QVtjZn6vhDZLntnCcUSi1mb_/s720/image1.png)

## Resource

### Official reference from kaggle site
- 2017 **[Membership Inference Attacks against Machine Learning Models](https://arxiv.org/abs/1610.05820)**
> We quantitatively investigate how machine learning models leak information about the individual data records on which they were trained. We focus on the basic membership inference attack: given a data record and black-box access to a model, determine if the record was in the model's training dataset. To perform membership inference against a target model, we make adversarial use of machine learning and train our own inference model to recognize differences in the target model's predictions on the inputs that it trained on versus the inputs that it did not train on.
We empirically evaluate our inference techniques on classification models trained by commercial "machine learning as a service" providers such as Google and Amazon. Using realistic datasets and classification tasks, including a hospital discharge dataset whose membership is sensitive from the privacy perspective, we show that these models can be vulnerable to membership inference attacks. We then investigate the factors that influence this leakage and evaluate mitigation strategies.

- 2021 **[Membership Inference Attacks From First Principles](https://arxiv.org/abs/2112.03570)**
> A membership inference attack allows an adversary to query a trained machine learning model to predict whether or not a particular example was contained in the model's training dataset. These attacks are currently evaluated using average-case "accuracy" metrics that fail to characterize whether the attack can confidently identify any members of the training set. We argue that attacks should instead be evaluated by computing their true-positive rate at low (e.g., <0.1%) false-positive rates, and find most prior attacks perform poorly when evaluated in this way. To address this we develop a Likelihood Ratio Attack (LiRA) that carefully combines multiple ideas from the literature. Our attack is 10x more powerful at low false-positive rates, and also strictly dominates prior attacks on existing metrics.

### The Machine Unlearning: papers
- 2020 **[Machine Unlearning](https://arxiv.org/abs/1912.03817)**
> Once users have shared their data online, it is generally difficult for them to revoke access and ask for the data to be deleted. Machine learning (ML) exacerbates this problem because any model trained with said data may have memorized it, putting users at risk of a successful privacy attack exposing their information. Yet, having models unlearn is notoriously difficult. We introduce SISA training, a framework that expedites the unlearning process by strategically limiting the influence of a data point in the training procedure. While our framework is applicable to any learning algorithm, it is designed to achieve the largest improvements for stateful algorithms like stochastic gradient descent for deep neural networks. SISA training reduces the computational overhead associated with unlearning, even in the worst-case setting where unlearning requests are made uniformly across the training set. In some cases, the service provider may have a prior on the distribution of unlearning requests that will be issued by users. We may take this prior into account to partition and order data accordingly, and further decrease overhead from unlearning. Our evaluation spans several datasets from different domains, with corresponding motivations for unlearning. Under no distributional assumptions, for simple learning tasks, we observe that SISA training improves time to unlearn points from the Purchase dataset by 4.63x, and 2.45x for the SVHN dataset, over retraining from scratch. SISA training also provides a speed-up of 1.36x in retraining for complex learning tasks such as ImageNet classification; aided by transfer learning, this results in a small degradation in accuracy. Our work contributes to practical data governance in machine unlearning.




## To be constructed
- Problem formulation
- literatures
- codes sample from kaggle
