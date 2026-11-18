# Xây dựng chiến dịch truyền thông tuyển sinh khóa Python bằng Prompt Chaining

## 1. Sơ đồ chuỗi prompt

```
[THÔNG TIN KHÓA HỌC] -> P1 Chân dung -> P2 Thông điệp -> P3 Lịch 7 ngày -> P4 Bài viết + kịch bản -> P5 Kiểm tra
```

Mỗi prompt nhận kết quả của prompt trước. Thông tin khóa học dán nguyên vào mọi prompt, không sửa.

**[THÔNG TIN KHÓA HỌC]:** Python cơ bản, sinh viên năm nhất 18 đến 20 tuổi, 8 tuần, mục tiêu 100 lượt đăng ký tư vấn, kênh Facebook và TikTok.

## 2. Các prompt

**P1:**

```
[THÔNG TIN KHÓA HỌC]
Hãy suy nghĩ từng bước, phân tích chân dung khách hàng mục tiêu: độ tuổi, mong muốn, nỗi lo, thói quen dùng Facebook và TikTok. Không tự thêm thông tin khóa học. Không lời chào, không lời kết.
```

**P2:**

```
[THÔNG TIN KHÓA HỌC]
Chân dung: [KẾT QUẢ P1]
Viết 1 thông điệp truyền thông chính đánh vào nỗi lo hoặc mong muốn trong chân dung, kèm giọng văn.
```

**P3:**

```
[THÔNG TIN KHÓA HỌC]
Chân dung: [KẾT QUẢ P1]
Thông điệp: [KẾT QUẢ P2]
Lập lịch đăng 7 ngày, có 2 bài Facebook và 2 video TikTok. Mỗi ngày ghi kênh, nội dung, mục đích. Mọi nội dung bám thông điệp.
```

**P4:**

```
[THÔNG TIN KHÓA HỌC]
Chân dung: [KẾT QUẢ P1]. Thông điệp: [KẾT QUẢ P2]. Lịch: [KẾT QUẢ P3].
Viết 2 bài Facebook và 2 kịch bản TikTok 30 đến 45 giây (theo mốc giây: hình ảnh, lời thoại). Đúng ngày trong lịch, giữ giọng văn, có lời kêu gọi đăng ký tư vấn. Không bịa học phí, giảng viên, ưu đãi.
```

**P5:**

```
Chiến dịch: [KẾT QUẢ P1, P2, P3, P4]
Kiểm tra: đúng đối tượng, đúng thông điệp, đúng thông tin khóa học, giọng văn thống nhất, có lời kêu gọi, khớp lịch. Mỗi mục ghi ĐẠT hoặc KHÔNG ĐẠT kèm lý do. Không đạt thì chỉ rõ sửa ở prompt nào.
```

## 3. Kết quả chạy thử

### Chân dung khách hàng

- Sinh viên năm nhất, 18 tuổi, chưa từng học lập trình
- Mong muốn: có thêm kỹ năng để xin việc làm thêm, thực tập
- Nỗi lo: sợ lập trình khó, không biết bắt đầu từ đâu
- Thói quen: lướt TikTok giải trí, xem Facebook nhóm trường lớp

### Thông điệp chính

"Chưa biết gì về lập trình? 8 tuần để bắt đầu Python từ con số 0." Giọng văn gần gũi, khích lệ.

### Lịch đăng 7 ngày

| Ngày | Kênh | Nội dung |
|---|---|---|
| 1 | TikTok | Video 1: "Sợ lập trình vì nghĩ nó khó?" |
| 2 | Facebook | Bài 1: giới thiệu khóa 8 tuần |
| 3 | Facebook | Trả lời bình luận, đăng lại bài 1 |
| 4 | TikTok | Video 2: "8 tuần để bắt đầu Python" |
| 5 | Facebook | Bài 2: kêu gọi đăng ký tư vấn |
| 6 | Facebook, TikTok | Trả lời câu hỏi của bạn đọc |
| 7 | Facebook, TikTok | Nhắc đăng ký tư vấn lần cuối |

### Bài Facebook 1 (ngày 2)

Chưa biết gì về lập trình, bạn có dám bắt đầu không? Ai cũng phải bắt đầu từ con số 0. Khóa Python cơ bản dành cho sinh viên năm nhất, học trong 8 tuần, bạn chưa biết gì cũng không sao.

👉 Đăng ký tư vấn tại: [LINK ĐĂNG KÝ]

### Bài Facebook 2 (ngày 5)

8 tuần nữa bạn muốn mình ở đâu? Vẫn lo lập trình khó, hay đã tự viết được những dòng Python đầu tiên? Khóa Python cơ bản 8 tuần đang nhận đăng ký tư vấn.

👉 Đăng ký tư vấn tại: [LINK ĐĂNG KÝ]

### Kịch bản TikTok 1 (ngày 1, 35 giây)

| Giây | Hình ảnh | Lời thoại |
|---|---|---|
| 0-5 | Bạn sinh viên nhìn màn hình code, nhăn mặt | "Lập trình khó quá, chắc mình không học nổi." |
| 5-15 | Chữ hiện: "Ai cũng từng nghĩ vậy" | "Mình cũng từng nghĩ thế. Ai cũng bắt đầu từ con số 0." |
| 15-30 | Gõ những dòng code Python đầu tiên | "Khóa Python cơ bản cho sinh viên năm nhất, chỉ 8 tuần." |
| 30-35 | Chữ: "Đăng ký tư vấn", link ở bio | "Bấm link ở bio để đăng ký tư vấn nhé." |

### Kịch bản TikTok 2 (ngày 4, 40 giây)

| Giây | Hình ảnh | Lời thoại |
|---|---|---|
| 0-5 | Lịch 8 tuần hiện lên màn hình | "8 tuần có thể làm được gì?" |
| 5-25 | Chữ hiện từng bước: viết dòng code đầu tiên, làm quen Python, tự viết chương trình nhỏ | "Từ chưa biết gì đến tự viết được chương trình Python cơ bản." |
| 25-35 | Bạn sinh viên cười, giơ ngón cái | "Khóa dành riêng cho sinh viên năm nhất, học từ con số 0." |
| 35-40 | Chữ: "Đăng ký tư vấn", link ở bio | "Đăng ký tư vấn ngay, link ở bio." |

## 4. Báo cáo kiểm tra nhất quán

| Tiêu chí | Kết quả |
|---|---|
| Đúng đối tượng sinh viên năm nhất | ĐẠT |
| Một thông điệp xuyên suốt | ĐẠT |
| Đúng thông tin khóa học, không bịa thêm | ĐẠT |
| Giọng văn thống nhất | ĐẠT |
| Có lời kêu gọi đăng ký tư vấn | ĐẠT |
| Khớp lịch (Facebook ngày 2, 5; TikTok ngày 1, 4) | ĐẠT |
| Video trong 30 đến 45 giây | ĐẠT |

Kết luận: chiến dịch nhất quán, không phải sửa.
