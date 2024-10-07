### Complete Guide on Using YouTube-DL to Download Videos

YouTube-DL is a command-line program used for downloading videos from YouTube and other video platforms. Here's a step-by-step guide on how to install and use it.

---

### **1. Installation of YouTube-DL**

#### **For Windows:**

- Download the `youtube-dl.exe` from the [official site](https://youtube-dl.org/).
- Move the downloaded `youtube-dl.exe` to a folder of your choice.
- Open the **Command Prompt** (CMD).
- Navigate to the folder where you saved `youtube-dl.exe`.

#### **For macOS:**

- Open **Terminal**.
- Install YouTube-DL using Homebrew:

  ```bash
  brew install youtube-dl
  ```

#### **For Linux:**

- Open a terminal.
- Run the following commands:

  ```bash
  sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
  sudo chmod a+rx /usr/local/bin/youtube-dl
  ```

---

### **2. Basic Usage**

Once installed, you can download videos by opening a terminal/command prompt and using the following basic command:

```bash
youtube-dl [VIDEO_URL]
```

For example, to download a video:

```bash
youtube-dl https://www.youtube.com/watch?v=VIDEO_ID
```

---

### **3. Downloading Audio Only**

To download just the audio (in MP3 format, for example), use:

```bash
youtube-dl -x --audio-format mp3 [VIDEO_URL]
```

Example:

```bash
youtube-dl -x --audio-format mp3 https://www.youtube.com/watch?v=VIDEO_ID
```

---

### **4. Downloading a Playlist**

You can download an entire playlist using the following command:

```bash
youtube-dl -i [PLAYLIST_URL]
```

The `-i` option allows it to continue downloading even if some videos in the playlist fail.

---

### **5. Downloading Videos in Specific Format or Quality**

You can list available video formats with:

```bash
youtube-dl -F [VIDEO_URL]
```

Once you have the list, download the desired format using:

```bash
youtube-dl -f [FORMAT_CODE] [VIDEO_URL]
```

For example:

```bash
youtube-dl -f 22 https://www.youtube.com/watch?v=VIDEO_ID
```

---

### **6. Customizing the Output File Name**

To specify a custom output name for your downloaded file, use:

```bash
youtube-dl -o '~/Downloads/%(title)s.%(ext)s' [VIDEO_URL]
```

This example saves the video in the Downloads folder with the title as the filename.

---

### **7. Downloading Subtitles**

You can download subtitles (if available) using:

```bash
youtube-dl --write-sub [VIDEO_URL]
```

To download subtitles in a specific language:

```bash
youtube-dl --sub-lang [LANGUAGE_CODE] --write-sub [VIDEO_URL]
```

Example:

```bash
youtube-dl --sub-lang en --write-sub https://www.youtube.com/watch?v=VIDEO_ID
```

---

### **8. Limiting Download Speed**

To limit the download speed, use the `--limit-rate` option:

```bash
youtube-dl --limit-rate 1M [VIDEO_URL]
```

This will limit the download speed to 1 MB/s.

---

### **9. Downloading Age-Restricted Videos**

For videos that require logging in, you can pass your YouTube credentials:

```bash
youtube-dl -u YOUR_USERNAME -p YOUR_PASSWORD [VIDEO_URL]
```

---

### **10. Troubleshooting**

- **Updating YouTube-DL**: YouTube-DL frequently updates, so to keep it working efficiently, update it using:

  ```bash
  youtube-dl -U
  ```

- **Error Handling**: Use the `-i` option to ignore errors (like unavailable videos):

  ```bash
  youtube-dl -i [VIDEO_URL]
  ```

---

### **Other Useful Commands**

- **Download the best quality video and audio**:

  ```bash
  youtube-dl -f best [VIDEO_URL]
  ```

- **Resume a previously interrupted download**:

  ```bash
  youtube-dl -c [VIDEO_URL]
  ```

- **Set download speed limit**:

  ```bash
  youtube-dl --limit-rate 500k [VIDEO_URL]
  ```

---

This guide provides a solid foundation for using YouTube-DL, but there are many other options and configurations available. For the full list of options, you can always consult the [YouTube-DL documentation](https://github.com/ytdl-org/youtube-dl/blob/master/README.md) or run:

```bash
youtube-dl --help
```