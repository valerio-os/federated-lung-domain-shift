# federated-lung-domain-shift

When building a histopathology classifier with CNNs we encounter two big challenges: how can we ensure privacy from hospital/lab data while also dealing with domain shifts from each source's image extraction methods?

Regarding the first challenge, federated learning comes as a powerful tool to descentrallize data and enable the training of big models with appropriate anonymization and computation efficiency. The premise of FL is simple: train small batches on client devices with local data and send the encrypted model weights back to the server so its aggregated and averaged with all the other nodes.

The second challenge is our main subject of study. In the state of the art science, methods such as data normalization can be used to reduce domain differences on same-category data. However, that is not always reliable. This project aims to study the effects of training CNN models with domain skews using two different lung histology datasets: LC25000 and LungHist700.

Our classification will consist of the following classes:
- lung adenocarcinoma
- lung squamous cell carcinoma
- benign lung tissue
