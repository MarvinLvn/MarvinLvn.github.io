---
layout: page
title: "BabAR: from phoneme recognition to developmental measures of young children's speech production"
img: assets/img/babar/babar_logo.png
importance: 1
category: work
---

## 1. What is BabAR?

Understanding how children learn to speak requires analyzing the sounds they produce, but doing this by hand is extremely time-consuming, limiting most studies to small samples. 
BabAR (Babbling Automatic Recognition) is an open-source tool that automatically transcribes young children's vocalizations into International Phonetic Alphabet (IPA) symbols, the standard notation used by linguists to represent speech sounds.

Analyzing a child's speech from a daylong recording is a two-step process. First, we need to figure out *when* the child is speaking. Daylong recordings contain hours of audio where most of the time the child is silent, and other people (parents, siblings) are talking. For this, we use [VTC](https://github.com/MarvinLvn/voice-type-classifier) (Voice Type Classifier), a neural network that scans the audio and detects segments where the target child is vocalizing. Second, once we have those segments, BabAR takes over and transcribes them into IPA phonemes.

**Paper:** *BabAR: from phoneme recognition to developmental measures of young children's speech production* (submitted to Interspeech 2026)
**Code:** If you'd like to run BabAR on your own data, check out the [GitHub repository](https://github.com/MarvinLvn/BabAR).

## 2. BabAR in action

Here's a video example of BabAR's predictions on a recording collected using a child-worn microphone: 

<div style="text-align: center;">
<video width="90%" controls>
    <source src="/assets/audio/babar/babar_final.mp4" type="video/mp4">
    Your browser does not support the video element.
</video>
</div>

## 3. Listening to development

Below are vocalizations randomly sampled from the same child recorded at three different ages: 6, 12, and 17 months from the SEEDLingS dataset. 
For each sample, we show BabAR's predicted IPA transcription.

BabAR sometimes returns an empty prediction. This can happen when VTC detects very short segments that don't contain enough acoustic information for BabAR to identify any phoneme, or when the child produces non-speech vocalizations (cries, laughs, vegetative sounds) that do not map onto phonemic categories.
Additionally, VTC can occasionally misattribute an older sibling's speech to the target child. The last sample at 17 months (*m ɑ m i j u k ɛ n f a ɪ n d ɔ ɹ r d*, i.e. "mommy you can find...") is an example of this: a sibling's utterance incorrectly detected as the target child's.

<table class="audio-table">
    <thead>
        <tr>
            <th colspan="2">6 months</th>
            <th colspan="2">12 months</th>
            <th colspan="2">17 months</th>
        </tr>
        <tr>
            <th>Audio</th><th>IPA</th>
            <th>Audio</th><th>IPA</th>
            <th>Audio</th><th>IPA</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_1.wav"></audio></td>
            <td>ɛ ɛ ɪ ɛ</td>
            <td><audio controls src="/assets/audio/babar/12mo_1.wav"></audio></td>
            <td><em>(empty)</em></td>
            <td><audio controls src="/assets/audio/babar/17mo_1.wav"></audio></td>
            <td><em>(empty)</em></td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_2.wav"></audio></td>
            <td><em>(empty)</em></td>
            <td><audio controls src="/assets/audio/babar/12mo_2.wav"></audio></td>
            <td>ɪ</td>
            <td><audio controls src="/assets/audio/babar/17mo_2.wav"></audio></td>
            <td>d ʒ æ</td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_3.wav"></audio></td>
            <td><em>(empty)</em></td>
            <td><audio controls src="/assets/audio/babar/12mo_3.wav"></audio></td>
            <td><em>(empty)</em></td>
            <td><audio controls src="/assets/audio/babar/17mo_3.wav"></audio></td>
            <td>m ʌ t u t i m ʌ t u t</td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_4.wav"></audio></td>
            <td>ɛ</td>
            <td><audio controls src="/assets/audio/babar/12mo_4.wav"></audio></td>
            <td>i ɡ o</td>
            <td><audio controls src="/assets/audio/babar/17mo_4.wav"></audio></td>
            <td>ʊ m a b ɔ</td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_5.wav"></audio></td>
            <td>j æ</td>
            <td><audio controls src="/assets/audio/babar/12mo_5.wav"></audio></td>
            <td>m o ə</td>
            <td><audio controls src="/assets/audio/babar/17mo_5.wav"></audio></td>
            <td>ɪ</td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_6.wav"></audio></td>
            <td><em>(empty)</em></td>
            <td><audio controls src="/assets/audio/babar/12mo_6.wav"></audio></td>
            <td>ʌ</td>
            <td><audio controls src="/assets/audio/babar/17mo_6.wav"></audio></td>
            <td><em>(empty)</em></td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_7.wav"></audio></td>
            <td>ɛ</td>
            <td><audio controls src="/assets/audio/babar/12mo_7.wav"></audio></td>
            <td>ʌ</td>
            <td><audio controls src="/assets/audio/babar/17mo_7.wav"></audio></td>
            <td>h æ h a f a d a</td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_8.wav"></audio></td>
            <td>ə ɛ ɛ</td>
            <td><audio controls src="/assets/audio/babar/12mo_8.wav"></audio></td>
            <td>ʊ d ʊ ʃ</td>
            <td><audio controls src="/assets/audio/babar/17mo_8.wav"></audio></td>
            <td>m m a t e w a t ʃ</td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_9.wav"></audio></td>
            <td><em>(empty)</em></td>
            <td><audio controls src="/assets/audio/babar/12mo_9.wav"></audio></td>
            <td>ʊ</td>
            <td><audio controls src="/assets/audio/babar/17mo_9.wav"></audio></td>
            <td>ɡ a</td>
        </tr>
        <tr>
            <td><audio controls src="/assets/audio/babar/6mo_10.wav"></audio></td>
            <td><em>(empty)</em></td>
            <td><audio controls src="/assets/audio/babar/12mo_10.wav"></audio></td>
            <td>d u d u ɡ ʌ</td>
            <td><audio controls src="/assets/audio/babar/17mo_10.wav"></audio></td>
            <td>m ɑ m i j u k ɛ n f a ɪ n d ɔ ɹ r d</td>
        </tr>
    </tbody>
</table>

<style>
.audio-table {
    width: 100%;
    border-collapse: collapse;
    margin: 1.5rem 0;
}
.audio-table th, .audio-table td {
    border: 1px solid var(--global-divider-color);
    padding: 8px 12px;
    text-align: center;
    vertical-align: middle;
}
.audio-table thead tr:first-child th {
    background-color: var(--global-theme-color);
    color: var(--global-card-bg-color);
    font-weight: bold;
    font-size: 1.1rem;
}
.audio-table thead tr:nth-child(2) th {
    background-color: var(--global-theme-color);
    color: var(--global-card-bg-color);
    font-weight: bold;
    font-size: 0.9rem;
    opacity: 0.9;
}
.audio-table tr:nth-child(even) {
    background-color: var(--global-bg-color);
}
.audio-table tr:nth-child(odd) {
    background-color: var(--global-card-bg-color);
}
.audio-table audio {
    width: 80px;
    height: 30px;
}
</style>