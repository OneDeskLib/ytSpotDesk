# ytSpotDesk

ytSpotDesk is a user-friendly desktop application designed to simplify downloading music from Spotify and YouTube. Leveraging the power of `spotdl` and `yt-dlp`, it provides a graphical interface to manage your music downloads, organize your library, and ensure high-quality audio.

## Features

*   **Download from Spotify and YouTube:** Easily download your favorite songs, playlists, and albums from both Spotify and YouTube.
*   **Multiple Output Formats:** Supports various audio formats including MP3, FLAC, WAV, OPUS, and M4A.
*   **Overwrite Policies:** Control how existing files are handled with options to skip, overwrite, or rename.
*   **YouTube Premium Support:**  Optionally use your YouTube Premium account for ad-free downloads and potentially higher quality audio (requires cookies).
*   **Output Template Customization:** Define custom output filenames using templates (e.g., `%(title)s.%(ext)s`).
*   **Concurrent Downloads:** Manage up to 3 concurrent download tasks for efficient downloading.
*   **File Renaming:** Automatically rename downloaded files based on track information fetched from Spotify, including track numbers and titles, using fuzzy matching for accuracy.
*   **Timing Verification:** Verify the downloaded music files against online playlist data to ensure accurate and complete downloads. Identify and manage potential timing mismatches.
*   **Settings Dialog:** Customize application settings including:
    *   Number of download threads.
    *   Output format and overwrite policy.
    *   YouTube Premium cookies and PO Token.
    *   Output template for filenames.
    *   Spotify API Client ID and Secret for enhanced Spotify functionality.
    *   Option to keep original WebM files from YouTube downloads.
*   **Log Output:**  Detailed logging to `SytytSpotDesk.log` for troubleshooting and monitoring. Output log is also displayed within the application.
*   **Update Functionality:**  Easily update `spotdl` and `yt-dlp` directly from the application.
*   **Dark Theme:**  A visually appealing dark theme for comfortable long-term use.
*   **Cross-Platform:** Designed to run on Windows, macOS, and Linux.

## Prerequisites

Before running ytSpotDesk, ensure you have the following dependencies installed:

*   **Python 3.6+:**  ytSpotDesk is written in Python and requires a Python 3.6 or later environment.
*   **pip:** Python package installer (usually comes with Python installations).

**Python Libraries:**

Install the necessary Python libraries using pip:

```bash
pip install spotdl yt-dlp tkinter ttkthemes spotipy tinytag thefuzz requests
