# Multicast Scanner

## Overview

`multicast-scanner.py` is a Python script designed to scan multicast IP addresses and ports for UDP streams. It identifies channels and adds them to a playlist.

## Features

- Scans a range of multicast IP addresses and ports.
- Identifies channels using `ffprobe`.
- Adds identified channels to a playlist file.
- Supports multithreading for faster scanning.

## Requirements

- Python 3.x
- `ffprobe` (part of the FFmpeg suite)

## Installation

1. Install Python 3.x from the official [Python website](https://www.python.org/).
2. Install FFmpeg by following the instructions on the [FFmpeg website](https://ffmpeg.org/download.html).
3. Clone this repository:
    ```sh
    git clone https://github.com/yourusername/multicast-scanner.git
    cd multicast-scanner
    ```

## Usage

1. Open a terminal and navigate to the project directory.
2. Run the script with the required arguments:
    ```sh
    python multicast-scanner.py --range 224.0.0.0/24 --port 1234 --threads 4 --size 28 --nic 192.168.1.24
    ```

### Arguments

- `--range`: The range of multicast IP addresses to scan (e.g., `224.0.0.0/24`).
- `--port`: The port(s) to scan (e.g., `1234`).
- `--threads`: The number of threads to use for scanning.( Default is `10`)
- `--size`: The subnet size for scanning.(Not Required)
- `--nic`: The network interface IP address to use for scanning.( Default is `0.0.0.0`)

## Example

```sh
python multicast-scanner.py --range 224.0.0.0/24 --port 1234