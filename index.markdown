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

### Result samples#1: Performance comparison on I2A methods

------

explanation



<br />

<table style="table-layout: fixed; word-wrap: normal;" borded="1" border-collapse="collapse">
  <colgroup>
    <col style="width: 150px;">   <!-- Input image -->
    <col style="width: 250px;">   <!-- Our I2A backbone -->
    <col style="width: 250px;">   <!-- Im2Wav -->
    <col style="width: 250px;">   <!-- V2A-Mapper -->
    <col style="width: 250px;">   <!-- Seeing and Hearing -->
  </colgroup>
    <tr>
    <td style="text-align:center"><strong>Input image</strong></td>
    <td style="text-align:center"><strong>AudioSketch w/o control</strong></td>
    <td style="text-align:center"><strong>Im2Wav</strong></td>
    <td style="text-align:center"><strong>V2A-Mapper</strong></td>
    <td style="text-align:center"><strong>Seeing and Hearing</strong></td>
    </tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/6pvMFjUm7D0_000044.jpg'></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/proposed/6pvMFjUm7D0_000044.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/im2wav/6pvMFjUm7D0_000044.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/v2amapper/6pvMFjUm7D0_000044.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/snh/6pvMFjUm7D0_000044.wav'></audio></td>
</tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/9PmzQI8ZYpg_000030.jpg'></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/proposed/9PmzQI8ZYpg_000030.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/im2wav/9PmzQI8ZYpg_000030.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/v2amapper/9PmzQI8ZYpg_000030.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/snh/9PmzQI8ZYpg_000030.wav'></audio></td>
</tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/Bg2XkNb5LZE_000140.jpg'></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/proposed/Bg2XkNb5LZE_000140.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/im2wav/Bg2XkNb5LZE_000140.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/v2amapper/Bg2XkNb5LZE_000140.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/snh/Bg2XkNb5LZE_000140.wav'></audio></td>
</tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/B-yqXExuYrk_000405.jpg'></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/proposed/B-yqXExuYrk_000405.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/im2wav/B-yqXExuYrk_000405.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/v2amapper/B-yqXExuYrk_000405.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/snh/B-yqXExuYrk_000405.wav'></audio></td>
</tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/DkAeTKwWXs8_000065.jpg'></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/proposed/DkAeTKwWXs8_000065.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/im2wav/DkAeTKwWXs8_000065.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/v2amapper/DkAeTKwWXs8_000065.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/snh/DkAeTKwWXs8_000065.wav'></audio></td>
</tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/FxkZsO4Kd78_000022.jpg'></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/proposed/FxkZsO4Kd78_000022.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/im2wav/FxkZsO4Kd78_000022.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/v2amapper/FxkZsO4Kd78_000022.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/snh/FxkZsO4Kd78_000022.wav'></audio></td>
</tr>
<tr>
<td><img src='./assets/demo_samples/i2a/image/WGOZNdTXITQ_000205.jpg'></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/proposed/WGOZNdTXITQ_000205.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/im2wav/WGOZNdTXITQ_000205.wav'></audio></td></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/v2amapper/WGOZNdTXITQ_000205.wav'></audio></td>
<td><audio controls style="width: 100%;"><source src='./assets/demo_samples/i2a/snh/WGOZNdTXITQ_000205.wav'></audio></td>
</tr>
</table>


​    

<br />

### Result samples#2: Performance comparison on various energy representations

------

explanation



<br />


<table style="table-layout: fixed; word-wrap: normal;" borded="1" border-collapse="collapse">
  <colgroup>
    <col style="width: 150px;">   <!-- Input image -->
    <col style="width: 500px;">   <!-- Timestamp -->
    <col style="width: 500px;">   <!-- Logmel mean+Smoothing+Z-norm -->
    <col style="width: 500px;">   <!-- RMS+Smoothing+Z-norm -->
  </colgroup>
    <tr>
    <td style="text-align:center"><strong>Input image</strong></td>
    <td style="text-align:center"><strong>RMS + Smoothing + Z-norm</strong></td>
    <td style="text-align:center"><strong>Timestamp</strong></td>
    <td style="text-align:center"><strong>Logmel mean + Smoothing + Z-norm<br><span style="color:red">Caution! Popping noise</span></strong></td>
    </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/i_rgOfS3NOSY_000108.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/rms_smoothing_znorm/v__rgOfS3NOSY_000108.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/timestamp/v__rgOfS3NOSY_000108.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/logmel_smoothing_znorm/v__rgOfS3NOSY_000108.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/0IqPUUWnnd8_000085.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/rms_smoothing_znorm/v_0IqPUUWnnd8_000085.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/timestamp/v_0IqPUUWnnd8_000085.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/logmel_smoothing_znorm/v_0IqPUUWnnd8_000085.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/3njuN-F2Ecs_000332.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/rms_smoothing_znorm/v_3njuN-F2Ecs_000332.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/timestamp/v_3njuN-F2Ecs_000332.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/logmel_smoothing_znorm/v_3njuN-F2Ecs_000332.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/AAyqgdDOUYA_000020.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/rms_smoothing_znorm/v_AAyqgdDOUYA_000020.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/timestamp/v_AAyqgdDOUYA_000020.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/logmel_smoothing_znorm/v_AAyqgdDOUYA_000020.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/CpoUHOCPaNw_000020.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/rms_smoothing_znorm/v_CpoUHOCPaNw_000020.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/timestamp/v_CpoUHOCPaNw_000020.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/logmel_smoothing_znorm/v_CpoUHOCPaNw_000020.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/DKSrNxPQrbY_000090.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/rms_smoothing_znorm/v_DKSrNxPQrbY_000090.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/timestamp/v_DKSrNxPQrbY_000090.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/logmel_smoothing_znorm/v_DKSrNxPQrbY_000090.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/eFwVC47pOig_000100.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/rms_smoothing_znorm/v_eFwVC47pOig_000100.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/timestamp/v_eFwVC47pOig_000100.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_ablation/cropped/logmel_smoothing_znorm/v_eFwVC47pOig_000100.mp4'></video></td>
  </tr>
</table>


<br />

### Result samples#3: Impact of energy modulator

------

explanation



<br />

<table style="table-layout: fixed; word-wrap: normal;" borded="1" border-collapse="collapse">
  <colgroup>
    <col style="width: 150px;">   <!-- Input image -->
    <col style="width: 500px;">   <!-- Timestamp -->
    <col style="width: 500px;">   <!-- Timestamp + energy modulation -->
    <col style="width: 500px;">   <!-- Timestamp + energy modulation w/o semantic embedding -->
  </colgroup>
    <tr>
    <td style="text-align:center"><strong>Input image</strong></td>
    <td style="text-align:center"><strong>Timestamp</strong></td>
    <td style="text-align:center"><strong>Timestamp + Energy modulation (AudioSketch) </strong></td>
    <td style="text-align:center"><strong>Timestamp + Energy modulation w/o semantic embedding</strong></td>
    </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/h6YMk2FOHHM_000017.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_h6YMk2FOHHM_000017.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_h6YMk2FOHHM_000017.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_h6YMk2FOHHM_000017.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/HOyov3OS0a0_000054.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_HOyov3OS0a0_000054.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_HOyov3OS0a0_000054.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_HOyov3OS0a0_000054.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/HQb2jhmw1BE_000310.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_HQb2jhmw1BE_000310.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_HQb2jhmw1BE_000310.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_HQb2jhmw1BE_000310.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/ioQdfK6Ae9k_000010.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_ioQdfK6Ae9k_000010.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_ioQdfK6Ae9k_000010.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_ioQdfK6Ae9k_000010.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/K1ASf4xAexc_000030.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_K1ASf4xAexc_000030.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_K1ASf4xAexc_000030.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_K1ASf4xAexc_000030.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/KQAR_64a35I_000011.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_KQAR_64a35I_000011.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_KQAR_64a35I_000011.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_KQAR_64a35I_000011.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/N4SfahxM8Z4_000004.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_N4SfahxM8Z4_000004.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_N4SfahxM8Z4_000004.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_N4SfahxM8Z4_000004.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/Q19VErS2iH4_000020.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_Q19VErS2iH4_000020.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_Q19VErS2iH4_000020.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_Q19VErS2iH4_000020.mp4'></video></td>
  </tr>
  <tr>
    <td><img src='./assets/demo_samples/image/xnA7O5ESAbY_000030.jpg'></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/timestamp/v_xnA7O5ESAbY_000030.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_sem/v_xnA7O5ESAbY_000030.mp4'></video></td>
	  <td><video controls style="width: 100%;" src='./assets/demo_samples/energy_modulation/cropped/em_only/v_xnA7O5ESAbY_000030.mp4'></video></td>
  </tr>
</table>