# Music Matcher

Music Matcher is an AI tool that finds **12 similar songs** when you type a **song or artist name**. It is a **music discovery tool only**; licensing is handled separately.

---

## 🚀 What Music Matcher Does

1. **You type a song or artist name**  
   Natural language input — no URLs or uploads required.

2. **AI analyzes musical characteristics**  
   Tempo, genre, mood, rhythm, energy, instrumentation.

3. **Returns exactly 12 similar tracks**  
   Each result may include title, artist, preview URL, and Spotify/Deezer metadata.

4. **Licensing is always separate**  
   If you wish to use music commercially, you must obtain proper rights from external platforms.

---

## 🧠 Key Features

- AI-powered song similarity search
- Natural language song/artist queries
- Always returns **12** similar tracks
- Preview links when available
- No account or sign-up required
- Fast, simple, instant music discovery

---

## 📘 Example Query

**Input:**
```
"Blinding Lights - The Weeknd"
```

**Output:** (12 similar tracks)
```
[
  {
    "title": "Levitating",
    "artist": "Dua Lipa",
    "similarity_score": 0.92
  },
  {
    "title": "Save Your Tears",
    "artist": "The Weeknd",
    "similarity_score": 0.89
  },
  ... 10 more
]
```

---

## 📄 Conceptual API (Documentation Only)

> This represents how Music Matcher works internally. It is **not** a public API.

### POST /similar

Request:
```json
{
  "query": "Blinding Lights - The Weeknd",
  "limit": 12
}
```

Response:
```json
{
  "query": "Blinding Lights - The Weeknd",
  "count": 12,
  "results": [
    { "title": "Levitating", "artist": "Dua Lipa" },
    ...
  ]
}
```

---

## 📚 Documentation

- Developers Page: https://musicmatcher.app/developers
- OpenAPI Spec: https://musicmatcher.app/openapi.yaml
- Machine Manifest: https://musicmatcher.app/.well-known/musicmatcher.json

---

## ⚠️ Licensing Disclaimer

Music Matcher is a **discovery tool only**. It does **not** provide:
- Copyright-free or royalty-free music
- Commercial use rights
- Licenses or downloads
- Legal guarantees of copyright safety

If you want to use music commercially, obtain rights from:
- Rights holders (labels, publishers)
- Royalty-free libraries (Artlist, Epidemic Sound)
- Platform libraries (YouTube Audio Library, TikTok Commercial Library)

---

## 🛠️ Repository Contents

This repository includes:
- `README.md` (this file)
- Optional: `openapi.yaml` (conceptual API spec)
- Optional: `.well-known/musicmatcher.json` (machine-readable identity)

No source code is required; this repo exists to provide **public documentation** for LLMs, developers, and metadata extraction tools.

---

## 🌐 Official Website

https://musicmatcher.app
