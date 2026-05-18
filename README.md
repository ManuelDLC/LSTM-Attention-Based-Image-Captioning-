# Image Captioning with Attention-Based LSTM

An end-to-end image captioning system combining a frozen ResNet-50 CNN encoder 
with a custom LSTM decoder and Bahdanau-style attention mechanism, trained on the Flickr8k dataset.

## Sample Outputs

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/e7b9f6d8-b977-4bae-b293-e790c6634f7a" />
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/50f9895e-6fde-4587-a76d-c2e890ed22df" />
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/96b4aed7-bbb7-42fd-8ce0-827e46ebb885" />

## Results

| Configuration | BLEU-4 |
|--------------|--------|
| Best         | 0.1069 |

Trained for 10 epochs on Flickr8k (8,091 images, 40,455 captions) across three experimental configurations.

## Architecture

- **Encoder:** Frozen ResNet-50 pretrained on ImageNet — extracts 49 spatial feature patches from each image
- **Attention:** Bahdanau-style additive attention — dynamically weights spatial patches at each decoding step
- **Decoder:** Custom LSTM implemented from scratch using four independent linear layers
- **Training:** Teacher forcing, gradient clipping, and doubly stochastic attention regularization

## How to Run

1. Open the file in Google Colab
2. Runtime → Change runtime type → T4 GPU
3. Runtime → Run All
4. Expected runtime: ~70 minutes (With T4 GPU)

The notebook will do the following automatically:
- Download and extract the Flickr8k dataset
- Build the vocabulary
- Train the model for 10 epochs
- Evaluate BLEU-4 score
- Generate sample captions with attention visualizations

## Requirements

All dependencies install automatically in Google Colab.

## References

- Xu et al., ["Show, Attend and Tell"](https://arxiv.org/abs/1502.03044) — ICML 2015
- Vinyals et al., ["Show and Tell"](https://arxiv.org/abs/1411.4555) — CVPR 2015  
- He et al., ["Deep Residual Learning for Image Recognition"](https://arxiv.org/abs/1512.03385) — CVPR 2016
- Hodosh et al., Flickr8k Dataset (2013)

