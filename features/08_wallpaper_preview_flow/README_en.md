# Wallpaper Preview & Set Wallpaper Flow

## Description
The preview and wallpaper-setting flow when a user selects a wallpaper from the grid on the Home screen.

## Access Location
Home > Tap wallpaper in grid > (Video Ad) > Preview > Next > (Ad) > Set Wallpaper

## Detailed Flow

### Step 1: Tap a wallpaper from the Home grid
- Tap any wallpaper in the grid
- **Mandatory video ad** is displayed (CapCut/Pangle Test Ads)
  - Duration: ~15-30 seconds
  - Shows "Skip after Xs" or "X seconds remaining" in the top-right corner
  - After the timer expires: an "Ad closed" button appears to dismiss
  - Cannot be skipped immediately - must wait for the countdown to finish

### Step 2: Preview Screen
- **Header**: Back arrow (left), "Preview" title, "Next" button (pink, right)
- **Wallpaper display**: Shown full-screen within a rounded card
- **Swipe**: Swipe left/right to browse other wallpapers in the same category
  - Adjacent wallpapers are shown as smaller cards on both sides (peek effect)
  - 3 cards visible simultaneously (current + 2 sides)
- **Ad banner**: Native ad (CapCut/Pangle) at the bottom of the screen, with a collapse button (btn_collapsible)

### Step 3: Tap Next from Preview
- A second mandatory video ad is displayed
- Wait for the timer to expire > dismiss the ad

### Step 4: Set Wallpaper Screen (or Editor)
Depends on the wallpaper type:

**Static wallpaper from grid:**
- Opens in the **Editor** (can be customized before setting)
- The Editor displays the pre-loaded wallpaper on the canvas
- Full set of tools available: BG, Import, Text, Sticker
- Tap "Next" from Editor > "Get this item" popup appears

**"Get this item" Popup (Ad Gate):**
- 3D bunny mascot
- "Watch now" - Watch a rewarded ad to unlock
- "No, thanks" - Skip (may result in limited functionality)
- Tapping "Watch now": ~30-second video ad with "X seconds remaining" countdown

**After watching the ad / from wallpaper preview:**
- Full-screen **Set Wallpaper** screen:
  - Back button (pink, top-left corner)
  - "Preview" button (top-right corner) - preview on a home screen mockup
  - "Set wallpaper" button (pink, bottom of screen)

### Step 5: Set Wallpaper
- Tap the "Set wallpaper" button
- (Unable to confirm available options for home/lock/both due to ads continuously overlapping on the test emulator)

## Ad Flow Summary
| Trigger | Ad Type | Skippable? | Duration |
|---------|---------|------------|----------|
| Tap wallpaper from grid | Video interstitial | Yes, after countdown | ~15-30s |
| After closing ad #1 | Native fullscreen (Pangle) | Yes, btn_collapsible | Immediate |
| Tap Next from Preview | Video interstitial | Yes, after countdown | ~15-30s |
| After closing ad #2 | Native fullscreen (Pangle) | Yes, btn_collapsible | Immediate |
| Tap Next from Editor | "Get this item" popup | "No thanks" or watch ad | ~30s if watched |

Total: **4-5 ads** per view + set wallpaper flow

## Swipe Preview Feature
- Swipe left/right to browse through wallpapers
- Carousel-style display: main wallpaper centered, two smaller wallpapers on each side
- Each card has rounded corners
- Wallpapers are from the same category/tab

## Image Quality
- Preview displays high quality, full resolution
- Wallpaper fits the entire screen when set
- Supports both static and live wallpapers

## Live Wallpaper
- Live wallpapers have a "(>) Live" badge on the Home grid
- In Preview, live wallpapers play their animation
- Flow is similar to static wallpapers but includes motion effects

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/preview_static2.png | Preview screen - static wallpaper with heart lollipops |
| screenshots/get_this_item_popup.png | "Get this item" popup - ad gate with Watch now/No thanks |
| screenshots/after_watch_ad.png | Rewarded video ad - "3 seconds remaining" |
| screenshots/set_wallpaper_final.png | Wallpaper loaded in the Editor |
| screenshots/set_wallpaper_screen.png | Loading screen during screen transition |

## Notes
- The app displays a significant number of ads throughout this flow (4-5 ads per single flow)
- Ads considerably degrade the user experience
- "Watch now" is a rewarded ad - users watch an ad to unlock the wallpaper for free
- The emulator runs test ads (Pangle Test Ads), so behavior may differ from production
- Some fullscreen native ads may cover the "Set wallpaper" button and need to be collapsed first
- Due to test environment limitations, the full Set Wallpaper options (home/lock/both) could not be confirmed
