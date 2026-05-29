# End-to-End Voice Cloning Pipeline using Audio Cleaning, Whisper Transcription, and CSM-1B Preparation

## Overview

This project implements a complete voice cloning data preparation and model adaptation pipeline. The system automates the conversion of raw speech recordings into a structured dataset suitable for fine-tuning modern speech foundation models such as CSM-1B.

The pipeline includes:

* Audio collection from uploaded recordings and online sources
* Audio cleaning and normalization using FFmpeg
* Automatic transcription using OpenAI Whisper
* Sentence-aware audio segmentation
* Hugging Face dataset generation
* LoRA-based CSM-1B fine-tuning preparation
* Speech synthesis inference framework

---

## Project Architecture

Raw Audio Files
↓
FFmpeg Audio Cleaning
↓
Whisper Large-v3 Transcription
↓
Sentence-Aware Chunking
↓
Hugging Face Dataset Creation
↓
CSM-1B + LoRA Configuration
↓
Voice Cloning Fine-Tuning Pipeline

---

## Features

### Audio Preprocessing

* High-pass filtering
* Low-pass filtering
* Spectral denoising
* Loudness normalization
* Mono conversion
* 24 kHz resampling

### Automatic Transcription

* OpenAI Whisper Large-v3
* Word-level timestamps
* Sentence-level alignment
* JSON transcript generation

### Dataset Generation

* Automated speech segmentation
* Hugging Face compatible dataset format
* Audio-text pairing
* Metadata tracking

### Model Preparation

* CSM-1B integration
* PEFT (LoRA) configuration
* Hugging Face Transformers support

---

## Dataset

The generated dataset is publicly available on Hugging Face:

Dataset Link:

https://huggingface.co/datasets/Mrinal007/mkbhd_tts_medium_clean

Dataset Structure:

```python
{
    "audio": {
        "path": "clip.wav",
        "sampling_rate": 24000
    },
    "text": "Transcript corresponding to the audio clip.",
    "source": "original_file_identifier"
}
```

Dataset Statistics:

* Total Audio Duration: 22.4 Minutes
* Total Segments: 185 Clips
* Training Split: 166 Clips
* Validation Split: 19 Clips
* Sampling Rate: 24 kHz

## Required Dependencies

```text
torch
transformers
datasets
peft
accelerate
openai-whisper
ffmpeg
yt-dlp
numpy
soundfile
```

---

## Usage

### Step 1: Upload Audio Files


Supported formats:

* WAV
* MP3
* M4A

---

### Step 2: Audio Cleaning


### Step 3: Generate Transcripts



### Step 4: Create Audio Segments



### Step 5: Build Hugging Face Dataset


### Step 6: Configure CSM-1B Fine-Tuning


---

## Current Status

Completed:

* Audio collection workflow
* Audio cleaning pipeline
* Whisper transcription pipeline
* Sentence-aware chunking
* Hugging Face dataset creation
* CSM-1B integration setup
* LoRA training configuration

Future Work:

* Full-scale CSM-1B fine-tuning
* Multi-speaker voice cloning
* Cross-lingual synthesis
* Emotion-aware speech generation
* Real-time inference

---
