# 🖥 Overview
Gdrive-To-Gsheet is an advanced Google Apps Script utility designed to scan any Google Drive folder and generate a structured, formatted, and analysis-ready Google Sheet output.

It supports files, folders, metadata, deep folder trees, multiple profiles, resume-based execution, and custom column preservation — all in a user-friendly, reliable workflow.

Perfect for teams and individuals performing audits, compliance checks, inventory management, migrations, or simply trying to understand the structure of a complex Drive hierarchy.

# Features
## 1. Multi-Profile Scan Engine
Set up multiple scan jobs in the Profiles sheet. Each profile runs independently with its own Name, Folder ID, Mode, and Depth limits.

## 2. Three Powerful Scan Modes
Files — scans only files
Folders — scans only folders with folder-level metrics
Both — full content + folder structure, ideal for audits

## 3. Time-Sliced Smart Worker
Large folder trees often time out in Google Apps Script.
This tool avoids that by using a resume-safe, slice-based worker system:

Handles tens of thousands of items

Never exceeds script limits

Automatically continues in the background

Robust against interruptions

4. Automatic Resume

If a scan is interrupted (quota hit, script time, browser close):

State is saved

Tool picks up exactly where it stopped

No duplicates, no resets, no lost time

5. Custom Column Preservation

If you add custom columns (Owner, ReviewedBy, Status, etc.):

They are not deleted

The tool merges them back into new scan results

Perfect for manual tagging, governance, or cleanup workflows

6. Clean, Professional Output Format

Each output sheet includes:

Hyperlinked file or folder names

Fixed-width columns for Path and File/Name

Auto-resized metadata columns

Hidden technical columns (ID)

Optional raw URL column (if enabled)

7. Profile-Level Navigation

Upon completion:

The ProfileName becomes a hyperlink

Clicking it jumps directly to the output sheet

Older output is archived as <ProfileName>_Old

8. Lightweight & Admin-Friendly

No external libraries.
No add-ons.
Runs inside your Google Sheet.
No installation for end users.

# Who Needs This Tool
# Use Cases
# How It Works (recommended by me — gives clarity without being a user manual)
# Download Contents
# Version History
V1.0 - Initial base version. 
# License
# Support
 





Purpose
Primary code and documentation editor:
- Edit Python scripts
- Preview and write Markdown
- Manage folder and project structure

## 🔌 Recommended Extensions
- Python
- Markdown All in One
- Rainbow CSV
