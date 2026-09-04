# Contributing to PublicDomainM3U

First off, thank you for considering contributing to PublicDomainM3U! This repository relies on community contributions to build a comprehensive, legally free library of public domain movies and television.

## Ground Rules for Submissions

To ensure the repository remains legal, functional, and organized, all pull requests **must** adhere to the following rules:

1. **Strictly Public Domain:** You must verify that the content you are submitting is legally in the public domain in the United States. **Do not submit copyrighted material, pirated streams, or "abandonware" whose legal status is ambiguous.**
2. **Direct Video Links Only:** The URL provided must point directly to a video file (e.g., `.mp4`, `.mkv`). It cannot be a link to a web player, a YouTube page, or an HTML document. The [Internet Archive](https://archive.org/) is the highly preferred host for these files.
3. **Valid Image Links:** The `tvg-logo` URL must point directly to an image file (`.jpg`, `.png`). Do not link to a webpage containing the image.
4. **No Duplicates:** This goes without saying, do not try to submit duplicates in videos. If you find a better quality version than you can replace the existing one. Do not, however, replace a movie or TV show with a different movie or TV show. That is not the point of this repository.

---

## How to Add Media

### 1. Find the Media
Locate a high-quality direct `.mp4` link for the public domain film or episode. Also, find a high-quality poster or title card image.

### 2. Format the Entry
Every entry consists of exactly two lines. You must use this exact structure:

```text
#EXTINF:[DURATION] group-title="[FOLDER_NAME]" tvg-logo="[IMAGE_URL]", [DISPLAY_TITLE]
[DIRECT_VIDEO_URL]
```

#### Understanding the Syntax
* **`[DURATION]`**: The total length of the video in seconds (e.g., `5753`). If you do not wish to calculate the exact seconds, use `-1` to tell the player to calculate the duration automatically.
* **`group-title="Folder Name"`**: 
  * **For Movies:** Use a standard genre (e.g., `"Horror"`, `"Sci-Fi"`, `"Comedy"`, `"Western"`, `"Noir"`).
  * **For TV Shows:** Use the exact show name (e.g., `"The Beverly Hillbillies"`) so the different players group all episodes into a single folder.
* **`tvg-logo="https://..."`**: The direct link to the poster art (`.jpg` or `.png`).
* **The Comma `,`**: **Required.** This separates the metadata attributes from the visible title.
* **`[DISPLAY TITLE]`**: 
  * **For Movies:** `Title (Year)` sometimes a name included is valid such as Charlie Chaplin's 'Title'.
  * **For TV Shows:** `Show Name - SxxExx: Episode Title (Year)`

#### Example Movie Entry
```text
#EXTINF:5753 group-title="Horror" tvg-logo="https://archive.org/download/night-of-the-living-dead-movie-poster/NOTLD2x1200.jpg", Night of the Living Dead (1968)
https://archive.org/download/Night.Of.The.Living.Dead_1080p/NightOfTheLivingDead.mp4
```

#### Example TV Show Entry
```text
#EXTINF:1492 group-title="The Beverly Hillbillies" tvg-logo="https://images.squarespace-cdn.com/content/v1/60b9247ece6e73688b26f5ac/1744319008295-NBUXYXD9SIG887PP0MKH/Beverly%2BHillbillies%2BThe.png?format=750w", The Beverly Hillbillies - S01E01: The Clampetts Strike Oil (1962)
https://archive.org/download/Beverly_Hillbillies_Ep01_The_Clampetts_Strike_Oil/BH01_The_Clampetts_Strike_Oil.mp4
```

### 3. Submit Your Pull Request
1. Fork the repository.
2. Add your correctly formatted entries to the bottom of the appropriate file (`movies.m3u` or `series.m3u`).
3. Commit your changes with a clear message (e.g., `Add His Girl Friday (1940)`).
4. Open a Pull Request.

In your PR description, please briefly mention how you verified the media is in the public domain.
