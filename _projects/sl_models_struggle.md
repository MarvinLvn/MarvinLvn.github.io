---
layout: page
title: "Statistical learning models of early phonetic acquisition struggle with child-centered audio data (2022)"
img: assets/img/struggle/longforms.png
importance: 4
category: work
---

In this work, we trained self-supervised representation learning model (Contrastive Predictive Coding) on:

1. child-centered long-form recordings (acquired with child-worn microphones)
  
2. audiobooks (clean read-speech commonly used in self-supervised representation learning)
   
3. simulated long-forms, that are audiobooks contaminated with additive noise and reverberation.

Below, you'll find some audio samples that the model is exposed to during training.

### Child-centered long-form recordings

Audio samples extracted from child-centered long-form recordings:

<table>
    <tr>    
        <th>
            <figure>
                <figcaption>Female speech (storytelling):</figcaption>
                <audio
                    controls
                    src="/assets/audio/struggle/daylong_fem_story.wav">
                </audio>
            </figure>
        </th>
        <th>
            <figure>
                <figcaption>Male speech (storytelling):</figcaption>
                <audio
                    controls
                    src="/assets/audio/struggle/daylong_mal_story.wav">
                </audio>
            </figure>
        </th>
    </tr>
    <tr>    
        <th>
            <figure>
                <figcaption>Female speech (with cries):</figcaption>
                <audio
                    controls
                    src="/assets/audio/struggle/daylong_fem_cries.wav">
                </audio>
            </figure>
        </th>
        <th>
            <figure>
                <figcaption>Male speech (in the car):</figcaption>
                <audio
                    controls
                    src="/assets/audio/struggle/daylong_mal_car.wav">
                </audio>
            </figure>
        </th>
    </tr>
    <tr>    
        <th>
            <figure>
                <figcaption>Female speech (conversation):</figcaption>
                <audio
                    controls
                    src="/assets/audio/struggle/daylong_fem_farfield.wav">
                </audio>
            </figure>
        </th>
        <th>
            <figure>
                <figcaption>Male speech (conversation):</figcaption>
                <audio
                    controls
                    src="/assets/audio/struggle/daylong_very_farfield.wav">
                </audio>
            </figure>
        </th>
    </tr>
</table>

### Audiobooks

Audio samples extracted from audiobooks:

<table>
    <th>
        <figure>
            <figcaption>Female speech (reading):</figcaption>
            <audio
                controls
                src="/assets/audio/struggle/audiobooks1.wav">
            </audio>
        </figure>
    </th>
    <th>
        <figure>
            <figcaption>Female speech (reading):</figcaption>
            <audio
                controls
                src="/assets/audio/struggle/audiobooks2.wav">
            </audio>
        </figure>
    </th>
</table>

### Simulated long-forms

The same audio samples contaminated with additive noise and reverberation to simulate the challenging acoustic conditions found in long-forms:

<table>
    <th>
        <figure>
            <figcaption>Contaminated female speech (reading):</figcaption>
            <audio
                controls
                src="/assets/audio/struggle/simulated_longforms1.wav">
            </audio>
        </figure>
    </th>
    <th>
        <figure>
            <figcaption>Contaminated female speech (reading):</figcaption>
            <audio
                controls
                src="/assets/audio/struggle/simulated_longforms2.wav">
            </audio>
        </figure>
    </th>
</table>
