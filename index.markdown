---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


# AudioSketch: Controllable Image-to-Audio Generation via Semantic-Temporal Energy Modulation

Submitted to ICASSP 2026

<br />
### Authors
Jihyun Lee, Jiahao Li, Woojin Chung, Yan Lu, Hong-Goo Kang

<br />



### Proposed Method

<br />
<img src="./assets/proposed.png"> 

<br />

In this paper, we propose AudioSketch, a diffusion-based image-to-audio (I2A) generation model with an effective and user-friendly energy guidance mechanism.
Unlike prior methods that either employ overly simplistic or impractically complex energy controls, our approach introduces an energy modulator that transforms user-provided energy inputs into a more effective representation, enabling the synthesis of high-quality and natural audio.
To identify the optimal energy structure, we conduct an in-depth analysis of how different energy representations influence audio quality, temporal fidelity, and image-audio relevance.
Integrated with a lightweight neural network that maps image features to audio-related representations, our I2A framework enables a progressive translation process: from the image and a user-provided control to a refined energy representation, and then from those conditions to controlled audio synthesis.
Both quantitative and qualitative evaluations demonstrate that our model outperforms previous I2A approaches in terms of audio quality, image-audio semantic consistency, and temporal alignment with user controls. 


<br />

### Samples

<br />

**Baseline**: ParallelWaveGAN trained with MAESTRO dataset (down-sampled to 16 kHz)

**Ablation 1**: Proposed method without a harmonic-percussive separator module

**Ablation 2**: Proposed method switching the roles of the harmonic and percussive discriminators



