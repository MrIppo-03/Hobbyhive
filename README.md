# HobbyHive – Hobby Discovery Web App

## Overview

HobbyHive is a **static, client‑side web application** that helps users discover a hobby based on a 15‑question quiz, view the resulting hobby with a personalized roadmap, and explore community links (Reddit, Discord, YouTube, Meetups, etc.).

- **No backend/server** is required – just open `index.html` in a modern browser.
- All data (user profile, quiz answers, community posts) are stored in **`localStorage`**.
- Includes:
  - Landing page (`index.html`)
  - Login/registration (`login.html`)
  - Quiz flow (`quiz.html`)
  - Result page (`result.html`)
  - All‑hobbies catalog (`communities.html`)
  - In‑app community feed (`community-feed.html`)
  - Profile dashboard (`profile.html`) for quiz history, active hobby, and saved communities
  - Supporting scripts (`js/` folder) and Tailwind-based styling (`css/style.css`).

## File Structure
```
hobby-discovery/
├─ index.html               # Home / landing page
├─ login.html               # Demo, guest & registration UI
├─ quiz.html                # 15‑question quiz UI
├─ result.html              # Hobby allotment & community cards
├─ communities.html         # Catalog of every hobby with links
├─ community-feed.html      # Mini forum / feed for hobby posts
├─ profile.html             # Personal hobby dashboard
├─ css/
│   └─ style.css            # Tailwind + custom glass‑morphism CSS
└─ js/
    ├─ quiz-data.js          # Quiz questions & weights
    ├─ communities-data.js   # Hobby catalog & community URLs
    ├─ quiz-engine.js        # Scoring & result generation
    ├─ auth.js               # LocalStorage‑based auth & profile
    ├─ feed.js               # In‑app community feed logic
    ├─ app.js                # UI helpers (toast, confetti, clipboard)
    └─ ... (other utilities)
```

## How to Run
1. **Open the site**
   - Navigate to the `hobby-discovery` folder.
   - Double‑click `index.html` **or** right‑click → *Open with* → your browser (Chrome, Edge, Firefox, Safari).
   - Ensure the browser permits `localStorage` for `file://` URLs (most modern browsers do).
2. **Explore the flow**
   - Click **“Take 15‑Question Quiz”** → answer any options.
   - After the last question you’ll see a short “calculating” overlay, then you’ll be redirected to `result.html`.
   - The result page shows your primary hobby, match percentage, a starter‑kit, roadmap, and community cards.
   - Use **“Save to My Profile”** to persist the result and **“Share Allotment”** to copy a summary to the clipboard.
   - Bookmark community cards – the state is saved per user.
3. **Login / Demo**
   - Click **Login** in the navigation bar.
   - Use **Demo Login** (pre‑filled) or **Guest Login** (temporary account). You can also register a new user.
   - After login the navbar updates with your avatar and a logout button.
4. **Community Feed**
   - From the navbar, go to **Feed** → `community-feed.html`.
   - Create a new post, like posts, and add comments. All interactions persist via `localStorage`.
5. **All Hobbies Catalog**
   - Click **All Communities** in the navbar or go to `communities.html`.
   - Browse every hobby card; each card links to a dedicated hub (currently the same page, but you can extend it).

## Notes & Future Improvements
- The app is fully static; for a production deployment you might host it on GitHub Pages, Netlify, or any static‑site host.
- The profile dashboard is available from the navbar after login and also supports guest sessions.
- The community hub links (`communities.html?hobby=…`) are placeholders; you can expand them to dedicated hobby pages.
- Mobile responsiveness has been tested with Tailwind’s default breakpoints, but fine‑tuning may be desired.
- All external links open in a new tab (`target="_blank"`).

---

© 2026 HobbyHive • All rights reserved
