# DIY Wallpaper Maker Collage - Tổng hợp tính năng

> **Package**: `com.diy.wallpaper.maker.collage`
> **Developer**: LeafMotion Software (buihieu2568@gmail.com)
> **Mô hình**: 100% Ad-supported (miễn phí, không có subscription/IAP)
> **Ngày khám phá**: 2026-02-27

---

## Mục lục

1. [Onboarding Flow](#1-onboarding-flow)
2. [Home Screen](#2-home-screen)
3. [Wallpaper Categories & Templates](#3-wallpaper-categories--templates)
4. [Wallpaper Creation (Editor)](#4-wallpaper-creation-editor)
5. [Wallpaper Preview & Set Flow](#5-wallpaper-preview--set-flow)
6. [My Gallery](#6-my-gallery)
7. [Settings](#7-settings)
8. [Monetization (Quảng cáo)](#8-monetization-quảng-cáo)

---

## 1. Onboarding Flow
**Folder**: `09_onboarding/`

| Bước | Nội dung | Chi tiết |
|------|----------|----------|
| 0 | App Open Ad | Interstitial ad toàn màn hình (Google AdMob), countdown + Close |
| 1 | Chọn ngôn ngữ | 19 ngôn ngữ (English mặc định), có quốc kỳ |
| 2 | Intro Slide 1 | "1000+ Unique Wallpaper" |
| 3 | Intro Slide 2 | "Design your own wallpaper" |
| 4 | Chọn sở thích | 11 categories, chọn 1+, tap "Get Started" |

- **Không thể skip** - phải đi qua tất cả các bước
- **Không có nút Back** giữa các slides
- **Lỗi chính tả**: "Ducth" (Dutch), "Let select" (Let's select)

---

## 2. Home Screen
**Folder**: `01_home_screen/`

### Layout
- **Header**: Banner hình ảnh 3D + "My Gallery" + Settings icon
- **Create wallpaper**: Nút "TRY NOW" (gradient hồng) -> mở Editor
- **Category tabs**: 11 tabs scroll ngang
- **Filter**: All / Favorite
- **Wallpaper grid**: 3 cột, infinite scroll, heart/favorite icon
- **Live badge**: "(>) Live" cho live wallpapers

### Các thành phần tương tác
| Element | Hành động |
|---------|-----------|
| TRY NOW | Mở Wallpaper Editor (canvas trống) |
| My Gallery | Mở thư viện wallpaper cá nhân |
| Settings (gear) | Mở Settings |
| Category tab | Lọc wallpapers theo category |
| Wallpaper card | Xem preview (qua interstitial ad) |
| Heart icon | Đánh dấu Favorite |
| Filter dropdown | Chuyển All / Favorite |

---

## 3. Wallpaper Categories & Templates
**Folder**: `07_wallpaper_categories/`

| # | Category | Số lượng | Phong cách |
|---|----------|----------|------------|
| 1 | For you | 20+ | Tổng hợp theo sở thích, tab mặc định |
| 2 | DIY | 15+ | Collage, scrapbook, polaroid |
| 3 | Love | 12+ | Trái tim, neon, 3D, couples |
| 4 | Live | 10+ | Wallpapers động (animated) |
| 5 | Lock Screen | 10+ | Tối ưu cho màn hình khóa |
| 6 | Kawaii | 8+ | Dễ thương Nhật Bản, pastel |
| 7 | Aesthetic | 8+ | Dreamy, pastel hồng/tím |
| 8 | Quote | 8+ | Câu nói truyền cảm hứng + typography |
| 9 | Famous | 6+ | Ronaldo, Spider-Man, Messi (pop art) |
| 10 | Car | 6+ | Siêu xe Ferrari, Lamborghini |
| 11 | Anime | 6+ | Anime scenery, nhân vật, hoa anh đào |

**Tổng**: ~100+ wallpaper templates
**Filter**: All / Favorite

---

## 4. Wallpaper Creation (Editor)
**Folder**: `02_wallpaper_creation/` và `03_collage_creation/`

### Truy cập
- Home > "TRY NOW" (tạo mới, canvas trống)
- Home > Tap wallpaper > Preview > Next (edit wallpaper có sẵn)

### 4 Công cụ chính

#### 4.1 BG (Background)
- Color picker (vòng tròn gradient)
- 9+ preset solid colors
- "Add Image" - import ảnh làm background
- 15-20 background templates (hearts, gradients, clouds, kawaii)

#### 4.2 Import
- Mở "Select Photo" từ gallery
- Tabs: "All albums" / "Recent"
- Yêu cầu permission lần đầu (Allow limited / Allow all / Don't allow)

#### 4.3 Text
- Input field (placeholder "Hello")
- Text Library: 5 decorative patterns (symbols: hearts, stars, sparkles)
- 8+ fonts (serif, sans-serif, handwriting, decorative)
- 9+ preset colors + color wheel

#### 4.4 Sticker
- 30+ stickers:
  - Hoa, trái tim, động vật (mèo, gấu, thỏ)
  - Hello Kitty, vương miện, cầu vồng
  - Nơ/ribbon, bướm, ngôi sao, bóng đá
  - Nhân vật, text decorative

### Tính năng bổ sung
| Tính năng | Mô tả |
|-----------|-------|
| Layer Management | Quản lý thứ tự layers, lock/unlock |
| Undo/Redo | Hoàn tác / làm lại thao tác |
| Preview | Xem wallpaper dạng lock screen (hiển thị giờ/ngày) |

### Điều KHÔNG có
- Không có filters/effects
- Không có crop/resize/rotate riêng biệt
- Không có tab "Collage" riêng - editor là layer-based compositor

---

## 5. Wallpaper Preview & Set Flow
**Folder**: `08_wallpaper_preview_flow/` và `05_export_share/`

### Flow đầy đủ (6 bước + 3-4 ads)
```
Tap wallpaper -> [Interstitial Ad] -> Preview (swipe) -> [Interstitial Ad]
-> Edit -> Next -> [Rewarded Ad "Get this item"] -> Set Wallpaper
```

### Chi tiết
| Bước | Màn hình | Ad? |
|------|----------|-----|
| 1 | Tap wallpaper từ grid | Interstitial video (bắt buộc) |
| 2 | Preview: swipe trái/phải, carousel 3 cards | Banner ad cuối màn hình |
| 3 | Tap Next -> chuyển sang Edit | Interstitial video (bắt buộc) |
| 4 | Edit: có thể chỉnh sửa hoặc Next | - |
| 5 | Popup "Get this item" | Watch now (rewarded) / No thanks |
| 6 | Set Wallpaper | Chọn: Home / Lock / Both |

### Set Wallpaper Options
- **Home Screen** - hình nền màn hình chính
- **Lock Screen** - hình nền màn hình khóa
- **Home Screen and Lock Screen** - cả hai

### Hạn chế
- **Không có** Download/Save as file
- **Không có** Share wallpaper (chỉ share app link)
- Chỉ có set wallpaper trực tiếp qua Android wallpaper service

---

## 6. My Gallery
**Truy cập**: Home > "My Gallery"

- Lưu trữ wallpapers đã tải/tạo
- Khi trống: "Nothing here yet" + mascot 3D + "Explore now"
- Nút "Select" để chọn nhiều items
- Filter: All / Favorite
- Banner ad cuối màn hình

---

## 7. Settings
**Folder**: `04_settings/`

| Mục | Hành động |
|-----|-----------|
| Language | Chọn 1/19 ngôn ngữ |
| Term of Service | Mở trang web (sites.google.com) |
| Privacy Policy | Mở trang web (sites.google.com) |
| Rating 5 Stars | In-app rating dialog |
| Share with Friend | Android Share Sheet (link Play Store) |

### Điều KHÔNG có trong Settings
- Không có Account/Profile/Login
- Không có Notifications settings
- Không có Dark mode
- Không có "Remove Ads" / "Go Premium"
- **Màn hình duy nhất KHÔNG có quảng cáo**

### Thông tin pháp lý
- **Company**: LeafMotion Software
- **Contact**: buihieu2568@gmail.com
- **Độ tuổi tối thiểu**: 13+
- **Permissions**: INTERNET, ACCESS_NETWORK_STATE, CAMERA, VIBRATE, POST_NOTIFICATIONS

---

## 8. Monetization (Quảng cáo)
**Folder**: `06_monetization/`

### Mô hình
- **100% ad-supported** - KHÔNG có subscription, IAP, paywall
- Tất cả tính năng miễn phí nhưng phải xem quảng cáo

### 4 Loại quảng cáo

| Loại | Vị trí | Bắt buộc? | Tần suất |
|------|--------|-----------|----------|
| **Banner** | Cuối hầu hết màn hình | Có (luôn hiển thị) | Mỗi màn hình |
| **Interstitial** (video) | Mỗi transition giữa màn hình | Có (countdown + skip) | Mỗi chuyển màn hình |
| **Rewarded** (video) | Khi lưu wallpaper ("Get this item") | Có (bắt buộc để lưu) | Mỗi lần lưu |
| **Native** | Xen kẽ trong grid, lists | Có | Rải rác |

### Ad Networks
| Network | Vai trò | Loại ad |
|---------|---------|---------|
| **Pangle** (TikTok for Business) | Chính | Banner, Interstitial, Rewarded, Native |
| **Google AdMob** | Phụ | App Open Ad, có thể mediation |

### Vị trí quảng cáo theo màn hình
| Màn hình | Loại ad |
|----------|---------|
| App launch (lần đầu) | Interstitial (AdMob) |
| Onboarding slides | Banner (Pangle) |
| Home screen | Banner (Pangle/CapCut) |
| Tap wallpaper | Interstitial video |
| Preview | Banner |
| Preview -> Edit | Interstitial video |
| Edit -> Save | Rewarded dialog ("Get this item") |
| Set Wallpaper | Banner |
| My Gallery | Banner |
| **Settings** | **KHÔNG có ad** |

### UX Impact
- Trung bình **4-5 quảng cáo** cho 1 flow xem + set wallpaper
- Mỗi transition đều có interstitial ad
- **Bắt buộc xem rewarded ad** để lưu wallpaper
- Banner chiếm ~15-20% màn hình dưới
- **Chỉ Settings không có ad**

---

## Tổng kết nhanh

### Điểm mạnh
- Thư viện wallpaper phong phú (100+ templates, 11 categories)
- Hỗ trợ live wallpapers (animated)
- Editor đa năng với layer system
- Hỗ trợ 19 ngôn ngữ
- Hoàn toàn miễn phí

### Điểm yếu
- Quảng cáo quá nhiều, gây gián đoạn trải nghiệm
- Không có download/save as file
- Không có share wallpaper
- Không có filters/effects cho ảnh
- Không có crop/resize/rotate
- Settings rất đơn giản
- Không có account/profile system
- Có lỗi chính tả ("Ducth", "Let select")

### Số liệu thống kê
| Metric | Giá trị |
|--------|---------|
| Tổng categories | 11 |
| Tổng wallpaper templates | ~100+ |
| Ngôn ngữ hỗ trợ | 19 |
| Công cụ editor | 4 (BG, Import, Text, Sticker) |
| Stickers | 30+ |
| Fonts | 8+ |
| Background templates | 15-20 |
| Số ad trung bình/flow | 4-5 |
| Subscription/IAP | Không có |

---

## Cấu trúc thư mục output

```
features/
├── FEATURE_LIST.md              <- File này
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
│   ├── 01_for_you/ ~ 11_anime/ (mỗi category 1 folder + screenshots)
│   └── screenshots/
├── 08_wallpaper_preview_flow/
│   ├── README.md                (6 screenshots)
│   └── screenshots/
└── 09_onboarding/
    ├── README.md                (7 screenshots)
    └── screenshots/
```

**Tổng cộng**: 9 khu vực tính năng, ~75+ screenshots
