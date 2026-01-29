# Raspberry Pi 4

Raspberry Pi 4 đóng vai trò là Gateway trung tâm điều phối dữ liệu trong mạng nội bộ.

![Raspberry Pi 4](../assets/images/raspberry_pi_4.png)

## Technical Specifications

| Feature | Details |
| :--- | :--- |
| **CPU** | Broadcom BCM2711, Quad-core Cortex-A72 (ARM v8) 64-bit SoC @ 1.5GHz |
| **RAM** | 8GB LPDDR4-3200 SDRAM |
| **Storage** | MicroSD card slot (for OS and data) |
| **Wireless** | 2.4 GHz and 5.0 GHz IEEE 802.11ac wireless, Bluetooth 5.0, BLE |
| **Ethernet** | Gigabit Ethernet (Full throughput) |
| **Video** | 2x micro-HDMI ports (up to 4Kp60 supported) |
| **USB** | 2x USB 3.0 ports + 2x USB 2.0 ports |
| **Interfaces** | Standard 40-pin GPIO header, 2-lane MIPI DSI display port, 2-lane MIPI CSI camera port |
| **Multimedia** | H.265 (4kp60 decode), H264 (1080p60 decode, 1080p30 encode), OpenGL ES 3.1, Vulkan |
| **Power** | 5V DC via USB-C (minimum 3A) or PoE (requires separate PoE HAT) |

## Vai trò trong hệ thống
- Chạy MQTT Broker (Mosquitto) để nhận dữ liệu từ các node ESP32.
- Lưu trữ đệm dữ liệu (Local buffering).
- Chạy các thuật toán AI nhẹ để giám sát thời gian thực.
- Chuyển tiếp dữ liệu lên Cloud Server.
