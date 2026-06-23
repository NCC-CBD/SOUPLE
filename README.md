# SOUPLE: Enhancing Audio-Visual Localization and Segmentation with Learnable Prompt Contexts

**CVPR 2026** | [Paper](CVPR_2026___SouPLe.pdf) 

## Authors

**Khanh Binh Nguyen**¹ and **Chae Jung Park**²*

¹ Deakin University, Australia  
² National Cancer Center, South Korea

*Corresponding author: cjp@ncc.re.kr

---

## 📄 Abstract

Large-scale pre-trained image-text models exhibit robust multimodal representations, yet applying the Contrastive Language-Image Pre-training (CLIP) model to audio-visual localization remains challenging. Replacing the classification token ([CLS]) with an audio-embedded token ([VA]) struggles to capture semantic cues, and the prompt "a photo of a [VA]" fails to establish meaningful connections between audio embeddings and context tokens. To address these issues, we propose Sound-aware Prompt Learning (SOUPLE), which replaces fixed prompts with learnable context tokens. These tokens incorporate visual features to generate conditional context for a mask decoder, effectively bridging semantic correspondence between audio and visual inputs. Experiments on VGGSound, SoundNet, and AVSBench demonstrate that SOUPLE improves localization and segmentation performance.

---

## 🎯 Key Contributions

- **Prompt Learning Framework**: Replace fixed handcrafted prompts with learnable instance-conditional context tokens
- **Meta-Net Architecture**: A nonlinear bottleneck that generates context tokens from visual features
- **Label-Free Approach**: End-to-end framework without requiring ground-truth class labels
- **Strong Generalization**: Achieves state-of-the-art results on multiple benchmarks (VGG-SS, SoundNet-Flickr, AVSBench)

---

## 📊 Results

### VGG-SS Benchmark
| Method | cIoU ↑ | AUC ↑ |
|--------|--------|-------|
| ACL-SSL | 49.46 | 46.32 |
| **SOUPLE** | **53.21** | **48.15** |
| Improvement | +3.75 | +1.83 |

### SoundNet-Flickr Benchmark
| Method | cIoU ↑ | AUC ↑ |
|--------|--------|-------|
| ACL-SSL | 80.80 | 64.62 |
| **SOUPLE** | **84.80** | **67.64** |
| Improvement | +4.00 | +3.02 |

### AVSBench S4 (Single Sound Source)
| Method | mIoU ↑ | F-Score ↑ |
|--------|--------|-----------|
| ACL-SSL | 59.76 | 69.03 |
| **SOUPLE** | **62.89** | **71.47** |
| Improvement | +3.13 | +2.44 |

---


## 🔗 Citation


```bibtex
@InProceedings{Nguyen_2026_CVPR,
    author    = {Nguyen, Khanh Binh and Park, Chae Jung},
    title     = {SOUPLE: Enhancing Audio-Visual Localization and Segmentation with Learnable Prompt Contexts},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2026},
    pages     = {8674-8683}
}
```

