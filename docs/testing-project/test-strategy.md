# Chiến lược Kiểm thử (Test Strategy)

Tài liệu này mô tả các phương pháp và kịch bản kiểm thử cho hệ thống IIoT Bearing PdM.

## Các kịch bản kiểm thử (Test Cases)

### 1. Kiểm thử phần cứng (Hardware Testing)
- **TC-HW-01**: Kiểm tra độ chính xác của cảm biến gia tốc so với thiết bị chuẩn.
- **TC-HW-02**: Kiểm tra khả năng chịu nhiệt của ESP32 trong môi trường công nghiệp.
- **TC-HW-03**: Kiểm tra mức tiêu thụ điện năng của node cảm biến.

### 2. Kiểm thử kết nối (Connectivity Testing)
- **TC-CN-01**: Kiểm tra khả năng tự động kết nối lại khi mất tín hiệu Wi-Fi/LoRa.
- **TC-CN-02**: Kiểm tra độ trễ truyền tin từ ESP32 đến Gateway.

### 3. Kiểm thử phần mềm & AI (Software & AI Testing)
- **TC-SW-01**: Kiểm tra độ chính xác của mô hình dự báo RUL.
- **TC-SW-02**: Kiểm tra thời gian phản hồi của Dashboard khi truy vấn dữ liệu lớn.
