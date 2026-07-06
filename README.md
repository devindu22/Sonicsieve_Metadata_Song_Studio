# Sonicsieve_Metadata_Song_Studio

https://jade-kulfi-46c7a8.netlify.app/ 

<img width="1919" height="917" alt="Screenshot 2026-06-30 113206" src="https://github.com/user-attachments/assets/cec0da1f-9347-49a1-a938-8d6cc3457ae3" />

# SonicSieve - Lossless Music & Metadata Studio

SonicSieve is an advanced, client-side web application designed for music enthusiasts who want to manage, preview, and enrich audio files with high-fidelity metadata. Built entirely as a single-file application (`index.html`), it combines live metadata scraping via the iTunes API, an offline Web Audio Synthesis Engine, interactive image filtering for album art, and an integrated ID3v2 tagging suite with synced lyrics (`.lrc`) generation.

---

## 🚀 Features

### 1. Advanced Metadata Search
* **iTunes API Integration:** Instantly fetch high-resolution album artwork, genres, record labels, track names, and official release dates directly from official commercial servers.
* **Quick Load Demo:** Test the studio instantly with a pre-configured sample track.

### 2. Formats & Quality Matrix
* Supports target quality configurations across various standard audio containers:
  * **FLAC:** Lossless 24-bit studio quality archiving.
  * **WAV:** Raw Studio Master uncompressed streams.
  * **MP3:** Extreme 320kbps CBR configuration.
  * **AAC:** High-Efficiency Advanced Audio Coding.

### 3. Client-Side Audio Synthesis
* **Procedural Composition:** Generate high-fidelity 10-second preview/ambient tracks (*Synthwave*, *Lofi Chill*, or *Ambient Space*) locally using the browser's native Web Audio API. 
* **Zero Server Overhead:** Renders raw sample rates entirely on your local machine.

### 4. Album Cover Art Studio
* **Interactive Canvas Filters:** Adjust image parameters in real-time before embedding.
* **Filters Included:** Contrast, Warmth, Vintage Sepia, and Vivid Saturation.
* Bakes down visual configurations straight into the downloaded file's raw binary payload.

### 5. Lyrics Sync & LRC Editor
* **Live Syncer Engine:** Paste raw text lyrics and tap the spacebar or timing button in sync with the audio player to generate industry-standard `.lrc` timestamp files.
* Supports dual modes: Unsynchronized plain text tags or accurate, time-stamped metadata.

### 6. Local Audio Tagger Mode
* Drag and drop existing audio tracks (`.mp3`, `.wav`) directly from your local hard drive to update, clean, or completely replace outdated cover art, tags, and embedded lyrics.

---

## 🛠️ Tech Stack & Architecture

* **Frontend Framework:** HTML5, Tailwind CSS (Modern Dark Mode / Cyber-grid layout).
* **UI Components:** Glassmorphic overlays, custom animated canvas audio visualizer, responsive flex/grid wrappers, and custom-styled interactive components.
* **Core APIs used:**
  * **Web Audio API:** Used for browser-level synthesis and frequency spectrum management.
  * **HTML5 Canvas API:** Used for rendering real-time filters onto high-res images.
  * **Fetch API:** Used for cross-origin search querying (iTunes Search Directory).
* **Notification Engine:** Completely custom modern toast notification layout (replaces restrictive native browser `alert()` popups).

---

## 📂 Installation & Setup

Because the application is completely self-contained within a single file, it requires no local Node.js environment, database setups, or dependency downloads.

1. **Clone or Download the Project:**
   Save your functional file as `index.html`.

2. **Launch the Application:**
   * **Option A (Double-Click):** Simply double-click `index.html` to open it locally in any modern web browser (Chrome, Edge, Firefox, Safari).
   * **Option B (Local Server - Recommended):** To bypass occasional aggressive Cross-Origin (CORS) image caching protections on certain modern browsers, serve the file using a simple lightweight server:
     ```bash
     # If you have Python installed
     python -m http.server 8000
     ```
     Then navigate to `http://localhost:8000` in your web browser.

---

## 📖 How to Use

### Step 1: Fetching or Loading a Track
* Type an artist or song name into the main search bar and hit **Search**, or click **Quick Load Demo Track** to fill the workspace instantly.

### Step 2: Styling the Album Art
* Use the slider controls under the album art viewer to adjust Contrast, Saturation, or apply Vintage styles. The modified canvas is what gets written to the final output file.

### Step 3: Aligning Lyrics
* Paste your lyrics into the Lyrics Text Area. Play the audio preview, and tap the **Timestamp** button (or spacebar) at the precise moment a line is sung to append the `.lrc` timing signature.

### Step 4: Exporting the Package
* Select your desired audio container and quality preset from the dropdown menu, then click **Download Track with Metadata**. The app compiles the audio, packages the custom artwork and lyrics inside the ID3 tag metadata, and triggers a clean browser download.

---

## 🔒 Security & Privacy

* **100% Client-Side:** No audio data, local files, or scraped lyrics are ever uploaded to an external server. Your files are processed entirely inside your browser's sandboxed memory context.
* **No Track Storage:** This utility does not store or host pirated commercial audio content. Audio files are either generated synthetically or edited locally by the user.

---

## 📝 License

Distributed under the MIT License. Feel free to modify, scale, and tailor the studio to your personal workflow needs!
