ML Project - Image Captioning with Attention-based LSTM Decoder

How to Run
1. Open the file in Google Colab
2. Runtime > Change runtime type > T4 GPU
3. Runtime > Run All
4. Expected runtime is around 70 mins

The notebook will:
- Download and extract the Flickr8k dataset
- Build the vocabulary
- Train the model for 10 epochs
- Evaluate BLEU-4 score
- Generate sample captions with images

Requirements
All are installed automatically in Colab.
- Python 3.x
- PyTorch
- torchvision
- Pillow
- NLTK
- matplotlib

References
- Xu et al., "Show, Attend and Tell" (ICML 2015)
- Vinyals et al., "Show and Tell" (CVPR 2015)
- He et al., "Deep Residual Learning" (CVPR 2016)
- Flickr8k Dataset - Hodosh et al. (2013)

