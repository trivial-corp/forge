# Trip1 Forge - Free Online Tools

## Overview
Public-facing single-file HTML tools by Trip1. Each app is a standalone `.html` file with zero external dependencies (except Google Fonts). All apps share a unified design system. Goal: attract users, provide value, drive traffic to trip1.com via UTM links.

## Design System

### Theme
- Dark/light mode toggle (persisted via localStorage)
- Dark: bg `#0c0c0f`, surface `#16161a`/`#1a1a1f`, border `#2a2a30`, text `#e0e0e6`/`#c0c0d0`/`#8888a0`
- Light: bg `#F4F5F7`, surface `#fff`, border `#E5E7EB`, text `#070A14`/`#4B5563`/`#6B7280`
- Accent: purple `#a855f7`/`#7c3aed` (primary), cyan `#38bdf8` (secondary), red `#f87171` (danger), green `#4ade80` (success)
- Font: Inter via Google Fonts, system-ui fallback

### Shared Elements
- Sticky topbar with Trip1 logo + app name + back button to Forge index
- Subtle Trip1 ad/link in footer or statusbar ("Built by Trip1 - Book 3M+ hotels worldwide, pay with crypto")
- Consistent button styles: ghost, primary (gradient), danger, save
- Smooth transitions (0.15s ease), rounded corners (8px)
- Toast notifications for user feedback
- SEO: each page has a descriptive `<title>` and a visually-hidden `<h1>` for search engines

### SEO & Tracking
- All Trip1 links use UTM params: `utm_source=forge&utm_medium=tool&utm_campaign={app-name}`
- Tracking via server-side analytics (host on apps.trip1.com or similar)
- No client-side analytics to avoid cookie consent requirements

## Apps

### 1. Image Tools (`image-tools.html`)
Photo editor with watermark removal, background removal, and mask painting.
- Brush + Magic Wand tools
- Auto background selection (edge-aware flood fill)
- Inpainting engine (distance-field based)
- Drag & drop upload, keyboard shortcuts, zoom

### 2. Email Signature (`signature.html`)
Generates HTML email signatures.
- Contact fields: name, title, email, phone, LinkedIn
- **Style selector**: Classic / Compact / Minimal layouts
- **Logo selector**: Trip1 (default, base64 embedded), or Custom (URL input field)
- Toggle options: tagline, phone, LinkedIn visibility
- Copy as rich text or raw HTML

## Rules
- Every app must be a single self-contained HTML file (no external JS/CSS besides Google Fonts)
- No server dependencies -- everything runs from `file://`
- Trip1 does NOT accept cards -- only crypto. Never mention card payments.
- Always use USDC not USDT in any Trip1 content
- No em dashes in Trip1 content
- Trip1 ad must be non-intrusive (footer link or small badge, not a banner)
