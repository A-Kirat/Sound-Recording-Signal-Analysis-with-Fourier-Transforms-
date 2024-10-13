# Sound-Recording-Signal-Analysis-with-Fourier-Transforms-
Python


This project provides a set of functions to record, manipulate, filter, and analyze audio signals using Python. It includes features like recording audio, applying Fourier transforms, low-pass and high-pass filters, signal shifting, and playing audio back.

## Requirements

To run this project, you'll need the following Python packages:
- `numpy`
- `matplotlib`
- `sounddevice`
- `soundfile`
- `scipy`

You can install them using pip:

```bash
pip install numpy matplotlib sounddevice soundfile scipy
```

## Main Functions

### `record_audio(filename, duration, samplerate)`
- **Description**: Records audio for a specified `duration` and saves it as a `.wav` file.
- **Parameters**:
  - `filename`: Path to save the recorded file.
  - `duration`: Recording duration in seconds.
  - `samplerate`: Sampling rate for the recording.

### `plot_signal(signal, samplerate, title)`
- **Description**: Plots the time-domain representation of the signal.
- **Parameters**:
  - `signal`: The audio signal array.
  - `samplerate`: Sampling rate of the signal.
  - `title`: Title for the plot.

### `scale_and_shift(signal, scale, shift, samplerate)`
- **Description**: Scales and shifts the audio signal.
- **Parameters**:
  - `signal`: The input audio signal.
  - `scale`: The scaling factor for time dilation.
  - `shift`: Time shift in seconds.
  - `samplerate`: The signal's sampling rate.

### `add_signals(signal1, signal2)`
- **Description**: Adds two audio signals together.

### `compute_fourier(signal)`
- **Description**: Computes the Fourier transform of the signal.

### `inverse_fourier(signal_freq)`
- **Description**: Computes the inverse Fourier transform from the frequency domain back to the time domain.

### `shift_frequency(fourier_transform, ws)`
- **Description**: Shifts the frequency components of a Fourier transformed signal.

### `low_pass_filter(signal_freq, cutoff, samplerate)`
- **Description**: Applies a low-pass filter to the signal's frequency domain representation.
- **Parameters**:
  - `signal_freq`: The Fourier transformed signal.
  - `cutoff`: The cutoff frequency for the low-pass filter.
  - `samplerate`: The signal's sampling rate.

### `high_pass_filter(signal_freq, cutoff, samplerate)`
- **Description**: Applies a high-pass filter to the signal's frequency domain representation.

### `play_wav(data, samplerate)`
- **Description**: Plays the given audio signal using the system's audio output.

### `triangular_filter(filepath, wc)`
- **Description**: Applies a triangular filter to the frequency domain of the signal.

## Main Execution Flow

The project includes a `mainMethod` function, which demonstrates the application of the various functions:

1. **Load and Play Audio**: It reads the audio file and plays it.
2. **Plot Original Signal**: The original time-domain signal is plotted.
3. **Scale and Shift Signal**: The signal is scaled and shifted in time, and then played.
4. **Add Signals**: The original and modified signals are added, and the result is played.
5. **Fourier Transform**: The Fourier transform of the original signal is computed and plotted.
6. **Frequency Shift**: The Fourier transformed signal is shifted in frequency, and the result is played.
7. **Low-Pass and High-Pass Filters**: Both filters are applied, and the filtered signals are plotted and played.
8. **Triangular Filter**: Finally, a triangular filter is applied, and the response is plotted.

## Example

```python
# Run the main method on audio files
kiratsFile = "C:/Users/Ahmed.Kirat/Desktop/Kirat.wav"
mainMethod(kiratsFile, 44100)

nourhansFile = "C:/Users/Ahmed.Kirat/Desktop/Nourhan.wav"
mainMethod(nourhansFile, 44100)
```

## License

This project is open-source and free to use under the MIT License.
