# Self-Supervised Contrastive Learning for Colon Pathology Classification


 <div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/contrastive-ssl-pathology/blob/master/Self_Supervised_Contrastive_Learning_for_Colon_Pathology_Classification.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
 </div>


Self-supervised learning, or SSL, has become a modern way to learn the hidden representation of data points. A dataset is not always provided with a label that marks a data point's category or value. SSL mitigates this issue by projecting a data point into an embedding vector representing information beneath. SSL can be trained contrastively, i.e., to measure the similarity of the projected embedding using certain metrics, e.g., cosine similarity, Euclidean distance, Manhattan distance, etc. By learning the latent representation, the SSL model can be utilized as a pre-trained model and fine-tuned as needed. The SSL model is divided into three parts: the backbone feature extractor, the embedding projection head, and the classification head. The backbone feature extractor leverages ResNet 18. Here, two other models are also introduced: the baseline model and the fine-tuned pre-trained SSL model. Both of them consist of a backbone feature extractor and a classification head. Yet, the latter makes use of the trained SSL model's backbone as its own backbone. To evaluate the performance of the models, the PathMNIST of the MedMNIST dataset is utilized.


## Experiment


Click [here](https://github.com/reshalfahsi/contrastive-ssl-pathology/blob/master/Self_Supervised_Contrastive_Learning_for_Colon_Pathology_Classification.ipynb) to carry out experiments on the baseline model, the SSL model, and the fine-tuned pretrained SSL model.


## Result

## Quantitative Result

The table below presents the quantitative result of the models on the test set.

Model | Loss | Accuracy |
------------ | ------------- | ------------- |
Baseline |  0.367 | 91.89% |
SSL | 0.480 | 86.32% |
Fine-tuned | 0.438 | 91.05% |


## Validation Accuracy and Loss Curve

<p align="center"> <img src="https://github.com/reshalfahsi/contrastive-ssl-pathology/blob/master/assets/val_acc_curve.png" alt="loss_curve" > <br /> Comparison of accuracy curves between the baseline model, the SSL model, and the fine-tuned pre-trained SSL model on the validation set </p>

<p align="center"> <img src="https://github.com/reshalfahsi/contrastive-ssl-pathology/blob/master/assets/val_loss_curve.png" alt="loss_curve" > <br /> Comparison of loss curves between the baseline model, the SSL model, and the fine-tuned pre-trained SSL model on the validation set </p>


## Qualitative Result

The qualitative results of the model on the inference set are shown below.

<p align="center"> <img src="https://github.com/reshalfahsi/contrastive-ssl-pathology/blob/master/assets/baseline_qualitative.png" alt="baseline_qualitative" > <br /> The qualitative result of the baseline model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/contrastive-ssl-pathology/blob/master/assets/ssl_qualitative.png" alt="ssl_qualitative" > <br /> The qualitative result of the SSL model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/contrastive-ssl-pathology/blob/master/assets/fine-tuned_qualitative.png" alt="fine-tuned_qualitative" > <br /> The qualitative result of the fine-tuned pre-trained SSL model. </p>


## Credit

- [Semi-supervised image classification using contrastive pretraining with SimCLR](https://keras.io/examples/vision/semisupervised_simclr/)
- [MedMNIST v2 - A large-scale lightweight benchmark for 2D and 3D biomedical image classification](https://medmnist.com/)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
