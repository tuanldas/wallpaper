# Wallpaper Creation

## Description
The DIY wallpaper creation feature allows users to design wallpapers from scratch using tools: Background, Import photo, Text, and Sticker. Users can also select pre-made wallpaper templates and set them as wallpaper.

## Access
Home > "TRY NOW" button (Create wallpaper)

## UI/UX Design

### Wallpaper Editor Screen
- **Top bar**:
  - Back button (btnBack) - returns to Home
  - "Edit" title
  - Undo button (icUndo)
  - Redo button (icRedo)
  - Preview button (icPreview) - preview wallpaper
  - "Next" button (btnNext, pink) - proceed to export/save
- **Canvas area**: Main workspace, checkered pattern when empty (transparent)
- **Layer button** (btnLayer): Bottom-left corner, opens layer management panel
- **Bottom toolbar**: 4 main tools

### Bottom Toolbar (4 tools)
1. **BG** (Background) - Select/change background
2. **Import** - Import photo from gallery
3. **Text** - Add text
4. **Sticker** - Add sticker

## User Flow

### 1. Creating a New Wallpaper
1. Tap "TRY NOW" on Home
2. Editor opens with blank canvas
3. Use tools to design
4. Tap "Next" -> "Get this item" popup appears (ad gate)
   - "Watch now" - Watch ad to continue for free
   - "No, thanks" - Skip
5. Continue editing or export

### 2. Viewing a Wallpaper Template
1. Tap a wallpaper from Home grid
2. Video ad plays (mandatory)
3. Preview screen displays:
   - Full-screen wallpaper
   - Swipe left/right to view other wallpapers
   - "Preview" button (preview on home screen)
   - "Next" button (leads to Set wallpaper)
4. "Set wallpaper" screen:
   - Full-screen wallpaper preview
   - "Preview" button in top-right
   - "Set wallpaper" button (pink) - sets as wallpaper

## Tool Details

### BG (Background)
- **Color Picker**: Gradient color circle + black
- **Solid Colors**: Color swatches: white/gray, light pink, pink, red, light yellow, orange, ...
- **Add Image**: "+" button to add image as background from gallery
- **Background Templates**: Grid of pre-made background templates (hearts, gradients, drawings, ...)
- **Checkmark** (btnOk) to confirm background selection

### Import
- Opens "Select Photo" screen
- Requests photo access permission on first use: "Allow limited access", "Allow all", "Don't allow"
- Displays device photo gallery
- Tabs: "All albums" and "Recent"
- "Done" button to confirm photo selection

### Text
- **Text input**: Text field (default "Hello")
- **Text Library**: Decorative text library with decorative dividers/borders using special characters (flowers, stars, hearts, etc.)
- **Font selection**: Multiple fonts (displayed in horizontally scrollable list)
- **Color picker**: Gradient circle + solid colors (black, gray, pink, red, yellow, orange, ...)
- **Checkmark** (btnOk) to confirm

### Sticker
- **Grid stickers**: Diverse sticker collection:
  - Flowers, vinyl record, roses
  - Speech bubble, Hello Kitty, heart
  - Rainbow, bow, butterfly
  - Crown, music note, soccer ball
  - Bear, cat, fire, Happy Birthday
  - And many more stickers...
- Scroll down to view more stickers
- Tap sticker to add to canvas
- **Checkmark** (btnOk) to close panel

### Layer Management
- Tap Layer icon (bottom-left corner)
- Shows "Layer" panel with layer thumbnails
- Lock icon to lock/unlock layers
- Checkmark to close panel

## Sub-features
- Background library (colors + templates)
- Photo import from gallery
- Text with multiple fonts and colors
- Text Library (decorative text)
- Sticker library (very extensive)
- Layer management
- Undo/Redo
- Preview mode

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/create_wallpaper_01.png | Editor screen - blank canvas with 4 tools |
| screenshots/bg_panel.png | Background panel - color picker and templates |
| screenshots/import_screen.png | Import - access permission request |
| screenshots/import_gallery2.png | Import - photo gallery |
| screenshots/text_panel.png | Text panel - input, fonts, colors |
| screenshots/text_library.png | Text Library - decorative text dividers |
| screenshots/sticker_panel2.png | Sticker panel - sticker grid |
| screenshots/sticker_panel_scrolled.png | Sticker panel - more stickers on scroll |
| screenshots/layers_panel2.png | Layer management panel |
| screenshots/wallpaper_preview.png | Wallpaper Preview - swipeable |
| screenshots/set_wallpaper.png | Set wallpaper screen - full preview |
| screenshots/set_wallpaper_options.png | Ad gate before setting wallpaper |

## Notes
- Tapping "Next" from the Editor shows a "Get this item" popup requiring ad viewing - this is a monetization point
- Video ads are mandatory when tapping a wallpaper from the Home grid
- The app uses Pangle (TikTok Ad Network) and CapCut as ad providers
- Live wallpapers have animated effects
- Canvas supports multiple layers with lock/unlock capability
- Sticker library is quite extensive with many themes (kawaii, love, nature, etc.)
