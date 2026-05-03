# LED-Button-Matrix-PCB-22-Button-22-LED-
A custom-designed peripheral PCB featuring a 4x5 grid of tactile buttons paired with 22 high-brightness blue LEDs. This board connects to a main microcontroller via dual FPC connectors (24-pin and 10-pin) and is ideal for creating custom keyboard macros, lighting control panels, or specialized user interfaces.
# 🔴 LED & Button Matrix Interface PCB

![PCB_Preview](images/PCB_Layout.png)

This repository contains the complete hardware design files for a **22-Button and 22-LED matrix interface board**. Built around a grid of tactile switches and vibrant blue LEDs, it functions as a peripheral I/O board intended to be connected to a separate microcontroller board via its FPC connectors.

This is a perfect building block for custom keyboards, macro pads, game controllers, or interactive lighting panels.

---

## ✨ Key Features

*   **22x Tactile Switches:** High-quality 4-pin SMD switches for robust input.
*   **22x High-Brightness Blue LEDs:** Clear visual feedback for any application.
*   **Ergonomic Layout:** Custom PCB shape designed for efficient user interface.
*   **Dual Connector Interface:**
    *   **24-Pin FPC Connector:** Primary I/O for scanning the button matrix and driving the LEDs. 
    *   **10-Pin FPC Connector:** Secondary header for auxiliary power or additional signals (e.g., I2C, UART).
*   **Compact Surface-Mount Design:** Ideal for modern, small-factor implementations.

---

## 📦 Bill of Materials (BOM)

The complete BOM is available in the file [`BOM_LED_PCB_2026-05-03.csv`](BOM_LED_PCB_2026-05-03.csv).

| Component | Designator | Quantity | Description |
<img width="1803" height="1003" alt="Schematic_LED_PCB_2026-05-03" src="https://github.com/user-attachments/assets/cf422f17-9f5b-49c3-925a-c785112823e2" />

| :--- | :--- | :--- | :--- |
<img width="652" height="520" alt="LED_PCB_3D_Top_View" src="https://github.com/user-attachments/assets/6e338c53-000a-4907-be94-6b3826ce70e4" />

| **Blue LED** | LED1-LED22 | 22 | Kingbright KPTD-3216QBC-D |
<img width="682" height="550" alt="LED_PCB_3D_Bottom_View" src="https://github.com/user-attachments/assets/d20a5cb4-6239-4f34-9bae-3112b04cacc2" />

| **Tactile Switch** | SW1-SW22 | 22 | K2-1157SP-I4SW-04 |
<img width="692" height="501" alt="LED_PCB_2D_View" src="https://github.com/user-attachments/assets/7fa6be19-9a35-460d-b5c5-fa0c5a0ba440" />

| **24-Pin FPC** | U3 | 1 | X1311FR-24-C43D24 |

| **10-Pin FPC** | U1 | 1 | HX PM1.0-1X10P ZC |
| **PCB** | - | 1 | Custom Ergonomic Shape |

---

## 🔌 Connectivity & Usage

Since this board is a **peripheral**, it requires a host microcontroller (MCU) to function. The MCU will drive the LED matrix and read the switch states.

*   **Primary Interface:** Connect a 24-pin FPC cable to `U3` to link the board to your main MCU (like an ESP32, Arduino, or STM32). This handles the scanning and driving logic.
*   **Auxiliary Interface:** The 10-pin connector `U1` can be used for dedicated power input, I2C/SPI communication, or other custom signals.
*   **No Onboard MCU:** This board is purely an I/O board—no microcontroller is included.

### Example Functional Diagram:
