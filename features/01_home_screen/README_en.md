# Home Screen

## Description
The main screen of the "DIY Wallpaper Maker Collage" app, displayed when the app opens. This is the central hub where users browse wallpaper templates, access their personal gallery, and start creating new wallpapers.

## Access
Open app > Home Screen (first screen after onboarding)

## Onboarding Flow (First Launch)
1. **Language selection** - Languages screen with 8 languages: English, Francais, Marathi (India), Espanol, Chinese, Portugues (Portugal), Russkiy, Indonesian
2. **Feature introduction** - 2 onboarding pages:
   - Page 1: "1000+ Unique Wallpaper - Find endless styles to spark your creativity"
   - Page 2: "Design your own wallpaper - Use background, sticker, color, text... to create your style"
3. **Interest selection** - "Let select your interest" with 11 categories: For you, DIY, Love, Live, Lock Screen, Kawaii, Aesthetic, Quote, Famous, Car, Anime

## UI/UX Design

### Header Area
- **Image banner** - Top-left corner, displays wallpaper preview with 3D card effects
- **My Gallery** - Button in top-right with gallery icon, leads to personal library
- **Settings** - Gear icon in top-right corner (ID: btnSetting)
- **Create wallpaper** - "Create wallpaper" text and **TRY NOW** button (pink gradient) - leads to Wallpaper Editor

### Category Tabs (Horizontally Scrollable)
Horizontally scrollable tab list:
1. **For you** - Suggestions based on interests
2. **DIY** - Scrapbook/collage style wallpapers
3. **Love** - Love theme, hearts
4. **Live** - Live wallpapers (with animated effects)
5. **Lock Screen** - Lock screen wallpapers
6. **Kawaii** - Cute Japanese style theme
7. **Aesthetic** - Aesthetic theme
8. **Quote** - Wallpapers with quotes
9. **Famous** - Celebrities
10. **Car** - Car theme
11. **Anime** - Anime theme

### Filter
- **Filter by** label on the left
- **All** dropdown on the right with 2 options: "All" and "Favorite"

### Wallpaper Grid
- 3-column grid layout
- Each wallpaper card displays:
  - Thumbnail preview
  - Heart/Favorite icon (btnFavorite) in the top-right corner
  - "Live" badge for live wallpapers
- Infinite vertical scroll to load more wallpapers
- Native ads (Pangle/CapCut) interspersed between wallpapers

### Ads
- Native ad banner at the bottom of the screen (CapCut, Pangle)
- Collapsible with btn_collapsible button

## User Flow

### Browsing Wallpapers
1. Select a category tab (For you, DIY, Love, ...)
2. Scroll vertically through the wallpaper grid
3. Tap a wallpaper -> Video ad plays -> Preview screen
4. On Preview: swipe left/right to view other wallpapers
5. Tap "Next" or "Set wallpaper" to continue

### My Gallery
1. Tap "My Gallery" on the header
2. View list of saved wallpapers
3. When empty: shows "Nothing here yet" with "Explore now" button and mascot
4. "Select" button in top-right for multi-item selection

### Creating a New Wallpaper
1. Tap "TRY NOW" -> Opens Wallpaper Editor

## Sub-features
- Wallpaper Grid browsing
- Category filtering (11 categories)
- Favorite filtering
- My Gallery (personal library)
- Quick create wallpaper access

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/home_screen_01.png | Ad screen when opening app for the first time |
| screenshots/onboarding_01.png | Onboarding page 1 - 1000+ Unique Wallpaper |
| screenshots/onboarding_02.png | Onboarding page 2 - Design your own wallpaper |
| screenshots/onboarding_03_interests.png | Interest selection (11 categories) |
| screenshots/home_main.png | Main home screen with wallpaper grid |
| screenshots/home_scrolled.png | Home screen after scrolling down |
| screenshots/home_scrolled2.png | Home screen scrolled further - TikTok ad |
| screenshots/tab_diy.png | DIY tab - scrapbook style wallpapers |
| screenshots/tab_love.png | Love tab - love theme wallpapers |
| screenshots/tab_live.png | Live tab - live wallpapers |
| screenshots/tabs_more.png | More tabs: Aesthetic, Quote, Famous, Car |
| screenshots/tabs_more2.png | More tabs: Car, Anime |
| screenshots/filter_all.png | Filter dropdown: All / Favorite |
| screenshots/my_gallery.png | My Gallery - empty, no wallpapers yet |

## Notes
- The app displays a large number of ads (Pangle Test Ads, CapCut) - including native ads, video ads, and interstitial ads
- Ads appear when: opening the app, switching screens, tapping a wallpaper, returning to home
- Live wallpapers have a "(>) Live" badge to distinguish them from static wallpapers
- Wallpaper grid loads more items on scroll (infinite scroll)
- The app supports 8 languages
