<div align="center">

# ReplyPilot AI

**An Android app that helps Facebook sellers in Bangladesh reply faster and track customers, orders, stock and follow-ups.**

![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)
![Riverpod](https://img.shields.io/badge/State-Riverpod-00B0FF)
![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)

[**Download APK**](https://github.com/sumaiya-akter-runa/ReplyPilot_AI/releases/latest) [API Docs](https://replypilot-backend-recc.onrender.com/docs)

</div>

---

## Overview

Facebook sellers answer the same questions all day: *"What is the price?"*, *"Is size M available?"* ReplyPilot reads the seller's own products, prices and stock, and writes a ready-to-send reply in Bangla, Banglish or English. The seller reviews, edits and sends it.

> **Prices and stock come from the database. The AI only writes the language.**
> Nothing is sent automatically.

## Features

- **Reply Studio:** paste a message, pick language and tone, refine with one tap
- **Customers:** new, interested, follow-up, ordered, lost, with message history
- **Orders:** stock decreases automatically, cancelling restores it
- **Follow-up reminders:** AI-drafted follow-up messages
- **Products:** size variants, stock levels, low-stock alerts, FAQs
- **Home:** today's customers, orders and sales, plus AI usage

## Screenshots

| Home | Reply Studio | Customers |
|:---:|:---:|:---:|
| ![Home](screenshots/home.png) | ![Reply](screenshots/reply.png) | ![Customers](screenshots/customers.png) |

## Install

1. Download `app-release.apk` from the [latest release](https://github.com/sumaiya-akter-runa/ReplyPilot_AI/releases/latest)
2. Open it on an Android phone (allow *Install from unknown sources* if asked)
3. Register, add your products and start replying

> The server may take up to a minute to respond after being idle.

## Run from Source

```bash
git clone https://github.com/sumaiya-akter-runa/ReplyPilot_AI.git
cd ReplyPilot_AI
flutter pub get
flutter run --dart-define=API_BASE_URL=https://replypilot-backend-recc.onrender.com
```

## Tech Stack

| Layer | Technology |
|---|---|
| App | Flutter, Dart, Riverpod, Dio |
| Backend | FastAPI, SQLAlchemy, Pydantic |
| Database | PostgreSQL (Neon) |
| Security | JWT, Argon2 |
| Deployment | Docker, Render |
| AI | Groq API |

## Known Limitations

- Messenger is not connected yet, so messages are pasted manually
- No push notifications
- Android only

## Roadmap

- [ ] Messenger webhook for automatic incoming messages
- [ ] Push notifications for follow-ups
- [ ] Share-to-app from Messenger

## Author

**Sumaiya Akter Runa**, Flutter developer
