# Export / Save / Share

## Description
This feature allows users to save wallpapers and set them as phone backgrounds. The app does not have a standalone file export function - instead, the main flow is **Preview -> Edit -> Set Wallpaper**. Wallpapers are saved to the app's "My Gallery" and can be set as backgrounds directly.

## How to Access
- **View wallpaper**: Home > Tap any wallpaper in the grid
- **My Gallery**: Home > "My Gallery" (top-right corner)
- **Set Wallpaper**: Preview > Next (Edit) > Next > Watch ad > Set Wallpaper

## UI/UX Design

### Preview Screen
- **Header**: "Preview" with Back button and "Next" button (pink)
- **Canvas**: Displays wallpaper in full screen, swipeable left/right to view other wallpapers
- **Banner ad** at the bottom of the screen

### Edit Screen (Wallpaper Editor)
- **Header**: "Edit" with Back, Undo, Redo, Visibility toggle, and "Next" button (pink)
- **Canvas**: Wallpaper being edited on a checkered (transparent) background
- **Bottom toolbar**: BG (Background), Import, Text, Sticker
- *(Detailed editing tools are covered in the Collage & Editing section)*

### Set Wallpaper Screen
- **Header**: Back button, "Preview" link
- **Wallpaper preview**: Full-screen wallpaper display
- **Title**: "Set your wallpaper"
- **3 action buttons**:
  1. **Home Screen** - Set as home screen wallpaper
  2. **Lock Screen** - Set as lock screen wallpaper
  3. **Home Screen and Lock Screen** - Set for both
- **Set wallpaper** button to confirm (after selecting an option)
- **Banner ad** at the bottom of the screen

### My Gallery
- **Header**: "My Gallery" with Back and "Select" buttons
- When empty: Displays a 3D character + "Nothing here yet" + "Explore now" button
- **Banner ad** at the bottom of the screen (TikTok Lite)

## User Flows

### Flow for viewing and saving wallpapers from the library:
1. Tap a wallpaper in the Home grid
2. **Interstitial ad** appears (video ~5-20 seconds, with Skip/Close button)
3. **Preview** screen displays the wallpaper
4. Tap **Next** -> another **Interstitial ad** appears
5. **Edit** screen - the wallpaper can be edited
6. Tap **Next** -> **"Get this item"** dialog appears:
   - **Watch now**: Watch a rewarded video ad (~20 seconds) to receive the wallpaper
   - **No, thanks**: Decline (wallpaper cannot be saved)
7. After watching the ad -> **Set Wallpaper** screen
8. Choose location (Home Screen / Lock Screen / Both)
9. Tap **Set wallpaper** to complete

### Flow for wallpapers from gallery:
1. Home > "My Gallery"
2. Select a saved wallpaper
3. Options to set as wallpaper or delete

## Sub-features
- **Preview wallpaper**: Preview the wallpaper before saving
- **Swipe gallery**: Swipe left/right to view other wallpapers in the same category
- **Edit wallpaper**: Edit the wallpaper before saving (BG, Import, Text, Sticker)
- **Set as wallpaper**: Set directly as phone wallpaper
- **My Gallery**: Store downloaded/created wallpapers
- **Filter**: Filter wallpapers by "All" or "Favorite"
- **Favorite**: Tap the heart icon on a wallpaper card to add to favorites

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/01_my_gallery.png | My Gallery - no wallpapers yet |
| screenshots/02_wallpaper_preview.png | Interstitial ad before viewing wallpaper |
| screenshots/05_save_screen.png | Interstitial video ad (CapCut) |
| screenshots/07_actual_export.png | Edit wallpaper screen |
| screenshots/08_export_final.png | "Get this item" dialog - Rewarded ad |
| screenshots/10_save_result.png | Set Wallpaper screen with 3 options |
| screenshots/11_set_wallpaper_buttons.png | Set Wallpaper screen (scrolled) |

## Notes
- **No** standalone Download/Save as file function (only direct wallpaper setting)
- **No** Share wallpaper with friends function (only app link sharing from Settings)
- Each screen transition may display an **interstitial ad**
- Saving a wallpaper **requires watching a rewarded ad** (~20 seconds)
- The app uses Android's **wallpaper service** system to set backgrounds
- The number of ads in this flow is very high (3-4 ads per wallpaper)
