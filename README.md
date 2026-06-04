# EduShare 📡

**Offline classroom screen sharing — no internet, no projector, no excuses.**

EduShare lets teachers broadcast their screen to every student's device over a local Wi-Fi network in real time. Built for classrooms where internet is unreliable or unavailable.

---

## ✨ Why It Exists

Most screen-sharing tools (Google Meet, Zoom, AnyDesk) need the internet. In many Indian classrooms and exam halls, that's not a given. EduShare works entirely offline — the teacher's device acts as the server, students connect over the same Wi-Fi, and the stream starts instantly.

---

## 🚀 Features

- **Sub-100ms latency** — real-time screen sharing over local network via WebSockets
- **Zero internet dependency** — fully peer-to-peer over LAN
- **Cross-platform** — Flutter frontend works on Android; server runs on any machine
- **Lightweight** — no heavy infrastructure, no accounts, no setup friction


---

## 🛠️ Tech Stack

| Layer | Tech |
|---|---|
| Mobile Client | Flutter (Dart) |
| Screen Capture | Kotlin + Android MediaProjection API |
| Streaming | WebSocket (low-latency binary frames) |


---

## 📐 Architecture

```
[Teacher's Device]
    └── Screen captured via MediaProjection API
    └── Encoded with FFmpeg
    └── Streamed over WebSocket (LAN)
            │
            ▼
[Student Devices — Flutter App]
    └── Connect to teacher's WebSocket server
    └── Decode and render frames in real time
```

---

## 📊 Performance

| Metric | Value |
|---|---|
| Latency | < 100ms over LAN |
| Protocol | WebSocket (binary) |
| Network | Local Wi-Fi only |
| Supported Clients | Multiple simultaneous viewers |

---

> *"Built for the 40% of Indian classrooms that don't have a working projector."*
