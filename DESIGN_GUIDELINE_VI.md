# Hướng Dẫn Thiết Kế Giao Diện (UI Design Guidelines)
**Chủ đề: Soft Glassmorphism (Hiệu ứng kính mờ mềm mại) & Pastel**

Tài liệu này đóng vai trò là "kim chỉ nam" (Design System/Guidelines) giúp thiết kế các màn hình, thành phần mới trong ứng dụng một cách nhất quán dựa trên bản concept thiết kế cốt lõi.

---

## 1. Phong Cách Cốt Lõi (Core Aesthetic)
- **Glassmorphism (Hiệu ứng kính mờ):** Các thành phần chức năng nổi (floating) như thanh công cụ phía trên (top toolbar), thanh điều hướng đáy (bottom nav), và popup đều dùng giao diện "kính". Đặc điểm là nền trắng bán trong suốt, kết hợp với hiệu ứng làm mờ nền phía sau (backdrop blur).
- **Mềm mại, Thân thiện (Soft & Friendly):** Bố cục không có cạnh sắc nhọn. Sử dụng nhiều đường bo tròn góc (rounded corners), biểu tượng nét mảnh (thin outline icons), typography nét tròn trịa.
- **Sáng và Pastel (Light & Pastel):** Giao diện giữ ở mức tươi sáng. Tận dụng tối đa sự pha trộn các mảng màu gradient ánh phấn (pastel) để chúng ánh lên ngay bên dưới các lớp kính mờ.

## 2. Màu Sắc (Color Palette)

### 2.1. Màu Nền (Backgrounds)
- **App Background (Nền ứng dụng chính):** Trắng ngà ấm, màu kem nhạt hoặc xám hơi pha vàng (ví dụ: `#F8F7F4`, `#FAF9F6`). Không dùng màu trắng bóc `#FFFFFF` làm nền tổng để tạo cảm giác dịu mắt và ấm áp.
- **Gradient Backgrounds (Mảng màu sắc bên dưới):** Các vùng gradient mờ phía sau dưới giao diện thường dùng cụm màu mộng mơ (Dreamscape) như: xanh lơ (Light baby blue), hồng đào (Pastel pink), tím nhạt (Lilac).

### 2.2. Màu Chữ (Typography Colors)
- **Primary Text (Văn bản chính, Tiêu đề):** Xanh đen thẫm hoặc Xám tro đậm (Slate/Navy) (ví dụ: `#2D3A4B`, `#334155`). Sắc độ này giúp chữ dễ đọc nhưng lại mềm hơn là màu đen kịt `#000000`.
- **Secondary Text (Văn bản phụ, Mô tả nhỏ):** Cùng tông với Primary Text nhưng nhạt hơn (ví dụ: `#64748B`, `#94A3B8`).

### 2.3. Màu Thành Phần (Components & Surfaces)
- **Lớp kính (Glass Layer):** Sử dụng dải màu `rgba(255, 255, 255, 0.4)` đến `rgba(255, 255, 255, 0.7)`.
- **Viền sáng (Light Borders):** Đặc trưng bắt buộc của Glassmorphism là phải có viền trắng mỏng (viền kính sáng) để tách biệt với nền. Kích cỡ `1px solid rgba(255, 255, 255, 0.6)`.
- **Đổ bóng (Shadows):** Đổ bóng lan tỏa xa, nhạt để tạo chiều sâu và độ nảy cho thành phần kính (ví dụ: `0 10px 30px rgba(0, 0, 0, 0.05)`).

## 3. Nghệ Thuật Chữ (Typography)
Dựa theo thông tin trên concept, bộ font đôi (Font pairing) nên áp dụng:
- **Heading / Title Font: `Poiret One`** (hoặc nét tương đương). Dùng riêng cho tiêu đề trang, logo, tên chức năng lớn. Phông chữ hiện đại, mỏng, mang tính nghệ thuật trang trí cao.
- **Body / General UI Font: `Quicksand`** (hoặc Nunito, mã tương đương). Dùng cho mọi văn bản thông thường, nhãn nút, mô tả. Đặc điểm là một phông chữ bo tròn (rounded sans-serif), phù hợp tuyệt đối với tổng thể "soft curve" của thiết kế.

## 4. Hình Khối & Tương Tác (Shapes & UI Components)

### 4.1. Bo Góc (Border Radius)
- **Bo tối đa (Pill-shape):** Thường sử dụng bo góc hình viên thuốc tròn hai đầu (`border-radius: 999px`) cho các biểu tượng/nút trạng thái nhỏ (Ví dụ: opacity, text).
- **Bo góc lớn (Large Radius):** Tối thiểu 24px - 32px cho các panel nổi (floating toolbar nằm ngang, pop-over sticker dọc).

### 4.2. Khối Float Containers (Thanh công cụ, Thanh điều hướng, Popup)
- Không chạm viền thiết bị: Luôn để lại **khoảng trống (margins)** xung quanh để các hộp chứa này có thể "nổi" lên trên nội dung.
- Dùng tổ hợp: `Nền Glass` + `Viền Trắng mỏng` + `Đổ bóng nhẹ`.

### 4.3. Thành Phần Tương Tác (Buttons & Controls)
- **Trạng thái đang chọn (Active/Selected State):** Nút đang active sẽ có nền trắng đặc hoặc rõ hơn rất nhiều (solid white background), có chút đổ bóng nhẹ chìm khiến nút bật hẳn lên khỏi dải kính.
- **Thanh trượt (Slider):**
   - **Rãnh trượt (Track):** Dập chìm xuống tạo rãnh sâu (Inner shadow), màu rãnh tối nhẹ `rgba(0,0,0,0.05)`.
   - **Nút kéo (Thumb):** Rõ khối 3D, tròn nhẵn với đổ bóng drop-shadow đậm ngay sát dưới.

### 4.4. Biểu Tượng (Icons)
- **Phong cách:** Nét vẽ mảnh (Outline styling, xấp xỉ 1 - 1.5px stroke).
- Đồng bộ và nên chọn bộ icon có đầu vuốt bo tròn (rounded caps/joints).

### 4.5. Hiển Thị Hình Ảnh / Nội Dung (Cards & Photos)
- Ảnh được viền khung trắng vuông vức kiểu như ảnh in máy cơ (Polaroid-style photos) và có thể đặt các mảng ảnh xoay xiên lệch nhau (tạo hiệu ứng scrapbook/collage sống động) kèm đổ bóng cho từng lớp ảnh rời.

---

## 5. CSS Styling (Mã Giả Tham Khảo - Code Snippets)

Dưới đây là Code snippet (CSS thuần) tham khảo cho lõi kính mờ (Glasspanel) để tái sử dụng ở bất cứ element nào:

```css
/* Lớp Kính Mờ Định Chuẩn */
.glass-surface {
  background: rgba(255, 255, 255, 0.45);
  /* Hiệu ứng mờ không chịu ảnh hưởng của chữ bên trong */
  backdrop-filter: blur(20px); 
  -webkit-backdrop-filter: blur(20px); /* Hỗ trợ Safari */
  
  /* Viền hắt sáng */
  border: 1px solid rgba(255, 255, 255, 0.8);
  
  /* Độ bo nổi bật */
  border-radius: 32px; 
  
  /* Bắt bóng đổ sâu và mềm để bề mặt kính bứt lên */
  box-shadow: 0 12px 32px rgba(31, 38, 135, 0.07);
}

/* Kiểu chữ hệ thống */
.ui-title {
  font-family: 'Poiret One', cursive;
  color: #2D3A4B;
}

.ui-body {
  font-family: 'Quicksand', sans-serif;
  color: #64748B;
  font-weight: 500;
}
```
