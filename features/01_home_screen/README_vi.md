# Home Screen (Màn hình chính)

## Mô tả
Màn hình chính của app "DIY Wallpaper Maker Collage" hiển thị khi mở app. Đây là hub trung tâm để người dùng duyệt wallpaper templates, truy cập gallery cá nhân, và bắt đầu tạo wallpaper mới.

## Vị trí truy cập
Mở app > Home Screen (màn hình đầu tiên sau onboarding)

## Onboarding Flow (Lần đầu mở app)
1. **Chọn ngôn ngữ** - Màn hình Languages với 8 ngôn ngữ: English, Francais, Marathi (India), Espanol, Chinese, Portugues (Portugal), Russkiy, Indonesian
2. **Giới thiệu tính năng** - 2 trang onboarding:
   - Trang 1: "1000+ Unique Wallpaper - Find endless styles to spark your creativity"
   - Trang 2: "Design your own wallpaper - Use background, sticker, color, text... to create your style"
3. **Chọn sở thích** - "Let select your interest" với 11 categories: For you, DIY, Love, Live, Lock Screen, Kawaii, Aesthetic, Quote, Famous, Car, Anime

## UI/UX Design

### Header Area
- **Banner hình ảnh** - Góc trái trên, hiển thị hình preview wallpaper với hiệu ứng 3D cards
- **My Gallery** - Nút ở góc phải trên với icon gallery, dẫn đến thư viện cá nhân
- **Settings** - Icon gear ở góc phải trên cùng (ID: btnSetting)
- **Create wallpaper** - Text "Create wallpaper" và nút **TRY NOW** (màu hồng, gradient) - dẫn đến Wallpaper Editor

### Category Tabs (Scrollable ngang)
Danh sách tabs có thể scroll ngang:
1. **For you** - Gợi ý theo sở thích
2. **DIY** - Wallpaper kiểu scrapbook/collage
3. **Love** - Theme tình yêu, trái tim
4. **Live** - Live wallpapers (có hiệu ứng động)
5. **Lock Screen** - Wallpaper cho màn hình khóa
6. **Kawaii** - Theme dáng yêu kiểu Nhật
7. **Aesthetic** - Theme thẩm mỹ
8. **Quote** - Wallpaper có câu nói
9. **Famous** - Người nổi tiếng
10. **Car** - Theme xe hơi
11. **Anime** - Theme anime

### Filter
- **Filter by** label bên trái
- **All** dropdown bên phải với 2 options: "All" và "Favorite"

### Wallpaper Grid
- Layout grid 3 cột
- Mỗi wallpaper card hiển thị:
  - Thumbnail preview
  - Heart/Favorite icon (btnFavorite) ở góc phải trên
  - Badge "Live" cho live wallpapers
- Scroll dọc vô hạn để load thêm wallpapers
- Xen kẽ quảng cáo native (Pangle/CapCut) giữa các wallpapers

### Quảng cáo
- Native ad banner ở cuối màn hình (CapCut, Pangle)
- Collapsible với nút btn_collapsible

## Luồng hoạt động (Flow)

### Duyệt Wallpaper
1. Chọn tab category (For you, DIY, Love, ...)
2. Scroll dọc xem grid wallpapers
3. Tap vào wallpaper -> Hiện quảng cáo video -> Màn hình Preview
4. Tại Preview: swipe trái/phải xem wallpapers khác
5. Tap "Next" hoặc "Set wallpaper" để tiếp tục

### My Gallery
1. Tap "My Gallery" trên header
2. Hiện danh sách wallpapers đã lưu
3. Khi trống: hiện "Nothing here yet" với nút "Explore now" và mascot
4. Có nút "Select" ở góc phải trên để chọn nhiều items

### Tạo Wallpaper Mới
1. Tap "TRY NOW" -> Mở Wallpaper Editor

## Tính năng con
- Wallpaper Grid browsing
- Category filtering (11 categories)
- Favorite filtering
- My Gallery (thư viện cá nhân)
- Quick create wallpaper access

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/home_screen_01.png | Màn hình quảng cáo khi mở app lần đầu |
| screenshots/onboarding_01.png | Onboarding trang 1 - 1000+ Unique Wallpaper |
| screenshots/onboarding_02.png | Onboarding trang 2 - Design your own wallpaper |
| screenshots/onboarding_03_interests.png | Chọn sở thích (11 categories) |
| screenshots/home_main.png | Home screen chính với grid wallpapers |
| screenshots/home_scrolled.png | Home screen sau khi scroll xuống |
| screenshots/home_scrolled2.png | Home screen scroll thêm - TikTok ad |
| screenshots/tab_diy.png | Tab DIY - wallpapers scrapbook style |
| screenshots/tab_love.png | Tab Love - wallpapers theme tình yêu |
| screenshots/tab_live.png | Tab Live - live wallpapers |
| screenshots/tabs_more.png | Các tabs: Aesthetic, Quote, Famous, Car |
| screenshots/tabs_more2.png | Các tabs: Car, Anime |
| screenshots/filter_all.png | Dropdown filter: All / Favorite |
| screenshots/my_gallery.png | My Gallery - trống, chưa có wallpaper |

## Ghi chú
- App hiển thị rất nhiều quảng cáo (Pangle Test Ads, CapCut) - bao gồm native ads, video ads, và interstitial ads
- Quảng cáo xuất hiện khi: mở app, chuyển màn hình, tap wallpaper, quay lại home
- Live wallpapers có badge "(>) Live" để phân biệt với static wallpapers
- Grid wallpapers load thêm khi scroll xuống (infinite scroll)
- App hỗ trợ 8 ngôn ngữ
