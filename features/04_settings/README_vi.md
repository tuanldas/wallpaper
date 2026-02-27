# Settings (Cài đặt)

## Mô tả
Trang Settings cung cấp các tùy chọn cấu hình cơ bản cho ứng dụng DIY Wallpaper Maker Collage. Trang này đơn giản, tập trung vào ngôn ngữ, pháp lý và chia sẻ app.

## Vị trí truy cập
Home > Icon Settings (gear icon ở góc phải trên, bên cạnh "My Gallery")

## UI/UX Design
- **Layout**: Danh sách dọc (vertical list) các mục cài đặt
- **Background**: Gradient pastel (hồng, xanh, tím nhạt) giống toàn app
- **Header**: "Setting" với nút Back (arrow hồng trong vòng tròn)
- **Các mục**: Thẻ (card) trắng bo góc với icon bên trái và text
- **Không có ad** trên trang Settings (một trong số ít màn hình không có quảng cáo)

## Các mục cài đặt

### 1. Language (Ngôn ngữ)
- **Icon**: Globe icon
- Mở trang chọn ngôn ngữ với danh sách 19 ngôn ngữ:
  - English (mặc định), Francais, Marathi (India), Espanol, Chinese, Portugues (Portugal), Russkiy, Indonesian, Philippines, Bangla, Portugues (Brazil), Afrikaans, Deutsch, Canada, English (UK), Korean, Dutch, Vietnamese
- Mỗi ngôn ngữ hiển thị cờ quốc gia tương ứng
- Ngôn ngữ đang chọn có tick đỏ
- Xác nhận bằng nút checkmark (hồng) ở góc phải trên
- Trang này cũng chính là màn hình đầu tiên trong onboarding flow
- **Có banner ad** ở cuối trang Languages (CapCut/Pangle)

### 2. Term of Service (Điều khoản dịch vụ)
- **Icon**: Document icon
- Mở trang web (Chrome) tại sites.google.com
- **Nội dung chính**:
  - Effective Date: Jan 12, 2026
  - App Name: DIY Wallpaper
  - Company: LeafMotion Software
  - Contact: buihieu2568@gmail.com
  - 10 sections: Acceptance of Terms, Eligibility (13+), Use of the App (entertainment only), Permissions, Intellectual Property, Disclaimer, Limitation of Liability, Termination, Changes to Terms, Contact Us
  - Permissions được liệt kê: INTERNET, ACCESS_NETWORK_STATE, CAMERA, VIBRATE, POST_NOTIFICATIONS

### 3. Privacy Policy (Chính sách bảo mật)
- **Icon**: Clock/info icon
- Mở trang web (Chrome) tại sites.google.com
- **Nội dung chính**:
  - Effective Date: Jan 28, 2026
  - App không yêu cầu đăng ký cá nhân, thông tin danh tính, hoặc dữ liệu giao tiếp thực
  - Thu thập: Device model, OS, app version, anonymous analytics
  - CAMERA: "no video or image data is stored or transmitted"
  - **Advertising**: Sử dụng third-party advertising (AdMob), anonymous identifiers
  - Children's Privacy: Không hướng đến trẻ dưới 13
  - Quyền người dùng: Xóa app để dừng thu thập dữ liệu, opt out personalized ads

### 4. Rating 5 Stars (Đánh giá 5 sao)
- **Icon**: Star rating icon
- Hiển thị **in-app rating dialog** (không redirect Play Store ngay):
  - Title: "Hey, can I ask you?"
  - Subtitle: "How is the experience of our app?"
  - 5 ngôi sao để chọn
  - Nút "Rate Us" (màu hồng)
  - Có thể dismiss bằng nút Back

### 5. Share with Friend (Chia sẻ với bạn bè)
- **Icon**: Share icon
- Mở **Android Share Sheet** gốc với link Google Play Store:
  - URL: `https://play.google.com/store/apps/details?id=com.diy.wallpaper.maker.collage`
  - Các tùy chọn chia sẻ: Quick Share, Chrome, Drive, Messages...

## Luồng hoạt động (Flow)
1. Từ Home, tap gear icon ở góc phải trên
2. Trang Settings hiển thị 5 mục
3. Tap từng mục để truy cập tính năng tương ứng
4. Nút Back (arrow hồng) để quay lại Settings hoặc Home

## Onboarding Flow
App có onboarding 3 bước khi lần đầu mở:
1. **Chọn ngôn ngữ** (Languages) - Cũng là màn hình trong Settings > Language
2. **Giới thiệu 1**: "1000+ Unique Wallpaper - Find endless styles to spark your creativity" + nút Next
3. **Giới thiệu 2**: "Design your own wallpaper - Use background, sticker, color, text... to create your style" + nút Next
4. **Chọn sở thích**: "Let select your interest - Please pick one or more to proceed" với 11 danh mục:
   - For you, DIY, Love, Live, Lock Screen, Kawaii, Aesthetic, Quote, Famous, Car, Anime
   - Nút "Get Started"
- **Quảng cáo Pangle** hiển thị ở cuối màn hình trong suốt onboarding

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/01_home_screen.png | Quảng cáo Pangle toàn màn hình khi mở app |
| screenshots/02_after_ad_close.png | Màn hình chọn ngôn ngữ (onboarding) |
| screenshots/07_onboarding2.png | Onboarding screen 2 - Giới thiệu tính năng |
| screenshots/08_onboarding3.png | Onboarding screen 3 - Chọn sở thích |
| screenshots/09_home_screen.png | Home screen sau onboarding |
| screenshots/10_settings_screen.png | Trang Settings chính |
| screenshots/11_language_from_settings.png | Trang Languages từ Settings |
| screenshots/12_term_of_service.png | Trang Terms of Service (Chrome) |
| screenshots/14_chrome_tos_page.png | Nội dung Terms of Service |
| screenshots/19_privacy_policy.png | Nội dung Privacy Policy |
| screenshots/24_rating.png | Dialog Rating 5 stars |
| screenshots/25_share.png | Android Share Sheet |
| screenshots/26_filter_dropdown.png | Filter dropdown (All / Favorite) |

## Ghi chú
- App thuộc công ty **LeafMotion Software**
- Contact email: buihieu2568@gmail.com
- App yêu cầu tối thiểu 13 tuổi
- Không có tính năng Account/Profile/Login
- Không có tính năng Notifications settings trong Settings
- Không có tính năng Dark mode
- Settings rất đơn giản, ít tùy chọn tùy chỉnh
