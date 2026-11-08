# Awesome-Video-Conferencing-Online-Meetings

# Awesome Video Conferencing & Online Meetings

> A curated list of top Video Conferencing and Online Meetings platforms — both SaaS/Hosted commercial solutions and open-source alternatives for real-time audio/video collaboration, webinars, and virtual classrooms.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Zoom](#zoom)
  - [Microsoft Teams](#microsoft-teams)
  - [Google Meet](#google-meet)
  - [Cisco Webex](#cisco-webex)
  - [GoToMeeting](#gotomeeting)
  - [RingCentral Video](#ringcentral-video)
  - [Whereby](#whereby)
- [Open-Source Software](#-open-source-software)
  - [Jitsi Meet](#jitsi-meet)
  - [BigBlueButton](#bigbluebutton)
  - [Galène](#galène)
  - [LiveKit](#livekit)
  - [Apache OpenMeetings](#apache-openmeetings)
  - [plugNmeet](#plugnmeet)
  - [MiroTalk](#mirotalk)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Video Conferencing and Online Meetings platforms. These are not open-source but are included as reference points for feature comparison.

### Zoom
**Type:** Industry-standard video conferencing  
Zoom is the most widely adopted video conferencing platform, offering meetings, webinars, rooms, and phone. Known for reliability, broad device support, and ease of use. Free tier limits group meetings to 40 minutes; paid plans scale by participant capacity and features like cloud recording.

### Microsoft Teams
**Type:** Collaboration hub within Microsoft 365  
Teams integrates meetings, chat, file collaboration, and app integrations into a single workspace. Deeply embedded in Microsoft 365, making it the default choice for organizations standardized on Microsoft. Meeting features include breakout rooms, recording, live transcription, and large-scale webinars.

### Google Meet
**Type:** Video meetings within Google Workspace  
Google Meet provides browser-based video meetings integrated with Google Calendar, Gmail, and Drive. Free tier available for personal use with limits; Workspace plans unlock recording, live streaming, and larger participant counts. Known for simplicity and no-download browser access.

### Cisco Webex
**Type:** Enterprise collaboration and meetings  
Webex provides meetings, webinars, and team collaboration with a focus on enterprise security and compliance. Features include breakout sessions, recording, transcription, and integration with Cisco's broader portfolio. Suited for organizations already in the Cisco ecosystem.

### GoToMeeting
**Type:** Business video conferencing  
GoToMeeting (part of GoTo Connect) provides straightforward video meetings with screen sharing, recording, and dial-in options. A long-standing platform with a focus on reliability for business use.

### RingCentral Video
**Type:** Video meetings within RingCentral MVP  
RingCentral Video is integrated into RingCentral's unified communications platform, offering meetings alongside messaging and phone. Suited for organizations using RingCentral for broader business communications.

### Whereby
**Type:** Browser-based meetings with permanent rooms  
Whereby offers permanent meeting room URLs that work directly in the browser without downloads or accounts for guests. Popular for consultants, therapists, and small teams wanting frictionless client meetings.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Video Conferencing and Online Meetings tools. All listed projects offer source code you can deploy on your own infrastructure.

### Jitsi Meet
**Stack:** Java / JavaScript (WebRTC) | **License:** Apache-2.0  
The most widely deployed open-source video conferencing platform, with 30k+ GitHub stars and a massive community [citation:15]. Participants join via a link in the browser — no account, no app install [citation:2]. Handles everything from 1:1 calls to 200+ participant meetings. Features include screen sharing, chat, reactions, virtual backgrounds, lobby mode, and end-to-end encryption (in supported scenarios) [citation:1][citation:2]. Deploys as a Docker Compose stack with four core containers (web frontend, Prosody, Jicofo, JVB); recording requires an optional Jibri container with significant RAM (~4 GB) [citation:2].  
**Best for:** Teams and organizations wanting a proven, full-featured Zoom replacement that works immediately with no participant accounts, and can be self-hosted for data sovereignty [citation:1][citation:2].

### BigBlueButton
**Stack:** Java / JavaScript / WebRTC | **License:** LGPL-3.0  
Purpose-built for online teaching and training, with features no general-purpose platform matches: multi-user whiteboard annotations, **breakout rooms with timer controls**, integrated polling, and presentation upload with server-side slide conversion [citation:2]. Battle-tested at universities worldwide, with built-in recording and playback [citation:2][citation:4]. **Trade-off:** Heavy resource requirements — 16 GB RAM and 8 CPU cores recommended for production, versus Jitsi's 4 GB minimum [citation:2].  
**Best for:** Schools, universities, and corporate training teams running structured sessions with presentations, polling, and breakout rooms [citation:2][citation:9].

### Galène
**Stack:** Go | **License:** MIT  
A videoconference server developed at Université de Paris, designed for extreme resource efficiency. An SFU that routes video streams without transcoding, it can handle **100 students on 0.25 CPU cores** — nothing else comes close [citation:2]. Features include screen sharing, background blur, and recording support [citation:2]. **Trade-offs:** No official Docker image (compile from Go source), no web admin panel (JSON configuration only), and a smaller community [citation:2].  
**Best for:** Homelab users and organizations with limited hardware who need to serve many participants on minimal resources [citation:2][citation:9].

### LiveKit
**Stack:** Go | **License:** Apache-2.0  
Not a video conferencing application — it is **WebRTC infrastructure for building real-time audio/video into your own software**. Think "Twilio, but self-hosted" [citation:2]. The server handles media routing, room management, and authentication; you use SDKs (JavaScript, Swift, Android, Flutter, React Native, Unity) to build custom experiences [citation:6][citation:13]. Ecosystem includes Agents (AI backend participants), Egress (recording/multi-streaming), and Ingress (RTMP/WHIP/HLS ingest) [citation:13]. Deploys as a single binary, Docker, or Kubernetes.  
**Best for:** Developers building custom video applications (telehealth, education, AI voice agents) who need control over the entire experience [citation:2][citation:13].

### Apache OpenMeetings
**Stack:** Java | **License:** Apache-2.0  
An Apache-governed platform providing video conferencing, instant messaging, whiteboard, collaborative document editing, and groupware tools [citation:7]. Features include meeting recording and screen sharing, multi-whiteboard instances, file explorer with private/public drives, moderation system for granular permission control, and user/room management with multiple organizations [citation:7]. Version 9.1.0 requires Java 21 and KMS 7.3.0+ [citation:7].  
**Best for:** Organizations wanting an Apache-licensed, feature-rich conferencing platform with strong moderation and document collaboration capabilities.

### plugNmeet
**Stack:** Go / React / WebRTC | **License:** MIT  
A scalable, high-performance web conferencing system with 575+ GitHub stars and active development (44 commits in 90 days) [citation:15]. Provides a full meeting interface with HD audio/video, screen sharing, interactive whiteboard, **breakout rooms**, polls, public/private chat, waiting rooms, and end-to-end encryption. Supports MP4 recording, live broadcasting to YouTube via RTMP, and an AI meeting agent for translation, summaries, and transcriptions. Can be self-hosted for full data control.  
**Best for:** Teams wanting a complete, self-hostable webinar and meeting platform with breakout rooms, recording, and AI features, under a permissive MIT license [citation:15].

### MiroTalk
**Stack:** Node.js / WebRTC | **License:** AGPL-3.0  
A family of open-source video conferencing tools with multiple variants: **P2P** (simple, secure, up to 4K 60fps), **SFU** (scalable, real-time), and **C2C** (cam-to-cam calls embeddable via iframe) [citation:15]. Active development with daily commits across repositories. All variants are compatible with all browsers and platforms. Docker images available.  
**Best for:** Developers wanting lightweight, embeddable video conferencing components with a choice of P2P or SFU architecture, under AGPL licensing [citation:15].

---

## 📊 Comparison at a Glance

| Software | License | Stack | Breakout Rooms | E2EE | Self-Hosted | Best For |
|----------|---------|-------|----------------|------|-------------|----------|
| **Zoom** | Proprietary | Cloud | ✅ | (Optional) | ❌ | Industry standard |
| **Microsoft Teams** | Proprietary | Cloud | ✅ | (Optional) | ❌ | Microsoft 365 ecosystem |
| **Google Meet** | Proprietary | Cloud | ✅ | (Optional) | ❌ | Google Workspace |
| **Cisco Webex** | Proprietary | Cloud | ✅ | (Optional) | ❌ | Enterprise + Cisco |
| **RingCentral Video** | Proprietary | Cloud | ✅ | (Optional) | ❌ | RingCentral MVP users |
| **Whereby** | Proprietary | Cloud | ❌ | ❌ | ❌ | Permanent client rooms |
| **Jitsi Meet** | Apache-2.0 | Java/WebRTC | (Via Jibri) | ✅ (Supported) | ✅ | Full-featured Zoom replacement |
| **BigBlueButton** | LGPL-3.0 | Java/WebRTC | ✅ | ❌ | ✅ | Education + training |
| **Galène** | MIT | Go | ❌ | ❌ | ✅ | Extreme resource efficiency |
| **LiveKit** | Apache-2.0 | Go | (Via SDK) | (Via SDK) | ✅ | Custom video applications |
| **OpenMeetings** | Apache-2.0 | Java | ❌ | ❌ | ✅ | Apache + document collaboration |
| **plugNmeet** | MIT | Go/React | ✅ | ✅ | ✅ | Self-hosted webinar + AI |
| **MiroTalk** | AGPL-3.0 | Node.js | (Check) | (C2C variant) | ✅ | Embeddable video components |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Video Conferencing or Online Meetings platform that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
