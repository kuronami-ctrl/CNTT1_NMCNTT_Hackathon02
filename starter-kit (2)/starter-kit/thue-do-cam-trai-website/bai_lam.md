# BÀI LÀM – HACKATHON 02

- **Mã đề:** 05
- **Họ tên: Nguyễn Bùi Gia Bảo**
- **Lớp: CNTT1**
- **Link repository:**
- **Hệ điều hành (Windows/macOS): Window**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
get-childitem -force
move-item .\quy_dinh_thue.txt .\docs\
mkdir backup
Copy-Item .\data\don_thue_thang_5.xlsx .\backup\
Remove-Item .\temp_505.tmp
cd .\logs
Get-ChildItem -Force
cd ..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Directory: C:\Users\Admin\Downloads\starter-kit (2)\starter-kit\thue-do-cam-trai-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   7:51 AM                backup
d-----        11/11/2026   7:36 AM                data
d-----        11/11/2026   7:49 AM                docs
d-----        11/11/2026   7:34 AM                evidence
d-----        11/11/2026   7:36 AM                logs
d-----         11/3/2026   7:07 AM                web
-a----         11/3/2026   7:07 AM             72 .env
-a----         11/3/2026   7:07 AM           2409 bai_lam.md


    Directory: C:\Users\Admin\Downloads\starter-kit (2)\starter-kit\thue-do-cam-trai-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM           6132 don_thue_thang_5.xlsx


    Directory: C:\Users\Admin\Downloads\starter-kit (2)\starter-kit\thue-do-cam-trai-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM           6132 don_thue_thang_5.xlsx


    Directory: C:\Users\Admin\Downloads\starter-kit (2)\starter-kit\thue-do-cam-trai-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM            159 quy_dinh_thue.txt


    Directory: C:\Users\Admin\Downloads\starter-kit (2)\starter-kit\thue-do-cam-trai-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM            934 Rental.log


    Directory: C:\Users\Admin\Downloads\starter-kit (2)\starter-kit\thue-do-cam-trai-website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         11/3/2026   7:07 AM                images
-a----         11/3/2026   7:07 AM            582 app.js
-a----         11/3/2026   7:07 AM            534 index.html
-a----         11/3/2026   7:07 AM            460 style.css


    Directory: C:\Users\Admin\Downloads\starter-kit (2)\starter-kit\thue-do-cam-trai-website\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   7:07 AM           3090 logo-campgo.png

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
Get-Content .\logs\rental.log | Select-String "status=500"| Set-Content .\logs\loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
Get-Content .\logs\loi_500.txt -TotalCount 2
2026-05-28 08:17:12 POST /api/kho-do status=500
2026-05-28 08:20:23 POST /api/thue-do status=500

```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
 Get-Content .\logs\rental.log | Select-String "status=404" | Measure-Object

```

```text
Count    : 4
Average  :
Sum      :
Maximum  :
Minimum  :
Property :

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
File script: tong_hop.ps1

Tác giả: Sinh viên PTIT

Ngày tạo: 11/11/2026

Lệnh chạy script:

.\tong_hop.ps1

Lệnh xử lý khi máy chặn chạy script:

Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\tong_hop.ps1

```

### Nội dung file logs/tong_hop.txt

```text
(Dán nội dung file vào đây – xoá dòng này)

```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 | Network | logo.png | sửa "logo.png" thành "images/logo-campgo.png" |
| 2 | console | HienThiBangThue | HienThiBangGiaThue() |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_thue_thang_5.xlsx`, không cần ghi vào đây.
