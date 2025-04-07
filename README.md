
# 🌟 Grandma’s Voice – Project Explanation (Step-by-Step)

## 🔹 Overview

**Grandma’s Voice** is a sentimental GenAI tool that transforms a written story (PDF) into a spoken audio file narrated in the voice of a loved one — like your grandmother. This is achieved using cutting-edge voice cloning and text-to-speech (TTS) technology. The system reads a story from a PDF and uses an audio sample of a person’s voice to synthesize the story in that exact voice, creating a unique and emotional listening experience.

---

## ✅ Step 1: Extracting Text from the Story (PDF)

The first step is to extract the text content from a PDF file. PDF files are not directly readable by speech models, so we convert them to plain text.

- The system uses a Python library to read through every page of the uploaded PDF.
- It pulls out all the text and combines it into a single continuous story string.
- This story text is then passed to the speech synthesis system.

**Why this is necessary:**  
Text-to-speech systems need raw text input. PDFs can have layout formatting, images, and structures that the TTS engine cannot process, so this step prepares clean, usable input.

---

## ✅ Step 2: Loading the Text-to-Speech (TTS) Model

Once the text is ready, the system loads a specialized multi-speaker and multilingual TTS model called **YourTTS**. This is a pre-trained deep learning model that converts text into speech.

### Why YourTTS is used:
- It supports voice cloning, meaning it can learn the characteristics of a specific speaker’s voice.
- It is multilingual, so it can read stories in various languages if needed.
- It is multi-speaker, allowing it to handle different voices across different inputs.

When this model is loaded, it sets up everything needed to process audio: sampling rate, mel spectrogram settings, FFT size, and more — all of which are part of how TTS models convert text into realistic speech.

---

## ✅ Step 3: Voice Cloning with a Reference Audio Sample

The next step involves providing a voice sample — a recording of the person whose voice we want the story to be told in. This could be a 30-second WAV file of your grandma reading or speaking naturally.

- The system analyzes the voice features from the reference sample.
- These features are used by the model to synthesize future text in the same voice tone, pitch, and style.

**Why this is powerful:**  
It recreates the emotional intimacy of being told a story by a familiar voice — even if that person is no longer around or can’t read aloud.

---

## ✅ Step 4: Generating the Final Audio Output

With the story text and the voice sample ready, the system then generates the final audio file:

- It converts the story into speech using the cloned voice.
- The speech is saved as a downloadable audio file (usually WAV format).
- This audio can be played, shared, or used as part of a memory project.

The output audio path can be customized, or it can be generated automatically using timestamps or story titles.

---

## ✅ Step 5: Inputs Required from the User

To generate the personalized narration, the user needs to provide three things:

1. A **PDF file** containing the story text.
2. A **WAV audio sample** of the speaker whose voice will be cloned.
3. A **file name or output location** where the final audio should be saved.

Once these are uploaded, the system takes care of the rest, combining AI with emotional storytelling.

---

## 💡 Why This Matters

“Grandma’s Voice” isn’t just a tech demo — it’s a way to preserve memories, voices, and stories in a personal and meaningful way. By combining:

- **Voice cloning** (to recreate someone’s voice)
- **PDF text extraction** (to digitize stories)
- **AI speech synthesis** (to narrate the story realistically)

you’re offering a new way for people to connect with the voices they love — even across time and distance.
