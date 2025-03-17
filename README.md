# Video Compression Tester Tool

Demo Link: https://video-compression-tester.web.app/

## Overview
The **Video Compression Tester Tool** is a web-based application designed to compress video files using various filters and parameters. It allows users to test different video compression settings, such as codecs, resolution, bitrate, and more, to achieve the desired balance between file size and quality. The tool also provides a detailed test history, including input/output file details, compression parameters, and time taken for each test.

---

## Purpose
The purpose of this tool is to:
1. **Test Video Compression**: Experiment with different compression settings to understand their impact on video quality and file size.
2. **Optimize Video Files**: Compress videos for specific use cases, such as streaming, mobile devices, or storage.
3. **Generate Reports**: Track and analyze compression tests with a detailed history table.
4. **Learn FFmpeg**: Understand how FFmpeg commands work and how different parameters affect video compression.

---

## Use Cases
- **Content Creators**: Compress videos for social media platforms or websites.
- **Developers**: Test and optimize video compression settings for applications.
- **Educators**: Teach video compression concepts and FFmpeg usage.
- **Enthusiasts**: Experiment with video compression to learn more about the process.

---

## Features
1. **Customizable Filters**:
   - Video Codec (e.g., H.264, H.265, VP9, AV1)
   - Resolution (e.g., 1080p, 720p, 480p)
   - Bitrate (e.g., 500 kbps, 2500 kbps)
   - Preset (e.g., ultrafast, medium, veryslow)
   - Threads (e.g., 1, 4, 16)
   - Frame Rate (e.g., 24 FPS, 30 FPS, 60 FPS)
   - Audio Codec (e.g., AAC, MP3, Opus)
   - Audio Bitrate (e.g., 96 kbps, 320 kbps)
   - Audio Sample Rate (e.g., 44.1 kHz, 48 kHz)
   - GOP Size (e.g., 30, 60)

2. **Real-Time Progress**:
   - Displays frames processed, FPS, time elapsed, bitrate, and speed during compression.

3. **Test History**:
   - Tracks all compression tests with details like input/output file size, compression parameters, and time taken.

4. **Download Compressed Video**:
   - Provides a download link for the compressed video.

5. **SweetAlert2 Integration**:
   - Displays success and error messages with a modern UI.

---

## How It Works
1. **Select Filters**: Choose the desired compression settings from the dropdown menus.
2. **Upload Video**: Select a video file to compress.
3. **Compress**: Click the "Compress Video" button to start the process.
4. **View Results**: The compressed video is available for download, and the test details are added to the history table.

---

## Code Explanation

### Key Components
1. **HTML**:
   - The UI is built using Bootstrap for a responsive design.
   - Dropdown menus allow users to select compression filters.
   - A file input is used to upload videos.
   - A table displays the test history.

2. **CSS**:
   - Custom styles for the preloader, progress bar, and table.

3. **JavaScript**:
   - Uses FFmpeg.js to handle video compression in the browser.
   - Dynamically constructs FFmpeg commands based on selected filters.
   - Captures real-time progress and updates the UI.
   - Tracks test history and displays it in a table.

4. **FFmpeg**:
   - The core library for video compression.
   - Processes the video file based on the selected parameters.

---

### Parameters Explained

#### Video Codec
- **libx264**: H.264 codec, widely compatible and good for streaming.
- **libx265**: H.265 codec, more efficient but requires newer devices.
- **libvpx**: VP8 codec, open-source and good for web.
- **libvpx-vp9**: VP9 codec, high-quality alternative to H.265.
- **libaom-av1**: AV1 codec, next-gen with better compression but slower encoding.
- **mpeg4**: Older codec, less efficient.
- **libxvid**: Good for AVI format.
- **copy**: No encoding, fastest option.

#### Resolution
- Adjusts the output video size (e.g., 1920x1080 for 1080p).

#### Bitrate
- Controls the video quality and file size (e.g., 500 kbps for low quality, 5000 kbps for high quality).

#### Preset
- Balances encoding speed and quality:
  - **ultrafast**: Fastest, lowest quality.
  - **veryslow**: Slowest, best quality.

#### Threads
- Number of CPU threads used for encoding (e.g., 1 for low CPU usage, 16 for high-performance machines).

#### Frame Rate (FPS)
- Adjusts the number of frames per second (e.g., 24 FPS for cinematic look, 60 FPS for smooth motion).

#### Audio Codec
- **AAC**: Best quality for MP4.
- **MP3**: Good for compatibility.
- **Opus**: High quality, low bitrate.
- **copy**: Keeps the original audio.

#### Audio Bitrate
- Controls audio quality (e.g., 96 kbps for low quality, 320 kbps for best quality).

#### Audio Sample Rate
- Adjusts the audio sample rate (e.g., 44.1 kHz for standard, 48 kHz for best quality).

#### GOP Size
- Controls the distance between keyframes (e.g., 30 for standard, 60 for better compression).

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/video-compression-tool.git
