# Music Matcher

An AI-powered music discovery tool that helps you find similar songs instantly.

**Music Matcher is an AI tool that finds 12 similar songs when you type a song or artist name. It is a discovery tool only; licensing is handled separately.**

Perfect for content creators, playlist curators, DJs, and music lovers looking to discover new tracks that match their favorite songs.

---

## 🎵 Features

- **Natural Language Input** – Type any song or artist name; no URLs or complex queries required
- **AI-Powered Similarity** – Advanced analysis of tempo, genre, mood, energy, and instrumentation
- **Consistent Results** – Returns exactly 12 similar tracks per query
- **Rich Metadata** – Includes artist, title, album art, preview URLs, and platform links
- **Preview Integration** – 30-second audio previews via Spotify and Deezer (where available)
- **No Account Required** – Instant results with no sign-up or login
- **Discovery Focused** – Pure music discovery tool; licensing handled externally

---

## 🚀 How It Works

1. **User types a song or artist name**  
   Natural language input like "Blinding Lights", "The Weeknd", or "Dua Lipa - Levitating"

2. **AI analyzes musical characteristics**  
   The system evaluates tempo, key, genre, mood, rhythm, energy level, and instrumentation to understand the song's essence

3. **Returns 12 similar tracks with metadata**  
   Results include artist, title, album artwork, preview URLs, Spotify/Deezer links, and similarity scores

4. **User handles licensing separately**  
   Music Matcher does not provide music licenses, downloads, or copyright-safe guarantees. Users must obtain proper licensing from rights holders or royalty-free platforms.

---

## 📡 Example Usage (Conceptual API)

Music Matcher's conceptual API demonstrates how similarity search works:

### Request
```http
POST /api/similar
Content-Type: application/json

{
  "query": "Blinding Lights - The Weeknd",
  "limit": 12
}
```

### Response
```json
{
  "query": "Blinding Lights - The Weeknd",
  "count": 12,
  "results": [
    {
      "title": "Levitating",
      "artist": "Dua Lipa",
      "spotify_id": "463CkQjx2Zk1yXoBuierM9",
      "preview_url": "https://p.scdn.co/mp3-preview/...",
      "image_url": "https://i.scdn.co/image/...",
      "similarity_score": 0.92
    },
    {
      "title": "Save Your Tears",
      "artist": "The Weeknd",
      "spotify_id": "5QO79kh1waicV47BqGRL3g",
      "preview_url": "https://p.scdn.co/mp3-preview/...",
      "image_url": "https://i.scdn.co/image/...",
      "similarity_score": 0.89
    }
    // ... 10 more tracks
  ]
}
```

For full API documentation: [OpenAPI spec (raw YAML)](https://musicmatcher.app/openapi.yaml) and [Developers page](https://musicmatcher.app/developers) (inline spec + download link).

---

## 🌐 Live Site

- **Website (tool):** [musicmatcher.app](https://musicmatcher.app) – single canonical URL for the similar-song finder
- **Developer docs:** [musicmatcher.app/developers](https://musicmatcher.app/developers) – API overview, OpenAPI spec (inline + download), technical deep dive
- **OpenAPI spec (raw):** [musicmatcher.app/openapi.yaml](https://musicmatcher.app/openapi.yaml) – OpenAPI 3.1, view or download
- **Machine-readable manifest:** [musicmatcher.app/.well-known/musicmatcher.json](https://musicmatcher.app/.well-known/musicmatcher.json)

### Resources (guides and articles)
- **Hub:** [musicmatcher.app/resources](https://musicmatcher.app/resources)
- [How to Find Similar Songs](https://musicmatcher.app/resources/how-to-find-similar-songs)
- [Royalty-Free Song Alternatives](https://musicmatcher.app/resources/royalty-free-song-alternatives)
- [AI Music Finder for Creators](https://musicmatcher.app/resources/ai-music-finder-for-creators)

---

## 🤖 For LLMs & AI crawlers

This repo (and the public copy at **musicmatcherapp**) is maintained so AI assistants and API clients can discover and use Music Matcher.

**Canonical URLs (use these):**
- **Tool:** `https://musicmatcher.app` – find 12 similar songs by typing a song or artist name; no auth.
- **API docs + OpenAPI:** `https://musicmatcher.app/developers` – spec is shown on the page and available for download.
- **OpenAPI spec (raw YAML):** `https://musicmatcher.app/openapi.yaml` – OpenAPI 3.1; `POST /api/similar` with body `{ "query": "Song - Artist", "limit": 12 }` returns similar tracks (conceptual; implementation may differ).
- **Resources hub:** `https://musicmatcher.app/resources` – guides (how-to, royalty-free, AI for creators).
- **Well-known:** `https://musicmatcher.app/.well-known/musicmatcher.json` – machine-readable manifest.

**Important:** Music Matcher is a **discovery tool only**. It does not provide music licenses, royalty-free guarantees, or downloads. Users obtain licensing separately.

---

## ⚖️ Legal & Licensing Disclaimer

**Important:** Music Matcher is a **discovery tool only**. We help you find songs that sound similar to tracks you love, but we do **not** provide:

- ❌ Music licenses or rights to use tracks commercially
- ❌ Royalty-free music or copyright-safe guarantees
- ❌ Music downloads or offline access
- ❌ Legal protection regarding copyright claims

**Users must obtain proper licensing separately** from:
- Rights holders (record labels, publishers, distributors)
- Royalty-free music platforms (Epidemic Sound, Artlist, AudioJungle, etc.)
- Platform-specific music libraries (YouTube Audio Library, TikTok Commercial Music Library)

Music Matcher shows you what exists; you handle licensing separately.

---

## 🛠️ Tech Stack

### Frontend
- **Framework:** React 18 with TypeScript
- **Build Tool:** Vite
- **UI Components:** Radix UI + Tailwind CSS
- **State Management:** React Query (TanStack Query)
- **Routing:** React Router v6

### Data Sources
- **Spotify API** – Track metadata, previews, and similarity data
- **Deezer API** – Additional preview URLs and album artwork
- **Last.fm API** – Similar track recommendations and enrichment

### Infrastructure
- **Deployment:** Static hosting (details omitted for security)
- **CDN:** Optimized asset delivery with compression
- **Analytics:** Privacy-focused user tracking

---

## 📊 Key Statistics

- **12 tracks** returned per query (consistent output)
- **70,000+ songs** matched across all users
- **2,100+ active users** discovering new music daily
- **Sub-2-second** response time for initial results
- **Zero cost** to users – completely free with no sign-up

---

## 🎯 Use Cases

Music Matcher is ideal for:

- **Content Creators** – Find background music inspiration for YouTube videos, TikToks, and reels
- **Playlist Curators** – Build cohesive playlists with similar-sounding tracks
- **DJs** – Discover smooth transitions and set-building tracks
- **Music Bloggers** – Find tracks to feature alongside trending songs
- **Casual Listeners** – Explore new music based on favorites
- **Streamers** – Build background music playlists for live streams

---

## 🚧 Roadmap / Future Ideas

Possible future enhancements (not guaranteed):

- [ ] Batch similarity search (multiple songs at once)
- [ ] Playlist import from Spotify/Apple Music
- [ ] Advanced filtering (tempo range, year, genre constraints)
- [ ] Mood-based discovery ("find upbeat songs like X")
- [ ] Collaborative playlist building
- [ ] Export to multiple streaming platforms
- [ ] API rate limiting and authentication for high-volume users

---

## 🤝 Contributing

This repository represents the public-facing codebase for Music Matcher. Contributions, bug reports, and feature requests are welcome.

### Development Setup

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### Code Standards
- TypeScript strict mode enabled
- ESLint + Prettier for code formatting
- Component-based architecture with hooks
- Responsive design (mobile-first)

---

## 📄 License

This project's code is provided as-is for reference and educational purposes. 

**Note:** Music Matcher does not grant any licenses for the music tracks it helps you discover. All music rights remain with their respective copyright holders.

---

## 📞 Contact & Support

- **Website:** [musicmatcher.app](https://musicmatcher.app)
- **Instagram:** [@musicmatcherapp](https://www.instagram.com/musicmatcherapp)
- **Product Hunt:** [Music Matcher](https://www.producthunt.com/products/music-matcher)

For developer-specific questions, see the [Developer Documentation](https://musicmatcher.app/developers).

---

## 🧠 How It Works (Technical Deep Dive)

### Similarity Algorithm
Music Matcher uses a multi-factor similarity algorithm that analyzes:

1. **Acoustic Features**
   - Tempo (BPM)
   - Key and mode
   - Time signature
   - Loudness and dynamics

2. **Musical Characteristics**
   - Genre classification
   - Mood and valence
   - Energy level
   - Danceability

3. **Structural Elements**
   - Instrumentation
   - Vocal presence
   - Production style
   - Era/decade indicators

4. **Collaborative Filtering**
   - Last.fm similar artist data
   - Spotify's related tracks API
   - User listening patterns (aggregated, anonymized)

The system combines these signals to generate a similarity score (0-1) and returns the top 12 matches.

### Data Flow
```
User Input → Search API → Track Resolution → Similarity Analysis → 
Result Ranking → Metadata Enrichment → JSON Response → UI Rendering
```

### Performance Optimization
- Initial results: < 2 seconds
- Metadata enrichment: Progressive (background)
- Caching: Aggressive for popular queries
- CDN: Global edge caching for static assets

---

## 🎓 Educational Value

Music Matcher demonstrates several modern web development patterns:

- **React Hooks** – Custom hooks for animation, mobile detection, and state
- **Lazy Loading** – Route-based code splitting for optimal bundle size
- **Progressive Enhancement** – Works without JavaScript (basic functionality)
- **SEO Optimization** – Server-side rendering compatible, semantic HTML
- **Accessibility** – ARIA labels, keyboard navigation, screen reader support
- **Performance** – Lighthouse scores > 90 across all metrics

---

## 🙏 Acknowledgments

Music Matcher wouldn't be possible without:

- **Spotify** – Track metadata and preview URLs
- **Deezer** – Additional preview coverage
- **Last.fm** – Similar artist relationships
- The open-source community for amazing tools and libraries

---

<div align="center">

**Music Matcher** – Discover music you'll actually like.

[Try it now](https://musicmatcher.app) • [Developers & OpenAPI](https://musicmatcher.app/developers) • [OpenAPI YAML](https://musicmatcher.app/openapi.yaml) • [Resources](https://musicmatcher.app/resources)

Made with ❤️ for music lovers everywhere.

</div>
