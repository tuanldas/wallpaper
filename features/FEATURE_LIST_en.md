# DIY Wallpaper Maker Collage - Feature Overview

> **Package**: `com.diy.wallpaper.maker.collage`
> **Developer**: LeafMotion Software (buihieu2568@gmail.com)
> **Business Model**: 100% Ad-supported (free, no subscription/IAP)
> **Exploration Date**: 2026-02-27

---

## Table of Contents

1. [Onboarding Flow](#1-onboarding-flow)
2. [Home Screen](#2-home-screen)
3. [Wallpaper Categories & Templates](#3-wallpaper-categories--templates)
4. [Wallpaper Creation (Editor)](#4-wallpaper-creation-editor)
5. [Wallpaper Preview & Set Flow](#5-wallpaper-preview--set-flow)
6. [My Gallery](#6-my-gallery)
7. [Settings](#7-settings)
8. [Monetization (Ads)](#8-monetization-ads)

---

## 1. Onboarding Flow
**Folder**: `09_onboarding/`

| Step | Content | Details |
|------|---------|---------|
| 0 | App Open Ad | Full-screen interstitial ad (Google AdMob), countdown + Close |
| 1 | Language Selection | 19 languages (English by default), with country flags |
| 2 | Intro Slide 1 | "1000+ Unique Wallpaper" |
| 3 | Intro Slide 2 | "Design your own wallpaper" |
| 4 | Interest Selection | 11 categories, select 1+, tap "Get Started" |

- **Cannot be skipped** - users must go through all steps
- **No Back button** between slides
- **Typos present**: "Ducth" (Dutch), "Let select" (Let's select)

---

## 2. Home Screen
**Folder**: `01_home_screen/`

### Layout
- **Header**: 3D image banner + "My Gallery" + Settings icon
- **Create wallpaper**: "TRY NOW" button (pink gradient) -> opens Editor
- **Category tabs**: 11 horizontally scrollable tabs
- **Filter**: All / Favorite
- **Wallpaper grid**: 3 columns, infinite scroll, heart/favorite icon
- **Live badge**: "(>) Live" for live wallpapers

### Interactive Elements
| Element | Action |
|---------|--------|
| TRY NOW | Opens Wallpaper Editor (blank canvas) |
| My Gallery | Opens personal wallpaper library |
| Settings (gear) | Opens Settings |
| Category tab | Filters wallpapers by category |
| Wallpaper card | Opens preview (through interstitial ad) |
| Heart icon | Marks as Favorite |
| Filter dropdown | Switches between All / Favorite |

---

## 3. Wallpaper Categories & Templates
**Folder**: `07_wallpaper_categories/`

| # | Category | Count | Style |
|---|----------|-------|-------|
| 1 | For you | 20+ | Curated based on interests, default tab |
| 2 | DIY | 15+ | Collage, scrapbook, polaroid |
| 3 | Love | 12+ | Hearts, neon, 3D, couples |
| 4 | Live | 10+ | Animated wallpapers |
| 5 | Lock Screen | 10+ | Optimized for lock screen |
| 6 | Kawaii | 8+ | Cute Japanese style, pastel |
| 7 | Aesthetic | 8+ | Dreamy, pink/purple pastel |
| 8 | Quote | 8+ | Inspirational quotes + typography |
| 9 | Famous | 6+ | Ronaldo, Spider-Man, Messi (pop art) |
| 10 | Car | 6+ | Supercars: Ferrari, Lamborghini |
| 11 | Anime | 6+ | Anime scenery, characters, cherry blossoms |

**Total**: ~100+ wallpaper templates
**Filter**: All / Favorite

---

## 4. Wallpaper Creation (Editor)
**Folder**: `02_wallpaper_creation/` and `03_collage_creation/`

### Access Points
- Home > "TRY NOW" (create new, blank canvas)
- Home > Tap wallpaper > Preview > Next (edit existing wallpaper)

### 4 Main Tools

#### 4.1 BG (Background)
- Color picker (gradient circle)
- 9+ preset solid colors
- "Add Image" - import photo as background
- 15-20 background templates (hearts, gradients, clouds, kawaii)

#### 4.2 Import
- Opens "Select Photo" from gallery
- Tabs: "All albums" / "Recent"
- Requests permission on first use (Allow limited / Allow all / Don't allow)

#### 4.3 Text
- Input field (placeholder "Hello")
- Text Library: 5 decorative patterns (symbols: hearts, stars, sparkles)
- 8+ fonts (serif, sans-serif, handwriting, decorative)
- 9+ preset colors + color wheel

#### 4.4 Sticker
- 30+ stickers:
  - Flowers, hearts, animals (cat, bear, bunny)
  - Hello Kitty, crown, rainbow
  - Bow/ribbon, butterfly, star, soccer ball
  - Characters, decorative text

### Additional Features
| Feature | Description |
|---------|-------------|
| Layer Management | Manage layer order, lock/unlock |
| Undo/Redo | Undo / redo actions |
| Preview | View wallpaper as lock screen (shows time/date) |

### What's NOT Included
- No filters/effects
- No dedicated crop/resize/rotate tools
- No separate "Collage" tab - the editor is a layer-based compositor

---

## 5. Wallpaper Preview & Set Flow
**Folder**: `08_wallpaper_preview_flow/` and `05_export_share/`

### Full Flow (6 steps + 3-4 ads)
```
Tap wallpaper -> [Interstitial Ad] -> Preview (swipe) -> [Interstitial Ad]
-> Edit -> Next -> [Rewarded Ad "Get this item"] -> Set Wallpaper
```

### Details
| Step | Screen | Ad? |
|------|--------|-----|
| 1 | Tap wallpaper from grid | Interstitial video (mandatory) |
| 2 | Preview: swipe left/right, carousel of 3 cards | Banner ad at bottom |
| 3 | Tap Next -> switch to Edit | Interstitial video (mandatory) |
| 4 | Edit: can modify or tap Next | - |
| 5 | Popup "Get this item" | Watch now (rewarded) / No thanks |
| 6 | Set Wallpaper | Choose: Home / Lock / Both |

### Set Wallpaper Options
- **Home Screen** - main screen wallpaper
- **Lock Screen** - lock screen wallpaper
- **Home Screen and Lock Screen** - both screens

### Limitations
- **No** Download/Save as file option
- **No** Share wallpaper feature (only shares app link)
- Only direct wallpaper setting via Android wallpaper service

---

## 6. My Gallery
**Access**: Home > "My Gallery"

- Stores downloaded/created wallpapers
- When empty: "Nothing here yet" + 3D mascot + "Explore now"
- "Select" button for multi-item selection
- Filter: All / Favorite
- Banner ad at bottom of screen

---

## 7. Settings
**Folder**: `04_settings/`

| Item | Action |
|------|--------|
| Language | Choose from 19 languages |
| Term of Service | Opens web page (sites.google.com) |
| Privacy Policy | Opens web page (sites.google.com) |
| Rating 5 Stars | In-app rating dialog |
| Share with Friend | Android Share Sheet (Play Store link) |

### What's NOT in Settings
- No Account/Profile/Login
- No Notification settings
- No Dark mode
- No "Remove Ads" / "Go Premium"
- **The only screen WITHOUT ads**

### Legal Information
- **Company**: LeafMotion Software
- **Contact**: buihieu2568@gmail.com
- **Minimum Age**: 13+
- **Permissions**: INTERNET, ACCESS_NETWORK_STATE, CAMERA, VIBRATE, POST_NOTIFICATIONS

---

## 8. Monetization (Ads)
**Folder**: `06_monetization/`

### Business Model
- **100% ad-supported** - NO subscription, IAP, or paywall
- All features are free but require watching ads

### 4 Ad Types

| Type | Placement | Mandatory? | Frequency |
|------|-----------|------------|-----------|
| **Banner** | Bottom of most screens | Yes (always visible) | Every screen |
| **Interstitial** (video) | Every screen transition | Yes (countdown + skip) | Every screen change |
| **Rewarded** (video) | When saving wallpaper ("Get this item") | Yes (required to save) | Every save |
| **Native** | Mixed into grids and lists | Yes | Scattered |

### Ad Networks
| Network | Role | Ad Types |
|---------|------|----------|
| **Pangle** (TikTok for Business) | Primary | Banner, Interstitial, Rewarded, Native |
| **Google AdMob** | Secondary | App Open Ad, possible mediation |

### Ad Placement by Screen
| Screen | Ad Type |
|--------|---------|
| App launch (first time) | Interstitial (AdMob) |
| Onboarding slides | Banner (Pangle) |
| Home screen | Banner (Pangle/CapCut) |
| Tap wallpaper | Interstitial video |
| Preview | Banner |
| Preview -> Edit | Interstitial video |
| Edit -> Save | Rewarded dialog ("Get this item") |
| Set Wallpaper | Banner |
| My Gallery | Banner |
| **Settings** | **No ads** |

### UX Impact
- Average of **4-5 ads** per view + set wallpaper flow
- Every transition includes an interstitial ad
- **Mandatory rewarded ad** to save wallpaper
- Banner takes up ~15-20% of bottom screen area
- **Only Settings is ad-free**

---

## Quick Summary

### Strengths
- Rich wallpaper library (100+ templates, 11 categories)
- Live wallpaper support (animated)
- Versatile editor with layer system
- Supports 19 languages
- Completely free

### Weaknesses
- Excessive ads that disrupt user experience
- No download/save as file option
- No wallpaper sharing
- No photo filters/effects
- No crop/resize/rotate tools
- Very basic Settings
- No account/profile system
- Contains typos ("Ducth", "Let select")

### Statistics
| Metric | Value |
|--------|-------|
| Total categories | 11 |
| Total wallpaper templates | ~100+ |
| Supported languages | 19 |
| Editor tools | 4 (BG, Import, Text, Sticker) |
| Stickers | 30+ |
| Fonts | 8+ |
| Background templates | 15-20 |
| Average ads per flow | 4-5 |
| Subscription/IAP | None |

---

## Output Directory Structure

```
features/
├── FEATURE_LIST.md              <- This file
├── 01_home_screen/
│   ├── README.md                (14 screenshots)
│   └── screenshots/
├── 02_wallpaper_creation/
│   ├── README.md                (12 screenshots)
│   ├── 01_templates/
│   └── screenshots/
├── 03_collage_creation/
│   ├── README.md                (13 screenshots)
│   ├── 01_editor_overview/
│   ├── 02_backgrounds/
│   ├── 03_import/
│   ├── 04_text/
│   ├── 05_stickers/
│   ├── 06_filters/
│   └── screenshots/
├── 04_settings/
│   ├── README.md                (12 screenshots)
│   └── screenshots/
├── 05_export_share/
│   ├── README.md                (7 screenshots)
│   └── screenshots/
├── 06_monetization/
│   ├── README.md                (2 screenshots)
│   └── screenshots/
├── 07_wallpaper_categories/
│   ├── README.md
│   ├── 01_for_you/ ~ 11_anime/ (one folder + screenshots per category)
│   └── screenshots/
├── 08_wallpaper_preview_flow/
│   ├── README.md                (6 screenshots)
│   └── screenshots/
└── 09_onboarding/
    ├── README.md                (7 screenshots)
    └── screenshots/
```

**Total**: 9 feature areas, ~75+ screenshots
