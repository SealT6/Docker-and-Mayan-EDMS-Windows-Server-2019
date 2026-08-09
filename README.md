# Docker + Mayan EDMS on Windows Server 2019

A concise, practical guide for deploying Mayan EDMS with Docker on Windows Server 2019.

Status
- The full guide is provided as a PDF. The PDF was removed from the repository due to file size and is available for direct download.
- Download the PDF: [Download the full PDF guide](https://github.com/SealT6/Docker-and-Mayan-EDMS-Windows-Server-2019/raw/main/Redding_Sean_Docker-and-Mayan-EDMS-Windows-Server-2019.pdf)

Quick links
- Full documentation (PDF): https://github.com/SealT6/Docker-and-Mayan-EDMS-Windows-Server-2019/raw/main/Redding_Sean_Docker-and-Mayan-EDMS-Windows-Server-2019.pdf
- Docker: https://www.docker.com/
- Mayan EDMS: https://www.mayan-edms.com/
- Windows Server 2019: https://www.microsoft.com/windows-server

Overview
This repository accompanies a step-by-step installation and configuration guide for running Mayan EDMS in Docker containers on Windows Server 2019. The PDF contains complete instructions, architecture notes, configuration examples, and troubleshooting tips.

What’s in this repo
- README.md — Overview and quick-start information
- (PDF removed from repo; download via the link above)

Quick start (high level)
1. Prepare Windows Server 2019
   - Ensure Windows Server 2019 is up to date.
   - Enable required features and install OS-level dependencies.
2. Install Docker
   - Install Docker Desktop or Docker Engine compatible with Windows Server 2019.
   - Configure Docker to use Linux containers (recommended for Mayan EDMS).
3. Download the PDF guide
   - Use the link above to download the full PDF for step-by-step commands and configuration files.
4. Follow the instructions in the PDF
   - The PDF includes Docker Compose examples, environment variables, volume mappings, backup/restore procedures, and recommended security settings.

Highlights included in the PDF
- Full Docker Compose example for Mayan EDMS and required services (PostgreSQL, Redis, storage)
- Environment variable reference and secure-secret recommendations
- Volumes and backup instructions for persistent storage
- Windows Server-specific notes and common issues
- Post-deploy checks and verification steps

System requirements
- Windows Server 2019 (latest updates recommended)
- Docker compatible with Windows Server 2019 (ensure Linux containers support)
- Recommended hardware and storage specifications are listed in the PDF

Troubleshooting
- If a browser cannot render the PDF, download it and open with a standalone reader (Adobe Reader, Preview on macOS, or a modern browser).
- For Docker-specific errors, ensure Docker Engine is running and required ports are free.
- See the PDF for a troubleshooting checklist and common error messages.

Contributing
- Open an issue to report bugs or request improvements.
- Submit pull requests for content changes with a clear description of the change.

Support
- For questions about the guide, open an issue in this repository and include relevant logs and configuration files.

License
- Add a LICENSE file to state the project's license (e.g., MIT).

Changelog
- 2026-08-09 — README rewritten and clarified; PDF hosted externally and linked from README.
