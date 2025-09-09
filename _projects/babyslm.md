---
layout: page
title: "BabySLM: language-acquisition-friendly benchmark of self-supervised spoken language models (2023)"
img: assets/img/babyslm/babyslm_logo.png
importance: 2
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/babyslm/babyslm_logo.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

This work aims at making language models more relevant to model language acquisition in infants. 

In particular, we advocate that language models should be: 
1. trained on developmentally plausible corpora. 
2. evaluated on appropriate benchmarks.

To this end, we propose a language-acquisition-friendly benchmark to evaluate written or spoken language models at the lexical and syntactic levels. 

Examples of audio files used in our benchmark are available on this webpage.

### Spot-the-word task

In this task, the model receives a word (✓) and a pseudo-word (✗) matched in phonotactic probabilities.

The model gets a score of 1 if it successfully assigns a higher probability to the real word than to the pseudo-word. It obtains a score of 0 otherwise.

<table>
    <tr>    
        <th>
            <figure>
                <figcaption>✓ hello</figcaption>
                <audio
                    controls
                    src="/assets/audio/babyslm/lexical/G_hello-en-US-Wavenet-I.wav">
                </audio>
            </figure>
        </th>
        <th>
            <figure>
                <figcaption>✗ lello</figcaption>
                <audio
                    controls
                    src="/assets/audio/babyslm/lexical/B_hello1-en-US-Wavenet-I.wav">
                </audio>
            </figure>
        </th>
        <th>
            <figure>
                <figcaption>✗ pello</figcaption>
                <audio
                    controls
                    src="/assets/audio/babyslm/lexical/B_hello2-en-US-Wavenet-I.wav">
                </audio>
            </figure>
        </th>
    </tr>
    <tr>    
        <th>
            <figure>
                <figcaption>✓ cookie</figcaption>
                <audio
                    controls
                    src="/assets/audio/babyslm/lexical/G_cookie-en-US-Wavenet-I.wav">
                </audio>
            </figure>
        </th>
        <th>
            <figure>
                <figcaption>✗ cootie</figcaption>
                <audio
                    controls
                    src="/assets/audio/babyslm/lexical/B_cookie1-en-US-Wavenet-I.wav">
                </audio>
            </figure>
        </th>
        <th>
            <figure>
                <figcaption>✗ boodie</figcaption>
                <audio
                    controls
                    src="/assets/audio/babyslm/lexical/B_cookie2-en-US-Wavenet-I.wav">
                </audio>
            </figure>
        </th>
    </tr>
</table>

### Grammatical acceptability judgment task

In this task, the model receives a grammatical (✓) and an ungrammatical (✗) sentence.

The model gets a score of 1 if it successfully assigns a higher probability to the grammatical sentence than to the ungrammatical one. It obtains a score of 0 otherwise.


<table>
<tr>
    <th>
        <figure>
            <figcaption>✓ The angry dragon</figcaption>
            <audio
                controls
                src="/assets/audio/babyslm/syntactic/GR_The_angry_dragon.wav">
            </audio>
        </figure>
    </th>
    <th>
        <figure>
            <figcaption>✗ The dragon angry</figcaption>
            <audio
                controls
                src="/assets/audio/babyslm/syntactic/UNGR_The_dragon_angry.wav">
            </audio>
        </figure>
    </th>
</tr>
<tr>
    <th>
        <figure>
            <figcaption>✓ The prince needs the princess</figcaption>
            <audio
                controls
                src="/assets/audio/babyslm/syntactic/GR_The_prince_needs_the_princess.wav">
            </audio>
        </figure>
    </th>
    <th>
        <figure>
            <figcaption>✗ The prince need the princess</figcaption>
            <audio controls>
                <source src="/assets/audio/babyslm/syntactic/UNGR_The_prince_need_the_princess.wav" type="audio/wav">
            </audio>
        </figure>
    </th>
</tr>
</table>

