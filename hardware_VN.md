# Hướng Dẫn Lắp Ráp Phần Cứng (Hardware Guide)

Tài liệu này hướng dẫn cách kết nối các linh kiện vật lý cho máy CNC Router sử dụng Arduino.

## 1. Ghép nối bộ điều khiển (Controller Stack)
Hệ thống sử dụng kiến trúc "shield", trong đó mạch điều khiển động cơ sẽ được cắm trực tiếp lên trên bo mạch xử lý.

* **Căn chỉnh:** Căn thẳng các chân cắm (pins) của **CNC Shield V3** với các khe cắm (headers) trên **Arduino Uno**.
* **Lắp đặt:** Ấn nhẹ nhàng nhưng dứt khoát. Đảm bảo cổng USB và jack nguồn của Arduino khớp với các khoảng trống trên Shield.
* **Cảnh báo:** Kiểm tra kỹ các chân cắm xem có bị cong hay lệch không. Cắm lệch chân có thể gây chập mạch (short circuit) ngay khi cấp nguồn.

## 2. Lắp đặt Driver điều khiển động cơ (Stepper Drivers)
Cắm các module **A4988 hoặc DRV8825** vào các khe cắm màu vàng trên Shield.
* **Hướng cắm (Orientation):** Biến trở nhỏ (vít kim loại) phải hướng về phía **dưới** của board mạch (ngược hướng với các tụ điện).
* **Lưu ý:** Nếu cắm ngược Driver, module sẽ bị cháy ngay lập tức.

## 3. Đấu nối dây và Nguồn điện
* **Động cơ:** Cắm cáp 4 chân của động cơ bước NEMA 17 vào các chân cắm được ký hiệu X, Y, Z.
* **Nguồn điện:** Sử dụng nguồn DC từ **12V đến 24V** nối vào đầu cốt màu xanh (blue screw terminals).
* **Quy tắc an toàn:** Tuyệt đối không cắm hoặc rút dây động cơ khi đang bật nguồn điện.
