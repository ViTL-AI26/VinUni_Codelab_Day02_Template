# 01 – PROBLEM SCAN & QUICK ASSESS

**Lab 02: AI Product Scoping – Vin Smart Future**

**Sinh viên:** Trương Lợi Vĩ

---

## PHASE 1 – SCAN (Cá nhân)

### 1.1. Mục tiêu

Sử dụng 4 Lenses để nhận diện các vấn đề và điểm nghẽn trong hoạt động vận hành của những công ty thành viên thuộc Vingroup, từ đó xác định các cơ hội ứng dụng AI nhằm cải thiện hiệu quả hoạt động.

### 1.2. Bốn lăng kính tìm kiếm bài toán AI (4 Lenses)

| Lens | Ý nghĩa | Ví dụ |
|---|---|---|
| **Repetitive** (Lặp lại) | Các tác vụ lặp đi lặp lại nhiều lần trong hoạt động hằng ngày. | So khớp hóa đơn sạc điện tại VinFast, điều phối lại chuyến taxi tại Xanh SM. |
| **Time-consuming** (Tốn thời gian) | Các tác vụ tiêu tốn nhiều thời gian xử lý thủ công của nhân viên. | Soạn thảo phản hồi đối với đánh giá 1 sao của cư dân Vinhomes. |
| **AI-upgrade** (AI có thể cải thiện) | Các dịch vụ hiện tại còn chậm, thiếu linh hoạt hoặc phản hồi rập khuôn. | Chatbot CSKH Vinpearl hỗ trợ đặt vé vui chơi. |
| **Stakeholder Pain** (Nỗi đau của các bên liên quan) | Các điểm nghẽn khiến khách hàng hoặc nhân viên vận hành gặp khó khăn, phát sinh phàn nàn. | Tài xế Xanh SM phản ánh hệ thống gợi ý điểm đón khách không chính xác. |

### 1.3. Danh sách các bài toán tiềm năng

| # | Công ty thành viên | Lens | Mô tả bài toán |
|---|---|---|---|
| 1 | Vinhomes | Repetitive | Phân loại tự động các khiếu nại của cư dân về điện, nước, vệ sinh và chuyển tiếp đến bộ phận phụ trách. |
| 2 | Vinpearl | Time-consuming | Phân tích và tổng hợp đánh giá của khách hàng trên các nền tảng trực tuyến nhằm phát hiện phản hồi tiêu cực và các vấn đề cần ưu tiên xử lý. |
| 3 | VinUni | Repetitive | Hỗ trợ chấm bài thực hành lập trình bằng cách phân tích mã nguồn, phát hiện lỗi và đề xuất phản hồi cải thiện cho sinh viên. |
| 4 | Xanh SM | Stakeholder Pain | Phân tích nguyên nhân khách hàng hủy chuyến dựa trên phản hồi của khách hàng và ghi chú từ tài xế. |
| 5 | VinFast | AI-upgrade | Phân loại sự cố xe điện từ mô tả bằng tiếng Việt của khách hàng nhằm hỗ trợ nhân viên kỹ thuật tiếp nhận và xử lý. |

**Kết quả Phase 1:** Xác định được 5 bài toán vận hành tiềm năng thuộc 5 công ty thành viên, làm cơ sở lựa chọn các bài toán để đánh giá chuyên sâu ở Phase 2.

---

## PHASE 2 – QUICK ASSESS (Cá nhân)

### 2.1. Mục tiêu

Lựa chọn 3 bài toán tiềm năng từ danh sách Phase 1 và xây dựng Quick Problem Cards nhằm phân tích tác nhân liên quan, quy trình thủ công hiện tại, điểm nghẽn, cơ hội ứng dụng AI và các chỉ số đánh giá hiệu quả.

### QUICK PROBLEM CARD #1 – VINHOMES

**Bài toán:** Tự động phân loại khiếu nại của cư dân Vinhomes và đề xuất bộ phận phụ trách xử lý.

**Công ty thành viên:** Vinhomes

**Ai đang gặp vấn đề? (Actor)**

- Nhân viên Chăm sóc khách hàng (CSKH).
- Ban Quản lý khu đô thị.
- Cư dân gửi phản ánh.

**Quy trình thủ công hiện tại (Workflow):**

1. Cư dân gửi khiếu nại qua ứng dụng, hotline hoặc email.
2. Nhân viên CSKH tiếp nhận và đọc nội dung phản ánh.
3. Nhân viên xác định nhóm vấn đề (điện, nước, vệ sinh, an ninh...).
4. Nhân viên chuyển yêu cầu đến bộ phận phụ trách.
5. Bộ phận liên quan xử lý và phản hồi cư dân.

**Điểm nghẽn (Bottleneck):**

Bước 2–4: Nhân viên phải đọc, phân loại và điều phối khiếu nại thủ công, với thời gian ước tính khoảng 3–5 phút/lượt.

**Giải pháp AI đề xuất (AI Solution):**

Sử dụng LLM tại bước 3 để phân tích nội dung, phân loại khiếu nại theo nhóm vấn đề và đề xuất bộ phận tiếp nhận. Nhân viên CSKH kiểm tra và phê duyệt trước khi chuyển yêu cầu.

**Chỉ số đánh giá thành công (Success Metrics):**

- Độ chính xác phân loại khiếu nại đạt ít nhất 90%.
- Giảm thời gian phân loại từ 3–5 phút xuống dưới 1 phút/lượt.

**Kiến trúc đề xuất (Quick Architecture):**

- [ ] No AI
- [ ] Rule
- [x] LLM
- [ ] Agent

---

### QUICK PROBLEM CARD #2 – VINPEARL

**Bài toán:** Phân tích đánh giá trực tuyến của khách hàng Vinpearl để nhận diện cảm xúc, chủ đề phản hồi và các vấn đề cần ưu tiên xử lý.

**Công ty thành viên:** Vinpearl

**Ai đang gặp vấn đề? (Actor)**

- Nhân viên Chăm sóc khách hàng.
- Bộ phận quản lý chất lượng dịch vụ.
- Quản lý khách sạn/khu nghỉ dưỡng.

**Quy trình thủ công hiện tại (Workflow):**

1. Thu thập đánh giá của khách hàng từ các nền tảng trực tuyến.
2. Nhân viên đọc và kiểm tra nội dung đánh giá.
3. Phân loại đánh giá theo cảm xúc tích cực, tiêu cực hoặc trung lập.
4. Xác định chủ đề phản hồi (phòng nghỉ, ăn uống, thái độ nhân viên, tiện ích...).
5. Tổng hợp báo cáo và chuyển các vấn đề cần xử lý đến bộ phận liên quan.

**Điểm nghẽn (Bottleneck):**

Bước 2–4: Đọc, phân loại và tổng hợp số lượng lớn đánh giá thủ công, với thời gian ước tính khoảng 3–5 phút/đánh giá.

**Giải pháp AI đề xuất (AI Solution):**

Sử dụng LLM/NLP tại bước 3–4 để phân tích cảm xúc, nhận diện chủ đề, trích xuất vấn đề chính và tổng hợp các phản hồi tiêu cực.

**Chỉ số đánh giá thành công (Success Metrics):**

- Độ chính xác phân loại cảm xúc đạt ít nhất 85%.
- Giảm thời gian phân tích từ 3–5 phút xuống dưới 1 phút/đánh giá.

**Kiến trúc đề xuất (Quick Architecture):**

- [ ] No AI
- [ ] Rule
- [x] LLM
- [ ] Agent

---

### QUICK PROBLEM CARD #3 – XANH SM

**Bài toán:** Phân tích phản hồi khách hàng và ghi chú tài xế Xanh SM để xác định nguyên nhân phổ biến dẫn đến hủy chuyến.

**Công ty thành viên:** Xanh SM

**Ai đang gặp vấn đề? (Actor)**

- Nhân viên quản lý vận hành.
- Bộ phận Chăm sóc khách hàng.
- Đội ngũ quản lý chất lượng dịch vụ.
- Tài xế Xanh SM (người cung cấp thông tin về tình huống phát sinh).

**Quy trình thủ công hiện tại (Workflow):**

1. Thu thập dữ liệu các chuyến đi bị hủy từ hệ thống.
2. Tiếp nhận phản hồi của khách hàng và ghi chú của tài xế.
3. Nhân viên đọc và phân tích nội dung phản hồi.
4. Phân loại nguyên nhân hủy chuyến (khách đổi ý, thời gian chờ lâu, sai điểm đón, vấn đề tài xế...).
5. Tổng hợp báo cáo nguyên nhân và đề xuất hướng cải thiện vận hành.

**Điểm nghẽn (Bottleneck):**

Bước 3–4: Đọc và phân loại phản hồi bằng ngôn ngữ tự nhiên, đặc biệt khi thông tin không đồng nhất, với thời gian ước tính khoảng 3–5 phút/lượt phản hồi.

**Giải pháp AI đề xuất (AI Solution):**

Sử dụng LLM tại bước 3–4 để trích xuất thông tin, phân loại nguyên nhân hủy chuyến và tổng hợp các xu hướng phổ biến từ phản hồi khách hàng và tài xế.

**Chỉ số đánh giá thành công (Success Metrics):**

- Độ chính xác phân loại nguyên nhân đạt ít nhất 85%.
- Giảm thời gian phân tích từ 3–5 phút xuống dưới 1 phút/lượt phản hồi.

**Kiến trúc đề xuất (Quick Architecture):**

- [ ] No AI
- [ ] Rule
- [x] LLM
- [ ] Agent

---

## 2.2. Tổng kết Phase 2

Ba bài toán được lựa chọn để đánh giá chuyên sâu:

| Thứ tự | Công ty | Bài toán | Kiến trúc đề xuất |
|---|---|---|---|
| 1 | Vinhomes | Phân loại khiếu nại cư dân | LLM |
| 2 | Vinpearl | Phân tích đánh giá trực tuyến | LLM |
| 3 | Xanh SM | Phân tích nguyên nhân hủy chuyến | LLM |

Trong ba bài toán trên, **Vinhomes – AI hỗ trợ phân loại khiếu nại cư dân** được lựa chọn để tiếp tục phân tích chuyên sâu và phát triển prototype ở các Phase tiếp theo.

*Lưu ý: Các thời gian xử lý và chỉ số mục tiêu trong các Quick Problem Cards là giả định ban đầu phục vụ việc xác định phạm vi và thiết kế giải pháp, chưa phải số liệu vận hành đã được xác minh tại các doanh nghiệp.*