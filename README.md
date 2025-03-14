# Sound FX Beat Pad

This project is a browser-based sound effects beat pad built using raw HTML, CSS, and JavaScript. It allows you to trigger MP3 tracks from a grid of pads, apply real-time audio effects via interactive knobs, record sequences, and view a real-time audio waveform. The project is designed to be simple and portable, contained within a single HTML file.

## Features

- **Dynamic Pad Grid:**  
  Pads are automatically generated from a hard-coded list of MP3 files. The pads are arranged in a responsive grid layout.

- **Interactive Mixer Controls:**  
  Adjust global volume, pan, delay, reverb, and EQ settings using canvas-based knobs arranged in a two-column grid on the left pane.

- **Recording & Saved Sequences:**  
  Record your pad triggers and save them as sequences. Saved recordings are displayed in a dedicated section.

- **Real-Time Audio Visualization:**  
  View a live audio waveform in the left pane that updates in real time.

- **Keyboard Shortcuts:**  
  Trigger pads and control features using hotkeys (e.g., R for record, M for multi-track toggle, S for sync tracks).

## Getting Started

### Prerequisites

- **Python 3:**  
  You can use Python's built-in HTTP server to serve the project files locally.

### Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/sound-fx-beat-pad.git
   cd sound-fx-beat-pad
   ```

2. **Place Your MP3 Files:**

   Ensure your MP3 files are placed in the same folder as the HTML file.  
   To update the tracks used by the pad grid, edit the `mp3Files` array in the HTML file and replace the filenames with your own. For example:

   ```js
   var mp3Files = [
     "track1.mp3",
     "track2.mp3",
     "track3.mp3"
   ];
   ```

### Running the Server

Start a local HTTP server using Python 3:

```bash
python3 -m http.server
```

Then, open your browser and navigate to [http://localhost:8000](http://localhost:8000) to view and interact with the beat pad.

## Usage

- **Trigger Pads:**  
  Click on any pad to play the corresponding track. Clicking the same pad again within 1.5 seconds will restart the track, and after 1.5 seconds it will stop playback.

- **Keyboard Shortcuts:**  
  - **R:** Toggle recording  
  - **M:** Toggle multi-track mode  
  - **S:** Sync tracks  
  - **Q, W, E, ...:** Trigger corresponding pads (as mapped in the code)

- **Recording:**  
  Click the "Record" button (or press R) to start recording your pad triggers. When you stop recording, you will be prompted to name the sequence. The saved sequence appears as a pad in the "Saved Recordings" section.

- **Mixer Controls:**  
  Adjust the knobs on the left pane to change global volume, pan, delay, reverb, and EQ settings. The audio effects update in real time.

- **Changing Themes:**  
  Use the theme selector in the left pane to change the visual style of the pads.

## Customization

- **Replace Tracks:**  
  Modify the `mp3Files` array in the HTML file to change the set of tracks loaded into the pad grid. Ensure that the MP3 files are placed in the same directory as the HTML file.

- **Adjust Layout & Styles:**  
  The project uses CSS for layout and styling. Feel free to modify the CSS within the `<style>` block in the HTML file to suit your design preferences.

## Contributing

Contributions are welcome! Please feel free to fork the repository and submit pull requests.

## License

This project is licensed under the MIT License.
