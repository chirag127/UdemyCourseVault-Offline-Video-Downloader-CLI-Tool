# UdemyCourseVault-Offline-Video-Downloader-CLI-Tool

A cross-platform Python CLI tool for downloading Udemy courses for offline use. Supports HLS streams and resumable downloads.

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/ci.yml?style=flat-square)](https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/actions/workflows/ci.yml)
[![Coverage Status](https://img.shields.io/codecov/c/github/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool?style=flat-square)](https://codecov.io/gh/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool)
[![Language](https://img.shields.io/badge/Language-Python-blue?style=flat-square)](https://www.python.org/)
[![Tech Stack](https://img.shields.io/badge/Stack-uv%2CRuff%2CPytest-informational?style=flat-square)](https://github.com/astral-sh/uv)
[![Linting](https://img.shields.io/badge/Lint%2FFormat-Ruff-success?style=flat-square)](https://github.com/astral-sh/ruff)
[![License](https://img.shields.io/github/license/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool?style=flat-square)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool?style=flat-square)](https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool)

---


<p align="center">
  <h1 align="center">Udemy Course Vault</h1>
  <p align="center">
    Empowering Udemy learners with the ability to download courses for truly offline, uninterrupted access.
    <br />
    <a href="https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/issues">Report Bug</a>
    ·
    <a href="https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/discussions">Request Feature</a>
  </p>
</p>

---


## Architecture Overview

This project employs a **Modular Monolith** architecture, ensuring a cohesive yet maintainable structure. The core components interact seamlessly, providing a robust CLI experience.

mermaid
graph TD
    A[CLI Interface] --> B(Course Downloader Logic)
    B --> C{HLS Stream Handler}
    B --> D{Resumable Download Manager}
    D --> E(File System Operations)
    C --> F(Video Segment Fetcher)
    F --> B
    B --> G(Udemy API Integration)
    G --> A


---


## Table of Contents

*   [About the Project](#about-the-project)
*   [Key Features](#key-features)
*   [Technology Stack](#technology-stack)
*   [Installation](#installation)
*   [Usage](#usage)
*   [Development](#development)
*   [Contributing](#contributing)
*   [License](#license)
*   [Contact](#contact)

---


## About the Project

Udemy Course Vault is a sophisticated command-line interface (CLI) tool meticulously crafted in Python. It enables users to download Udemy video courses, including those delivered via HLS (HTTP Live Streaming) protocols, for convenient offline viewing. With built-in support for resumable downloads, learners can ensure their course materials are always accessible, regardless of internet connectivity.

---


## Key Features

*   **Cross-Platform Compatibility:** Runs seamlessly on Windows, macOS, and Linux.
*   **Udemy Course Download:** Supports downloading entire courses or specific lectures.
*   **HLS Stream Support:** Capable of handling and downloading HLS video streams.
*   **Resumable Downloads:** Automatically resumes interrupted downloads, saving bandwidth and time.
*   **Modular Python Architecture:** Built with maintainability and extensibility in mind.
*   **Fast Dependency Management:** Leverages `uv` for efficient package installation.
*   **High-Performance Linting:** Utilizes `Ruff` for rapid code analysis and formatting.
*   **Robust Testing:** Comprehensive test suite powered by `Pytest`.

---


## Technology Stack

*   **Language:** Python 3.10+
*   **Package Manager:** `uv` (Lightning-fast Python package installer and dependency manager)
*   **Linter & Formatter:** `Ruff` (Extremely fast Python linter and formatter)
*   **Testing Framework:** `Pytest` (Simple yet powerful testing framework)
*   **CLI Framework:** `Click` (or similar for robust command-line argument parsing)
*   **HTTP Client:** `httpx` (Modern, high-performance HTTP client for Python)
*   **HLS Handling:** Libraries like `youtube-dl` (or specific HLS parsers if applicable)

---


## Installation

**Prerequisites:**

*   Python 3.10+ installed on your system.
*   `uv` installed (`pip install uv` or follow `uv`'s official installation guide).

**Steps:**

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool.git
    cd UdemyCourseVault-Offline-Video-Downloader-CLI-Tool
    

2.  **Install dependencies using `uv`:**
    bash
    uv pip install --frozen-lockfile --sysroot . --python 3.10 -r requirements.txt
    # Or for development:
    uv pip install --editable . --python 3.10
    

---


## Usage

Once installed, you can use the `udemycoursevault` command from your terminal.

**Example:**

bash
udemycoursevault download --url <udemy-course-url> --output /path/to/save/courses


**Commands:**

*   `download`: Initiates the download of a Udemy course.
    *   `--url` (required): The URL of the Udemy course page.
    *   `--output` (required): The directory where downloaded videos will be saved.
    *   `--quality`: Desired video quality (e.g., `720p`, `1080p`).
    *   `--resume`: Enables resumable download functionality (enabled by default).
*   `--help`: Displays help information for all commands.

---


## Development

This project adheres to the **Apex Technical Authority** standards, ensuring high-velocity development with zero defects.

**Setup:**

Follow the **Installation** steps above, ensuring you install dependencies in editable mode.

**Running Linters and Formatters:**

bash
# Format code
ruff format .

# Lint code
ruff check .


**Running Tests:**

bash
pytest


**Core Principles:**

*   **SOLID:** Ensuring maintainable and scalable code.
*   **DRY (Don't Repeat Yourself):** Minimizing code duplication.
*   **YAGNI (You Ain't Gonna Need It):** Focusing on necessary features.

<details>
<summary>🤖 <strong>AI Agent Directives</strong></summary>

## SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

### 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

### 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

### 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type (`pyproject.toml` for Python) and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
    *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for features like course downloading, HLS stream handling, and CLI interface, while maintaining a unified deployment.
    *   **CLI Framework:** Uses `Click` for a powerful and intuitive command-line interface.

### 4. DEVELOPMENT & VERIFICATION COMMANDS
*   **SETUP:**
    bash
    git clone https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool.git
    cd UdemyCourseVault-Offline-Video-Downloader-CLI-Tool
    uv pip install -r requirements.txt # Or uv pip install --editable .
    
*   **FORMATTING:**
    bash
    ruff format .
    
*   **LINTING:**
    bash
    ruff check .
    
*   **TESTING:**
    bash
    pytest
    
*   **BUILD:**
    *   *Note: Specific build instructions (e.g., for packaging) would be detailed in build scripts or documentation.* If packaging with PyInstaller/Briefcase, commands would vary.

### 5. ARCHITECTURAL PRINCIPLES
*   **SOLID:** Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion. Applied rigorously to ensure modularity and testability.
*   **DRY:** Avoid redundant code. Abstract common logic into reusable functions or classes.
*   **YAGNI:** Implement only what is needed now. Avoid speculative features.
*   **KISS:** Keep it simple and straightforward.

### 6. SECURITY MANDATES
*   **Dependency Scanning:** Regularly scan dependencies for vulnerabilities using tools like `Dependabot` or `Snyk`.
*   **Input Validation:** Sanitize and validate all user inputs and external data sources to prevent injection attacks.
*   **Secrets Management:** Never hardcode sensitive information (API keys, credentials). Use environment variables or a secure secrets management solution.
*   **Error Handling:** Implement robust error handling to prevent information leakage.

</details>

---


## Contributing

Contributions are welcome! Please read our [CONTRIBUTING.md](https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool/blob/main/.github/CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

---


## License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0). See the [LICENSE](LICENSE) file for more details.

---


## Contact

Chirag (Project Maintainer) - [chirag127@users.noreply.github.com](mailto:chirag127@users.noreply.github.com)

Project Link: [https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool](https://github.com/chirag127/UdemyCourseVault-Offline-Video-Downloader-CLI-Tool)
