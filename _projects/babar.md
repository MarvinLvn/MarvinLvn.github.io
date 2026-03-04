---
layout: page
title: "BabAR: from phoneme recognition to developmental measures of young children's speech production"
img: assets/img/babar/babar_logo.png
importance: 1
category: work
---

## What is BabAR?
Understanding how children learn to speak requires analyzing the sounds they producen, but doing this by hand is extremely time-consuming, limiting most studies to small samples. 
BabAR (Babbling Automatic Recognition) is an open-source tool that automatically transcribes young children's vocalizations into International Phonetic Alphabet (IPA) symbols, the standard notation used by linguists to represent speech sounds.

## BabAR in action

Here's a video example of BabAR's predictions on a recording collected using a child-worn microphone (LENA®): 


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <video width="60%" controls>
            <source src="{{ '/assets/audio/babar/babar_final.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video element.
        </video>
    </div>
</div>

## Listening to development

Below are vocalizations randomly sampled from the same child recorded at three different ages: 6, 12, and 17 months from the SEEDLingS dataset. 
For each sample, we show BabAR's predicted IPA transcription.

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