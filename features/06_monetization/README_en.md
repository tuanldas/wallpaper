# Monetization

## Description
The "DIY Wallpaper Maker Collage" app uses an **ad-supported** model as its primary revenue source. There are no subscriptions or in-app purchases. Ads appear on nearly every screen and at every transition point within the app.

## Revenue Model
- **100% ad-supported**
- **No** subscription/premium plans
- **No** in-app purchases (IAP)
- **No** paywall - all features are free but require watching ads

## Ad Types

### 1. Banner Ads
- **Location**: Bottom of the screen, taking up approximately 15-20% of the screen
- **Appears on**: Most screens - Home, Languages, Preview, Set Wallpaper, My Gallery
- **Providers**: Pangle (TikTok Ads), CapCut, TikTok Lite
- **Format**: Horizontal banner with logo, app name, and "View now" / "Download" button
- **Clickable**: Yes - redirects to Play Store or advertiser's website
- **Special note**: Some banners include video (NativeVideoTsView)

### 2. Interstitial Ads (Full-screen Ads)
- **Trigger points**:
  - When opening the app for the first time (before onboarding)
  - When tapping a wallpaper to view preview
  - When transitioning from Preview to Edit
  - When transitioning from Edit to Set Wallpaper
- **Format**: Full-screen video
- **Duration**: 5-30 second video, with a "Skip after Xs" button after a few seconds
- **Close button**: "Ad closed" (X) appears at the top-right corner after the skip timer expires
- **Providers**: Pangle (CapCut ads, TikTok Lite ads)
- **Frequency**: Very high - every major screen transition includes one

### 3. Rewarded Ads
- **Trigger point**: When the user wants to save/set a wallpaper
- **Flow**:
  1. After editing a wallpaper, tap Next
  2. "Get this item" dialog appears with a 3D character
  3. Two options:
     - **"Watch now"** (pink button) - Watch an ad to receive the wallpaper
     - **"No, thanks"** (pink outline button) - Decline (wallpaper cannot be saved)
  4. Rewarded video ad plays (~15-20 seconds)
  5. A countdown timer appears at the top-right corner (e.g., "19s")
  6. After watching the full ad -> "Ad closed" button appears -> wallpaper is unlocked
- **Mandatory**: Must watch a rewarded ad to save any wallpaper
- **Providers**: Pangle (CapCut, TikTok ads)

### 4. Native Ads
- **Location**: Interspersed within the language list and wallpaper grid
- **Format**: Integrated into the app's UI, designed to look like regular content
- **Providers**: Pangle

## Ad Providers
| Provider | Ad Types | Notes |
|----------|----------|-------|
| **Pangle** (TikTok for Business) | Banner, Interstitial, Rewarded, Native | Primary provider |
| **AdMob** (Google) | Mentioned in Privacy Policy | May be used for mediation |

## Detailed Ad Placements

| Screen | Ad Type | Notes |
|--------|---------|-------|
| App launch | Interstitial (full screen) | Ad immediately upon opening the app |
| Onboarding (Languages) | Banner (bottom) | CapCut/Pangle banner |
| Onboarding (Intro slides) | Banner (bottom) | Pangle banner |
| Home Screen | Banner (bottom) | CapCut/TikTok Lite banner |
| Wallpaper tap | Interstitial (video) | Before viewing preview |
| Preview Screen | Banner (bottom) | TikTok Lite/Pangle |
| Preview -> Edit | Interstitial (video) | Screen transition |
| Edit -> Save | Rewarded dialog | "Get this item" - mandatory ad viewing |
| Set Wallpaper Screen | Banner (bottom) | Pangle/CapCut |
| My Gallery | Banner (bottom) | TikTok Lite |
| **Settings** | **No ads** | The only screen without ads |

## User Experience with Ads
- **Very high ad volume**: An average of 4-5 ads for a simple flow (viewing and saving 1 wallpaper)
- **Ads at every transition**: Each screen transition may include an interstitial ad
- **Mandatory rewarded ads**: Cannot save a wallpaper without watching an ad
- **Persistent banners**: Take up space at the bottom of the screen, sometimes covering important content
- **Only Settings is ad-free**: The only "clean" screen without ads

## Information from Privacy Policy & ToS
- The app may use **AdMob** and **Pangle** to display ads
- Uses **anonymous identifiers** (advertising IDs) for ad relevance
- Users can **opt out of personalized ads** through device settings
- No personal data is collected for advertising purposes

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/01_interstitial_ad.png | Interstitial video ad (CapCut via Pangle) |
| screenshots/02_rewarded_ad.png | Rewarded video ad with 19s countdown |

## Notes
- The app **has no subscription model** - entirely free with ads
- **No** "Remove ads" or "Go Premium" button
- **No** in-app purchases of any kind
- Pangle (TikTok for Business) is the primary ad network, not Google AdMob directly
- Ads are primarily **test ads** (Pangle Test Ads) on the emulator - actual device experience may differ
- The monetization model relies entirely on **ad revenue** and **rewarded video ads**
- The ad frequency may be annoying to users (experience is frequently interrupted)
