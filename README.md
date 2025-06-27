# Digital Radio Signal Processing

This project demonstrates essential digital signal processing (DSP) techniques applied to audio signals, particularly focusing on **amplitude modulation**, **filtering**, and **demodulation**. The notebook walks through each step using real audio samples, visualizing the signal behavior in both time and frequency domains.

---

## Project Overview

The main stages of this notebook include:

1. **Loading and Visualizing Audio**
2. **Amplitude Modulation (AM)**
3. **Signal Combination**
4. **Bandpass and Lowpass Filtering**
5. **Demodulation**
6. **Comparison of Original and Reconstructed Signals**

---

## Signal Modulation

### Amplitude Modulation (AM)

Amplitude Modulation encodes information by varying the amplitude of a **carrier signal** based on the input (audio) signal.

### Why Use AM?

1. **Transmission:** Low-frequency audio signals cannot travel far in free space. By modulating them onto a high-frequency carrier wave, we can efficiently transmit them using antennas.
2. **Multiplexing:** Modulation allows multiple signals to share the same medium (e.g., radio channels on different frequencies).
3. **Noise Resistance:** Higher-frequency signals can sometimes be processed or filtered more effectively.

AM is widely used in analog broadcasting (e.g., AM radio). The goal is to shift the frequency content of the original signal to a higher frequency range suitable for transmission.

---

## Plots & What They Represent

### 1. **Time-Domain Signal**
Shows the waveform of the audio:
- X-axis: Time (seconds)
- Y-axis: Amplitude
- This gives insight into how the amplitude changes over time.

### 2. **Frequency-Domain Signal (DFT)**
Computed using `fft()`:
- X-axis: Frequency (Hz)
- Y-axis: Magnitude
- This reveals the frequency components (i.e., spectral content) of the audio signal.

---

## Filters

### Bandpass Filter

Designed to allow a specific frequency band (around the carrier) to pass through while attenuating others. Useful after modulation to isolate the desired modulated signal.

### Lowpass Filter

Allows low-frequency components (like speech or music) to pass and blocks high-frequency noise.
