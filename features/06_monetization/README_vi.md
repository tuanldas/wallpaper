# Monetization (Kiếm tiền)

## Mô tả
App "DIY Wallpaper Maker Collage" sử dụng mô hình **quảng cáo (ad-supported)** làm nguồn thu nhập chính. Không có subscription hoặc in-app purchases. Quảng cáo xuất hiện ở hầu hết mọi màn hình và mọi bước chuyển đổi (transition) trong app.

## Mô hình kiếm tiền
- **100% ad-supported** (hỗ trợ bởi quảng cáo)
- **Không có** gói subscription/premium
- **Không có** in-app purchases (IAP)
- **Không có** paywall - tất cả tính năng đều miễn phí nhưng phải xem quảng cáo

## Các loại quảng cáo

### 1. Banner Ads (Quảng cáo banner)
- **Vị trí**: Cuối màn hình (bottom), chiếm khoảng 15-20% màn hình
- **Xuất hiện tại**: Hầu hết mọi màn hình - Home, Languages, Preview, Set Wallpaper, My Gallery
- **Nhà cung cấp**: Pangle (TikTok Ads), CapCut, TikTok Lite
- **Format**: Banner ngang với logo, tên app, và nút "View now" / "Download" / "Xem ngay"
- **Có thể click**: Có - redirect đến Play Store hoặc website nhà quảng cáo
- **Đặc biệt**: Một số banner có video (NativeVideoTsView)

### 2. Interstitial Ads (Quảng cáo toàn màn hình)
- **Thời điểm xuất hiện**:
  - Khi mở app lần đầu (trước onboarding)
  - Khi tap vào wallpaper để xem preview
  - Khi chuyển từ Preview sang Edit
  - Khi chuyển từ Edit sang Set Wallpaper
- **Format**: Video toàn màn hình
- **Thời lượng**: Video 5-30 giây, có nút "Skip after Xs" sau vài giây
- **Nút đóng**: "Ad closed" (X) xuất hiện ở góc phải trên sau khi hết thời gian skip
- **Nhà cung cấp**: Pangle (CapCut ads, TikTok Lite ads)
- **Tần suất**: Rất cao - mọi bước chuyển màn hình chính đều có

### 3. Rewarded Ads (Quảng cáo thưởng)
- **Thời điểm xuất hiện**: Khi người dùng muốn lưu/set wallpaper
- **Flow**:
  1. Sau khi edit wallpaper, tap Next
  2. Dialog "Get this item" xuất hiện với nhân vật 3D
  3. Hai tùy chọn:
     - **"Watch now"** (nút hồng) - Xem quảng cáo để nhận wallpaper
     - **"No, thanks"** (nút viền hồng) - Từ chối (không lưu được)
  4. Rewarded video ad chạy (~15-20 giây)
  5. Có bộ đếm ngược (countdown) ở góc phải trên (VD: "19s")
  6. Sau khi xem hết -> nút "Ad closed" xuất hiện -> wallpaper được unlock
- **Bắt buộc**: Phải xem rewarded ad để lưu bất kỳ wallpaper nào
- **Nhà cung cấp**: Pangle (CapCut, TikTok ads)

### 4. Native Ads (Quảng cáo tự nhiên)
- **Vị trí**: Xen kẽ trong danh sách ngôn ngữ, trong wallpaper grid
- **Format**: Tích hợp vào UI của app, trông giống nội dung thường
- **Nhà cung cấp**: Pangle

## Nhà cung cấp quảng cáo
| Nhà cung cấp | Loại ad | Ghi chú |
|-------------|---------|---------|
| **Pangle** (TikTok for Business) | Banner, Interstitial, Rewarded, Native | Nhà cung cấp chính |
| **AdMob** (Google) | Được đề cập trong Privacy Policy | Có thể sử dụng mediation |

## Vị trí quảng cáo chi tiết

| Màn hình | Loại ad | Ghi chú |
|----------|---------|---------|
| App launch | Interstitial (full screen) | Quảng cáo ngay khi mở app |
| Onboarding (Languages) | Banner (bottom) | CapCut/Pangle banner |
| Onboarding (Intro slides) | Banner (bottom) | Pangle banner |
| Home Screen | Banner (bottom) | CapCut/TikTok Lite banner |
| Wallpaper tap | Interstitial (video) | Trước khi xem preview |
| Preview Screen | Banner (bottom) | TikTok Lite/Pangle |
| Preview -> Edit | Interstitial (video) | Chuyển màn hình |
| Edit -> Save | Rewarded dialog | "Get this item" - bắt buộc xem ad |
| Set Wallpaper Screen | Banner (bottom) | Pangle/CapCut |
| My Gallery | Banner (bottom) | TikTok Lite |
| **Settings** | **Không có ad** | Màn hình duy nhất không có quảng cáo |

## Trải nghiệm người dùng với quảng cáo
- **Số lượng ad rất cao**: Trung bình 4-5 quảng cáo cho một flow đơn giản (xem và lưu 1 wallpaper)
- **Ad xuất hiện ở mọi transition**: Mỗi lần chuyển màn hình đều có thể có interstitial ad
- **Rewarded ad bắt buộc**: Không thể lưu wallpaper mà không xem ad
- **Banner luôn hiện**: Chiếm không gian ở cuối màn hình, đôi khi che nội dung quan trọng
- **Chỉ Settings không có ad**: Là màn hình duy nhất "sạch" quảng cáo

## Thông tin từ Privacy Policy & ToS
- App có thể sử dụng **AdMob** và **Pangle** để hiển thị quảng cáo
- Sử dụng **anonymous identifiers** (advertising IDs) để quảng cáo relevance
- Người dùng có thể **opt out personalized ads** qua device settings
- Không thu thập personal data cho mục đích quảng cáo

## Screenshots
| Screenshot | Mô tả |
|-----------|-------|
| screenshots/01_interstitial_ad.png | Interstitial video ad (CapCut via Pangle) |
| screenshots/02_rewarded_ad.png | Rewarded video ad với countdown 19s |

## Ghi chú
- App **không có subscription model** - hoàn toàn miễn phí với quảng cáo
- **Không có** nút "Remove ads" hay "Go Premium"
- **Không có** in-app purchases nào
- Pangle (TikTok for Business) là ad network chính, không phải Google AdMob trực tiếp
- Quảng cáo chủ yếu là **test ads** (Pangle Test Ads) trên emulator - trên thiết bị thực có thể khác
- Mô hình monetization hoàn toàn dựa vào **ad revenue** và **rewarded video ads**
- Tần suất quảng cáo có thể gây khó chịu cho người dùng (trải nghiệm bị gián đoạn nhiều)
