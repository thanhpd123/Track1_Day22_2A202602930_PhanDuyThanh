# Track1_Day22_2A202602930_PhanDuyThanh

- **Họ tên:** Phan Duy Thành
- **MHV:** 2A202602930
- **Bài lab:** Monetization Model — Cost/Job · Value Metric · GTM · Evidence Pack
- **Sản phẩm:** AI dựng concept nội thất cho Freelance Interior Designer (tiếp nối Metrics Pack ở Lab20)
- **Ngày kiểm tra giá API:** 08/10/2026

## File nộp

| File                                                                                         | Nội dung                                                                                                                         |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| [Day25-AI-Product-GTM-Monetization-Model.xlsx](Day25-AI-Product-GTM-Monetization-Model.xlsx) | Model 7 tab, đã điền các ô vàng. Nguồn và giả định nằm trong comment của từng ô. Bảng giá cập nhật nằm ở cuối tab `6_Benchmarks` |
| [Day25-AI-Product-GTM-One-Pager-Template.docx](Day25-AI-Product-GTM-One-Pager-Template.docx) | Monetization One-Pager. Mọi con số trỏ về một ô trong file Excel                                                                 |
| [ai-support-log.md](ai-support-log.md)                                                       | AI Support Log                                                                                                                   |

## 5 con số chính

| Chỉ số                   | Giá trị                                      | Ô Excel         |
| ------------------------ | -------------------------------------------- | --------------- |
| Cost/Job (1 Design Pack) | $1,16 (≈ 30.239 ₫)                           | `2_Pricing!B5`  |
| Giá sàn (3×)             | $3,48                                        | `2_Pricing!B7`  |
| Giá bán đề xuất          | $4,78/pack (499.000 ₫/tháng gồm 4 pack)      | `2_Pricing!B19` |
| Gross Margin             | 75,8% (51% nếu tính cả overhead)             | `2_Pricing!B21` |
| Breakeven containment    | 42,4% (ước tính hiện tại: 70%, chưa có eval) | `2_Pricing!B33` |

Kênh đã chọn: **PLG**. Ngân sách CAC là $174/khách, trong khi CAC của motion có sales khoảng $25.200, tức gấp 145 lần (`4_Channel_Fit!B23`).

## Điều tôi mang về áp dụng cho dự án thật

Chi phí nằm ở ảnh, không nằm ở chữ.

Mỗi pack tốn khoảng $0,51 tiền sinh ảnh, còn phần LLM viết bảng vật liệu chỉ khoảng $0,01.
Prompt caching tiết kiệm 0% với model ảnh.
Việc làm được ngay: lượt nháp render ở 1K ($0,067), chỉ render 2K ($0,101) khi bấm Xuất.
Có thể thử đổi model rẻ hơn khoảng một nửa (Cost/Job khoảng $0,80), nhưng phải eval chất lượng trước.
Metric và giá là một sợi dây.

Counter-metric ở Lab20 là ">5 lượt render/phòng là AI đang ngáo". Ở Lab22, từ 13 lượt trở lên thì GM tụt dưới 50%.
Vậy event ai_render_completed gắn với design_id vừa đo chất lượng vừa là chuông báo lỗ. Phải log nó ngay từ ngày đầu.
Thu tiền theo kết quả nghĩa là mình gánh phần thất bại.

Tính tiền khi xuất pack (khớp với NSM) thì khách thích, nhưng mỗi lượt render lại là mình trả. Cần đặt trần render cho mỗi pack.
Tính giá xong vẫn phải trả lời được "sao không dùng Interior AI".

Quy ra cùng đơn vị, mình đắt gấp 4–19 lần đối thủ.
Trước khi build thêm tính năng, cần test xem designer có chịu trả 499k cho moodboard và bảng vật liệu theo thị trường VN không.
