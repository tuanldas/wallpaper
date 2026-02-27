# Wallpaper Creation (Tạo Wallpaper)

## Mô tả
Tính năng tạo wallpaper DIY cho phép người dùng thiết kế wallpaper từ đầu với các công cụ: Background, Import ảnh, Text và Sticker. Người dùng cũng có thể chọn wallpaper template có sẵn và set làm wallpaper.

## Vị trí truy cập
Home > nút "TRY NOW" (Create wallpaper)

## UI/UX Design

### Wallpaper Editor Screen
- **Top bar**:
  - Back button (btnBack) - quay lại Home
  - "Edit" title
  - Undo button (icUndo)
  - Redo button (icRedo)
  - Preview button (icPreview) - xem trước wallpaper
  - "Next" button (btnNext, màu hồng) - chuyển sang export/save
- **Canvas area**: Vùng làm việc chính, checkered pattern khi trống (transparent)
- **Layer button** (btnLayer): Góc dưới trái, mở panel quản lý layers
- **Bottom toolbar**: 4 công cụ chính

### Bottom Toolbar (4 tools)
1. **BG** (Background) - Chọn/thay đổi nền
2. **Import** - Nhập ảnh từ gallery
3. **Text** - Thêm text
4. **Sticker** - Thêm sticker

## Luồng hoạt động (Flow)

### 1. Tạo wallpaper mới
1. Tap "TRY NOW" trên Home
2. Mở Editor với canvas trống
3. Sử dụng các tool để thiết kế
4. Tap "Next" -> Hiện popup "Get this item" (ad gate)
   - "Watch now" - Xem quảng cáo để tiếp tục miễn phí
   - "No, thanks" - Bỏ qua
5. Tiếp tục edit hoặc export

### 2. Xem wallpaper template
1. Tap wallpaper từ Home grid
2. Quảng cáo video hiển thị (bắt buộc xem)
3. Màn hình Preview hiển thị:
   - Wallpaper full-screen
   - Swipe trái/phải xem các wallpapers khác
   - "Preview" button (xem trên home screen)
   - "Next" button (dẫn đến Set wallpaper)
4. Màn hình "Set wallpaper":
   - Full-screen wallpaper preview
   - "Preview" button góc phải trên
   - "Set wallpaper" button (màu hồng) - đặt làm wallpaper

## Chi tiết các công cụ

### BG (Background)
- **Color Picker**: Vòng tròn gradient màu + màu đen
- **Solid Colors**: Các ô màu đơn: trắng/xám, hồng nhạt, hồng, đỏ, vàng nhạt, cam, ...
- **Add Image**: Nút "+" để thêm hình ảnh làm background từ gallery
- **Background Templates**: Grid các background template có sẵn (hearts, gradients, hình vẽ, ...)
- **Checkmark** (btnOk) để xác nhận chọn background

### Import
- Mở màn hình "Select Photo"
- Yêu cầu quyền truy cập photos lần đầu: "Allow limited access", "Allow all", "Don't allow"
- Hiện gallery ảnh thiết bị
- Tabs: "All albums" và "Recent"
- Nút "Done" để xác nhận chọn ảnh

### Text
- **Text input**: Ô nhập text (mặc định "Hello")
- **Text Library**: Thư viện text trang trí với các decorative dividers/borders bằng ký tự đặc biệt (hoa, ngôi sao, trái tim, etc.)
- **Font selection**: Nhiều font khác nhau (hiển thị ngay trong danh sách cuộn ngang)
- **Color picker**: Vòng tròn gradient + các màu đơn (đen, xám, hồng, đỏ, vàng, cam, ...)
- **Checkmark** (btnOk) để xác nhận

### Sticker
- **Grid stickers**: Nhiều sticker đa dạng:
  - Hoa, vinyl record, bông hoa hồng
  - Speech bubble, Hello Kitty, heart
  - Rainbow, dải nơ (bow), butterfly
  - Crown, music note, soccer ball
  - Bear, cat, fire, Happy Birthday
  - Và nhiều sticker khác...
- Scroll xuống để xem thêm stickers
- Tap sticker để thêm vào canvas
- **Checkmark** (btnOk) để đóng panel

### Layer Management
- Tap icon Layer (góc dưới trái)
- Hiện panel "Layer" với thumbnail các layers
- Lock icon để khóa/mở khóa layer
- Checkmark để đóng panel

## Tính năng con
- Background library (màu + templates)
- Photo import từ gallery
- Text với nhiều fonts và màu sắc
- Text Library (decorative text)
- Sticker library (rất phong phú)
- Layer management
- Undo/Redo
- Preview mode

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/create_wallpaper_01.png | Editor screen - canvas trống với 4 tools |
| screenshots/bg_panel.png | Background panel - color picker và templates |
| screenshots/import_screen.png | Import - yêu cầu quyền truy cập |
| screenshots/import_gallery2.png | Import - gallery ảnh |
| screenshots/text_panel.png | Text panel - input, fonts, colors |
| screenshots/text_library.png | Text Library - decorative text dividers |
| screenshots/sticker_panel2.png | Sticker panel - grid stickers |
| screenshots/sticker_panel_scrolled.png | Sticker panel - thêm stickers khi scroll |
| screenshots/layers_panel2.png | Layer management panel |
| screenshots/wallpaper_preview.png | Wallpaper Preview - swipeable |
| screenshots/set_wallpaper.png | Set wallpaper screen - full preview |
| screenshots/set_wallpaper_options.png | Ad gate trước khi set wallpaper |

## Ghi chú
- Khi tap "Next" từ Editor, hiện popup "Get this item" yêu cầu xem quảng cáo - đây là monetization point
- Quảng cáo video bắt buộc xem khi tap wallpaper từ Home grid
- App sử dụng Pangle (TikTok Ad Network) và CapCut làm ad providers
- Live wallpapers có hiệu ứng động (animation)
- Canvas hỗ trợ multiple layers với khả năng lock/unlock
- Sticker library khá phong phú với nhiều theme (kawaii, love, nature, etc.)
