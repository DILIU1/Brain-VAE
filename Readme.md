# Brain-VAE

Brain-VAE is a deep generative framework based on **Variational Autoencoders (VAE)** for modeling and generating full-brain EEG signals.  
This project provides reproducible code for training, evaluation, and visualization of EEG reconstruction and generation.  
It is designed to support **neural decoding**, **brain-computer interface (BCI)** applications, and **multimodal alignment** with image/text embeddings.

---

## Features

- **EEG-specific VAE architecture**  
  - Input: multi-channel EEG signals (default: 63 channels × 250 time points)  
  - Latent dimension: configurable (default: 63 × 128)  
  - Includes spectral enhancement and temporal modeling modules

- **EEG Generation & Reconstruction**  
  - Label-controllable EEG synthesis  
  - Evaluation in both time and frequency domains  
  - Latent feature consistency checks

- **Multimodal Extension**  
  - Supports integration with CLIP image embeddings  
  - Enables EEG–image semantic alignment and cross-modal generation

- **Reproducible Training**  
  - Provided Jupyter notebook (`Generation_EEG_all_VAE_63_128_Train_stable.ipynb`)  
  - Includes training pipeline, visualization, and evaluation metrics

---

## Repository Structure

```
Brain-VAE/
│
├── Generation_EEG_all_VAE_63_128_Train_stable.ipynb   # Main training & analysis notebook
├── environment.yml                                    # Conda environment specification
├── requirements.txt                                   # Python dependencies
└── README.md                                          # Project documentation
```

---

## Installation

### 1. Clone the repository
```
git clone https://github.com/DILIU1/Brain-VAE.git
cd Brain-VAE
```

### 2. Setup environment
Option A – Using conda:
```
conda env create -f environment.yml
conda activate brain-vae
```

Option B – Using pip:
```
pip install -r requirements.txt
```

---

## Usage

### 1. Prepare Data
- EEG data should be formatted as [N, C, T]:  
  - N: number of samples  
  - C: number of EEG channels (default: 63)  
  - T: number of time points (default: 250)  

### 2. Run the training notebook
```
jupyter notebook Generation_EEG_all_VAE_63_128_Train_stable.ipynb
```
- Configure parameters inside the notebook (latent dimension, learning rate, epochs, etc.)  
- Execute cells step-by-step to train the model.

### 3. Outputs
- EEG reconstruction plots (time & frequency domain)  
- Latent space visualization (t-SNE, PCA)  
- Generated EEG samples from random or conditional latent vectors  
- Saved model checkpoints  

---

## Evaluation Metrics

- **MSE / MAE** – time-domain reconstruction error  
- **STFT loss** – frequency-domain consistency  
- **KL divergence** – latent regularization  
- **Cosine similarity** – latent alignment between original and generated EEG  
- **Pearson correlation** – signal similarity across channels  

---

## Example Results

| Metric             | Value (example) |
|--------------------|-----------------|
| Reconstruction MSE | 0.0123          |
| KL Divergence      | 0.0047          |
| Pearson r (avg)    | 0.83            |

(Add figures/plots generated from notebook here)

---

## Applications

- EEG signal reconstruction and denoising  
- Label-controllable EEG generation  
- Brain–image multimodal alignment (with CLIP)  
- Brain-inspired generative modeling for BCI research  

---

## Contributing

Contributions are welcome!  
If you would like to add new features (e.g., Diffusion models, Transformer-based encoders, multimodal fusion), feel free to open an issue or submit a pull request.

---

## License

This project is released under the MIT License.  
You are free to use, modify, and distribute this code with attribution.

---

## Citation

If you use this repository in your research, please cite:

```
@misc{BrainVAE2025,
  author = {Liu, Di},
  title = {Brain-VAE: Variational Autoencoder Framework for EEG Generation},
  year = {2025},
  howpublished = {\url{https://github.com/DILIU1/Brain-VAE}}
}
```
