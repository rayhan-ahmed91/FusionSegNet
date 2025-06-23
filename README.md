## FusionSegNet ##
FusionSegNet Architecture

FusionSegNet is a deep neural network architecture designed for precise medical image segmentation, incorporating advanced multi-scale feature extraction, attention mechanisms, and uncertainty modeling. The architecture integrates several key modules to progressively refine features, capture contextual dependencies, and handle prediction uncertainty.

**Key Components:**
- **FMSAN Encoder**: Combines feed-forward networks (FFN), Multi-Scale Contextual Attention Units (MCAU), and Fuzzy Learning Modules (FLM) in each stage. MCAU uses depthwise separable convolutions with varying kernel sizes to capture multi-scale spatial patterns, followed by channel attention refinement via ECA. FLM models uncertainty at the feature level using fuzzy membership functions and integrates Monte Carlo dropout for pixel-wise uncertainty estimation.  
- **GMFAM Module**: Fuses multi-scale features from different encoder stages using adaptive gating, multi-scale convolutions, and channel-wise attention to enhance discriminative power.  
- **AAFM Module**: Applies atrous (dilated) convolutions with increasing dilation rates to capture broader contextual information, integrated with efficient channel attention for precise feature refinement.  
- **HMAA Module**: Employs hierarchical multi-axis attention with both local and global context modeling, utilizing dense connections and dynamic gating mechanisms.  
- **WMFM Module**: Implements weighted multi-scale fusion of encoder features using trainable attention weights, promoting robustness to noise and variability in the data.  

**Architecture Highlights:**
- Multi-scale spatial and channel attention at every stage  
- Fuzzy logic-based uncertainty modeling for improved prediction reliability  
- Efficient feature refinement and fusion modules for context-aware segmentation  
- Residual connections and skip pathways to preserve spatial resolution and gradient flow  

**Applications:**  
This architecture is particularly suited for medical image segmentation tasks, such as lesion boundary delineation, organ segmentation, and anomaly detection in ultrasound, MRI, and CT imaging.

## Citation ##

If you use FusionSegNet in your research, please cite our paper:

> Md Rayhan Ahmed and Patricia Lasserre *FusionSegNet: A Hierarchical Multi-Axis Attention and gated feature fusion network for breast lesion segmentation with uncertainty modeling in ultrasound imaging*. Information Fusion, 2025. [https://doi.org/10.1016/j.inffus.2025.103399](https://doi.org/10.1016/j.inffus.2025.103399)

BibTeX:
```bibtex
@article{AHMED2025103399,
  title = {FusionSegNet: A Hierarchical Multi-Axis Attention and gated feature fusion network for breast lesion segmentation with uncertainty modeling in ultrasound imaging},
  journal = {Information Fusion},
  pages = {103399},
  year = {2025},
  issn = {1566-2535},
  doi = {https://doi.org/10.1016/j.inffus.2025.103399},
  url = {https://www.sciencedirect.com/science/article/pii/S1566253525004725}
}
