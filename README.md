# SafeLink 🛡️
### Women's Personal Safety App — IDLT Mini Project

<div align="center">

![SafeLink Banner](https://img.shields.io/badge/SafeLink-Women's%20Safety-purple?style=for-the-badge&logo=shield&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20Android-black?style=for-the-badge)
![Language](https://img.shields.io/badge/Built%20With-HTML%20CSS%20JavaScript-6B35CC?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-30D158?style=for-the-badge)

**An invisible shield. Always with you. Always silent.**

</div>

---

## 📌 About the Project

**SafeLink** is a women's personal safety web application designed to help women in distress silently trigger emergency alerts, record evidence, and connect with police — all without the attacker knowing.

The app is disguised as a normal **calculator**. Only the user knows that holding the `★` button for 3 seconds silently sends an SOS alert with live GPS location, starts camera recording, and notifies the police dashboard.

> Developed as part of the **IDLT (Innovation, Design, and Lab Techniques)** course mini-project at **East West Institute of Technology, Bengaluru**.

---

## 👥 Team Members

| Name | Role |
|------|------|
| Ruchitha | Project Lead & Developer |
| Bhavani | UI Design & Testing |
| Lasitha | Documentation & Research |
| Bhavana | Frontend Development |
| Fathima | Testing & Presentation |

**Mentor:** Prof. Ramadevi

---

## 🚨 Problem Statement

Women in India and worldwide face serious safety threats in public spaces, especially at night. Existing safety apps are **easily spotted** — opening a red SOS screen or making noise alerts the attacker. There is a need for a **silent, disguised, and intelligent** safety system that works even when the user cannot openly use their phone.

---

## 💡 Solution — SafeLink

SafeLink solves this with **4 layers of protection:**

| Layer | Feature | How it helps |
|-------|---------|--------------|
| 🧮 | **Calculator Disguise** | App looks like a normal calculator — no one suspects |
| 🆘 | **Silent SOS** | Hold ★ 3 seconds → alert sent silently in background |
| ⚠️ | **Suspicious Report** | Report threat with details + start background safety call |
| 🎙️ | **AI Voice Shield** | Mic listens for distress keywords → auto-alerts police |

---

## ✨ Features

### 🔐 Sign In & Profile Setup
- User enters name, phone number, city
- Add multiple emergency contacts
- Set police control room number
- All data stored locally on device — never shared

### 🧮 Calculator Disguise Mode
- Fully functional calculator (add, subtract, multiply, divide)
- Tap effects with ripple animation on every button press
- **Hold ★ button** → circular SVG progress ring fills up over 3 seconds → Silent SOS fires
- Calculator stays visible — attacker sees nothing unusual

### 🆘 SOS Alert System
- Hold 3 seconds → SOS overlay activates
- Shows: user's real name, phone, live GPS coordinates, timestamp
- Camera opens automatically and starts recording
- Live stream sent to police dashboard
- SMS alert sent to police number + emergency contacts
- All recordings auto-saved and backed up to cloud

### ⚠️ Suspicious Report
- Select number of people involved
- Choose reason (being followed, verbal harassment, physical threat, etc.)
- Describe the situation in your own words
- Start a **background safety call** to emergency contact
- Camera records automatically
- Full report sent to police dashboard with GPS

### 🎙️ AI Voice Shield
- Activates on **phone shake** (someone grabbing the phone)
- Microphone listens continuously every 5 seconds
- AI analyses audio for distress keywords in:
  - 🇬🇧 English: *help, save me, let go, don't touch me...*
  - 🇮🇳 Hindi: *bachao, madad karo, chod do, koi hai...*
  - 🇮🇳 Kannada: *yella bidappa, sahaya madi, kaapadiri...*
  - 🇮🇳 Telugu: *sahaayam, vadalandi, aagu...*
- If distress detected → automatically alerts police with GPS
- Confidence score and keyword detection shown on screen

### 📊 Police Dashboard
- Live view of all active alerts (SOS, Suspicious, AI Detected)
- Shows: victim name, phone number, GPS location, timestamp
- Direct call button to victim
- Dismiss resolved alerts
- Counter for each alert type

### 👤 Profile & Settings
- View and manage emergency contacts (with direct call buttons)
- Toggle: auto-camera on SOS, shake detection, silent mode
- Reset app / edit profile anytime

---

## 🗺️ App Flow

```
Sign In
   ↓
Calculator (disguise) ── hold ★ ──→ Silent SOS
   ↓ Next
Home Screen ── tap SOS ──→ Emergency Alert
   ↓ Next         └── Suspicious ──→ Report + Call
Dashboard           └── AI Shield ──→ Voice Detection
   ↓ Done
Free Navigation (bottom nav bar)
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|-----------|-------|
| HTML5 | App structure and screens |
| CSS3 | Black & purple UI, animations, SVG rings |
| Vanilla JavaScript | All logic, GPS, camera, speech recognition |
| Web Speech API | Real-time voice/audio analysis |
| Geolocation API | Live GPS coordinates |
| MediaDevices API | Camera access and recording |
| localStorage | Persistent user data storage |
| DeviceMotion API | Shake detection |

---

## 📱 How to Run

### Option 1 — Open directly in browser
```
1. Download safelink.html
2. Open in Google Chrome (Android recommended)
3. Allow permissions: Location, Camera, Microphone
4. Complete the 3-step sign-in setup
5. App is ready to use
```

### Option 2 — Host on GitHub Pages
```
1. Fork this repository
2. Go to Settings → Pages
3. Set source to main branch
4. Visit: https://yourusername.github.io/safelink
```

> ⚠️ **Best experience:** Use **Google Chrome on Android** for full Speech Recognition, Camera, GPS, and Shake Detection support.

---

## 🔐 Privacy & Security

- ✅ All personal data stored **locally on device only**
- ✅ No third-party servers — no data is ever uploaded without consent
- ✅ Emergency contacts and location shared **only during an active alert**
- ✅ Camera recording saved locally and to user's own cloud backup
- ✅ App can be fully reset and all data deleted anytime

---

## 📸 Screenshots

| Sign In | Calculator | SOS Active | Dashboard |
|---------|-----------|------------|-----------|
| 3-step profile setup | Disguised calculator | Live alert with GPS | Police alert feed |

---

## 🤖 AI Audio Analysis — System Prompt

The AI Voice Shield uses a structured prompt to classify audio every 5 seconds:

```
Threat Level: SAFE | MONITOR | ALERT
Action:       none | notify_police | escalate_sos
```

**Trigger logic:**
- `SAFE` → normal ambient sounds, stress score < 0.35
- `MONITOR` → ambiguous audio, partial keyword match
- `ALERT` → confirmed distress keyword OR two consecutive MONITORs OR stress > 0.65

---

## 🚀 Future Scope

- [ ] Flutter/React Native mobile app (iOS + Android)
- [ ] Real police API integration (Kavach / Dial 112)
- [ ] Firebase real-time cloud backup for recordings
- [ ] Wearable integration (smartwatch SOS trigger)
- [ ] Multilingual UI (Kannada, Hindi, Telugu)
- [ ] Offline SMS fallback when internet is unavailable
- [ ] Fake crash screen mode (phone appears to turn off)

---

## 📚 References

- Web Speech API — [MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)
- Geolocation API — [MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)
- MediaDevices API — [MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices)
- Women Safety Statistics India — National Crime Records Bureau (NCRB) 2023
- Nirbhaya Fund — Ministry of Women and Child Development

---

## 📄 License

This project is developed for **academic purposes** as part of the IDLT course at EWIT Bengaluru.

---

<div align="center">

Made with 💜 by Team SafeLink — EWIT Bengaluru

*"Because every woman deserves to feel safe."*

</div>
