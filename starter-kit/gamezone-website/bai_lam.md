# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên:Đào Tuấn Minh** 
- **Lớp:CNTT3** 
- **Link repository:https://github.com/tminhk32-bit/readme** 
- **Hệ điều hành (Windows/macOS):Windows** 

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```Powershell
# PS D:\starter-kit\gamezone-website> Get-ChildItem
# PS D:\starter-kit\gamezone-website> cd ".\cap_nhat.txt" ".\dogs"
# PS D:\starter-kit\gamezone-website> mv cap_nhat.txt /dogs
# PS D:\starter-kit\gamezone-website> mv .\Logo_GameZone.PNG /media
# PS D:\starter-kit\gamezone-website> cp ".\media\Logo_GameZone.PNG" ".\backup"
# PS D:\starter-kit\gamezone-website> rm ".\temp_207.tmp"
# PS D:\starter-kit\gamezone-website> cd logs
# PS D:\starter-kit\gamezone-website\logs> cd ..

```

### Kết quả liệt kê toàn bộ dự án

```

    Directory: D:\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:19 PM                backup
d-----        10/26/2026   1:20 PM                data
d-----        10/26/2026   1:18 PM                docs
d-----        10/26/2026   1:20 PM                logs
d-----        10/26/2026   1:18 PM                media
-a----        10/26/2026   1:16 PM             70 .env
-a----        10/26/2026   1:16 PM             61 cap_nhat.txt
-a----        10/26/2026   1:16 PM           8542 Logo GameZone.PNG
-a----        10/26/2026   1:16 PM             22 temp_207.tmp
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```Powershell
# PS D:\starter-kit\gamezone-website> Get-Content "logs/game.log" | Select-String  "ERROR"

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```
    2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
    2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [] Heading 1
- [] Mô tả in đậm + in nghiêng
- [] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [] Code block lệnh liệt kê
- [] Task list (≥2 việc, ≥1 đã xong)
- [] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```Powershell
# PS D:\starter-kit\gamezone-website> Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
# PS D:\starter-kit\gamezone-website> .\auto_report.ps1
```

### Nội dung file logs/auto_report.txt

```
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```Powershell
# PS D:\starter-kit\gamezone-website> Get-Content -Path "logs/game.log" | Select-String -Pattern "ERROR"
```

### Kết quả đếm

```
6
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```Powershell
# PS D:\starter-kit\gamezone-website> ni .\logs\tong_hop.txt
# PS D:\starter-kit\gamezone-website> Get-Content -Path "logs/game.log" | Select-String -Pattern "WARNING"
# PS D:\starter-kit\gamezone-website> (Get-Content "logs/game.log" | Select-String  "ERROR").Count

```

### Nội dung file logs/tong_hop.txt

```
=== TONG HOP LOG GAMEZONE ===
2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%
6
```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
