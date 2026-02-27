# DIY Wallpaper Maker Collage - Feature Exploration Plan

## Thông tin app
- **Package**: `com.diy.wallpaper.maker.collage`
- **ADB path**: `$HOME/Library/Android/sdk/platform-tools/adb`
- **Emulators**: emulator-5554, emulator-5558, emulator-5560

---

## CHIẾN LƯỢC SONG SONG (3 Emulators)

### Phân công Emulators:

| Emulator | Vai trò | Khu vực khám phá |
|----------|---------|-------------------|
| **emulator-5554** (Agent 1) | Home & Wallpaper Creation | Home screen, tạo wallpaper, templates, backgrounds, parallax/3D |
| **emulator-5558** (Agent 2) | Collage & Editing Tools | Tạo collage, editing tools, stickers, text, filters, frames |
| **emulator-5560** (Agent 3) | Settings, Export & Monetization | Settings, export/save/share, subscription/IAP, onboarding, permissions |

### Mỗi Agent thực hiện:
1. Mở app -> navigate đến khu vực được giao
2. Screenshot + UI dump mỗi màn hình
3. Liệt kê mọi button/element/interaction
4. Thử tương tác (tap, scroll, input)
5. Ghi kết quả vào file output riêng

---

## OUTPUT FILES

| File | Nội dung | Trạng thái |
|------|----------|------------|
| `EXPLORATION_PLAN.md` | File này - tracking tiến độ | Active |
| `01_STORE_INFO.md` | Thông tin từ Play Store | Pending |
| `02_AGENT1_HOME_WALLPAPER.md` | Agent 1: Home & Wallpaper Creation | Pending |
| `03_AGENT2_COLLAGE_EDITING.md` | Agent 2: Collage & Editing Tools | Pending |
| `04_AGENT3_SETTINGS_EXPORT.md` | Agent 3: Settings, Export, Monetization | Pending |
| `05_FEATURE_MATRIX.md` | Tổng hợp feature matrix | Pending |
| `06_USER_JOURNEYS.md` | Các user journeys chính | Pending |
| `07_SUMMARY.md` | Tổng hợp cuối cùng | Pending |

---

## ADB COMMANDS REFERENCE (cho agents)
```bash
ADB="$HOME/Library/Android/sdk/platform-tools/adb"

# Mở app
"$ADB" -s <emulator> shell am start -n com.diy.wallpaper.maker.collage/.MainActivity

# Screenshot
"$ADB" -s <emulator> shell screencap -p /sdcard/screen.png
"$ADB" -s <emulator> pull /sdcard/screen.png /tmp/<filename>.png

# UI dump
"$ADB" -s <emulator> shell uiautomator dump /sdcard/ui.xml
"$ADB" -s <emulator> pull /sdcard/ui.xml /tmp/<filename>.xml

# Parse UI dump
python3 -c "
import xml.etree.ElementTree as ET
tree = ET.parse('/tmp/<filename>.xml')
for node in tree.getroot().iter('node'):
    text = node.get('text', '')
    desc = node.get('content-desc', '')
    cls = node.get('class', '')
    bounds = node.get('bounds', '')
    if text or desc:
        print(f'TEXT: {text} | DESC: {desc} | BOUNDS: {bounds} | CLASS: {cls}')
"

# Tap
"$ADB" -s <emulator> shell input tap <x> <y>

# Scroll down
"$ADB" -s <emulator> shell input swipe 540 1500 540 500 300

# Scroll up
"$ADB" -s <emulator> shell input swipe 540 500 540 1500 300

# Back
"$ADB" -s <emulator> shell input keyevent KEYCODE_BACK
```

---

## TIẾN ĐỘ
- [x] Cài app trên 3 emulators
- [ ] Phase 1: Thu thập Play Store info (main agent)
- [ ] Phase 2: Khám phá song song (3 agents)
  - [ ] Agent 1: Home & Wallpaper
  - [ ] Agent 2: Collage & Editing
  - [ ] Agent 3: Settings & Export
- [ ] Phase 3: Tổng hợp feature matrix
- [ ] Phase 4: Summary & User journeys
