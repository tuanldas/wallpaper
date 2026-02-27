# Export / Save / Share (Xuất / Lưu / Chia sẻ)

## Mô tả
Tính năng cho phép người dùng lưu wallpaper và đặt làm hình nền điện thoại. App không có chức năng export file độc lập - thay vào đó, flow chính là **Preview -> Edit -> Set Wallpaper**. Wallpaper được lưu vào "My Gallery" của app và có thể đặt làm hình nền trực tiếp.

## Vị trí truy cập
- **Xem wallpaper**: Home > Tap vào bất kỳ wallpaper nào trong grid
- **My Gallery**: Home > "My Gallery" (góc phải trên)
- **Set Wallpaper**: Preview > Next (Edit) > Next > Watch ad > Set Wallpaper

## UI/UX Design

### Màn hình Preview
- **Header**: "Preview" với nút Back và nút "Next" (hồng)
- **Canvas**: Hiển thị wallpaper toàn màn hình, có thể swipe trái/phải để xem wallpaper khác
- **Banner ad** ở cuối màn hình

### Màn hình Edit (Wallpaper Editor)
- **Header**: "Edit" với nút Back, Undo, Redo, Visibility toggle, nút "Next" (hồng)
- **Canvas**: Wallpaper đang edit trên nền checkered (transparent)
- **Bottom toolbar**: BG (Background), Import, Text, Sticker
- *(Chi tiết editing tools thuộc khu vực Collage & Editing)*

### Màn hình Set Wallpaper
- **Header**: Nút Back, "Preview" link
- **Wallpaper preview**: Hiển thị wallpaper full screen
- **Title**: "Set your wallpaper"
- **3 nút chức năng**:
  1. **Home Screen** - Đặt làm hình nền màn hình chính
  2. **Lock Screen** - Đặt làm hình nền màn hình khóa
  3. **Home Screen and Lock Screen** - Đặt cho cả hai
- Nút **Set wallpaper** để xác nhận (sau khi chọn một tùy chọn)
- **Banner ad** ở cuối màn hình

### My Gallery
- **Header**: "My Gallery" với nút Back và "Select"
- Khi chưa có wallpaper: Hiển thị nhân vật 3D + "Nothing here yet" + nút "Explore now"
- **Banner ad** ở cuối màn hình (TikTok Lite)

## Luồng hoạt động (Flow)

### Flow xem và lưu wallpaper từ library:
1. Tap wallpaper trong Home grid
2. **Interstitial ad** xuất hiện (video ~5-20 giây, có nút Skip/Close)
3. Màn hình **Preview** hiển thị wallpaper
4. Tap **Next** -> **Interstitial ad** xuất hiện lại
5. Màn hình **Edit** - có thể chỉnh sửa wallpaper
6. Tap **Next** -> Dialog **"Get this item"** xuất hiện:
   - **Watch now**: Xem rewarded video ad (~20 giây) để nhận wallpaper
   - **No, thanks**: Từ chối (không lưu được)
7. Sau khi xem xong ad -> Màn hình **Set Wallpaper**
8. Chọn vị trí (Home Screen / Lock Screen / Both)
9. Tap **Set wallpaper** để hoàn tất

### Flow wallpaper từ gallery:
1. Home > "My Gallery"
2. Chọn wallpaper đã lưu
3. Có tùy chọn set wallpaper hoặc xóa

## Tính năng con
- **Preview wallpaper**: Xem trước wallpaper trước khi lưu
- **Swipe gallery**: Swipe trái/phải để xem wallpaper khác trong cùng category
- **Edit wallpaper**: Chỉnh sửa wallpaper trước khi lưu (BG, Import, Text, Sticker)
- **Set as wallpaper**: Đặt trực tiếp làm hình nền điện thoại
- **My Gallery**: Lưu trữ các wallpaper đã tải/tạo
- **Filter**: Lọc wallpaper theo "All" hoặc "Favorite"
- **Favorite**: Tap icon trái tim trên wallpaper card để yêu thích

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/01_my_gallery.png | My Gallery - chưa có wallpaper |
| screenshots/02_wallpaper_preview.png | Interstitial ad trước khi xem wallpaper |
| screenshots/05_save_screen.png | Interstitial ad video (CapCut) |
| screenshots/07_actual_export.png | Màn hình Edit wallpaper |
| screenshots/08_export_final.png | Dialog "Get this item" - Rewarded ad |
| screenshots/10_save_result.png | Màn hình Set Wallpaper với 3 tùy chọn |
| screenshots/11_set_wallpaper_buttons.png | Màn hình Set Wallpaper (scrolled) |

## Ghi chú
- **Không có** chức năng Download/Save as file riêng (chỉ set wallpaper trực tiếp)
- **Không có** chức năng Share wallpaper với bạn bè (chỉ share app link từ Settings)
- Mỗi bước chuyển màn hình đều có thể hiển thị **interstitial ad**
- Để lưu wallpaper, **bắt buộc phải xem rewarded ad** (~20 giây)
- App sử dụng hệ thống **wallpaper service** của Android để đặt hình nền
- Số lượng ad rất nhiều trong flow này (3-4 ad cho 1 wallpaper)
