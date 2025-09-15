# 📸 Camera Snapshot, AI & Notifications  
*Blueprint cho Home Assistant*

## 🚀 Giới thiệu  
Blueprint này cho phép **chụp ảnh từ camera**, **phân tích bằng AI**, và **gửi thông báo đa nền tảng** (Mobile App, Telegram, Zalo, Discord, TTS ra loa) khi cảm biến chuyển động hoặc hiện diện được kích hoạt.  

- **Phiên bản**: `v2025.08.30`  
- **Tác giả**: [Khaisilk1910 - Nguyễn Tiến Khải](https://github.com/khaisilk1910)  

---

## ⚡ Tính năng chính
- Tự động chụp ảnh khi có **motion, presence, hoặc cửa mở**.  
- Phân tích ảnh bằng AI: chỉ gửi thông báo khi phát hiện **có người**.  
- Hỗ trợ nhiều kênh thông báo:  
  - 📱 **Mobile App Home Assistant** (Android/iOS)  
  - 💬 **Zalo Bot**  
  - 📢 **Telegram**  
  - 🎮 **Discord**  
  - 🔊 **Text-to-Speech ra loa**  
- Tùy chọn **Actions** ngay trên thông báo để xác nhận hoặc hủy bỏ.  
- Lưu ảnh chụp vào thư mục **media** hoặc **www/local**.  
- Có thể thêm **Custom Actions** và **Global Conditions**.  

---

## 🛠️ Cấu hình yêu cầu
- Home Assistant (>= 2025.x)  
- Ít nhất một **cảm biến kích hoạt**:  
  - `binary_sensor.motion`  
  - `binary_sensor.occupancy`  
  - `binary_sensor.door`  
- Một hoặc nhiều **camera** (`camera.*`)  
- Các integration tùy chọn:  
  - [Zalo Bot](https://github.com/smarthomeblack/zalo_bot)  
  - [Telegram Bot](https://www.home-assistant.io/integrations/telegram_bot/)  
  - [Discord Notify](https://www.home-assistant.io/integrations/discord/)  
  - [TTS](https://www.home-assistant.io/integrations/tts/)  

---

## ⚙️ Cài đặt
1. Sao chép file YAML này vào thư mục **blueprints/automation/** trong Home Assistant.  
2. Trong Home Assistant, vào **Automation & Scenes → Blueprints → Import** và chọn file.  
3. Cấu hình:  
   - Chọn **cảm biến kích hoạt**.  
   - Chọn **camera**.  
   - Chọn nơi lưu ảnh (**media** hoặc **www**).  
   - Bật hoặc tắt các tuỳ chọn thông báo (Mobile, Zalo, Telegram, Discord, TTS).  
   - Tùy chỉnh AI Prompt nếu muốn.  

---

## 🔧 Các tùy chọn chính
- **Mobile App Notify**: Gửi thông báo với tiêu đề, màu sắc, icon, và ảnh snapshot.  
- **Actions Settings**: Thêm nút Confirm/Dismiss ngay trên thông báo.  
- **Zalo/Telegram/Discord**: Gửi ảnh và kết quả AI tới các nền tảng chat.  
- **Speakers (TTS)**: Đọc nội dung thông báo ra loa với âm lượng tùy chỉnh.  
- **AI Prompt**: Định nghĩa câu lệnh gửi tới AI để phân tích hình ảnh.  
- **Custom Actions**: Thực hiện thêm hành động tuỳ chỉnh sau khi có kết quả.  
- **Global Conditions**: Chỉ chạy automation khi thỏa điều kiện.  

---

## 📌 Ví dụ kịch bản
- Khi phát hiện **chuyển động**, camera chụp 3 ảnh, AI phân tích và gửi kết quả:  
  - Nếu có người:  
    - Gửi thông báo lên điện thoại kèm ảnh snapshot.  
    - Đẩy tin nhắn vào nhóm Telegram.  
    - Đọc thông báo ra loa Google Mini.  
  - Nếu không có người: **Không gửi thông báo**.  

---

## 📷 Demo
<img width="1080" height="2400" alt="image" src="https://github.com/user-attachments/assets/83ed0451-b896-4a7c-a607-61c523f47c2c" />

<img width="1082" height="937" alt="image" src="https://github.com/user-attachments/assets/05392bdb-4cbf-4550-959c-8d8368ed8b72" />

<img width="1054" height="883" alt="image" src="https://github.com/user-attachments/assets/3e146d8f-01fb-4419-b3d7-52d62344c61d" />




---

