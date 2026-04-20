*[English below](#-english-version)*

---

# 🇫🇷 Version Française

## GAN Conditionnel — Détection d'URLs de Phishing

### Description
Implémentation d'un Réseau Antagoniste Génératif Conditionnel (CGAN)
pour détecter et générer des URLs de phishing, en combinant
la Théorie des Jeux et le Deep Learning.

### Résultats
| Métrique | Score |
|----------|-------|
| Accuracy | 95.36% |
| Sensibilité | 96.52% |
| Précision | 94.33% |
| F1-score | 95.41% |
| Similarité Structurelle (SSIM) | 99.05% |

### Architecture
- **Générateur** : Générateur conditionnel avec module de classification
  auxiliaire (Convolution 1D, Dense, Leaky ReLU)
- **Discriminateur** : Discriminateur multi-tête pour la détection
  adversariale et la classification d'URLs
- **Fonction de perte** : LSGAN + perte de classification
  + perte de reconstruction

### Dataset
Kaggle — "Phishing Site URLs Dataset"
50 000 URLs extraites (bénignes + malveillantes), longueur max 200 caractères,
encodage one-hot avec 67 caractères uniques.

### Stack technique
Python · PyTorch · NLP · Scikit-learn · NumPy · Pandas

### Comment exécuter
Ouvrir `CGAN_Sreypich_MEN.ipynb` dans Google Colab ou Jupyter Notebook.

### Référence
Méthodologie complète dans :
`Sreypich_MEN_thesis_report_game_theory_deep_learning.pdf`

---

# 🇬🇧 English Version

## Conditional GAN — Phishing URL Detection

### Overview
Implementation of a Conditional Generative Adversarial Network (CGAN)
for detecting and generating phishing URLs, combining Game Theory
and Deep Learning.

### Results
| Metric | Score |
|--------|-------|
| Accuracy | 95.36% |
| Sensitivity | 96.52% |
| Precision | 94.33% |
| F1-score | 95.41% |
| Structural Similarity (SSIM) | 99.05% |

### Architecture
- **Generator** : Class-conditioned generator with auxiliary
  classification module (1D Convolution, Dense, Leaky ReLU)
- **Discriminator** : Multi-headed discriminator for adversarial
  detection and URL classification
- **Loss** : LSGAN adversarial loss + classification loss
  + reconstruction loss

### Dataset
Kaggle — "Phishing Site URLs Dataset"
50,000 URLs extracted (benign + malicious), max length 200 characters,
one-hot encoded with 67 unique characters.

### Tech Stack
Python · PyTorch · NLP · Scikit-learn · NumPy · Pandas

### How to Run
Open `CGAN_Sreypich_MEN.ipynb` in Google Colab or Jupyter Notebook.

### Reference
Full methodology detailed in :
`Sreypich_MEN_thesis_report_game_theory_deep_learning.pdf`
