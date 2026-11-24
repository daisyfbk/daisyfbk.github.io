---
contribution: FLADFlower
people:
  - RobertoDoriguzziCorin
  - SilvioCretti
peopleOrder: surname
---

FLAD (a Federated Learning approach to DDoS Attack Detection) is an adaptive Federated Learning (FL) approach for training feed-forward neural networks that implements a mechanism to monitor the classiﬁcation accuracy of the global model on the clients’ validations sets, without requiring any exchange of data. Thanks to this mechanism, FLAD can estimate the performance of the aggregated model and dynamically tune the FL process by assigning more computation to those clients whose attack profiles are harder to learn.

[Flower](https://flower.ai/) is a framework that provides a high-level interface for implementing FL strategies and managing the communication between the server and clients. Flower also offers a collection of _baselines_ that are community-contributed reproductions of experiments from published FL papers. Contributors can add new baselines by implementing the method described in a paper and reproducing its experiments with Flower.

FBK's DAISY research unit contributed FLAD to Flower by implementing a new [baseline](https://github.com/flwrlabs/flower/tree/main/baselines/flad) that integrates the adaptive federated learning approach into the Flower framework.

## What has been contributed

The contributed baseline includes both an implementation of the FLAD strategy and the code needed to reproduce a portion of the experiments presented in the paper

_Roberto Doriguzzi-Corin, Domenico Siracusa, "FLAD: Adaptive Federated Learning for DDoS Attack Detection", Computers & Security 137 (2024)._

Specifically, the implemented experiments focus on the evaluation of the convergence of the FLAD strategy on a highly non-i.i.d dataset of heterogeneous DDoS attacks.

The dataset used for the experimentation is a preprocessed, repartitioned derivative of the CIC-DDoS2019 dataset originally by the Canadian Institute for Cybersecurity of the University of New Brunswick (UNB). More details are available on [the dataset page](https://www.unb.ca/cic/datasets/ddos-2019.html) and in the paper.

_Iman Sharafaldin, Arash Habibi Lashkari, Saqib Hakak, and Ali A. Ghorbani, "Developing Realistic Distributed Denial of Service (DDoS) Attack Dataset and Taxonomy", IEEE 53rd International Carnahan Conference on Security Technology, Chennai, India, 2019\._

This derived dataset, named DOS2019_highly_unbalanced, is available on the [Hugging Face Hub](https://huggingface.co/datasets/silviocretti/DOS2019_highly_unbalanced).
