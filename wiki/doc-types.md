# Documentation Types in Real Repositories

This matrix categorizes open-source projects into the four core documentation types based on Chinchilla Chapter 2 (Getting Started, Tutorials, Reference, and API)[cite: 2, 4].

| Repository | Documentation Type | Typical User Query Answered | Typical File Path / URL Location |
| :--- | :--- | :--- | :--- |
| **FastAPI** | **Getting Started** | "Би хэрхэн FastAPI server үүсгэх вэ?" ("How do I create a FastAPI server?") | `/docs/en/docs/tutorial/first-steps.md`[cite: 5] |
| **FastAPI** | **Tutorial** | "Би хэрхэн FastAPI ашиглан API үүсгэх вэ?" ("How do I build an API using FastAPI?") | `/docs/en/docs/tutorial/`[cite: 5] |
| **FastAPI** | **Reference** | "Энэхүү FastAPI component ямар parameter болон method хүсэж байна вэ?" ("What parameters and methods does this FastAPI component require?") | `/docs/en/docs/reference/`[cite: 5] |
| **FastAPI** | **API** | "Миний application ямар endpoint-үүд угтаж байна, тэдгээрийг яаж дуудах вэ?" ("What endpoints does my application expose, and how do I call them?") | FastAPI-д өөрийн гэсэн API бий. Энэ нь API үүсгэдэг framework програм юм. (`/docs` or Swagger UI)[cite: 5] |
| **Docker** | **Getting Started** | "Би яаж Docker суулгаж container ажиллуулах вэ?" ("How do I install Docker and run a container?") | `docs.docker.com/get-started/`[cite: 5] |
| **Docker** | **Tutorial** | "Би яаж application-г container дотор build хийх вэ?" ("How do I build an application inside a container?") | `docs.docker.com/get-started/tutorials/`[cite: 5] |
| **Docker** | **Reference** | "Энэ Docker command юу хийдэг вэ?" ("What does this Docker command do?") | `docs.docker.com/reference/`[cite: 5] |
| **Docker** | **API** | "Docker daemon-той daemon-р хэрхэн харьцах болон ямар application-с хэрэглэх вэ?" ("How do I interact with the Docker daemon and use it from an application?") | `docs.docker.com/reference/api/engine/`[cite: 5] |
| **FFmpeg** | **Getting Started** | "Би FFmpeg-г яаж ашиглах вэ?" ("How do I get started with and use FFmpeg?") | `ffmpeg.org/ffmpeg.html`[cite: 6] |
| **FFmpeg** | **Tutorial** | "Би FFmpeg-р юу юу хийж болох вэ?" ("What workflows and tasks can I accomplish using FFmpeg?") | `ffmpeg.org/ffmpeg.html#Detailed-description`[cite: 6] |
| **FFmpeg** | **Reference** | "Энэ бүх option-ууд юу тодорхойлж байна вэ?" ("What does each configuration flag and option specify?") | `ffmpeg.org/ffmpeg.html#Options`[cite: 6] |
| **FFmpeg** | **API** | "Би FFmpeg-г хэрхэн application-доо холбож хэрэглэх вэ?" ("How do I integrate and call the FFmpeg libraries in my application?") | `ffmpeg.org/doxygen/trunk/index.html`[cite: 6] |
