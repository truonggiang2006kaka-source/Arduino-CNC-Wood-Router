# Hardware Assembly Guide

This guide describes the physical connection of the Arduino CNC Router components. 

## 1. The Controller Stack
The system uses a "shield" architecture where the motor controller sits directly on the logic board.

* **Alignment:** Align the male pins of the **CNC Shield V3** with the female headers on the **Arduino Uno**. 
* **Seating:** Press down firmly. Ensure the USB and Power Jack of the Arduino align with the cutouts on the Shield.
* **Warning:** Check for bent pins before pressing. A misaligned pin can cause a short circuit.

## 2. Stepper Driver Installation
Insert the **A4988/DRV8825 drivers** into the yellow sockets.
* **Orientation:** The tiny metal screw (potentiometer) must face the **bottom** of the board (away from the capacitors).
* **Polarity:** Installing a driver backwards will permanently damage both the driver and the shield.

## 3. Wiring & Power
* **Motors:** Connect the 4-pin NEMA 17 cables to the headers labeled X, Y, and Z.
* **Input Power:** Connect a **12V-24V DC** power source to the blue screw terminals. 
* **Safety Rule:** Never connect or disconnect motors while the power supply is active.

 English Term	                   Tiếng Việt (Technical)	Description				
CNC Shield	        Mạch mở rộng điều khiển CNC	Vỉ mạch cắm lên trên Arduino để điều khiển động cơ.				
Stepper Motor	      Động cơ bước	Loại động cơ quay theo từng bước nhỏ, dùng cho độ chính xác cao.				
Stepper Driver	    Module điều khiển động cơ bước	Linh kiện trung gian điều phối dòng điện cho động cơ (A4988).				
Lead Screw	        Trục vít me	Thanh ren dùng để biến chuyển động quay thành chuyển động tịnh tiến.				
Potentiometer	      Biến trở tinh chỉnh	Nút vặn nhỏ trên driver để điều chỉnh dòng điện (Ampe).				
Polarity	          Chiều cực / Phân cực	Thứ tự dây (+) và (-) cần phải chính xác để tránh cháy mạch.				
