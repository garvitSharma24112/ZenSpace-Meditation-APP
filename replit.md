# ZenSpace - Meditation & Breathing Exercises App

## Overview
ZenSpace is a meditation and breathing exercise web application with 100+ auto-generated guided sessions, customizable breath patterns, and ambient soundscapes. The app features a beautiful, responsive design with dark mode support.

## Current State
- **Frontend**: Complete with Library, Builder, and Player views
- **Backend**: Minimal Express server (sessions generated client-side)
- **Design**: Following design_guidelines.md with meditation theme colors

## Project Architecture

### Frontend (`client/src/`)
- **pages/home.tsx**: Main app with three views:
  - Library View: Browse 100+ meditation sessions with search/filter
  - Builder View: Create custom sessions with breath patterns
  - Player View: Interactive breathing visualizer with timer
- **components/theme-provider.tsx**: Dark/light mode context
- **components/theme-toggle.tsx**: Theme toggle button

### Backend (`server/`)
- **routes.ts**: Express API routes (minimal, mostly static)
- **storage.ts**: In-memory storage interface

### Shared (`shared/`)
- **schema.ts**: TypeScript types and Zod schemas

## Key Features
1. **100+ Meditation Sessions**: Auto-generated across 7 categories (Anxiety, Sleep, Focus, Gratitude, Healing, Morning, Vipassana)
2. **Breathing Visualizer**: Animated circle that scales with breath phases (inhale, hold, exhale)
3. **Customizable Breath Patterns**: Adjust inhale, hold, exhale timings
4. **Audio Playback**: 5 preset ambient sounds + custom URL support
5. **Search & Filter**: Find sessions by name or category
6. **Dark Mode**: Toggle between light and dark themes
7. **Responsive Design**: Works on mobile and desktop

## Design System
- **Primary Color**: Emerald/teal (160 84% 39%)
- **Fonts**: Playfair Display (serif headings), Inter (body text)
- **Category Colors**: Rose (Anxiety), Indigo (Sleep), Emerald (Focus), Amber (Gratitude), Teal (Healing), Orange (Morning), Slate (Vipassana)

## Running the Project
```bash
npm run dev
```
This starts both the Express backend and Vite frontend on port 5000.
