# CICFlowMeter (V2)

CICFlowMeter (V2) là một công cụ mã nguồn mở được phát triển bởi Canadian Institute for Cybersecurity, dùng để phân tích lưu lượng mạng. Công cụ này chuyển đổi các tệp PCAP thành định dạng CSV bằng cách tạo ra các luồng hai chiều (bidirectional flows) và trích xuất các đặc trưng thống kê liên quan đến thời gian.

## 🧩 Tính năng nổi bật

- Chuyển đổi tệp `.pcap` thành `.csv` để phục vụ cho mục đích phân tích và học máy.
- Tạo các luồng mạng hai chiều với thông tin phong phú.
- Tính toán hơn 80 đặc trưng lưu lượng như: thời gian giữa các gói, tốc độ truyền tải, entropy, v.v.

---

## 🛠️ Yêu cầu hệ thống

- **Java:** Phiên bản 8 hoặc 11  
  ❌ Không hỗ trợ Java 17 trở lên  
- **Thư viện:**  
  - [`jnetpcap`](https://github.com/slytechs/jnetpcap) (bao gồm `libjnetpcap.so` cho Linux)  
  - [`libpcap`](https://www.tcpdump.org/)

---

## ⬇️ Cài đặt

### Bước 1: Tải mã nguồn

```bash
git clone https://github.com/bqmxnh/CICFlowMeter.git
cd CICFlowMeter
```

### Bước 2: Cài đặt thư viện phụ thuộc
```bash

sudo apt update
sudo apt install libpcap-dev
```
### Bước 3: 
Đảm bảo thư viện jnetpcap nằm trong đường dẫn thư viện hệ thống hoặc chỉ định rõ đường dẫn. Chạy công cụ bằng lệnh sau:

```bash
java -Djava.library.path=/path/to/libjnetpcap -jar path/to/CICFlowMeter.jar ~/path/to/input/ ~/path/to/output/
```
- /path/to/input/: Thư mục chứa các tệp .pcap
- /path/to/output/: Thư mục để lưu các tệp .csv đầu ra

# Tài liệu tham khảo
- CICFlowMeter trên GitHub
- jNetPcap
- Canadian Institute for Cybersecurity
