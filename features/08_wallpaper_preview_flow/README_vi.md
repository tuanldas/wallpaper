# Wallpaper Preview & Set Wallpaper Flow

## Mô tả
Luồng xem trước và đặt wallpaper khi người dùng chọn một wallpaper từ grid trên Home screen.

## Vị trí truy cập
Home > Tap wallpaper trong grid > (Ad video) > Preview > Next > (Ad) > Set Wallpaper

## Luồng hoạt động chi tiết

### Bước 1: Tap wallpaper từ Home grid
- Tap vào bất kỳ wallpaper nào trong grid
- **Quảng cáo video bắt buộc** hiển thị (CapCut/Pangle Test Ads)
  - Thời lượng: ~15-30 giây
  - Có "Skip after Xs" hoặc "X seconds remaining" ở góc phải trên
  - Sau khi hết thời gian: hiện nút "Ad closed" để đóng
  - KHÔNG thể skip ngay lập tức - phải đợi hết countdown

### Bước 2: Màn hình Preview
- **Header**: Back arrow (trái), "Preview" title, "Next" button (hồng, phải)
- **Wallpaper display**: Hiển thị full-screen trong card bo tròn
- **Swipe**: Có thể swipe trái/phải để xem các wallpapers khác trong cùng category
  - Wallpaper bên trái và phải hiển thị nhỏ ở 2 bên (peek effect)
  - 3 cards hiển thị cùng lúc (current + 2 sides)
- **Ad banner**: Native ad (CapCut/Pangle) ở cuối màn hình, có nút collapse (btn_collapsible)

### Bước 3: Tap Next từ Preview
- Hiện quảng cáo video bắt buộc (lần 2)
- Đợi hết thời gian > đóng ad

### Bước 4: Màn hình Set Wallpaper (hoặc Editor)
Tùy thuộc vào loại wallpaper:

**Static wallpaper từ grid:**
- Mở trong **Editor** (có thể chỉnh sửa trước)
- Editor hiện wallpaper đã load sẵn trên canvas
- Có đầy đủ tools: BG, Import, Text, Sticker
- Tap "Next" từ Editor > Popup "Get this item"

**Popup "Get this item" (Ad Gate):**
- Mascot thỏ 3D
- "Watch now" - Xem quảng cáo rewarded để unlock
- "No, thanks" - Bỏ qua (có thể bị giới hạn tính năng)
- Khi tap "Watch now": quảng cáo video ~30 giây, có countdown "X seconds remaining"

**Sau khi xem ad / từ wallpaper preview:**
- Màn hình **Set Wallpaper** full-screen:
  - Back button (hồng, góc trái trên)
  - "Preview" button (góc phải trên) - xem trên home screen mock
  - "Set wallpaper" button (hồng, đáy màn hình)

### Bước 5: Set Wallpaper
- Tap "Set wallpaper" button
- (Chưa xác nhận được các options home/lock/both do ad che liên tục trên emulator test)

## Ad Flow Summary
| Thời điểm | Loại ad | Có skip? | Thời lượng |
|-----------|---------|----------|------------|
| Tap wallpaper từ grid | Video interstitial | Có, sau countdown | ~15-30s |
| Đóng ad lần 1 | Native fullscreen (Pangle) | Có, btn_collapsible | Ngay lập tức |
| Tap Next từ Preview | Video interstitial | Có, sau countdown | ~15-30s |
| Đóng ad lần 2 | Native fullscreen (Pangle) | Có, btn_collapsible | Ngay lập tức |
| Tap Next từ Editor | Popup "Get this item" | "No thanks" hoặc xem ad | ~30s nếu xem |

Tổng cộng: **4-5 quảng cáo** cho mỗi luồng xem + set wallpaper

## Tính năng Swipe Preview
- Swipe trái/phải để duyệt qua các wallpapers
- Hiển thị kiểu carousel: wallpaper chính ở giữa, 2 wallpaper nhỏ 2 bên
- Mỗi card có bo tròn (rounded corners)
- Các wallpaper trong cùng category/tab

## Chất lượng ảnh
- Preview hiển thị chất lượng cao, full resolution
- Wallpaper fit toàn bộ màn hình khi set
- Hỗ trợ cả static và live wallpapers

## Live Wallpaper
- Live wallpapers có badge "(>) Live" trên Home grid
- Trong Preview, live wallpaper có animation chạy
- Flow tương tự static wallpaper nhưng có thêm hiệu ứng động

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/preview_static2.png | Preview màn hình - static wallpaper heart lollipops |
| screenshots/get_this_item_popup.png | Popup "Get this item" - ad gate với Watch now/No thanks |
| screenshots/after_watch_ad.png | Quảng cáo rewarded video - "3 seconds remaining" |
| screenshots/set_wallpaper_final.png | Wallpaper loaded trong Editor |
| screenshots/set_wallpaper_screen.png | Loading screen khi chuyển màn hình |

## Ghi chú
- App hiển thị rất nhiều quảng cáo trong luồng này (4-5 ads cho 1 flow)
- Quảng cáo làm giảm trải nghiệm người dùng đáng kể
- "Watch now" là rewarded ad - người dùng xem ad để unlock wallpaper miễn phí
- Emulator chạy test ads (Pangle Test Ads) nên có thể khác với production
- Một số quảng cáo fullscreen native có thể che nút "Set wallpaper", cần collapse trước
- Do giới hạn của test environment, chưa xác nhận được đầy đủ options Set Wallpaper (home/lock/both)
