# The impacts of federated learning on CNNs with histological imagery: analysing domain-skews and class imbalance with lung tissue datasets.

  When building a histopathology classifier with CNNs we encounter two big challenges: how can we ensure privacy from hospital/lab data, deal with domain shifts from each source's image extraction methods and also deal with data imbalance from each local training node?

  Regarding the first challenge, federated learning comes as a powerful tool to descentrallize data and enable the training of big models with privacy at the cost of computation efficiency and speed. The premise of FL is simple: train small batches on client devices with local data and send the  model weights back to the server so its aggregated and averaged with all the other nodes.

  Challenge II. In the state of the art science, methods such as data normalization (Macenko et. al, for example) can be used to reduce domain differences on same-category data. However, that is not always reliable. This project aims to study the effects of training CNN models with domain skews using two different lung histology datasets: LC25000 and LungHist700.

  Challenge III. In real-life scenarios, clients with balanced amount of data is almost impossible. Some nodes will have a few units of samples while others might have thousands. Some nodes might have 90% of class X while others might have 90% of class Y. It is crucial that we ponder these divergences to ensure stable learning on our server model.

Our classification will consist of the following classes:
- lung adenocarcinoma (aca)
- lung squamous cell carcinoma (scc)
- benign lung tissue (nor)


_AI DISCLAIMER: Claude was used on this study to help coding/debugging dataset_split.py to eventually shorten the research's timespan invested on data processing._
