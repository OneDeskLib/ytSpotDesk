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


## Usage

This section will guide you on how to use ytSpotDesk to download and manage your music.

### Basic Download Workflow

1.  **Launch ytSpotDesk:** Run the `ytSpotDesk.py` file (or the executable if you created one). The ytSpotDesk main window will appear.

2.  **Add Download Tasks:**
    *   Click the **"Add URL"** button. A new "Download Task" row will be added to the UI. You can add up to 3 tasks concurrently.
    *   **Enter URL:** In the **URL field** of the new task row, paste the Spotify song, playlist, or album URL, or a YouTube or YouTube Music video or playlist URL you wish to download.
    *   **Select Save Folder:** Click the **"Select Folder"** button in the same task row. Choose the folder on your computer where you want to save the downloaded music files for this task. The selected folder name will appear in the field next to the "Select Folder" button.
    *   **Paste and Copy Links:** You can use the **"Paste Link"** button to paste a URL from your clipboard directly into the URL field. The **"Copy Link"** button allows you to copy the URL currently in the URL field to your clipboard.
    *   **Remove Task:** If you want to remove a download task, click the **"Remove"** button in the corresponding task row.

3.  **Start Downloads:** Once you have added your download tasks and selected folders, click the **"Start Download"** button located above the progress bar.
    *   ytSpotDesk will begin processing the download tasks in the queue.
    *   The **progress bar** will show an indeterminate animation while downloads are in progress.
    *   The **output log area** at the bottom of the window will display detailed information about the download process, including progress updates and any messages from `spotdl` or `yt-dlp`.
    *   The **progress label** below the progress bar will show the current status, such as "Downloading..." and the filename being downloaded.

4.  **Stop Downloads (Optional):** If you need to stop the downloads at any time, click the **"Stop"** button. ytSpotDesk will attempt to stop the current download processes gracefully.

5.  **Downloads Complete:** When all download tasks are finished, a **"Download finished!"** message box will appear. The progress bar will reset, and the progress label will return to "Idle."

### Managing Downloaded Files

After downloading your music, ytSpotDesk provides tools to help you manage your files:

*   **Open Folder:** In each "Download Task" row, click the **"Open Folder"** button to quickly open the selected destination folder in your system's file explorer.

*   **Rename Files:** To rename your downloaded MP3 files based on Spotify track information:
    1.  Ensure you have downloaded music from a Spotify playlist or album URL and have entered the same URL in the "URL" field of the download task row.
    2.  Click the **"Rename"** button in the task row for the folder containing the downloaded music.
    3.  The **"Rename Files" dialog** will open. Here you can configure renaming options:
        *   **Include Track Number:** Check this box to include track numbers at the beginning of the filenames.
        *   **Include Title:** Check this box to include the track title in the filenames.
        *   **Fetch Track Numbers from Playlist:**  Enable this to accurately fetch track numbers from the Spotify playlist. If disabled and renaming from an Album URL, default naming will be used.
    4.  Click the **"Rename"** button in the dialog to start the renaming process. ytSpotDesk will attempt to rename the MP3 files in the selected folder based on the track information from the provided Spotify URL.

*   **Verify Timing:** To verify the timing of your downloaded music files against the online Spotify playlist data:
    1.  Ensure you have downloaded music from a Spotify playlist and have entered the playlist URL in the "URL" field of the download task row.
    2.  Click the **"Verify Timing"** button in the task row.
    3.  The **"Verify Download Timing" dialog** will open. Click the **"Verify"** button in this dialog to start the verification process.
    4.  ytSpotDesk will compare the duration of your downloaded MP3 files with the durations from the Spotify API. Any potential timing mismatches will be displayed in a new dialog, allowing you to review and optionally delete mismatched files.

### Accessing Settings

To customize ytSpotDesk's behavior, you can access the settings dialog:

1.  Click on the **"Options"** menu in the menu bar.
2.  Select **"Settings"**.
3.  The **"Settings" dialog** will open, allowing you to configure various options like:
    *   **Download Engine:** Choose between available download engines (currently `ytdlp` is the primary option).
    *   **Threads:** Set the number of download threads to use for concurrent downloads.
    *   **YouTube Premium:** Enable YouTube Premium features and provide your cookies file and PO Token if you have a YouTube Premium account.
    *   **Output Format:** Select the default audio output format for downloads (MP3, FLAC, etc.).
    *   **Overwrite Policy:** Choose how to handle existing files with the same name.
    *   **Output Template:** Customize the output filename template.
    *   **Verify Tolerance:** Adjust the tolerance for timing verification.
    *   **Fetch Track Numbers from Playlist:**  Set the default behavior for fetching track numbers during renaming.
    *   **Keep Original WebM File:**  Optionally keep the original WebM file from YouTube downloads.
    *   **Spotify API Credentials:** Enter your Spotify API Client ID and Client Secret for enhanced Spotify functionality.
4.  Click the **"Save"** button in the Settings dialog to apply your changes.

### Spotify Login

For features that require Spotify API access (like fetching playlist track data for renaming and verification), you may need to log in to Spotify:

1.  Click on the **"Options"** menu in the menu bar.
2.  Select **"Login to Spotify"**.
3.  Your default web browser will open and redirect you to the Spotify login page.
4.  Log in to your Spotify account through the web browser.
5.  Once logged in, you may be redirected to a callback URL (you can close this page). ytSpotDesk will attempt to retrieve and cache your Spotify token automatically. A success message box will appear in ytSpotDesk if the login is successful.

### Updating spotdl and yt-dlp

To ensure you have the latest versions of `spotdl` and `yt-dlp`:

1.  Click on the **"Help"** menu in the menu bar.
2.  Select **"Update spotdl"** to update `spotdl`, or **"Update yt-dlp"** to update `yt-dlp`.
3.  ytSpotDesk will run the update command in the background, and the output log area will display the update progress.

### Checking for ytSpotDesk Updates

To check if there is a newer version of ytSpotDesk available:

1.  Click on the **"Help"** menu in the menu bar.
2.  Select **"Check for Updates"**.
3.  ytSpotDesk will check for the latest release on GitHub and display a message indicating if an update is available or if you are using the latest version.

### Clearing the Log

To clear the output log area in the ytSpotDesk window:

1.  Click on the **"Help"** menu in the menu bar.
2.  Select **"Clear Log"**.
    *   Alternatively, you can click the **"Clear Log"** button located below the output log area.
     
## Prerequisites

Before running ytSpotDesk, ensure you have the following dependencies installed:

*   **Python 3.6+:**  ytSpotDesk is written in Python and requires a Python 3.6 or later environment.
*   **pip:** Python package installer (usually comes with Python installations).

**Python Libraries:**

Install the necessary Python libraries using pip:

```bash
pip install spotdl yt-dlp tkinter ttkthemes spotipy tinytag thefuzz requests
