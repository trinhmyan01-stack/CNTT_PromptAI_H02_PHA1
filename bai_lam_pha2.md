# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 04
- **Họ tên:** Trịnh Mỹ An
- **Lớp:** CNTT1
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé xe ra JSON

**KET QUA AI**

[
{
"ma_tuyen": "SGDL",
"ngay_di": "2026-12-22",
"ve_nguoi_lon": 2,
"ve_tre_em": 1,
"loai_cho": "giuong",
"ghi_chu": null
},
{
"ma_tuyen": "SGNT",
"ngay_di": "2027-01-02",
"ve_nguoi_lon": 3,
"ve_tre_em": 0,
"loai_cho": null,
"ghi_chu": "một người đang mang thai 6 tháng"
},
{
"ma_tuyen": "SGCT",
"ngay_di": null,
"ve_nguoi_lon": 4,
"ve_tre_em": 0,
"loai_cho": "ghe",
"ghi_chu": "bà nội đi xe lăn"
}
]

**Link trò chuyện:**

https://share.gemini.google/CmnRIFuueTrp

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

[
{
"nha_xe": "Phương Nam Express",
"tuyen": "SGDL – Sài Gòn – Đà Lạt",
"don_gia_nguoi_lon": 320000,
"buoc_1_gia_ve_nguoi_lon_chua_giam": {
"so_luong": 8,
"thanh_tien": 2560000,
"lap_luan": "8 người lớn x 320.000 đồng = 2.560.000 đồng."
},
"buoc_2_gia_ve_nguoi_lon_sau_giam": {
"ty_le_giam": "5%",
"tien_giam_phan_nguoi_lon": 128000,
"thanh_tien_nguoi_lon_sau_giam": 2432000,
"lap_luan": "Đoàn có 8 người lớn (từ 6 người lớn trở lên) được giảm 5% trên tiền vé (tiền vé người lớn + tiền vé trẻ em). Phần tiền vé người lớn sau khi giảm 5% là 2.560.000 đồng - (5% x 2.560.000 đồng) = 2.432.000 đồng."
},
"buoc_3_gia_ve_tre_em": {
"tre_em_5_den_10_tuoi": {
"so_luong": 3,
"do_tuoi": [6, 7, 9],
"ty_le_gia_ve": "75%",
"don_gia_tre_em": 240000,
"thanh_tien_chua_giam": 720000,
"giam_5_phan_tram": 36000,
"thanh_tien_sau_giam": 684000
},
"tre_duoi_5_tuoi": {
"so_luong": 1,
"do_tuoi": [2],
"don_gia": 0,
"thanh_tien": 0
},
"tong_tien_ve_chua_giam_nguoi_lon_va_tre_em": 3280000,
"tong_tien_giam_5_phan_tram": 164000,
"tong_tien_ve_sau_giam": 3116000,
"lap_luan": "3 trẻ em (6, 7 và 9 tuổi) thuộc nhóm từ 5 đến 10 tuổi, giá mỗi vé bằng 75% x 320.000 đồng = 240.000 đồng; 3 vé chưa giảm là 720.000 đồng. Bé 2 tuổi dưới 5 tuổi ngồi cùng người lớn miễn phí (0 đồng). Tổng tiền vé người lớn và trẻ em chưa giảm là 2.560.000 đồng + 720.000 đồng = 3.280.000 đồng; giảm 5% là 164.000 đồng; tiền vé sau giảm là 3.116.000 đồng."
},
"buoc_4_phu_thu_hanh_ly_cong_kenh": {
"so_kien": 2,
"don_gia_phu_thu": 100000,
"thanh_tien": 200000,
"lap_luan": "2 kiện hành lý cồng kềnh x 100.000 đồng/kiện = 200.000 đồng; phụ thu không được giảm giá."
},
"buoc_5_tong_tien": {
"tien_ve_sau_giam": 3116000,
"tien_phu_thu_hanh_ly_cong_kenh": 200000,
"tong_tien": 3316000,
"lap_luan": "Tổng tiền = 3.116.000 đồng + 200.000 đồng = 3.316.000 đồng."
}
}
]

**Link trò chuyện:**

https://share.gemini.google/ZyD82SwRKP0C

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

[
  {
    "tram_1": {
      "loai_su_co": "sai_loai_xe",
      "so_khach": 3,
      "so_chang_bi_doi": 2,
      "tom_tat": "Khách đặt xe giường nằm tuyến Sài Gòn - Đà Lạt nhưng bị đổi sang ghế ngồi cả 2 chặng cho 3 người."
    },
    "tram_2": {
      "loai_su_co": "sai_loai_xe",
      "muc_den_bu": 720000,
      "can_duyet": true
    },
    "tram_3": {
      "email_phan_hoi": "Kính gửi Quý khách,\n\nNhà xe Phương Nam Express chân thành xin lỗi Quý khách về trải nghiệm không mong muốn trong chuyến đi tuyến Sài Gòn – Đà Lạt ngày 01/11/2026 và 04/11/2026 khi xe giường nằm bị đổi sang xe ghế ngồi ở cả hai chặng.\n\nTheo chính sách đền bù của nhà xe, chúng tôi xin gửi đến Quý khách mức hoàn tiền là 720.000 đồng (120.000 đồng/khách/chặng cho 3 khách và 2 chặng bị đổi). Hiện yêu cầu đền bù này đang được chuyển đến Trưởng phòng điều hành phê duyệt theo quy định. Bộ phận Chăm sóc khách hàng sẽ liên hệ lại với Quý khách ngay sau khi hoàn tất thủ tục.\n\nCảm ơn Quý khách đã ghi nhận sự tận tâm của tài xế. Rất mong nhận được sự thông cảm từ Quý khách.\n\nTrân trọng,\nBộ phận Chăm sóc khách hàng - Phương Nam Express"
    }
  }
]

**Link trò chuyện:**

https://share.gemini.google/KV02nxS5m4Ho

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

[
  {
    "diem_dung_thong_tin": 0,
    "diem_day_du": 1.5,
    "diem_giong_dieu": 0.5,
    "tong_diem": 2.0,
    "nhan_xet": "Sai giá vé (báo 350.000đ thay vì 380.000 đồng/vé người lớn) và sai chính sách đổi vé (báo đổi trước 12 tiếng miễn phí thay vì đổi từ 6 đến dưới 24 giờ mất phí 20% giá vé). Trả lời đủ hai câu hỏi của khách nhưng thiếu mời khách cung cấp ngày đi, số vé để đặt chỗ. Giọng điệu chưa chuyên nghiệp, dùng từ ngữ suồng sã ('nha chị', 'xịn lắm luôn', 'nhắn em liền')."
  }
]

**Link trò chuyện:**

https://share.gemini.google/IMR7DIHXmG4l
