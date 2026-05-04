# 🤖 AI Lab Data Sorter for Notion

Welcome to the automated lab data workflow. This repository contains tools to instantly convert folders of raw, messy experimental files (SEM, Raman, PL, OM) into clean, structured Notion tables and automation-ready JSON.

No more manual data entry. Name your files correctly, feed them to an AI, and copy-paste the result directly into your Notion database.

## ✨ Features
*   **Auto-Parsing:** Extracts laser wavelengths, magnifications, voltages, and more straight from the filename.
*   **Chronological Sequencing:** Automatically orders your measurements by creation date.
*   **Smart Artifact Detection:** Warns you if you accidentally ran SEM on a sample *before* running Raman/PL (which can cause e-beam artifacts).
*   **Notion-Ready:** Generates a Markdown table that pastes perfectly into Notion, complete with raw-data hyperlink placeholders.

## 🚀 How to Use

### Step 1: Initialize the AI
Copy the entire contents of [`Skill.md`](Skill.md) and paste it into your AI assistant (ChatGPT, Gemini, Claude, etc.) as a system prompt or your first message.

### Step 2: Name Your Files
Follow the simple guidelines in [`NamingTemplate.md`](NamingTemplate.md). 
*(Example: `SEM_Sample1_5kV 10000x_edge.tif`)*

### Step 3: Give the AI Your Files (Choose One Method)
To get the table, the AI needs to know what files you have. Choose the easiest method for you:

**Method A: The "Zip Upload" (Easiest)**
1. Put all your daily/weekly data files in one folder.
2. Compress/Zip the folder.
3. Upload the `.zip` file to the AI chat and say: *"Process these lab files."*

**Method B: The "Copy Path" (Fastest)**
1. Open your data folder.
2. Select all files.
3. **Windows:** Right-click and select "Copy as path". **Mac:** Press `Command + Option + C`.
4. Paste the text block into the AI chat.

**Method C: The "Pro Sequence" (Best for Artifact Detection)**
If you want the AI to accurately check timestamps for sequence artifacts, run a quick command to copy the exact file creation dates:
*   **Windows:** Shift+Right-click inside the folder, click "Open PowerShell here", paste this, and hit Enter:
  ```bash
    Get-ChildItem | Select-Object Name, CreationTime | clip
  ```
*   **Mac:** Open Terminal in the folder, paste this, and hit Enter:
  ```bash
    stat -f "%N %SB" * | pbcopy
  ```

*Now just paste your clipboard into the AI chat!*
