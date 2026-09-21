# StreamBox

StreamBox is a lightweight, self-hosted web platform designed for storing, managing, and streaming personal video files directly on your own hardware. Watch and organize your personal videos in any web browser without manual conversion or complicated server setup.

---

## 1. Project Overview

StreamBox allows administrators and authorized users to upload home videos, view a shared media library, and play back video streams on any modern web browser without relying on third-party cloud streaming services.

### Core Features

* **User Authentication**: Secure role-based login for administrators and authorized viewers.
* **Video Upload & Progress**: Direct web-based media ingestion with status reporting.
* **Automated Processing**: Automatically converts phone and camera recordings into web-friendly video formats so they play smoothly without buffering.
* **Metadata Persistence**: Reliable storage of video tags, titles, and technical specs.
* **Browser Video Playback**: Clean, responsive HTML5 streaming player.
* **Library Management**: Fast media cataloging, filtering, and video deletion.
* **Containerized Deployment**: Multi-container Docker and Docker Compose environment.
* **Automated Testing & CI/CD**: Validated build pipelines via GitHub Actions.

---

## 2. Architecture

StreamBox runs its database, video converter, and web player as separate background services so uploads never interrupt ongoing video playback.
```text
                     ┌──────────────────┐
                     │     Browser      │
                     │   Web Frontend   │
                     └────────┬─────────┘
                              │ HTTP / REST
                              ▼
                     ┌──────────────────┐
                     │   API Service    │
                     │  Authentication  │
                     │  Video Metadata  │
                     └────────┬─────────┘
                              │
               ┌──────────────┼──────────────┐
               │              │              │
               ▼              ▼              ▼
         ┌──────────┐  ┌────────────┐  ┌───────────┐
         │PostgreSQL│  │   Video    │  │   Video   │
         │ Metadata │  │  Storage   │  │ Processor │
         └──────────┘  └────────────┘  └───────────┘
```

3. Quick Start & Installation
    * PrerequisitesDocker (v24.0+)
    * Docker Compose (v2.20+)
    * Git

    Setup Instructions
        1. Clone the repository:
            git clone [https://github.com/your-username/StreamBox.git](https://github.com/your-username/StreamBox.git)
            cd StreamBox
        2. Configure environment variables:
            cp .env.example .env
        3. Start the application containers:
            docker compose up -d
        4. Access the application:
            Open http://localhost:8080 in your web browser.
