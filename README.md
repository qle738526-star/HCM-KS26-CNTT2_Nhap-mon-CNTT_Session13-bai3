# HCM-KS26-CNTT2_Nhap-mon-CNTT_Session13-bai3
**1. Terminal (Chạy 1 dòng trong PowerShell)**

md smartfarm-system\docs, smartfarm-system\scripts, smartfarm-system\data, smartfarm-system\backup; cd smartfarm-system\data; "DB_PASSWORD=demo_123456" > ..\.env; (Get-Item ..\.env).Attributes += 'Hidden'; cd ..



**3. Excel (Sheet `trang-thai-tram`)**

* **E2 (`ma_linh_kien_sach`):** `=TRIM(B2)`
* **F2 (`ten_thiet_bi`):** `=VLOOKUP(E2, 'danh-muc-linh-kien'!$A$2:$D$100, 2, FALSE)`
* *Thao tác:* Kéo công thức xuống, bôi đen hàng 1 nhấn `Ctrl + Shift + L` (AutoFilter), xóa các hàng trống.

**4. File `docs/README.md**`

```markdown
# SmartFarm System Management

## Hướng dẫn chạy script
```powershell
cd scripts
powershell -ExecutionPolicy Bypass -File .\auto_report.ps1

```

## Checklist kiểm tra

* [x] Kiểm tra nguồn điện tủ PLC
* [ ] Kiểm tra kết nối mạng cảm biến
* [ ] Hiệu chuẩn bơm

## Bảng thiết bị

| Thiết bị | Đơn giá | Storage |
| --- | --- | --- |
| Cảm biến ẩm | 350,000 | EEPROM 4KB |
| PLC | 4,500,000 | Flash 512MB |
| Camera | 1,200,000 | MicroSD 64GB |

## Phân tích IPO

* **Input:** `log-he-thong.log`
* **Process:** Lọc lỗi bằng PowerShell `Select-String`
* **Output:** `bao-cao-su-co.txt`

## Phân loại DIKW

* **Data:** (b) 2026-10-12 08:15:01 [ERROR]...
* **Information:** (c) Hôm nay hệ thống ghi nhận 8 sự cố...
* **Knowledge:** (d) Trạm sensor-03 hay mất kết nối...
* **Wisdom:** (a) Quyết định thay modem...

## Thời gian tải file

* Tốc độ: 100 Mbps / 8 = 12.5 MB/s
* Thời gian tải 500 MB: 500 / 12.5 = 40 giây

```

```
