# Collage & Editing Tools

## Mô tả
App "DIY Wallpaper Maker Collage" cung cấp một editor đa lớp (layer-based) cho phép người dùng tạo wallpaper từ đầu hoặc chỉnh sửa wallpaper có sẵn. Editor hỗ trợ 4 công cụ chính: Background, Import, Text, và Sticker. Người dùng cũng có thể xem trước wallpaper dưới dạng lock screen preview.

## Vị trí truy cập
- **Tạo mới**: Home > "Create wallpaper / TRY NOW" button
- **Chỉnh sửa wallpaper có sẵn**: Home > Tap wallpaper > Preview screen > Next

## UI/UX Design

### Editor chính (Edit screen)
- **Top bar**:
  - Nút Back (mũi tên trái, màu hồng)
  - Tiêu đề "Edit"
  - Undo button
  - Redo button
  - Preview button (icon mắt) - hiển thị wallpaper dưới dạng lock screen
  - Nút "Next" (màu hồng/đỏ, bo tròn)
- **Canvas**: Khu vực chính hiển thị wallpaper đang tạo, nền trong suốt (checkerboard) khi chưa có background
- **Layer icon**: Góc dưới trái, icon lớp chồng
- **Bottom toolbar**: 4 tab - BG | Import | Text | Sticker

### Màu sắc chính
- Hồng/Đỏ (primary): các nút chính, tab active
- Trắng (background)
- Đen (text, icons)

## Luồng hoạt động (Flow)

### Flow 1: Tạo wallpaper mới
1. Từ Home, tap "Create wallpaper / TRY NOW"
2. Vào Editor với canvas trống
3. Chọn Background (BG)
4. Thêm Import/Text/Sticker tùy ý
5. Xem trước bằng Preview (hiển thị như lock screen với ngày/giờ)
6. Tap Next để lưu/export (có thể hiện reward ad popup "Get this item")

### Flow 2: Chỉnh sửa wallpaper có sẵn
1. Từ Home, tap 1 wallpaper template
2. Xem trước trong Preview screen (có thể swipe sang wallpaper khác)
3. Tap Next để vào Editor
4. Chỉnh sửa với các công cụ
5. Tap Next để lưu/export

## Tính năng con

### 1. BG (Background)
- **Vị trí**: Bottom toolbar > tab "BG"
- **Mô tả**: Đặt background cho wallpaper
- **Các tùy chọn**:
  - **Color picker** (biểu tượng cầu vồng): Chọn màu bất kỳ
  - **Preset colors**: Đen, xám, nhiều sắc hồng, đỏ, kem, cam, vàng
  - **Add Image**: Import ảnh từ thư viện làm background
  - **Background templates**: ~15-20 templates có sẵn (trái tim, gradient hồng, stars, glow, spiral, clouds, v.v.)
- **Xác nhận**: Nút checkmark (OK) ở góc trên phải của panel

### 2. Import
- **Vị trí**: Bottom toolbar > tab "Import"
- **Mô tả**: Thêm ảnh từ thư viện vào canvas
- **Luồng**:
  1. Tap Import > Mở màn hình "Select Photo"
  2. Yêu cầu permission truy cập ảnh (Allow limited/Allow all/Don't allow)
  3. Hiển thị ảnh theo tabs: "All albums" / "Recent"
  4. Chọn ảnh > Tap "Done"
- **Giao diện**:
  - Top: Back, "Select Photo", Done
  - Grid ảnh thư viện
  - Quảng cáo native ở cuối

### 3. Text
- **Vị trí**: Bottom toolbar > tab "Text"
- **Mô tả**: Thêm text vào wallpaper
- **Các tùy chọn**:
  - **Input field**: Nhập text (placeholder "Hello")
  - **Text Library**: Thư viện text trang trí với các ký tự đặc biệt (hearts, stars, sparkles, diamonds, bows) - khoảng 5 patterns
  - **Font selector**: 8+ font khác nhau (serif, sans-serif, handwriting, decorative)
  - **Color picker**: 9+ màu preset + color wheel
- **Xác nhận**: Nút checkmark (OK)

### 4. Sticker
- **Vị trí**: Bottom toolbar > tab "Sticker"
- **Mô tả**: Thêm sticker trang trí vào wallpaper
- **Bộ sưu tập**: 30+ stickers bao gồm:
  - Hoa (daisy, cherry blossom)
  - Trái tim (nhiều kiểu)
  - Động vật (mèo, gấu, chó, hổ, thỏ)
  - Nhân vật (Hello Kitty)
  - Biểu tượng (vương miện, nốt nhạc, cầu vồng, ngôi sao, lửa)
  - Nơ/Ribbon (nhiều kiểu)
  - Bướm (nhiều màu)
  - Text decorative ("YOU", "10A", "DAL")
  - Khác (CD/vinyl, clipboard, frame, bóng đá)
- **Xác nhận**: Nút checkmark (OK)

### 5. Layer Management
- **Vị trí**: Icon lớp chồng ở góc dưới trái canvas
- **Mô tả**: Quản lý thứ tự các layer trên canvas
- **Hiển thị**: Danh sách layer với thumbnail, icon lock cho background layer
- **Xác nhận**: Nút checkmark (OK)

### 6. Preview (Lock Screen Preview)
- **Vị trí**: Icon mắt ở top bar
- **Mô tả**: Xem trước wallpaper đang tạo dưới dạng màn hình khóa
- **Hiển thị**:
  - Wallpaper full screen
  - Ngày tháng (VD: "Friday, February 27")
  - Đồng hồ lớn (VD: "21:52")
  - Nút back để quay lại editor

### 7. Undo/Redo
- **Vị trí**: Top bar, 2 icon mũi tên
- **Mô tả**: Hoàn tác và làm lại các thao tác chỉnh sửa

## Quảng cáo (Ads)
App hiển thị nhiều loại quảng cáo:
- **Native ads**: Hiển thị trong các màn hình (home, Select Photo, v.v.)
- **Interstitial ads**: Hiển thị khi chuyển màn hình (thoát editor, chọn wallpaper)
- **Reward ad popup**: "Get this item" - xem quảng cáo để nhận item, có nút "Watch now" và "No, thanks"
- **Ad providers**: Pangle, CapCut (TikTok Lite)

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/01_editor_overview.png | Editor chính với canvas trống |
| screenshots/02_bg_tool.png | Background tool với colors và templates |
| screenshots/03_bg_selected.png | Background đã được chọn |
| screenshots/04_text_tool.png | Text tool với font và color options |
| screenshots/05_text_library.png | Text Library với decorative patterns |
| screenshots/06_sticker_tool.png | Sticker tool với 30+ stickers |
| screenshots/07_import_permission.png | Import - yêu cầu permission |
| screenshots/08_import_select_photo.png | Select Photo screen |
| screenshots/09_layer_panel.png | Layer management panel |
| screenshots/10_reward_ad_popup.png | Reward ad popup "Get this item" |
| screenshots/11_preview_lockscreen.png | Preview mode - lock screen |
| screenshots/12_wallpaper_preview.png | Wallpaper preview trước khi edit |
| screenshots/13_editor_with_wallpaper.png | Editor với wallpaper có sẵn |

## Ghi chú
- App không có tab/section "Collage" riêng biệt. Thay vào đó, editor hoạt động như collage maker cho phép kết hợp nhiều layer (background + imported images + text + stickers)
- Quảng cáo xuất hiện rất nhiều, đặc biệt khi chuyển giữa các màn hình
- Background templates chủ yếu theo phong cách cute/kawaii với tông màu hồng
- Không tìm thấy tính năng crop, resize, rotate riêng biệt - editor tập trung vào compositing (ghép layer)
- Không tìm thấy tính năng filters/effects cho ảnh
- Categories wallpaper trên home: For you, DIY, Love, Live, Lock Screen, Kawaii, Aesthetic, Quote, Famous, Car, Anime
