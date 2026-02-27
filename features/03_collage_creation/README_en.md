# Collage & Editing Tools

## Description
The "DIY Wallpaper Maker Collage" app provides a layer-based editor that allows users to create wallpapers from scratch or edit existing ones. The editor supports 4 main tools: Background, Import, Text, and Sticker. Users can also preview wallpapers as a lock screen preview.

## How to Access
- **Create new**: Home > "Create wallpaper / TRY NOW" button
- **Edit existing wallpaper**: Home > Tap wallpaper > Preview screen > Next

## UI/UX Design

### Main Editor (Edit screen)
- **Top bar**:
  - Back button (left arrow, pink)
  - Title "Edit"
  - Undo button
  - Redo button
  - Preview button (eye icon) - displays wallpaper as lock screen
  - "Next" button (pink/red, rounded)
- **Canvas**: Main area displaying the wallpaper being created, transparent background (checkerboard) when no background is set
- **Layer icon**: Bottom-left corner, stacked layers icon
- **Bottom toolbar**: 4 tabs - BG | Import | Text | Sticker

### Main Colors
- Pink/Red (primary): main buttons, active tab
- White (background)
- Black (text, icons)

## User Flows

### Flow 1: Create New Wallpaper
1. From Home, tap "Create wallpaper / TRY NOW"
2. Enter Editor with blank canvas
3. Choose Background (BG)
4. Add Import/Text/Sticker as desired
5. Preview using Preview (displays as lock screen with date/time)
6. Tap Next to save/export (may show reward ad popup "Get this item")

### Flow 2: Edit Existing Wallpaper
1. From Home, tap a wallpaper template
2. Preview in Preview screen (can swipe to other wallpapers)
3. Tap Next to enter Editor
4. Edit with available tools
5. Tap Next to save/export

## Sub-features

### 1. BG (Background)
- **Location**: Bottom toolbar > "BG" tab
- **Description**: Set background for the wallpaper
- **Options**:
  - **Color picker** (rainbow icon): Choose any color
  - **Preset colors**: Black, gray, various pinks, red, cream, orange, yellow
  - **Add Image**: Import photo from gallery as background
  - **Background templates**: ~15-20 preset templates (hearts, pink gradient, stars, glow, spiral, clouds, etc.)
- **Confirm**: Checkmark button (OK) at the top-right of the panel

### 2. Import
- **Location**: Bottom toolbar > "Import" tab
- **Description**: Add photos from the gallery to the canvas
- **Flow**:
  1. Tap Import > Opens "Select Photo" screen
  2. Requests photo access permission (Allow limited/Allow all/Don't allow)
  3. Displays photos by tabs: "All albums" / "Recent"
  4. Select photo > Tap "Done"
- **Interface**:
  - Top: Back, "Select Photo", Done
  - Photo gallery grid
  - Native ad at the bottom

### 3. Text
- **Location**: Bottom toolbar > "Text" tab
- **Description**: Add text to the wallpaper
- **Options**:
  - **Input field**: Enter text (placeholder "Hello")
  - **Text Library**: Decorative text library with special characters (hearts, stars, sparkles, diamonds, bows) - approximately 5 patterns
  - **Font selector**: 8+ different fonts (serif, sans-serif, handwriting, decorative)
  - **Color picker**: 9+ preset colors + color wheel
- **Confirm**: Checkmark button (OK)

### 4. Sticker
- **Location**: Bottom toolbar > "Sticker" tab
- **Description**: Add decorative stickers to the wallpaper
- **Collection**: 30+ stickers including:
  - Flowers (daisy, cherry blossom)
  - Hearts (various styles)
  - Animals (cat, bear, dog, tiger, rabbit)
  - Characters (Hello Kitty)
  - Symbols (crown, music note, rainbow, star, fire)
  - Bows/Ribbons (various styles)
  - Butterflies (various colors)
  - Decorative text ("YOU", "10A", "DAL")
  - Others (CD/vinyl, clipboard, frame, soccer ball)
- **Confirm**: Checkmark button (OK)

### 5. Layer Management
- **Location**: Stacked layers icon at the bottom-left of the canvas
- **Description**: Manage the order of layers on the canvas
- **Display**: Layer list with thumbnails, lock icon for the background layer
- **Confirm**: Checkmark button (OK)

### 6. Preview (Lock Screen Preview)
- **Location**: Eye icon on the top bar
- **Description**: Preview the wallpaper being created as a lock screen
- **Display**:
  - Full-screen wallpaper
  - Date (e.g., "Friday, February 27")
  - Large clock (e.g., "21:52")
  - Back button to return to editor

### 7. Undo/Redo
- **Location**: Top bar, 2 arrow icons
- **Description**: Undo and redo editing actions

## Ads
The app displays multiple types of ads:
- **Native ads**: Shown within screens (home, Select Photo, etc.)
- **Interstitial ads**: Shown during screen transitions (exiting editor, selecting wallpaper)
- **Reward ad popup**: "Get this item" - watch an ad to receive the item, with "Watch now" and "No, thanks" buttons
- **Ad providers**: Pangle, CapCut (TikTok Lite)

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/01_editor_overview.png | Main editor with blank canvas |
| screenshots/02_bg_tool.png | Background tool with colors and templates |
| screenshots/03_bg_selected.png | Background selected |
| screenshots/04_text_tool.png | Text tool with font and color options |
| screenshots/05_text_library.png | Text Library with decorative patterns |
| screenshots/06_sticker_tool.png | Sticker tool with 30+ stickers |
| screenshots/07_import_permission.png | Import - permission request |
| screenshots/08_import_select_photo.png | Select Photo screen |
| screenshots/09_layer_panel.png | Layer management panel |
| screenshots/10_reward_ad_popup.png | Reward ad popup "Get this item" |
| screenshots/11_preview_lockscreen.png | Preview mode - lock screen |
| screenshots/12_wallpaper_preview.png | Wallpaper preview before editing |
| screenshots/13_editor_with_wallpaper.png | Editor with existing wallpaper |

## Notes
- The app does not have a separate "Collage" tab/section. Instead, the editor functions as a collage maker allowing users to combine multiple layers (background + imported images + text + stickers)
- Ads appear very frequently, especially during screen transitions
- Background templates are primarily in a cute/kawaii style with pink tones
- No standalone crop, resize, or rotate features were found - the editor focuses on compositing (layer combination)
- No photo filters/effects features were found
- Wallpaper categories on home: For you, DIY, Love, Live, Lock Screen, Kawaii, Aesthetic, Quote, Famous, Car, Anime
