# Siamese Network Example

Siamese network for image similarity estimation. The network is composed of two identical networks, one for each input. The output of each network is concatenated and passed to a linear layer.  The output of the linear layer passed through a sigmoid function. `["FaceNet"](https://arxiv.org/pdf/1503.03832.pdf)` is a variant of the Siamese network.

This implementation varies from FaceNet as we use the `ResNet-18` model from `["Deep Residual Learning for Image Recognition"](https://arxiv.org/pdf/1512.03385.pdf)` as our feature extractor. In addition, we aren't using `TripletLoss` as the MNIST dataset is simple, so `BCELoss` can do the trick.

```bash
pip install -r requirements.txt
python main.py
# CUDA_VISIBLE_DEVICES=2 python main.py  # to specify GPU id to ex. 2
```
