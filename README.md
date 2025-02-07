# ytSpotDesk - Your User-Friendly Interface for spotDL and More

**The Story Behind ytSpotDesk:**

ytSpotDesk was created with a simple goal: to make the power of command-line tools like [spotDL](https://github.com/spotdl/spotify-downloader) and [yt-dlp](https://github.com/yt-dlp/yt-dlp) accessible to everyone, even those who prefer a graphical user interface (GUI).

spotDL and yt-dlp are incredible open-source projects that allow you to download music and videos from various online platforms. However, using them directly often requires typing commands in a terminal, which can be intimidating for some users.

ytSpotDesk is designed to be a **user-friendly graphical "wrapper"** around spotDL (with potential future support for yt-dlp directly). It provides an intuitive desktop application where you can easily manage your music downloads, configure settings, and enjoy the benefits of spotDL without writing any command-line instructions.

**Think of ytSpotDesk as a "friendly face" for powerful download tools.** It's a project born out of the desire to simplify and streamline the process of downloading music from Spotify, making it easy and efficient for everyone.

---

**ytSpotDesk - A User-Friendly Interface for spotDL Spotify Downloads**

ytSpotDesk is a user-friendly desktop application that provides an intuitive graphical interface for the powerful `spotdl` Spotify downloader.  It leverages the robust downloading capabilities of `spotdl` while offering a streamlined and easy-to-use experience for managing your Spotify music downloads.  Built with efficiency and ease of use in mind, ytSpotDesk ensures a smooth and responsive workflow for accessing your favorite Spotify tracks.

## Features

*   **Download Spotify Tracks, Playlists, and Albums:** Easily download individual songs, entire playlists, or full albums from Spotify, powered by `spotdl`.
*   **Multiple Download Tasks:** Queue up multiple downloads and manage them within the application.
*   **Output Format and Bitrate Control:** Choose your preferred audio format (mp3, flac, ogg, opus, m4a, wav) and bitrate for downloads, utilizing `spotdl`'s versatile format options.
*   **Audio Provider Selection:** Select your preferred audio source (youtube-music, youtube, slider-kz, soundcloud, bandcamp, piped) as supported by `spotdl`.
*   **Overwrite Options:** Control how ytSpotDesk handles existing files (skip, overwrite metadata, force overwrite).
*   **YouTube Premium Support:** Utilize your YouTube Premium account for ad-free and potentially higher quality audio (requires cookies or PO token), leveraging `spotdl`'s YouTube Premium integration.
*   **Spotify Login (Optional):** Log in to Spotify to access private playlists and enhance playlist information retrieval.
*   **Track Renaming:** Rename downloaded tracks based on playlist or album information for better organization.
*   **Clear Output Log:** Easily clear the application's output log.
*   **Update Spotdl:** Keep your `spotdl` dependency up-to-date directly from the application.
*   **Cross-Platform Compatibility:** Designed to run on Windows and Linux.

## Requirements

*   **Python:** Python 3.8 or higher is required. You can download Python from [python.org](https://www.python.org/downloads/).
*   **pip:**  pip, the Python package installer, is necessary to install dependencies. It usually comes bundled with Python installations.
*   **Internet Connection:**  An active internet connection is required for downloading music and Spotify API interaction, as utilized by `spotdl`.
*   **YouTube Premium Account (Optional):** To utilize YouTube Premium features with `spotdl`.

## Installation

To install and run ytSpotDesk, follow these steps for your operating system:

**Prerequisites (For Source Code Installation - Optional for Executable):**

*   **Python:** Ensure you have Python 3.8 or higher installed if you are running from source code. You can download it from [python.org](https://www.python.org/downloads/).
*   **pip:**  pip, the Python package installer, is required for source code installation. It usually comes bundled with Python installations. You can check if pip is installed by opening a terminal or command prompt and running `pip --version` (or `pip3 --version` on some systems).

**Installation Options:**

You have two primary ways to install and run ytSpotDesk:

**Option 1: Using Pre-built Executable (Easier for most users)**

**Windows:**

1.  **Download the Executable:** You can download the latest pre-built executable (`ytSpotDesk.exe`) from the **[Releases Tab](Link to your Releases Tab here - Replace with actual link)** of this GitHub repository. Look for the latest release and download the `.exe` file for Windows.
2.  **Run ytSpotDesk:** Once downloaded, simply double-click the `ytSpotDesk.exe` file to run the application.  **No Python or separate spotdl installation is needed.**

**Linux:**

1.  **Download the Executable:** You can download the latest pre-built executable for Linux from the **[Releases Tab](Link to your Releases Tab here - Replace with actual link)** of this GitHub repository. Look for the latest release and download the Linux executable file (the filename might not have an extension, or might have `.bin` or similar).
2.  **Make Executable (Linux only):** After downloading, you might need to make the file executable. Open a terminal, navigate to the directory where you downloaded the file, and run:
    ```bash
    chmod +x ytSpotDesk  # Replace 'ytSpotDesk' with the actual filename if different
    ```
3.  **Run ytSpotDesk:** Execute the downloaded executable from the terminal:
    ```bash
    ./ytSpotDesk  # Replace 'ytSpotDesk' with the actual filename if different
    ```
    **No Python or separate spotdl installation is needed.**

**Option 2: Installing from Source Code (For developers or advanced users)**

Follow these steps if you want to run ytSpotDesk directly from the Python source code:

**Windows:**

1.  **Download the ytSpotDesk source code:** Download the source code of ytSpotDesk, usually by cloning the Git repository or downloading a ZIP archive and extracting it to a folder on your computer.
2.  **Navigate to the ytSpotDesk directory:** Open a Command Prompt or PowerShell and navigate to the directory where you extracted the ytSpotDesk files using the `cd` command (e.g., `cd path\to\ytSpotDesk`).
3.  **Install Python Dependencies:** It is recommended to create a virtual environment to isolate project dependencies.  However, for simplicity, you can install them system-wide. Run the following command to install the necessary Python packages:

    ```bash
    pip install -r requirements.txt
    ```
    **(Optional but Recommended):** If you have a `requirements.txt` file. If you don't have a `requirements.txt` file, install the dependencies individually:
    ```bash
    pip install spotdl spotipy ttkthemes fastapi requests
    ```
4.  **Run ytSpotDesk:** Execute the `main.py` file to start the application:
    ```bash
    python main.py
    ```

**Linux:**

1.  **Download the ytSpotDesk source code:** Download the source code of ytSpotDesk, usually by cloning the Git repository or downloading a ZIP archive and extracting it to a folder on your computer.
2.  **Navigate to the ytSpotDesk directory:** Open a terminal and navigate to the directory where you extracted the ytSpotDesk files using the `cd` command (e.g., `cd /path/to/ytSpotDesk`).
3.  **Install Python Dependencies:** It is recommended to create a virtual environment to isolate project dependencies. However, for simplicity, you can install them system-wide. Run the following command to install the necessary Python packages:

    ```bash
    pip install -r requirements.txt
    ```
    **(Optional but Recommended):** If you have a `requirements.txt` file. If you don't have a `requirements.txt` file, install the dependencies individually (you might need to use `pip3` instead of `pip` depending on your Python setup):
    ```bash
    pip install spotdl spotipy ttkthemes fastapi requests
    ```
    or
    ```bash
    pip3 install spotdl spotipy ttkthemes fastapi requests
    ```
4.  **Run ytSpotDesk:** Execute the `main.py` file to start the application:
    ```bash
    python main.py
    ```
    or
    ```bash
    python3 main.py
    ```

**Creating a `requirements.txt` file (Recommended):**

It's good practice to include a `requirements.txt` file in your project. You can generate one by running the following command in your ytSpotDesk directory after installing the dependencies:

```bash
pip freeze > requirements.txt
