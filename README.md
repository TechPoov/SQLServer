<p style="margin: 0; padding: 0;">
  <img src="img/tp_logo.png"
       width="36"
       style="vertical-align: middle; margin-right: 10px;" />
  <span style="font-size: 32px; font-weight: 700; vertical-align: middle;">
    GDrive-to-GSheet
  </span>
</p>


# GDrive-to-GSheet

Short one–sentence tagline that says **what it does** and **for whom**.  
_For example:_  
Automated Google Drive folder replication tool with progress persistence, duplicate avoidance, and detailed logging.
[display text](https://example.com)

**User Guide:** [techpoov.github.io](https://techpoov.github.io)

**User Guide:** [GdriveFolderCopy User Guide](https://techpoov.github.io/docs/GdriveFolderCopy_UserGuide.pdf)

**User Guide:** [Open User Guide](https://docs.google.com/document/d/XXXXXXXXXXXX)

**User Guide:** [Make a copy](https://docs.google.com/document/d/XXXXX/copy)


If you want dynamic linking

If your tool name is GdriveFolderCopy, you can write:

**User Guide:** [Visit TechPoov Docs](https://techpoov.github.io/#GdriveFolderCopy)


Your website already loads README when clicked, so this will act like a documentation hub.


---

## 1. Overview

{{ToolName}} is a {{platform / technology}} utility that helps you {{primary outcome}}.

It is designed for:

- {{User type 1}} – e.g., IT admins who manage large Google Drives
- {{User type 2}} – e.g., team leads who need transparent folder copies
- {{User type 3}} – e.g., anyone who wants reliable, resumable automation

Key benefits:

- **Reliable** – handles large jobs without manual intervention
- **Transparent** – clear logs and status for every run
- **Repeatable** – same settings can be reused safely across runs

---

## 2. Key Features

- **Feature 1** – short, concrete description  
- **Feature 2** – what problem it solves  
- **Feature 3** – anything that makes it stand out  
- **Safety / Protection** – e.g., duplicate avoidance, read-only operations, etc.  
- **Reporting / Logs** – how users can see what happened  

_Example for GdriveFolderCopy:_

- **Recursive Folder Copying** – copies full folder hierarchies (subfolders + files)  
- **Progress Persistence & Auto-Resume** – safely resumes long jobs using stored state  
- **Duplicate Avoidance** – skips files that already exist at the destination  
- **Row-Based Job Management** – drive copy jobs are defined in a Profiles sheet  
- **Execution Logging** – writes a detailed log row for each completed or failed job  

---

## 3. When to Use This Tool

Use {{ToolName}} when:

- You need to **{{situation 1}}**  
- You regularly **{{situation 2}}**  
- You are preparing for **{{audit / cleanup / migration}}**  

Not a good fit when:

- {{Case where tool is overkill or wrong}}  

---

## 4. How It Works (High-Level)

1. You configure one or more jobs in the **Profiles** sheet / config file.  
2. The tool reads these jobs and validates the inputs.  
3. For each job, it processes items in batches to avoid timeouts.  
4. State is stored between runs to enable **resume**.  
5. A **Log** sheet / log file captures results, errors, and summary.

_(Adjust steps for each specific tool.)_

---

## 5. Quick Start

Follow these steps to run your first job in a few minutes.

1. **Get the Tool**
   - Open the public copy: {{Link to “Make a copy” or Releases page}}
   - (Optional) Rename it for your environment.

2. **Authorize the Script / Executable**  
   - Run `▶ {{entry function / script name}}` once.  
   - Approve required permissions when prompted.

3. **Configure One Profile**
   - Open the **Profiles** sheet (or config file).
   - Fill in the required columns for a single test job (see next section).

4. **Run the Tool**
   - From the menu: **TechPoov Menu → {{Action name}}**  
   - Wait for the status message / toast.

5. **Review Results**
   - Check the **Log** sheet / log file.
   - Verify the output in Google Drive / Windows folder / SQL etc.

---

## 6. Profiles / Configuration

Describe the configuration sheet or file in a simple table.

**Profiles Sheet (Required Columns)**

| Column Name      | Required? | Description                                                   |
|------------------|-----------|---------------------------------------------------------------|
| `ProfileName`    | Yes       | Friendly name for this job (used in logs and emails).        |
| `SourceFolderId` | Yes       | ID / path of the source folder to scan or copy.              |
| `TargetFolderId` | Yes       | ID / path of the destination folder (for copy tools).        |
| `Active`         | Yes       | `Y` to enable this job, anything else to ignore.             |

**Optional Columns**

| Column Name      | Description                                                   |
|------------------|---------------------------------------------------------------|
| `NotifyEmail`    | Send completion / error emails to this address.              |
| `Notes`          | Free-text comments about this job.                           |

_(Adjust columns per tool.)_

---

## 7. Running the Tool

### 7.1 From the Menu (Recommended)

- In the Sheet, use **TechPoov Menu → {{Action name}}**.  
- The tool will:
  - Read all active profiles
  - Execute each job in sequence
  - Log results and show a summary alert

### 7.2 Rerun / Resume Behavior

Explain what happens on reruns:

- **Resumable:** if a previous run stopped, the next run **continues where it left off**.  
- **Idempotent:** safe to run the same job multiple times.  
- **State clear:** how to reset state if needed.

---

## 8. Output & Logs

Describe what the user can inspect after a run.

- **Log Sheet / Log File**
  - One row per job / per item
  - Includes timestamps, status, counts, errors, and summary text.

- **Output Folder / Report**
  - Where copies are written or where the final report file appears
  - Example: `{{Output/Reports}}` folder under the tool’s root.

_Add a small example table if useful._

---

## 9. Error Handling & Troubleshooting

Common issues and what to do:

- **“Authorization required”** – run `{{entry point}}` and approve access.  
- **“Cannot find folder ID”** – verify the folder ID / path in the Profiles sheet.  
- **Timeouts** – tool will auto-resume next run; do not delete the log or state.  
- **Permission errors** – ensure you have access to both source and destination.

If something looks wrong:

1. Check the **Log** sheet for `Status = Error`.  
2. Note the error message and failing profile.  
3. Fix the configuration and run again.

---

## 10. Limitations (Current Version)

Be honest and clear – this builds trust.

Examples:

- Does not copy **shared drives** yet (only My Drive).  
- Files larger than **X MB** may be skipped or slower to process.  
- Currently supports up to **N profiles per run** for best performance.  

---

## 11. Version History

| Version | Date       | Summary                                      |
|---------|------------|----------------------------------------------|
| v1.0    | 2025-11-30 | Initial public release.                      |
| v1.1    | 2025-12-10 | Improved logging and resume reliability.     |

_(Mirror what you already track in your internal Version_Tracking sheet, but short.)_

---

## 12. Support

- **User Guide:** {{link to detailed PDF / GDoc if available}}  
- **Issues / Bugs:** use the GitHub **Issues** tab in this repository.  
- **Email:** `TechPoov+{{ToolName}}@gmail.com` (or generic support address).  

---

## 13. License

Short note if you use a standard license (MIT, etc.), and link to `LICENSE` file.

