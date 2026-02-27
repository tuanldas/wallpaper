# Onboarding Flow (Luồng giới thiệu)

## Mô tả
Onboarding flow xuất hiện khi người dùng mở app lần đầu (hoặc sau khi clear data). Flow bao gồm 4 bước: App Open Ad -> Chọn ngôn ngữ -> Giới thiệu tính năng (2 slides) -> Chọn sở thích. Sau khi hoàn tất, người dùng được đưa đến Home screen.

## Vị trí truy cập
- Tự động xuất hiện khi lần đầu mở app
- Không thể quay lại onboarding từ trong app (trừ khi clear data)
- Phần "Language" có thể truy cập lại từ Settings > Language

## Luồng hoạt động (Flow)

### Bước 0: App Open Ad
- **Loại**: Interstitial/App Open Ad (toàn màn hình)
- **Nhà cung cấp**: Google AdMob (Test Ad)
- **Format**: Video quảng cáo sản phẩm (skincare, etc.)
- **Thời gian**: Có countdown (VD: "2" giây), sau đó nút "Close" xuất hiện
- **Nút Close**: Ở góc trái dưới với checkmark xanh
- **Bắt buộc**: Phải đợi hết countdown mới đóng được

### Bước 1: Chọn ngôn ngữ (Languages)
- **Title**: "Languages"
- **Layout**: Danh sách dọc các ngôn ngữ, mỗi dòng có:
  - Cờ quốc gia (tròn)
  - Tên ngôn ngữ
  - Radio button ở bên phải (hồng khi được chọn)
- **Background**: Gradient pastel (hồng, xanh, tím)
- **19 ngôn ngữ hỗ trợ**:
  1. English
  2. Francais (Pháp)
  3. Marathi - India
  4. Espanol (Tây Ban Nha)
  5. Chinese (Trung Quốc)
  6. Portugues - Portugal (Bồ Đào Nha)
  7. Russkiy (Nga)
  8. Indonesian
  9. Philippines
  10. Bangla (Bangladesh)
  11. Portugues - Brazil
  12. Afrikaans (Nam Phi)
  13. Deutsch (Đức)
  14. Canada
  15. English (UK)
  16. Korean (Hàn Quốc)
  17. Dutch (Hà Lan) - *ghi là "Ducth" trong app (lỗi chính tả)*
  18. Vietnamese (Việt Nam)
- **Ngôn ngữ mặc định**: English (US) - tự động chọn khi mở
- **Xác nhận**: Tap checkmark (hồng) ở góc phải trên header
- **Ad**: Banner ad (TikTok/Pangle) ở cuối màn hình

### Bước 2: Giới thiệu - Slide 1
- **Hình ảnh**: Montage các mẫu wallpaper (collage, aesthetic, birthday...)
- **Title** (hồng): "1000+ Unique Wallpaper"
- **Subtitle**: "Find endless styles to spark your creativity."
- **Dot indicators**: 2 dots (dot 1 active - hồng)
- **Nút**: "Next" (gradient hồng, full width)
- **Ad**: Banner ad Pangle ở cuối

### Bước 3: Giới thiệu - Slide 2
- **Hình ảnh**: Giao diện editor với các tool (BG, Import, Text, Sticker) và sticker ngôi sao
- **Title** (hồng): "Design your own wallpaper"
- **Subtitle**: "Use background, sticker, color, text... to create your style."
- **Dot indicators**: 2 dots (dot 2 active - hồng)
- **Nút**: "Next" (gradient hồng, full width)
- **Ad**: Banner ad Pangle ở cuối

### Bước 4: Chọn sở thích (Interest Selection)
- **Title** (hồng): "Let select your interest"
- **Subtitle**: "Please pick one or more to proceed"
- **Layout**: Grid 3 cột x 4 hàng (11 categories)
- **Categories** (mỗi category có hình minh họa tròn và tên):
  | Category | Mô tả |
  |----------|-------|
  | For you | Galaxy/Space theme |
  | DIY | Craft/Handmade theme |
  | Love | Heart/Romance theme |
  | Live | Gradient pastel theme |
  | Lock Screen | Moon/Night theme |
  | Kawaii | Cute/Cupcake theme |
  | Aesthetic | Butterfly/Nature theme |
  | Quote | Flamingo/Text theme |
  | Famous | Celebrity theme (Taylor Swift) |
  | Car | Vehicle theme |
  | Anime | Manga/Anime character theme |
- **Chọn**: Tap vào card -> viền hồng + checkmark đỏ ở góc trên phải
- **Có thể chọn nhiều**: "pick one or more"
- **Nút**: "Get Started" (gradient hồng, full width)
- **Không có ad** trên màn hình này

### Kết thúc: Home Screen
- Sau khi tap "Get Started", app chuyển đến Home screen
- Category tab đầu tiên ("For you") được chọn mặc định
- Wallpaper grid hiển thị theo sở thích đã chọn

## UI/UX Design
- **Theme nhất quán**: Gradient pastel (hồng, xanh, tím) xuyên suốt
- **Font**: Rounded, modern
- **Màu chính**: Hồng (#FF1493 - deep pink) cho title, button, highlight
- **Dot indicators**: Nhỏ, ở giữa, cho biết đang ở slide nào
- **Button style**: Full-width, gradient hồng -> đỏ, bo tròn
- **Ad placement**: Banner ở cuối màn hình (trừ interest selection)
- **Không có** nút Skip ở bất kỳ bước nào (trừ ad)
- **Không có** nút Back giữa các slides (chỉ có thể đi tới)

## Lỗi chính tả phát hiện
- "Ducth" -> đúng là "Dutch"
- "Let select your interest" -> đúng là "Let's select your interest"
- "Espanol" -> đúng là "Espanol" (có thể thiếu dấu ngữ)

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/01_app_open_fresh.png | App Open Ad khi mở app lần đầu |
| screenshots/02_language_fresh.png | Màn hình chọn ngôn ngữ |
| screenshots/03_intro_slide1_fresh.png | Intro slide 1 - 1000+ Unique Wallpaper |
| screenshots/04_intro_slide2_fresh.png | Intro slide 2 - Design your own wallpaper |
| screenshots/05_interest_fresh.png | Màn hình chọn sở thích (chưa chọn) |
| screenshots/06_interest_selected.png | Màn hình chọn sở thích (đã chọn For you + Anime) |
| screenshots/07_notification_permission.png | Home screen sau onboarding |

## Ghi chú
- Onboarding **không thể bỏ qua** - phải đi qua tất cả các bước
- Không có đăng nhập/đăng ký tài khoản trong onboarding
- Sở thích đã chọn ảnh hưởng đến nội dung wallpaper hiển thị trên Home
- App Open Ad xuất hiện **trước** onboarding (ngay khi mở app)
- Nếu chưa chọn ngôn ngữ nào, English được chọn mặc định (có fingerprint icon)
- Onboarding chỉ xuất hiện 1 lần duy nhất (trừ khi clear data)
