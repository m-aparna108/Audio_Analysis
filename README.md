# Audio Analysis: Automated Speech Data Exploration

This project demonstrates **audio analysis** using a small English podcast dataset from Hugging Face. The main goal is to understand how audio data is loaded, preprocessed, and analyzed before applying ML or speech recognition techniques.

---

## Dataset

- **Source:** [vietnhat/gsl-english-podcast-dataset](https://huggingface.co/datasets/vietnhat/gsl-english-podcast-dataset)
---

## Project Overview

### Steps Performed

1. **Load Audio**
   - Dataset loaded using `datasets` library and decoded into numpy arrays.

2. **Preprocessing**
   - Resample to 16 kHz
   - Convert to mono
   - Normalize amplitude
   - Noise reduction
   - Silence removal
   - Voice Activity Detection (VAD)
   - Framing and windowing
   - Feature extraction (MFCC)
   - Padding/trimming to fixed length (5 seconds)
   - Data augmentation (demonstrated on first clip)

3. **EDA (Exploratory Data Analysis)**
   - Audio duration distribution
   - Waveform and Mel Spectrogram visualization
   - Amplitude statistics (mean, max, min)

---

## Libraries Used

- `datasets` (Hugging Face)
- `librosa`
- `numpy`
- `matplotlib`
- `torchaudio`
- `noisereduce`
- `webrtcvad`
- `IPython.display`

---

## Results / Observations

- Preprocessing standardizes audio clips for further ML tasks.
- Mean amplitude across clips is near zero; some clips contain significant silence.
- Mel Spectrograms reveal frequency content of speech, useful for ASR or embedding tasks.
- The pipeline demonstrates how raw audio can be cleaned and transformed into model-ready features.

---

## Usage

1. Clone this repository.
2. Open the notebook in Google Colab.
3. Install required libraries 
4. Run cells step by step to explore audio preprocessing and EDA.

---

## Key Takeaway

This notebook provides a **hands-on understanding of audio preprocessing, feature extraction, and analysis** for a beginner-friendly speech dataset. It prepares the audio data for downstream tasks like **speech recognition, embedding extraction, and topic segmentation**.
