Markdown
# Bài Thực Hành Kiểm Định Chất Lượng Dữ Liệu Với Great Expectations (GX)

Tài liệu này hướng dẫn các bước thiết lập môi trường và thực thi kiểm định chất lượng dữ liệu trên tệp dữ liệu giao dịch bẩn (`dirty_transactions.csv`) bằng thư viện **Great Expectations (GX)**.

---

## 📌 Mục Tiêu Bài Lab
* Hiểu và áp dụng **6 Tiêu chí Chất lượng Dữ liệu (6 Dimensions of Data Quality)** vào thực tế.
* Thành thục cách cài đặt, khởi tạo và viết luật kiểm định bằng **Great Expectations (GX)**.
* Đọc và phân tích báo cáo chất lượng dữ liệu trực quan qua giao diện **Data Docs**.

---

## Bước 1: Chuẩn Bị Thư Mục Và Môi Trường Ảo

Để tránh xung đột thư viện trên máy tính cá nhân, thực hiện tạo một không gian làm việc độc lập theo các lệnh dưới đây:

Tạo thư mục dự án
Mở Terminal (hoặc CMD/PowerShell) và chạy cú pháp:
```bash
mkdir datahub-gx-lab
cd datahub-gx-lab
```

## Bước 2: Khởi tạo môi trường ảo Python
Khuyến nghị: Sử dụng phiên bản Python từ 3.8 đến 3.10.

Trên macOS / Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

Trên Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

## Bước 3: Thêm Dữ Liệu Và Cài Đặt Thư Viện
1. Chuẩn bị file dữ liệu bẩn
Kiểm tra file dirty_transactions.csv trong đường dẫn repository

2. Cài đặt Great Expectations
Thực hiện nâng cấp bộ quản lý gói pip và cài đặt thư viện kiểm định:

```bash
pip install --upgrade pip
pip install great_expectations pandas
```

## Bước 4: Khởi Tạo GX Project
Tạo file Python script, sử dụng package great_expectations
```bash
import great_expectations as gx
import os
...
```
