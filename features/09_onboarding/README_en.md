# Onboarding Flow

## Description
The onboarding flow appears when the user opens the app for the first time (or after clearing data). The flow consists of 4 steps: App Open Ad -> Language selection -> Feature introduction (2 slides) -> Interest selection. After completion, the user is taken to the Home screen.

## Access Location
- Appears automatically on first app launch
- Cannot return to onboarding from within the app (unless data is cleared)
- The "Language" section can be accessed again from Settings > Language

## Flow

### Step 0: App Open Ad
- **Type**: Interstitial/App Open Ad (fullscreen)
- **Provider**: Google AdMob (Test Ad)
- **Format**: Product video ad (skincare, etc.)
- **Duration**: Has a countdown (e.g., "2" seconds), after which the "Close" button appears
- **Close button**: Located in the bottom-left corner with a green checkmark
- **Mandatory**: Must wait for the countdown to finish before closing

### Step 1: Language Selection
- **Title**: "Languages"
- **Layout**: Vertical list of languages, each row contains:
  - Country flag (circular)
  - Language name
  - Radio button on the right (pink when selected)
- **Background**: Pastel gradient (pink, blue, purple)
- **19 supported languages**:
  1. English
  2. Francais (French)
  3. Marathi - India
  4. Espanol (Spanish)
  5. Chinese
  6. Portugues - Portugal (Portuguese)
  7. Russkiy (Russian)
  8. Indonesian
  9. Philippines
  10. Bangla (Bangladesh)
  11. Portugues - Brazil
  12. Afrikaans (South Africa)
  13. Deutsch (German)
  14. Canada
  15. English (UK)
  16. Korean
  17. Dutch - *misspelled as "Ducth" in the app (typo)*
  18. Vietnamese
- **Default language**: English (US) - automatically selected on launch
- **Confirmation**: Tap the pink checkmark in the top-right header
- **Ad**: Banner ad (TikTok/Pangle) at the bottom of the screen

### Step 2: Introduction - Slide 1
- **Image**: Montage of wallpaper samples (collage, aesthetic, birthday...)
- **Title** (pink): "1000+ Unique Wallpaper"
- **Subtitle**: "Find endless styles to spark your creativity."
- **Dot indicators**: 2 dots (dot 1 active - pink)
- **Button**: "Next" (pink gradient, full width)
- **Ad**: Pangle banner ad at the bottom

### Step 3: Introduction - Slide 2
- **Image**: Editor interface with tools (BG, Import, Text, Sticker) and a star sticker
- **Title** (pink): "Design your own wallpaper"
- **Subtitle**: "Use background, sticker, color, text... to create your style."
- **Dot indicators**: 2 dots (dot 2 active - pink)
- **Button**: "Next" (pink gradient, full width)
- **Ad**: Pangle banner ad at the bottom

### Step 4: Interest Selection
- **Title** (pink): "Let select your interest"
- **Subtitle**: "Please pick one or more to proceed"
- **Layout**: 3-column x 4-row grid (11 categories)
- **Categories** (each with a circular illustration and label):
  | Category | Description |
  |----------|-------------|
  | For you | Galaxy/Space theme |
  | DIY | Craft/Handmade theme |
  | Love | Heart/Romance theme |
  | Live | Gradient pastel theme |
  | Lock Screen | Moon/Night theme |
  | Kawaii | Cute/Cupcake theme |
  | Aesthetic | Butterfly/Nature theme |
  | Quote | Flamingo/Text theme |
  | Famous | Celebrity theme (Taylor Swift) |
  | Car | Vehicle theme |
  | Anime | Manga/Anime character theme |
- **Selection**: Tap a card -> pink border + red checkmark appears in the top-right corner
- **Multi-select supported**: "pick one or more"
- **Button**: "Get Started" (pink gradient, full width)
- **No ads** on this screen

### Completion: Home Screen
- After tapping "Get Started", the app navigates to the Home screen
- The first category tab ("For you") is selected by default
- The wallpaper grid displays content based on selected interests

## UI/UX Design
- **Consistent theme**: Pastel gradient (pink, blue, purple) throughout
- **Font**: Rounded, modern
- **Primary color**: Pink (#FF1493 - deep pink) for titles, buttons, highlights
- **Dot indicators**: Small, centered, indicate the current slide
- **Button style**: Full-width, pink-to-red gradient, rounded corners
- **Ad placement**: Banner at the bottom of the screen (except interest selection)
- **No Skip button** at any step (except ads)
- **No Back button** between slides (forward-only navigation)

## Typos Found
- "Ducth" -> should be "Dutch"
- "Let select your interest" -> should be "Let's select your interest"
- "Espanol" -> should be "Espanol" (may be missing the tilde)

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/01_app_open_fresh.png | App Open Ad on first launch |
| screenshots/02_language_fresh.png | Language selection screen |
| screenshots/03_intro_slide1_fresh.png | Intro slide 1 - 1000+ Unique Wallpaper |
| screenshots/04_intro_slide2_fresh.png | Intro slide 2 - Design your own wallpaper |
| screenshots/05_interest_fresh.png | Interest selection screen (none selected) |
| screenshots/06_interest_selected.png | Interest selection screen (For you + Anime selected) |
| screenshots/07_notification_permission.png | Home screen after onboarding |

## Notes
- Onboarding **cannot be skipped** - all steps must be completed
- No login/account registration during onboarding
- Selected interests affect the wallpaper content displayed on the Home screen
- The App Open Ad appears **before** onboarding (immediately on launch)
- If no language is selected, English is chosen by default (with a fingerprint icon)
- Onboarding only appears once (unless data is cleared)
