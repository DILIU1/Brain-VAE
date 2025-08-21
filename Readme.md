# 🧠 Brain-VAE  

> <span style="color:#4CAF50; font-weight:bold;">Variational Autoencoder (VAE) framework for EEG generation & reconstruction</span>  
> Designed for **neural decoding**, **BCI applications**, and **multimodal alignment**.  

---

## ✨ Features  

- ⚡ **EEG-specific VAE architecture**  
  <span style="color:#2196F3">63 channels × 250 time points → Latent 63×128</span>  
- 🎛 **EEG Generation & Reconstruction**  
  <span style="color:#9C27B0">Time & frequency domain evaluation, label control</span>  
- 🔗 **Multimodal Extension**  
  <span style="color:#FF9800">Supports CLIP embeddings for EEG–image alignment</span>  
- 🧪 **Reproducible Training**  
  Notebook + metrics + visualization  

---

## 📂 Repository Structure  

```
Brain-VAE/
├── 📒 Generation_EEG_all_VAE_63_128_Train_stable.ipynb   # Training notebook
├── ⚙️ environment.yml                                    # Conda environment
├── 📦 requirements.txt                                   # Dependencies
└── 📘 README.md                                          # Documentation
```

---

## ⚙️ Installation  

```bash
# Clone repo
git clone https://github.com/DILIU1/Brain-VAE.git
cd Brain-VAE

# Option A – conda
conda env create -f environment.yml
conda activate brain-vae

# Option B – pip
pip install -r requirements.txt
```

---

## 🧠 Usage  

1️⃣ **Prepare Data**  
- Format: `[N, C, T]`  
  - *N*: samples  
  - *C*: channels (default 63)  
  - *T*: time points (default 250)  

2️⃣ **Run Notebook**  
```bash
jupyter notebook Generation_EEG_all_VAE_63_128_Train_stable.ipynb
```  

3️⃣ **Outputs**  
- 📊 EEG reconstruction plots (time & frequency)  
- 🌀 Latent space visualization (t-SNE, PCA)  
- 🧩 Generated EEG samples  
- 💾 Saved model checkpoints  

---

## 📊 Evaluation Metrics  

| Metric              | Description                                |
|---------------------|--------------------------------------------|
| 🟦 **MSE / MAE**    | Time-domain reconstruction error           |
| 🟩 **STFT Loss**    | Frequency-domain consistency               |
| 🟪 **KL Divergence**| Latent space regularization                |
| 🟧 **Cosine Sim.**  | Latent alignment between signals            |
| 🟥 **Pearson r**    | Cross-channel similarity                   |

---

## 📈 Example Results  

| Metric             | Value (example) |
|--------------------|-----------------|
| 🟦 MSE             | 0.0123          |
| 🟪 KL Divergence   | 0.0047          |
| 🟥 Pearson r (avg) | 0.83            |

---

## 🚀 Applications  

- 🧹 EEG signal reconstruction & denoising  
- 🧩 Label-controllable EEG generation  
- 🎨 Brain–image multimodal alignment  
- 🧬 Brain-inspired generative modeling for BCI  

---

## 🤝 Contributing  

Contributions are welcome!  
- 📝 Open an issue  
- 🔀 Submit a pull request  
- 💡 Suggest new features (Diffusion, Transformers, multimodal fusion)  

---

## 📜 License  

📄 Released under the **MIT License** – free to use, modify & distribute with attribution.  

---

## 📚 Citation  

If you use this project in your research:  

```
@misc{BrainVAE2025,
  author = {Liu, Di},
  title = {Brain-VAE: Variational Autoencoder Framework for EEG Generation},
  year = {2025},
  howpublished = {\url{https://github.com/DILIU1/Brain-VAE}}
}
```
