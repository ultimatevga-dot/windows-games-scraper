# Windows Games Scraper

A portable, Zero-API Python scraper for PC games (Batocera/RetroBat/EmulationStation). It downloads metadata, clear logos, covers, and high-quality YouTube gameplays automatically, without needing API keys or user accounts.

## Features
* **Zero API:** No SteamGridDB, RAWG, or YouTube API keys required. Completely anonymous.
* **Native Dark GUI:** Graphical interface built with Tkinter featuring a dark theme and no complex external dependencies.
* **Multi-language:** Built-in support for Spanish, English, Italian, French, and Portuguese.
* **Smart Gameplay Download:** Uses `yt-dlp` for fast extraction and `ffmpeg` to download, trim to 30 seconds (with audio), and convert to `.mp4` (H.264/AAC).
* **Anti-Spoiler Filters:** Automatically discards movie trailers, console videos (PS5, Switch), and music videos.

## How to use
1. Place your `gamelist.xml` file in the same folder as the executable.
2. Run `scraper.exe`.
3. Select your language from the dropdown menu.
4. Click **Start Scraping**.
5. The program will interactively ask which videos you want to download for each game.

## Build instructions
If you wish to compile the source code yourself using PyInstaller, ensure you have `ffmpeg.exe` and `ffprobe.exe` in the same directory, then run the following command to embed them into the final binary:

`pyinstaller --noconsole --onefile --add-binary "ffmpeg.exe;." --add-binary "ffprobe.exe;." scraper.py`

<img width="807" height="631" alt="preview" src="https://github.com/user-attachments/assets/788bde52-4564-4e96-bae0-3896c013dd57" />
