# Máy CNC Wood Router Tự Chế (DIY) với Arduino
Đọc bằng: [**🇺🇸 Tiếng Anh**](./README.md) | [🇻🇳 Tiếng Việt](#)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GRBL Version](https://img.shields.io/badge/GRBL-1.1-green)](https://github.com/gnea/grbl)

Một dự án mã nguồn mở về máy CNC router giá rẻ phục vụ ngành mộc, sử dụng hệ điều hành **Arduino Uno** và firmware **GRBL**. Máy được thiết kế để cắt, khắc và tạo mẫu trên các vật liệu như gỗ, MDF và acrylic.

![home-made-cnc-router](https://github.com/user-attachments/assets/8cbeabe3-ba70-4162-a8bf-8df84fd56445)
> Nguồn: [hackaday.com](https://hackaday.com/2014/06/27/building-a-wood-cnc-router-from-scratch/)

---

## Mục lục
- [Tính năng](#tính-năng)
- [Yêu cầu phần cứng](#yêu-cầu-phần-cứng)
- [Cảnh báo an toàn](#-cảnh-báo-an-toàn)
- [Hướng dẫn bắt đầu](#-hướng-dẫn-bắt-đầu)
- [Cấu trúc thư mục](#cấu-trúc-thư-mục)
- [Giấy phép](#giấy-phép)

---

## Tính năng
- **Firmware GRBL 1.1**: Điều khiển chuyển động độ chính xác cao với quản lý gia tốc.
- **Điều khiển Trục chính (Spindle)**: Trục DC (motor 775) điều khiển bằng xung PWM kèm quạt tản nhiệt.
- **Động cơ bước NEMA 17**: Góc bước 1.8° kết hợp với driver A4988.
- **Công tắc hành trình (Limit Switches)**: Hỗ trợ tự động tìm gốc (auto-homing) và vận hành an toàn.
- **Hỗ trợ G-code**: Tương thích hoàn toàn với các phần mềm CAM tiêu chuẩn công nghiệp.

---

## Yêu cầu phần cứng
| Linh kiện              | Thông số kỹ thuật                      |
|------------------------|----------------------------------------|
| **Bộ điều khiển** | Arduino Uno + CNC Shield V3            |
| **Động cơ bước** | NEMA 17 (1.7A, 12V)                    |
| **Trục chính** | Motor DC 775 (10,000 RPM)              |
| **Nguồn điện** | Nguồn tổ ong 24V 10A                   |
| **Cơ cấu truyền động** | Ray trượt MGN12 + Trục vít me T8       |

---

## ⚠️ Cảnh báo an toàn
- **Bảo vệ mắt:** Luôn đeo kính bảo hộ. Máy CNC tạo ra bụi gỗ và mảnh vụn bắn ra với tốc độ cao.
- **Dừng khẩn cấp:** Phải có nút ngắt nguồn vật lý để dừng máy ngay lập tức khi có sự cố.
- **Quản lý bụi:** Bụi gỗ rất dễ cháy và có hại cho hô hấp. Hãy vận hành ở nơi thông thoáng hoặc có hệ thống hút bụi.
- **Nguy hiểm cơ học:** Tuyệt đối không đưa tay gần trục chính hoặc trục vít me khi máy đang được cấp nguồn.

---

## 🚀 Hướng dẫn bắt đầu
Để lắp đặt máy thành công, vui lòng thực hiện theo đúng thứ tự các hướng dẫn dưới đây:

1. [**Hướng dẫn lắp ráp Phần cứng**](./hardware_VN.md) — Cách ghép nối bo mạch, cắm driver và đấu dây động cơ.
2. [**Thiết lập Phần mềm & Cấu hình**](./software_VN.md) — Cách nạp firmware GRBL và cài đặt phần mềm điều khiển.
3. [**Hiệu chuẩn máy (Calibration)**](#) — *Đang cập nhật.*

---

## Cấu trúc thư mục
- `src/`: Mã nguồn cho bộ điều khiển.
- `docs/`: Tài liệu chi tiết và sơ đồ lắp ráp.
- `gcode_examples/`: Các tệp mẫu để chạy thử máy.

---

## Giấy phép
Dự án này được cấp phép theo **Giấy phép MIT**. Xem tệp [LICENSE](LICENSE) để biết thêm chi tiết.
