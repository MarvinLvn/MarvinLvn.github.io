---
layout: page
title: "Brouhaha: multi-task training for voice activity detection, speech-to-noise ratio, and C50 room acoustics estimation (2023)"
img: assets/img/brouhaha/brouhaha.png
importance: 3
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/brouhaha/brouhaha.png" title="Brouhaha predictions" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption"><i>Brouhaha</i> predicts: 1) speech/non-speech segments; 2) Speech-to-Noise Ratio; 3) and C50 room acoustic measure.
</div>

## Training time

In this project, we contaminated read-speech audio samples (retrieved from LibriSpeech) with noise and reverberation.

The noise level is measured with the signal-to-noise ratio (**SNR**): the lower the SNR, the noisier the resulting audio. Similarly, the  reverberation level is measured with **C50**: the lower the C50, the more reverberated the resulting audio.

Here are some contaminated audio samples used to train *Brouhaha*:




<table class="doubletable">
    <tr>
        <td class="first"></td><th>Low SNR</th><th>High SNR</th>
    </tr>
    <tr>
        <th>Low C50</th>
        <td>
            <audio controls src="/assets/audio/brouhaha/c50_9_7_snr_5.wav"></audio>
        </td>
        <td>
            <audio controls src="/assets/audio/brouhaha/c50_7_5_snr_25.wav"></audio>
        </td>
    </tr>
    <tr>
        <th>High C50</th>
        <td>
            <audio controls src="/assets/audio/brouhaha/c50_40_snr_5.wav"></audio>
        </td>
        <td>
            <audio controls src="/assets/audio/brouhaha/c50_32_snr_25.wav"></audio>
        </td>
    </tr>
</table>

## Inference time

I recorded myself with an Olympus VN-540PC in three locations: 1) my place; 2) the front of the beautiful [church of Notre-Dame Dijon](https://en.wikipedia.org/wiki/Church_of_Notre-Dame_of_Dijon) (semi-enclosed space); 3) inside the same church.
Here's what Brouhaha C50 prediction looks like as a function of time:

<table>
<tr>
<td>
    Home:
    <audio controls src="/assets/audio/brouhaha/home.wav"></audio>
</td>
<td rowspan="3"> 
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/brouhaha/brouhaha_test_c50.png" title="Brouhaha C50 test" class="img-fluid rounded z-depth-1" %}
    </div>
</td>
</tr>
<tr>
<td>
    Church front:
    <audio controls src="/assets/audio/brouhaha/parvis_eglise.wav"></audio>
</td>
</tr>
<tr>
<td>
    Church:
    <audio controls src="/assets/audio/brouhaha/eglise.wav"></audio>
</td>
</tr>
</table>

Predicted C50 in the semi-enclosed space (Church front) or the closed space (Home) are around 57 dB.
*Brouhaha* predicts a lower C50 (more reverberation) for the audio sample recorded within the church (35 dB). 

