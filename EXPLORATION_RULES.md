# QUY TẮC KHÁM PHÁ APP - DIY Wallpaper Maker Collage

## Thông tin kỹ thuật
- **Package**: `com.diy.wallpaper.maker.collage`
- **ADB**: `$HOME/Library/Android/sdk/platform-tools/adb`
- **Emulators**: emulator-5554, emulator-5558, emulator-5560
- **Thư mục gốc**: `/Users/tuanldas/Desktop/Codes/tmp`

---

## 1. QUẢN LÝ TODO (TaskCreate / TaskUpdate)

- Mỗi **tính năng lớn** = 1 task trong todo list
- Khi agent phát hiện tính năng mới chưa có trong todo -> **TaskCreate** để thêm
- Khi hoàn thành khám phá 1 tính năng -> **TaskUpdate** đánh dấu completed
- Trước khi tạo task mới -> **TaskList** kiểm tra trùng lặp
- Subject task = tên tính năng (VD: "Wallpaper Creator", "Collage Editor")

---

## 2. CẤU TRÚC THƯ MỤC OUTPUT

```
features/
├── FEATURE_LIST.md              # Tổng hợp tất cả tính năng
├── 01_ten_tinh_nang_lon/
│   ├── README.md                # Mô tả UI/UX, luồng hoạt động
│   ├── screenshots/             # Ảnh chụp màn hình
│   │   ├── main_screen.png
│   │   └── ...
│   ├── 01_tinh_nang_nho_1/
│   │   ├── README.md
│   │   └── screenshots/
│   │       └── ...
│   ├── 02_tinh_nang_nho_2/
│   │   ├── README.md
│   │   └── screenshots/
│   │       └── ...
│   └── ...
├── 02_ten_tinh_nang_lon_2/
│   ├── README.md
│   ├── screenshots/
│   └── ...
└── ...
```

---

## 3. NỘI DUNG FILE README.md CỦA MỖI TÍNH NĂNG

```markdown
# Tên tính năng

## Mô tả
Mô tả ngắn gọn tính năng làm gì.

## Vị trí truy cập
Cách navigate đến tính năng này từ home (VD: Home > tab Collage > nút Create)

## UI/UX Design
- Layout: mô tả bố cục màn hình
- Các thành phần UI chính (buttons, tabs, lists...)
- Màu sắc, icons đáng chú ý

## Luồng hoạt động (Flow)
1. Bước 1...
2. Bước 2...
3. ...

## Tính năng con
- [ ] Tính năng con 1 (có folder riêng)
- [ ] Tính năng con 2

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/xxx.png | Mô tả |

## Ghi chú
Những điểm đáng chú ý, bugs, UX issues...
```

---

## 4. QUY TẮC CHO AGENTS

### Khi khám phá mỗi màn hình:
1. **Screenshot** -> lưu vào folder `screenshots/` tương ứng
2. **UI dump** -> parse để lấy danh sách elements
3. **Ghi nhận** tất cả buttons, text, interactive elements
4. **Tap thử** từng element để xem dẫn đến đâu
5. **Scroll** để kiểm tra nội dung ẩn bên dưới
6. Nếu phát hiện tính năng mới -> **TaskCreate**
7. Ghi kết quả vào **README.md** của folder tương ứng

### Quy tắc đặt tên:
- Folder: snake_case, có prefix số thứ tự (01_, 02_...)
- Screenshots: mô_tả_ngắn.png (VD: home_main.png, collage_editor_toolbar.png)
- Dùng tiếng Anh cho tên folder/file, tiếng Việt cho nội dung mô tả

### ADB Commands:
```bash
ADB="$HOME/Library/Android/sdk/platform-tools/adb"

# Screenshot + save
"$ADB" -s <emu> shell screencap -p /sdcard/s.png
"$ADB" -s <emu> pull /sdcard/s.png <local_path>

# UI dump + parse
"$ADB" -s <emu> shell uiautomator dump /sdcard/ui.xml
"$ADB" -s <emu> pull /sdcard/ui.xml /tmp/<name>.xml
python3 -c "
import xml.etree.ElementTree as ET
tree = ET.parse('/tmp/<name>.xml')
for node in tree.getroot().iter('node'):
    t = node.get('text',''); d = node.get('content-desc','')
    b = node.get('bounds',''); c = node.get('class','')
    ck = node.get('clickable','')
    if t or d:
        print(f'TEXT:{t} | DESC:{d} | BOUNDS:{b} | CLICK:{ck} | CLASS:{c}')
"

# Interactions
"$ADB" -s <emu> shell input tap <x> <y>
"$ADB" -s <emu> shell input swipe 540 1500 540 500 300   # scroll down
"$ADB" -s <emu> shell input swipe 540 500 540 1500 300   # scroll up
"$ADB" -s <emu> shell input keyevent KEYCODE_BACK        # back
```

---

## 5. PHÂN CÔNG AGENTS

| Agent | Emulator | Khu vực bắt đầu |
|-------|----------|-----------------|
| Agent 1 | emulator-5554 | Home screen -> khám phá Wallpaper features |
| Agent 2 | emulator-5558 | Home screen -> khám phá Collage features |
| Agent 3 | emulator-5560 | Home screen -> khám phá Settings, Export, Monetization |

Mỗi agent tự navigate từ home đến khu vực được giao.
Nếu agent phát hiện tính năng thuộc khu vực agent khác -> vẫn tạo TaskCreate nhưng chỉ ghi chú, không deep dive.
