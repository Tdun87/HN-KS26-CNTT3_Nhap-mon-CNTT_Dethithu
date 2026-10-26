# bai_lam

# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên: Nguyễn Tiến Dũng**
- **Lớp: HN-KS26-CNTT3**
- **Link repository:** https://github.com/Tdun87/HN-KS26-CNTT3_Nhap-mon-CNTT_Dethithu
- **Hệ điều hành (Windows/macOS): Windows**

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```bash
pwd
Get-ChildItem -Recurse -Force
mv .\Cap_nhat.txt .\docs\
mv .\Logo_gameZone.PNG .\media\
cp .\media\Logo_gameZone.PNG .\backup\
rm .\temp_207.tmp
cd .\logs\
ls -Force
cd ..
```

### Kết quả liệt kê toàn bộ dự án

```
 Directory: C:\Users\Admin\OneDrive\Đính kèm\de-on-tap-game\starter-kit\gamezone-website

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:15 PM                backup
d-----        10/26/2026   1:16 PM                data
d-----        10/26/2026   1:14 PM                docs
d-----        10/26/2026   1:16 PM                logs
d-----        10/26/2026   1:15 PM                media
-a----        10/26/2026   1:10 PM             70 .env
-a----        10/26/2026   1:10 PM           1437 bai_lam.md
-a----        10/26/2026   1:10 PM             61 Cap_Nhat.txt
-a----        10/26/2026   1:10 PM           8542 Logo_gameZone.PNG
-a----        10/26/2026   1:10 PM             22 temp_207.tmp

    Directory: C:\Users\Admin\OneDrive\Đính kèm\de-on-tap-game\starter-kit\gamezone-website\data

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           5814 Giao_dich_thang_11.xlsx

    Directory: C:\Users\Admin\OneDrive\Đính kèm\de-on-tap-game\starter-kit\gamezone-website\logs

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM            986 Game.log
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```bash
Get-Content .\logs\Game.log | Select-String "ERROR" > .\logs\daily_report.txt
Get-Content .\logs\daily_report.txt -Totalcount 2
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.
> 
- [x]  Heading 1
- [x]  Mô tả in đậm + in nghiêng
- [x]  Bảng `Thư mục | Nội dung` (≥3 dòng)
- [x]  Code block lệnh liệt kê
- [x]  Task list (≥2 việc, ≥1 đã xong)
- [x]  Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```bash
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\auto_report.ps1
```

### Nội dung file logs/auto_report.txt

```
# Tac gia: "Nguyen_Tien_Dung"
# Ngay tao: "26/10/2026"

"=== BAO CAO LOI GAMEZONE ===" > logs\auto_report.txt
Get-Content logs\game.log | Select-String "ERROR" >> logs\auto_report.txt
Write-Host "Da tao bao cao: Thanh Cong!!"
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```bash

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi

```

### Kết quả đếm

```
6
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```bash
"=== TONG HOP LOG GAMEZONE ===" > .\logs\tong_hop.txt
Get-Content .\logs\Game.log | Select-String "Warning" >> .\logs\tong_hop.txt
Get-Content .\logs\Game.log | Select-String "error" >> .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```
=== TONG HOP LOG GAMEZONE ===

2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi

```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
>
