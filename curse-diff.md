# US-1.3: "Curse of Knowledge" Self-Audit on Project README


---

## Flagged Sentences from README.md

### 1. Header Subtitle Sentence
* **Current Text:**
  > *"It features an intuitive web dashboard, automated video processing, and native in-browser playback powered by a containerized Docker architecture."*
* **Flaw:**
  > **Focuses on backend implementation rather than user capability.** Leading with *"powered by a containerized Docker architecture"* highlights the underlying infrastructure rather than what the user actually achieves on the platform (Bhatti et al. p. 4, 58).

### 2. Automated Processing Bullet Point
* **Current Text:**
  > *"Automated Processing: Background validation and transcoding to ensure media formats are compatible with standard browser players."*
* **Flaw:**
  > **High-friction video-engineering jargon.** Words like *"transcoding"* and *"media formats compatible with standard browser players"* sound obvious to streaming engineers, but obscure what the system actually does for non-technical users uploading home videos (Bhatti et al. p. 3, 70).

### 3. Architecture Service Description
* **Current Text:**
  > *"StreamBox is split into decoupled services to keep playback performant and ingestion reliable."*
* **Flaw:**
  > **Opaque architect-level abstraction.** Phrases like *"decoupled services"* and *"ingestion reliable"* describe distributed system design patterns instead of concrete application functions that explain why the user needs multiple containers running (Bhatti et al. p. 3, 70).

---

## Before vs. After Diff Comparison

```diff
- It features an intuitive web dashboard, automated video processing, and native in-browser playback powered by a containerized Docker architecture.
+ Watch and organize your personal videos in any web browser without manual conversion or complicated server setup.

- Automated Processing: Background validation and transcoding to ensure media formats are compatible with standard browser players.
+ Automated Processing: Automatically converts phone and camera recordings into web-friendly video formats so they play smoothly without buffering.

- StreamBox is split into decoupled services to keep playback performant and ingestion reliable.
+ StreamBox runs its database, video converter, and web player as separate background services so uploads never interrupt ongoing video playback.
