# Vietnamese Learning Web App — Stitch AI Design Prompt

## App Overview

Design a modern, gamified **web application for learning Vietnamese**, targeting adult international learners (English-speaking). The visual style should be **clean, friendly, and motivating** — inspired by Duolingo but with a more mature, premium feel. Use a warm color palette anchored in Vietnamese cultural colors: deep red (`#C0392B`), golden yellow (`#F39C12`), with white backgrounds and soft neutral grays.

**Typography:** Rounded sans-serif (e.g. Nunito or Poppins). Large, legible font sizes for lesson content.
**Component style:** Rounded corners (12–16px radius), subtle drop shadows, colorful iconography, smooth micro-interactions.

---

## Design System Tokens

- **Primary:** `#C0392B` (Vietnamese Red)
- **Secondary:** `#F39C12` (Golden Yellow)
- **Accent:** `#27AE60` (Success Green)
- **Background:** `#FAFAFA`
- **Surface:** `#FFFFFF`
- **Text Primary:** `#1A1A2E`
- **Text Secondary:** `#6B7280`
- **Border:** `#E5E7EB`
- **XP / Gamification:** `#8B5CF6` (Purple)

---

## Pages to Design

---

### PAGE 1: Landing Page (`/`)

**Layout:** Full-width, single scroll page.

**Sections:**

**Hero Section**
- Bold headline: *"Speak Vietnamese with Confidence"*
- Subheadline: *"Learn through real conversations, not just textbooks."*
- Interactive demo widget: a small audio card showing a Vietnamese phrase with playback button and English translation
- Two CTAs: `[Start for Free]` (primary, red) and `[Watch how it works]` (ghost button)
- Background: subtle illustrated Vietnamese motifs (lotus, lantern) in light wash

**Social Proof Bar**
- "2,400,000+ learners" | "4.8★ rated" | "50+ countries"
- Logos of media mentions

**Features Section (3-column grid)**
- Card 1: 🎙️ AI Pronunciation Coaching
- Card 2: 📚 6 Tone Mastery System
- Card 3: 🔥 Daily Streak & Gamification

**Testimonials Section**
- 3 user quote cards with avatar, name, country flag

**Final CTA Section**
- Dark red background, white text
- Headline: *"Start your first lesson today — it's free"*
- Single CTA button: `[Create Free Account]`

---

### PAGE 2: Placement Test (`/onboarding/placement`)

**Layout:** Centered single-column, progress bar at top.

**Components:**
- Progress bar: step indicator (e.g. "Question 3 of 12") with animated fill
- Question card (large, centered, white surface):
  - Question text in large font (Vietnamese phrase or audio clip)
  - 4 answer options as large tap-friendly buttons (full width)
  - Selected state: highlighted with primary color border + light fill
- Audio playback button (circular, prominent) for listening questions
- `[Skip question]` ghost link at bottom
- Animated transition between questions (slide left)

---

### PAGE 3: Goal Setting (`/onboarding/goals`)

**Layout:** Centered, 2-step card wizard.

**Step 1 — Learning Goal**
- Title: *"Why are you learning Vietnamese?"*
- 4 large selectable cards in 2x2 grid:
  - ✈️ Travel & Tourism
  - 💬 Everyday Conversation
  - 💼 Business & Work
  - 👨‍👩‍👧 Connect with Family
- Each card: icon + label + short description. Selected state: red border + checkmark badge

**Step 2 — Daily Commitment**
- Title: *"How much time can you commit each day?"*
- 4 pill-style selectable options: `5 min` / `10 min` / `15 min` / `20 min`
- Motivational message updates dynamically based on selection
- Toggle: "Remind me daily at [time picker]"
- `[Let's Go →]` primary CTA button

---

### PAGE 4: Dashboard (`/dashboard`)

**Layout:** Left sidebar navigation + main content area (2-column on desktop, stacked on mobile).

**Left Sidebar:**
- App logo at top
- Nav links with icons: Home, Courses, Vocabulary, Stories, Listening, Progress, Leaderboard
- User avatar + level badge at bottom
- Collapse toggle

**Main Content — Top Row:**
- **Streak Card:** Fire emoji 🔥, "Day 14 Streak", calendar heatmap mini-view (7 days)
- **XP Card:** Progress bar toward next level, "320 / 500 XP"
- **Today's Goal Card:** Circular progress ring, "8 / 10 min today"

**Main Content — Center:**
- **Resume Card** (full-width, red gradient): "Continue where you left off" → Unit 3, Lesson 2: *"At the Market"* — `[Continue →]` button

**Main Content — Course Roadmap Preview:**
- Horizontal scrollable node-based roadmap
- Nodes: circular icons representing Units, connected by a dotted path
- States: Completed (green check), Current (pulsing red highlight), Locked (gray + lock icon)

**Main Content — Right Column:**
- **Review Alert:** "🃏 18 cards due for review today" — `[Review Now]`
- **Daily Challenge:** Themed card, e.g. "☕ Today: Ordering Coffee" — `[Start Challenge]`
- **Leaderboard Mini:** Top 3 users this week, user's current rank

---

### PAGE 5: Lesson Screen (`/lesson/:lessonId`)

> Most critical screen — design as a focused, distraction-free modal/full-screen experience.

**Layout:** Full-screen overlay (no sidebar). Top bar only.

**Top Bar:**
- `[✕ Exit]` button (left)
- XP progress bar (center, animated fill as exercises complete)
- Heart/lives indicator (right): 3 hearts ❤️❤️❤️

**Exercise Cards (6 types — design all):**

**Type A — Listen & Repeat**
- Large audio waveform visualization (animated while playing)
- Vietnamese text (large, centered) with tone marks clearly visible
- English translation below (smaller, gray)
- `[▶ Play]` circular button
- `[🎙 Record]` button → shows recording waveform → AI score badge (e.g. "87 / 100 — Great!")
- `[Try Again]` or `[Continue]` CTA

**Type B — Flashcard**
- Flip card: Front = image + Vietnamese word + audio icon; Back = English meaning + example sentence
- Swipe gesture indicator

**Type C — Fill in the Blank**
- Sentence with a blank `___` prominently shown
- Vietnamese keyboard / word bank chips below (tap to fill)
- Submit button activates after answer selected

**Type D — Word Order**
- Jumbled word chips in random order (draggable)
- Drop zone area below showing the sentence structure
- Visual snap-into-place interaction

**Type E — Image Match**
- 4-grid image cards
- Vietnamese word/audio prompt above
- Tap correct image — correct: green flash; wrong: red shake

**Type F — Dialogue**
- Chat bubble UI simulating a Vietnamese conversation
- User must select the correct reply from 3 options
- Animated chat bot avatar (Vietnamese character illustration)

**Completion Screen:**
- Confetti animation
- XP earned badge
- Accuracy score (e.g. "92% Accuracy")
- Pronunciation score if applicable
- `[Continue to next lesson]` + `[Back to Map]`

---

### PAGE 6: Pronunciation Lab (`/pronunciation`)

**Layout:** Two-column. Left = tone selector panel. Right = practice area.

**Left Panel:**
- Title: *"Vietnamese Tones"*
- 6 selectable tone cards:
  - Flat (ngang) — a
  - Falling (huyền) — à
  - Rising (sắc) — á
  - Dipping (hỏi) — ả
  - Broken (ngã) — ã
  - Heavy (nặng) — ạ
- Each shows tone contour diagram (pitch curve line illustration)
- Selected: highlighted with red border

**Right Practice Area:**
- Large Vietnamese word display (the word being practiced)
- Native speaker audio: waveform player
- User recording zone: animated microphone button + recording waveform
- Side-by-side waveform comparison (native vs user)
- Score badge: circular progress ring with percentage
- Feedback label: "Too flat — try more rising pitch" (contextual AI tip)
- `[Try Again]` / `[Next Word]` buttons

---

### PAGE 7: Vocabulary Bank (`/vocabulary`)

**Layout:** Full-width with filter sidebar.

**Filter Sidebar (left):**
- Search input
- Filter by: Unit / Topic (checkboxes)
- Filter by mastery: New / Learning / Mastered
- Sort by: Recent / Alphabetical / Due for Review

**Main Grid:**
- Masonry or 4-column card grid
- Each **Vocab Card** contains:
  - Vietnamese word (large, bold, with tone mark)
  - Romanized pronunciation (small, gray)
  - English meaning
  - Topic tag chip (e.g. "Food", "Travel")
  - Mastery indicator: colored dot (red = new, yellow = learning, green = mastered)
  - Audio icon button
- Hover state reveals: example sentence + `[Add to Review]` button

**Review Queue Banner (top):**
- "12 words due for review" with `[Start Review Session]` CTA

---

### PAGE 8: Progress Dashboard (`/progress`)

**Layout:** Full-width dashboard with chart widgets.

**Top Stats Row (4 metric cards):**
- Total XP Earned
- Current Streak (days)
- Words Mastered
- Lessons Completed

**Charts Section:**
- Weekly activity bar chart: minutes studied per day (Mon–Sun)
- Monthly XP line chart
- Vocabulary growth curve

**Skill Radar Chart:**
- Pentagon/hexagon radar showing: Listening / Speaking / Reading / Writing / Vocabulary / Grammar
- Two overlays: "This month" vs "Last month"

**Achievements / Badges Grid:**
- Earned badges (full color) + locked badges (grayscale)
- Each badge: icon + name + unlock condition

---

### PAGE 9: Leaderboard (`/leaderboard`)

**Layout:** Centered single column, max-width 600px.

**Tabs:** `Friends` | `Global`

**Top 3 Podium:**
- Visual podium design: 1st = center/tallest, 2nd = left, 3rd = right
- Each: avatar, username, XP, flag
- 1st place: gold crown icon + gold card

**Ranked List (4th onwards):**
- Row per user: rank number, avatar, name, country flag, XP this week
- Current user row: highlighted with subtle purple background
- "You are ranked #47 this week"

**Reset Timer:**
- "Leaderboard resets in: 3d 14h 22m" — countdown timer

---

## User Flows (for flow diagram generation)

### Flow 1: New User Activation
```
Landing Page
  → [Click CTA] → Sign Up Screen
  → [Complete signup] → Placement Test (10 questions)
  → [Submit] → Level Result Screen ("You're a Beginner!")
  → [Continue] → Goal Setting (Step 1: Why / Step 2: Time)
  → [Complete] → Dashboard (first visit with guided tooltip overlay)
  → [Auto-open] → First Lesson (Unit 1, Lesson 1)
  → [Complete lesson] → Celebration Screen + XP earned
  → [Prompt] → "Enable daily reminder?" → Dashboard
```

### Flow 2: Daily Returning User Loop
```
Open App → Dashboard
  → See streak status + today's goal progress
  → [Tap "Continue"] → Resume lesson in progress
  → Complete exercises → +XP animation
  → Lesson complete → suggested next lesson
  → Daily goal met → "🔥 Streak Maintained!" toast
  → [Check leaderboard] → Leaderboard Page
  → Return to Dashboard
```

### Flow 3: Vocabulary Review (Spaced Repetition)
```
Dashboard → "18 cards due" banner
  → [Tap "Review Now"] → Review Session Screen
  → Flashcard shown → User self-rates:
      [Again] / [Hard] / [Good] / [Easy]
  → SRS algorithm adjusts next review date
  → All cards done → Summary screen
      (cards by difficulty, next review date)
  → [Back to Dashboard]
```

### Flow 4: Pronunciation Practice
```
Dashboard → [Mic shortcut icon]
  → Pronunciation Lab
  → Select tone to practice (e.g. Tone 3 — Hỏi)
  → See pitch diagram + example words list
  → Select word → [Play native audio]
  → [Record] → AI analyzes → Score shown
  → [Try Again] or [Next Word]
  → End session → Accuracy summary + XP
```

---

## Key UX Notes for Stitch AI

- **Lesson Screen** should feel like a **native mobile app** even on web — full-screen, no distractions, keyboard navigation supported.
- **Tone marks** (diacritics) on Vietnamese characters must be large and legible — minimum 24px in lesson context.
- Use **celebratory micro-interactions**: confetti on lesson complete, pulse on streak maintained, shimmer on XP bar fill.
- All interactive elements should have **clear hover + active + disabled states**.
- The **Daily Loop** (Dashboard → Lesson → Complete → Dashboard) must have the shortest possible tap/click path — maximum 2 taps from open to first exercise.
- Design for **both light mode (default) and dark mode**.
- Mobile-first responsive: lesson screen collapses to full-screen on mobile, dashboard sidebar becomes bottom navigation.
