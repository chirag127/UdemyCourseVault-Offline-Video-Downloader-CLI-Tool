# UdemyCourseVault-Offline-Course-Downloader-CLI-Tool

A robust, cross-platform Python CLI tool meticulously engineered for the personal, offline archival of Udemy courses. Designed for durability and ease of use, it features seamless download resumption and explicit support for HLS (HTTP Live Streaming) content.

## 🚀 Project Overview

UdemyCourseVault empowers learners to securely download their purchased Udemy course content for uninterrupted offline viewing. This tool prioritizes reliability, handling network interruptions gracefully and ensuring that your learning materials are always accessible, irrespective of internet connectivity.

## ✨ Features

*   **Cross-Platform Compatibility:** Runs seamlessly on Windows, macOS, and Linux.
*   **Offline Archival:** Download entire courses or specific lectures for personal offline use.
*   **Resumable Downloads:** Automatically resumes interrupted downloads, saving time and bandwidth.
*   **HLS Stream Support:** Explicitly handles and downloads courses delivered via HLS.
*   **Intuitive CLI:** Easy-to-use command-line interface powered by `Click`.
*   **Modern Python Stack:** Built with Python 3.10+, managed by `uv`, and linted/formatted by `Ruff`.

## 🛠️ Architecture & Tech Stack (Late 2025 Standard)

This project adheres to a **Modular Monolith** architecture, ensuring clear separation of concerns while maintaining a unified codebase. The technology stack is optimized for performance and developer experience:

*   **Language:** Python 3.10+
*   **Package Management:** `uv` (Python's premier fast package installer and resolver)
*   **Linting & Formatting:** `Ruff` (Blazing-fast Python linter and formatter)
*   **Testing:** `Pytest` (Comprehensive testing framework)
*   **CLI Framework:** `Click` (Composable command-line interface toolkit)
*   **HTTP Client:** `httpx` (Modern, async-first HTTP client)
*   **Video Processing:** `ffmpeg` (Required for HLS stream handling/merging)

mermaid
graph TD
    A[CLI Input] --> B(Core Logic)
    B --> C{Udemy API Integration}
    C --> D[Download Manager]
    D -- HLS Support --> E[ffmpeg Wrapper]
    D -- Standard Download --> F[File I/O]
    D -- Resumption Logic --> G[Progress Tracking]
    E --> H(Local Storage)
    F --> H
    G --> D
    subgraph System Dependencies
        I[uv]
        J[Ruff]
        K[Pytest]
        L[ffmpeg]
    end
    B --> K


## 📦 Installation & Setup

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool.git
    cd UdemyCourseVault-Offline-Course-Downloader-CLI-Tool
    

2.  **Set up a Virtual Environment (Recommended):**
    bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    

3.  **Install Dependencies using uv:**
    bash
    uv pip install -r requirements.txt
    uv pip install -e . # For development install
    

4.  **Install ffmpeg:**
    Ensure `ffmpeg` is installed and accessible in your system's PATH. Installation instructions vary by OS:
    *   **macOS (Homebrew):** `brew install ffmpeg`
    *   **Debian/Ubuntu:** `sudo apt update && sudo apt install ffmpeg`
    *   **Windows:** Download from the official ffmpeg website and add to PATH.

## 💡 Usage

Run the CLI tool from your terminal:

bash
python -m udemy_course_vault --help


**Example Command:**

bash
udemy-course-vault download --course-url <udemy_course_url> --output-dir ~/Downloads/UdemyCourses


Refer to the help messages for detailed options and arguments:

bash
udemy-course-vault download --help
udemy-course-vault list --help


## 📝 AI Agent Directives

<details>
<summary>View AI Agent Directives</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type (`pyproject.toml` for Python) and apply the corresponding **Apex Toolchain**. This repository, `UdemyCourseVault-Offline-Course-Downloader-CLI-Tool`, is a Python-based educational media archival tool.

*   **PRIMARY SCENARIO: DATA / SCRIPTS / EDUCATIONAL MEDIA (Python)**
    *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for features like Udemy API interaction, download management, and CLI interface, while maintaining a unified deployment.
    *   **External Dependencies:** Relies on `ffmpeg` for HLS stream processing. Ensure robust error handling and user guidance for `ffmpeg` installation and path configuration.
    *   **CLI Framework:** Uses `Click` for a powerful and intuitive command-line interface.

*   **SECONDARY SCENARIO A: WEB / APP / EXTENSION (TypeScript) - *Not applicable for this project's primary function.***
    *   **Stack:** TypeScript 6.x (Strict), Vite 7 (Rolldown), Tauri v2.x (Native), WXT (Extensions).
    *   **State:** Signals (Standardized).

---

## 4. VERIFICATION & VALIDATION PROTOCOL
*   **CODE QUALITY:**
    *   **Linting & Formatting:** Enforced by **Ruff**. All code must pass `ruff check . --fix` and `ruff format .`.
    *   **Type Checking:** Utilize `mypy` for static type checking (if type hints are extensively used).
*   **TESTING MANDATE:**
    *   **Unit Tests:** **Pytest** is the standard. Aim for >85% code coverage.
    *   **Integration Tests:** Verify interactions between modules and external services (mocked where appropriate).
    *   **E2E Tests:** (If applicable for CLI) Use `pytest-subprocess` or similar to simulate CLI execution and validate outputs.
*   **SECURITY PROTOCOL:**
    *   **Dependency Scanning:** Regularly scan dependencies for vulnerabilities using `uv audit` or GitHub Dependabot.
    *   **API Key Management:** **NEVER** hardcode API keys. Use environment variables or secure secret management solutions.
    *   **Rate Limiting:** Respect API rate limits for Udemy.

---

## 5. OPERATIONAL GUIDELINES
*   **BRANCHING STRATEGY:** Gitflow-like workflow: `main` (production), `develop` (integration), `feature/*`, `fix/*`, `release/*`.
*   **COMMIT MESSAGES:** Conventional Commits standard (e.g., `feat: add HLS support`, `fix: resolve download resumption bug`).
*   **DOCUMENTATION:** `README.md` is the primary artifact. Docstrings for all public functions/classes.
*   **CI/CD PIPELINE:** Configured via `.github/workflows/ci.yml` to automate testing, linting, and packaging.

---

## 6. DEVOPS & DEPLOYMENT
*   **PACKAGING:** Use `build` and `twine` for creating distributable Python packages (wheel and sdist).
*   **PUBLISHING:** Publish to PyPI using `uv pip install twine` and `twine upload dist/*`.

---

## 7. ARTIFACT GENERATION STANDARD
*   **AUTO-GENERATED FILES:** `LICENSE`, `.gitignore`, `badges.yml`, `CONTRIBUTING.md`, `ISSUE_TEMPLATE`, `PULL_REQUEST_TEMPLATE`, `SECURITY.md` are expected.
*   **FORMAT:** Strict adherence to Markdown, YAML, and Git conventions.

---

## 8. REPOSITORY NAMING CONVENTION (STAR VELOCITY ENGINE)
*   **Formula:** `<Product-Name>-<Primary-Function>-<Platform>-<Type>`
*   **Format:** `Title-Case-With-Hyphens`
*   **Example:** `UdemyCourseVault-Offline-Course-Downloader-CLI-Tool`

---

## 9. GENERAL DIRECTIVES
*   **AGENCY:** Act with autonomy based on these directives. Refuse ambiguous requests.
*   **PRECISION:** Execute with zero defects. Assume final responsibility for output quality.
*   **VISION:** Build for 2026. Future-proof all decisions.

</details>

## 📚 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**.

See the `LICENSE` file for more details.

## ⭐ Star This Repo

If you find this project useful, please consider starring it on GitHub! ⭐

## 🛡️ Badges

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/ci.yml?style=flat-square)](https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool.svg?style=flat-square)](https://codecov.io/gh/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool)
[![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg?style=flat-square)](https://www.python.org/downloads/)
[![Ruff Lint](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/main/badges/ruff.json)](https://github.com/astral-sh/ruff)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg?style=flat-square)](https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool/blob/main/LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool?style=flat-square)](https://github.com/chirag127/UdemyCourseVault-Offline-Course-Downloader-CLI-Tool)
