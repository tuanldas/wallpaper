# Settings

## Description
The Settings page provides basic configuration options for the DIY Wallpaper Maker Collage app. This page is simple, focusing on language, legal information, and app sharing.

## How to Access
Home > Settings icon (gear icon at the top-right corner, next to "My Gallery")

## UI/UX Design
- **Layout**: Vertical list of setting items
- **Background**: Pastel gradient (pink, blue, light purple) consistent with the rest of the app
- **Header**: "Setting" with a Back button (pink arrow in a circle)
- **Items**: White rounded-corner cards with an icon on the left and text
- **No ads** on the Settings page (one of the few screens without ads)

## Setting Items

### 1. Language
- **Icon**: Globe icon
- Opens a language selection page with a list of 19 languages:
  - English (default), Francais, Marathi (India), Espanol, Chinese, Portugues (Portugal), Russkiy, Indonesian, Philippines, Bangla, Portugues (Brazil), Afrikaans, Deutsch, Canada, English (UK), Korean, Dutch, Vietnamese
- Each language displays the corresponding country flag
- The currently selected language has a red checkmark
- Confirmed by tapping the pink checkmark button at the top-right corner
- This page also serves as the first screen in the onboarding flow
- **Has a banner ad** at the bottom of the Languages page (CapCut/Pangle)

### 2. Term of Service
- **Icon**: Document icon
- Opens a web page (Chrome) at sites.google.com
- **Key content**:
  - Effective Date: Jan 12, 2026
  - App Name: DIY Wallpaper
  - Company: LeafMotion Software
  - Contact: buihieu2568@gmail.com
  - 10 sections: Acceptance of Terms, Eligibility (13+), Use of the App (entertainment only), Permissions, Intellectual Property, Disclaimer, Limitation of Liability, Termination, Changes to Terms, Contact Us
  - Listed permissions: INTERNET, ACCESS_NETWORK_STATE, CAMERA, VIBRATE, POST_NOTIFICATIONS

### 3. Privacy Policy
- **Icon**: Clock/info icon
- Opens a web page (Chrome) at sites.google.com
- **Key content**:
  - Effective Date: Jan 28, 2026
  - The app does not require personal registration, identity information, or real communication data
  - Collects: Device model, OS, app version, anonymous analytics
  - CAMERA: "no video or image data is stored or transmitted"
  - **Advertising**: Uses third-party advertising (AdMob), anonymous identifiers
  - Children's Privacy: Not targeted at children under 13
  - User rights: Delete the app to stop data collection, opt out of personalized ads

### 4. Rating 5 Stars
- **Icon**: Star rating icon
- Displays an **in-app rating dialog** (does not redirect to Play Store immediately):
  - Title: "Hey, can I ask you?"
  - Subtitle: "How is the experience of our app?"
  - 5 stars to select
  - "Rate Us" button (pink)
  - Can be dismissed with the Back button

### 5. Share with Friend
- **Icon**: Share icon
- Opens the **native Android Share Sheet** with the Google Play Store link:
  - URL: `https://play.google.com/store/apps/details?id=com.diy.wallpaper.maker.collage`
  - Sharing options: Quick Share, Chrome, Drive, Messages...

## User Flow
1. From Home, tap the gear icon at the top-right corner
2. The Settings page displays 5 items
3. Tap each item to access its corresponding feature
4. Use the Back button (pink arrow) to return to Settings or Home

## Onboarding Flow
The app has a 3-step onboarding when first launched:
1. **Choose language** (Languages) - Also the screen found in Settings > Language
2. **Introduction 1**: "1000+ Unique Wallpaper - Find endless styles to spark your creativity" + Next button
3. **Introduction 2**: "Design your own wallpaper - Use background, sticker, color, text... to create your style" + Next button
4. **Choose interests**: "Let select your interest - Please pick one or more to proceed" with 11 categories:
   - For you, DIY, Love, Live, Lock Screen, Kawaii, Aesthetic, Quote, Famous, Car, Anime
   - "Get Started" button
- **Pangle ads** are displayed at the bottom of the screen throughout the onboarding process

## Screenshots
| Screenshot | Description |
|-----------|-------------|
| screenshots/01_home_screen.png | Full-screen Pangle ad when opening the app |
| screenshots/02_after_ad_close.png | Language selection screen (onboarding) |
| screenshots/07_onboarding2.png | Onboarding screen 2 - Feature introduction |
| screenshots/08_onboarding3.png | Onboarding screen 3 - Interest selection |
| screenshots/09_home_screen.png | Home screen after onboarding |
| screenshots/10_settings_screen.png | Main Settings page |
| screenshots/11_language_from_settings.png | Languages page from Settings |
| screenshots/12_term_of_service.png | Terms of Service page (Chrome) |
| screenshots/14_chrome_tos_page.png | Terms of Service content |
| screenshots/19_privacy_policy.png | Privacy Policy content |
| screenshots/24_rating.png | Rating 5 stars dialog |
| screenshots/25_share.png | Android Share Sheet |
| screenshots/26_filter_dropdown.png | Filter dropdown (All / Favorite) |

## Notes
- The app belongs to **LeafMotion Software**
- Contact email: buihieu2568@gmail.com
- The app requires a minimum age of 13
- No Account/Profile/Login features
- No Notification settings within Settings
- No Dark mode feature
- Settings are very simple with few customization options
