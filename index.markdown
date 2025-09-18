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

### Comparison of I2A backbone with baselines

<br />

<head>
	<style>
		table{
			border-width : 1px;
			border-style : solid;
			border-collapse : collapse;
		}
		td{
			border-width : 1px;
			border-style : solid;
			text-align: center;
		}
	</style>
</head>



<table style="table-layout: fixed; word-wrap: normal;" borded="1" border-collapse="collapse">
    <tr>
    <td style="column-width: 150px; padding-left: 10px; padding-right: 10px"><strong>Input image</strong></td>
    <td style="column-width: 200px; padding-left: 10px; padding-right: 10px"><strong>Our I2A backbone</strong></td>
    <td style="column-width: 200px; padding-left: 10px; padding-right: 10px"><strong>Im2Wav</strong></td>
	<td style="column-width: 200px; padding-left: 10px; padding-right: 10px"><strong>V2A-Mapper</strong></td>
	<td style="column-width: 200px; padding-left: 10px; padding-right: 10px"><strong>Seeing and Hearing</strong></td>
</tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/6pvMFjUm7D0_000044.jpg'></td>
<td><audio controls><source src='./assets/demo_samples/proposed/6pvMFjUm7D0_000044.wav'></audio>
<td><audio controls><source src='./assets/demo_samples/im2wav/6pvMFjUm7D0_000044.wav'></audio>
<td><audio controls><source src='./assets/demo_samples/v2amapper/6pvMFjUm7D0_000044.wav'></audio>
<td><audio controls><source src='./assets/demo_samples/snh/6pvMFjUm7D0_000044.wav'></audio>
</tr>
</table>

​    
