# Hướng Dẫn Cấu Hình Phần Mềm (Software Guide)

Tài liệu này hướng dẫn cách nạp firmware GRBL vào Arduino Uno và cài đặt phần mềm điều khiển trên máy tính.

## 1. Thiết lập Arduino IDE
Để nạp code cho máy, bạn cần môi trường lập trình Arduino.
* **Tải về:** Cài đặt [Arduino IDE v2.x](https://www.arduino.cc/en/software).
* **Thêm thư viện GRBL:** 1. Tải file [GRBL 1.1 ZIP](https://github.com/gnea/grbl/archive/master.zip).
    2. Trong Arduino IDE, chọn **Sketch** > **Include Library** > **Add .ZIP Library**.
    3. Chọn tệp `grbl-master.zip` vừa tải về.

## 2. Nạp Firmware (Flashing)
"Nạp firmware" là quá trình cài đặt "hệ điều hành" cho máy CNC vào bo mạch Arduino.
1. Kết nối Arduino Uno với máy tính qua cổng USB.
2. Trong IDE, vào **File** > **Examples** > **grbl** > **grblUpload**.
3. Chọn đúng Board là **Arduino Uno** và chọn đúng **Cổng (Port)** đang kết nối.
4. Nhấn nút **Upload** (mũi tên hướng sang phải).
5. Đợi đến khi hiện thông báo **"Done uploading"**.

## 3. Cài đặt phần mềm điều khiển (G-Code Sender)
Sau khi nạp code, bạn cần một giao diện để ra lệnh cho máy chạy.
* **Khuyến nghị:** Sử dụng [Universal Gcode Sender (UGS)](https://winder.github.io/ugs_website/).
* **Kết nối:** Mở UGS, chọn đúng cổng COM của Arduino, đặt tốc độ **Baud rate là 115200** và nhấn **Connect**.

---

## 📖 Từ điển phần mềm
| Thuật ngữ | Ý nghĩa |
| :--- | :--- |
| **Flash / Upload** | Quá trình đẩy dữ liệu từ máy tính xuống vi điều khiển. |
| **Baud rate** | Tốc độ truyền dữ liệu (phải khớp giữa máy tính và Arduino). |
| **G-Code** | Ngôn ngữ lệnh để máy hiểu phải di chuyển đi đâu, làm gì. |
| **Firmware** | Phần mềm cố định trong phần cứng để điều khiển thiết bị. |
