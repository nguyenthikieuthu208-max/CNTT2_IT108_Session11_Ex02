


# Bài 2: Khắc phục sự cố dữ liệu trong kho thiết bị IoT

## Phần 1: Phân tích lỗi

Bảng Excel vi phạm 3 quy tắc vàng:

1.  Không gộp ô (Merge Cell): Hàng tiêu đề bị gộp ô làm AutoFilter hoạt động không chính xác.
    
2.  Không để hàng trống: Hàng trống khiến Filter không áp dụng cho toàn bộ dữ liệu.
    
3.  Dữ liệu phải thống nhất: Cột Trạng thái có khoảng trắng thừa khiến “Hỏng” và “Hỏng ” bị hiểu là hai giá trị khác nhau.
    

## Phần 2: Hoàn thiện dữ liệu

Bước 1: Chọn hàng tiêu đề, vào Home → Merge & Center → Unmerge Cells để bỏ gộp ô.

Bước 2: Xóa các hàng trống trong bảng dữ liệu.

Bước 3: Dùng hàm TRIM để làm sạch cột Trạng thái. Ví dụ, nếu dữ liệu ở ô E2:

```
=TRIM(E2)
```

Kéo công thức xuống các dòng còn lại, sau đó sao chép kết quả và Paste Special → Values vào cột Trạng thái.

Bước 4: Chọn toàn bộ bảng và nhấn `Ctrl + Shift + L` để bật AutoFilter. Lọc trạng thái “Hỏng” để kiểm tra kết quả.
