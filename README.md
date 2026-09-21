# StreamBox

StreamBox is a lightweight, self-hosted web platform designed for storing, managing, and streaming personal video files directly on your own hardware[cite: 1, 3]. It features an intuitive web dashboard, automated video processing, and native in-browser playback powered by a containerized Docker architecture[cite: 1, 3].

---

## 1. Project Overview

StreamBox allows administrators and authorized users to upload home videos, view a shared media library, and play back video streams on any modern web browser without relying on third-party cloud streaming services[cite: 1, 3].

### Core Features

* **User Authentication**: Secure role-based login for administrators and authorized viewers.
* **Video Upload & Progress**: Direct web-based media ingestion with status reporting.
* **Automated Processing**: Background validation and transcoding to ensure media formats are compatible with standard browser players.
* **Metadata Persistence**: Reliable storage of video tags, titles, and technical specs.
* **Browser Video Playback**: Clean, responsive HTML5 streaming player.
* **Library Management**: Fast media cataloging, filtering, and video deletion[cite: 1].
* **Containerized Deployment**: Multi-container Docker and Docker Compose environment[cite: 1, 3].
* **Automated Testing & CI/CD**: Validated build pipelines via GitHub Actions[cite: 1, 3].

---

## 2. Architecture

StreamBox is split into decoupled services to keep playback performant and ingestion reliable[cite: 1]:

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
