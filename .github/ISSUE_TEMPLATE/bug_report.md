# Bug Report Template

Thank you for identifying an issue with **UdemyCourseVault-Offline-Video-Downloader-CLI-Tool**. Following Apex standards, please provide exhaustive detail so we can maintain Zero-Defect status.

---

## 1. Core Issue Summary

**What is the bug?**
<!-- A concise, single-sentence summary of the observable problem. -->


## 2. Expected Behavior vs. Actual Behavior

**Expected Behavior:**
<!-- What *should* have happened? (e.g., Course downloaded completely and structured correctly.) -->

**Actual Behavior:**
<!-- What *actually* happened? (e.g., Download failed mid-stream with exit code 1, or the CLI exited unexpectedly.) -->


## 3. Steps to Reproduce (STR)

Provide a minimal, reproducible sequence of steps. Use exact commands.

1.  Ensure environment is clean (e.g., `rm -rf .venv`).
2.  Install dependencies using the standard Apex workflow:
    bash
    uv venv
    source .venv/bin/activate
    uv sync
    
3.  Execute the specific command that triggered the bug (sanitized URLs/tokens):
    bash
    udemyvault download --course-url <SANITIZED_URL> --output ./test_downloads
    
4.  [Optional] Note the exact line number or file if relevant to the source code.

## 4. Environment Details

To ensure proper architectural isolation, detail your execution environment:

*   **Tool Version:** `udemyvault --version` (or output of `python -c "import ucvault; print(ucvault.__version__)"`)
*   **Operating System:** (e.g., Linux 6.5, Windows 11 Pro, macOS Sonoma)
*   **Python Version:** `python --version`
*   **Dependency State:** Are you using the `main` branch or a specific tagged release?

## 5. Diagnostics & Logs

**Crucial:** If the CLI provided any tracebacks, logs, or error messages, paste the *entire* block here. If HLS stream inspection was involved, include the relevant segment failure indicators.

text
[PASTE TRACEBACK/LOGS HERE]


## 6. Architectural Context Assessment

Based on the project's adherence to **Modular Monolith** principles, please assess if this issue appears related to:

- [ ] **Input/Validation Layer** (Parsing CLI arguments/URLs)
- [ ] **Core Processing Layer** (HLS segment handling/retries)
- [ ] **I/O Layer** (File system writing/resumability)
- [ ] **External Dependency** (Udemy API response change)

---

**Reinforce Apex Standards:** Please review the project's guiding principles in the [AGENTS.md](https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/blob/main/AGENTS.md) before submitting, particularly regarding idempotency and error handling.