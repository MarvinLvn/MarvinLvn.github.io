---
layout: page
title: "From perception to production: how acoustic invariance facilitates articulatory learning in a self-supervised vocal imitation model"
img: assets/img/from_perception_to_production/model.png
importance: 1
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/from_perception_to_production/model.png" title="Overview of the model" class="img-fluid rounded" %}
    </div>
</div>
<div class="caption">Overview of the model.</div>

## From Perception to Production: How Acoustic Invariance Facilitates Articulatory Learning

How do infants learn to map variable speech sounds to articulatory movements without instruction? Our self-supervised model tackles this challenge by learning to imitate speech through minimizing distance between input and output speech representations.

We found that intermediate layers of wav2vec 2.0 provide optimal speech representations—balancing phonetic information with speaker invariance. This enables learning human-like articulatory patterns and producing intelligible speech across multiple speakers.

**Paper:** [https://arxiv.org/html/2509.05849v1](https://arxiv.org/html/2509.05849v1)

## Single speaker training / Single speaker testing

In this section, we show examples of audio when the model is trained and evaluated on a single speaker (PB2009, the same speaker used to train the artificial vocal tract). 
We compare two different models:

- One imitating in the Mel-Frequency Cepstral Coefficients (MFCC) space
- One imitating in the representational space defined by the 7th layer of wav2vec 2.0 (which was found to work best) 

<table class="audio-comparison-table">
    <thead>
        <tr>
            <th rowspan="2">Sentence</th>
            <th rowspan="2">Input speech</th>
            <th colspan="2">Speech imitated in the:</th>
        </tr>
        <tr>
            <th>MFCC space</th>
            <th>Wav2Vec 2.0 layer 7 space</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>1</strong></td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/pb_sentence2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/pb2009/pb2009_mfcc_delta_delta2_cosine_seed_0/pb_sentence2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/pb2009/pb2009_layer_7_cosine_seed_0/pb_sentence2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
        </tr>
        <tr>
            <td><strong>2</strong></td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/pb_sentence1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/pb2009/pb2009_mfcc_delta_delta2_cosine_seed_0/pb_sentence1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/pb2009/pb2009_layer_7_cosine_seed_0/pb_sentence1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
        </tr>
    </tbody>
</table>

Both models seem to do quite well in the single-speaker setting, but what happens when training on a more naturalistic training set (read speech + different speakers from the one used to train the artificial vocal tract)?

## Multi speaker training / Single speaker testing

Here, we train our imitation models on Audiocite (100 hours of read speech produced by 8 spekaers). Again, the model is trained to imitate speech either in the MFCC space, or the space defined by wav2vec 2.0's 7th layer. We test them on PB2009 (also used to train the artificial vocal tract).

<table class="audio-comparison-table">
    <thead>
        <tr>
            <th rowspan="2">Sentence</th>
            <th rowspan="2">Input speech</th>
            <th colspan="2">Speech imitated in the:</th>
        </tr>
        <tr>
            <th>MFCC space</th>
            <th>Wav2Vec 2.0 layer 7 space</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>1</strong></td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/pb_sentence2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_mfcc_delta_delta2_cosine_seed_0/pb_sentence2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_layer_7_cosine_seed_0/pb_sentence2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
        </tr>
        <tr>
            <td><strong>2</strong></td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/pb_sentence1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_mfcc_delta_delta2_cosine_seed_0/pb_sentence1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
            <td>
                <audio controls>
                    <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_layer_7_cosine_seed_0/pb_sentence1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </td>
        </tr>
    </tbody>
</table>

Here, we observe that the model trained to imitate our 8 speakers' speech in the MFCC space completely fails: it cannot imitate the speech of an unknown speaker in an intelligible manner. 
The model imitating in the wav2vec 2.0's 7th layer seems to do better and is completely intelligible. 

## Multi speaker training / multi speaker testing

To make the task even more challenging, we train our model using only 8 speakers from the Audiocite dataset, but then test it on completely different speakers that the model has never encountered during training. This creates a speaker-independent evaluation where the test speakers are entirely unseen by the model throughout the entire training process.
We will only consider the model imitating in the wav2vec 2.0's 7th layer space since the model using MFCCs failed previously. 

<table class="audio-comparison-table">
    <thead>
        <tr>
            <th>Sentence</th>
            <th>Input speech</th>
            <th>Speech imitated in the Wav2Vec 2.0 layer 7 space</th>
            <th>Notes</th>
        </tr>
    </thead>
    <tbody>
    <tr>
        <td><strong>1</strong></td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/male_audiobook.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_layer_7_cosine_seed_0/M6_1_s_48.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            Same gender as the vocal tract
        </td>
    </tr>
    <tr>
        <td><strong>2</strong></td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/quebec_french.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_layer_7_cosine_seed_0/M7_2_s_42.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            Quebecois accent + background noise
        </td>
    </tr>
    <tr>
        <td><strong>3</strong></td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/female_audiobook_reverb.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_layer_7_cosine_seed_0/F6_3_s_38.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            Different gender + reverb
        </td>
    </tr>
    <tr>
        <td><strong>4</strong></td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/original/female_audiobook_music.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            <audio controls>
                <source src="/assets/audio/from_perception_to_production_EMNLP_2025/multi_speaker/8_speakers_6000_mn/8_speakers_6000_mn_layer_7_cosine_seed_0/F4_2_s_0.wav" type="audio/wav">
                Your browser does not support the audio element.
            </audio>
        </td>
        <td>
            Different gender + music
        </td>
    </tr>
    </tbody>
</table>

Across all 4 examples, our imitation model is quite intelligible. Interestingly, the model seems to remove background noise (sentence 2), reverberation artifacts (sentence 3), and music (sentence 4) as those are acoustic feats that cannot easily be generated by the artificial vocal tract. 


<style>
.audio-comparison-table, .audio-examples-table, .audio-layers-table {
    width: 100%;
    border-collapse: collapse;
    margin: 2rem 0;
    background-color: var(--global-card-bg-color);
}

.audio-comparison-table th, .audio-examples-table th, .audio-layers-table th,
.audio-comparison-table td, .audio-examples-table td, .audio-layers-table td {
    border: 1px solid var(--global-divider-color);
    padding: 12px;
    text-align: center;
    vertical-align: middle;
    color: var(--global-text-color);
}

.audio-comparison-table th, .audio-examples-table th, .audio-layers-table th {
    background-color: var(--global-theme-color);
    color: var(--global-card-bg-color);
    font-weight: bold;
}

.audio-comparison-table audio, .audio-examples-table audio, .audio-layers-table audio {
    width: 100%;
    max-width: 300px;
}

.audio-comparison-table tr:nth-child(even), .audio-examples-table tr:nth-child(even), 
.audio-layers-table tr:nth-child(even) {
    background-color: var(--global-bg-color);
}

.audio-comparison-table tr:nth-child(odd), .audio-examples-table tr:nth-child(odd), 
.audio-layers-table tr:nth-child(odd) {
    background-color: var(--global-card-bg-color);
}
.img-fluid.rounded {
    background-color: white;
    padding: 10px;
    border-radius: 8px;
}
</style>