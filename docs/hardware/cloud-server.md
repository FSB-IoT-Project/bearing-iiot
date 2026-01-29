# Cloud Server

Cloud Server là nơi xử lý trung tâm, lưu trữ dữ liệu lớn và chạy các mô hình dự báo phức tạp.

## Thành phần hệ thống
- **Database**: InfluxDB (Time-series) & PostgreSQL.
- **Backend**: Python (FastAPI/Flask) hoặc Node.js.
- **AI Engine**: Chạy các mô hình Deep Learning để dự báo RUL.
- **Visualization**: Dashboard (Grafana hoặc React/Next.js).

## Vai trò trong hệ thống
- Lưu trữ dữ liệu lịch sử dài hạn.
- Phân tích xu hướng và đưa ra cảnh báo bảo trì dự báo.
- Cung cấp giao diện Web và Mobile cho người dùng cuối.
