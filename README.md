# 🎵 SongSphere - Local Music Streaming Platform

<div align="center">

### A Terminal-Based Music Database & Music Player in C

Manage, organize, search, update, delete, and play local songs directly from your terminal using a persistent file-based database system.

![Language](https://img.shields.io/badge/Language-C-blue)
![Platform](https://img.shields.io/badge/Platform-Windows-green)
![Storage](https://img.shields.io/badge/Storage-Binary%20Files-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

</div>

---

# 📌 Project Overview

**Local Music Player** is a command-line music management application developed in **C Programming Language**.

The project simulates a lightweight music library manager that allows users to store and organize local songs using a unique ID-based system. Song information is permanently stored using binary files, ensuring that records remain available even after the program is closed.

This project demonstrates practical implementation of:

- File Handling
- Structures (`struct`)
- Persistent Storage
- CRUD Operations
- ID-Based Record Management
- Command-Line Interfaces

---

# ✨ Features

## 🎶 Music Management

✅ Add songs with title, artist, and file path

✅ Automatically generate unique song IDs

✅ Display all songs stored in the library

✅ Search songs by ID

✅ Update existing song information

✅ Delete songs from the database

---

## ▶️ Song Playback

✅ Play songs directly from the terminal

✅ Opens audio files using the default Windows media player

✅ No external multimedia libraries required

---

## 💾 Persistent Storage

✅ Stores records permanently in binary files

✅ Restores song library on every execution

✅ Maintains unique IDs across system restarts

---

## ⚡ Performance

✅ Lightweight memory usage

✅ Fast sequential file operations

✅ Simple and responsive CLI interface

---

# 🏗️ System Architecture

The application uses a structure-based data model.

```c
struct Song
{
    int id;
    char title[100];
    char artist[100];
    char path[260];
};
```

Each record is stored inside a binary database file.

---

## 📂 Database Layout

| Field | Description |
|---------|------------|
| ID | Unique Song Identifier |
| Title | Song Name |
| Artist | Artist Name |
| Path | Full Song File Path |

---

# 🔄 Program Workflow

## 1️⃣ Program Startup

- Load previous ID from `song_id.dat`
- If file doesn't exist, ID starts from `1`

---

## 2️⃣ Menu System

User selects an operation:

| Option | Operation |
|----------|------------|
| 1 | Add Song |
| 2 | Display Songs |
| 3 | Search Song |
| 4 | Update Song |
| 5 | Delete Song |
| 6 | Play Song |
| 7 | Exit |

---

## 3️⃣ Data Processing

### ➕ Add Song

Stores a new `Song` structure inside `songs.dat`

### 📃 Display Songs

Reads and displays all records sequentially

### 🔍 Search Song

Searches records using song ID

### ✏️ Update Song

Modifies existing record directly inside file

### 🗑️ Delete Song

Copies all records except selected one into a temporary file

### ▶️ Play Song

Launches audio file using Windows `start` command

---

## 4️⃣ Program Exit

- Current ID is saved
- Database remains intact
- Data is available during next execution

---

# 📁 Project Structure

```text
local_music_player/
│
├── main.c
├── songs.dat
├── song_id.dat
├── temp.dat
└── README.md
```

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| C Language | Core Development |
| Structures | Data Modeling |
| Binary Files | Persistent Storage |
| File Handling | Data Management |
| CLI | User Interaction |
| Windows API Commands | Song Playback |

---

# 📋 Functional Requirements

## 👤 User Requirements

The user must provide:

- Song Title
- Artist Name
- Full File Path

Example:

```text
C:\Users\Teja\Music\song.mp3
```

The user interacts through a numeric terminal menu.

Songs must be stored locally on the system.

---

## ⚙️ Technical Requirements

- Windows Operating System
- GCC / Clang / MSVC Compiler
- VS Code or Windows Terminal
- Support for `system()` calls

---

# 🚀 Installation & Execution

## Compile

```bash
gcc main.c -o music.exe
```

## Run

```bash
music.exe
```

### Multiple Source Files

```bash
gcc *.c -o music.exe
```



# 🔒 Security & Stability

## ✅ Advantages

- Persistent Database Storage
- Lightweight Application
- Fast Binary File Operations
- Modular Function Design
- Efficient ID-Based Record Management

---

## ⚠️ Current Limitations

- Windows-specific playback implementation
- No duplicate song detection
- Long path validation is limited
- Playback depends on Windows file associations
- `gets()` should be replaced with `fgets()`

---

# 🔮 Future Improvements

- 🎵 Playlist Support
- 🎼 Genre Classification
- ⭐ Favorite Songs
- 🔤 Sorting Options
- 📊 Song Statistics
- 🌐 Cross-Platform Support
- 🗄️ Database Integration
- 🎨 Enhanced Terminal UI
- 📂 Folder Scanning
- 🎧 Audio Metadata Extraction

---

# 🎯 Learning Outcomes

This project demonstrates:

- C Programming Fundamentals
- Structure-Based Data Design
- Binary File Handling
- Persistent Data Storage
- CRUD Operations
- File-Based Database Systems
- Command-Line Application Development
- Software Engineering Principles

---

# 📜 Conclusion

The **Local Music Player** is a lightweight yet practical music management solution built entirely in C. It demonstrates real-world concepts such as persistent storage, binary file operations, record management, and terminal-based interaction while providing a functional and user-friendly music library system.

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a star!

</div>
