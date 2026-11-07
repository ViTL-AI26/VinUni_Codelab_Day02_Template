# PHASE 6 – PHẢN ÁNH CÁ NHÂN (PERSONAL AI REFLECTION)

## 1. Tôi đã sử dụng AI như thế nào trong buổi học hôm nay?

Trong buổi Lab hôm nay, tôi sử dụng AI như một công cụ hỗ trợ xuyên suốt quá trình xác định vấn đề, xây dựng ý tưởng và phát triển giải pháp AI. AI hỗ trợ tôi nhận diện các vấn đề vận hành tiềm năng tại những công ty thành viên thuộc Vingroup, phân tích quy trình nghiệp vụ hiện tại và lựa chọn bài toán phù hợp để ứng dụng AI.

Cụ thể, tôi đã sử dụng AI để:

- Đề xuất và phân tích các vấn đề vận hành có tiềm năng ứng dụng AI.
- Xây dựng Problem Statement, xác định điểm nghẽn (Bottleneck) và mô tả quy trình nghiệp vụ hiện tại.
- Thiết kế System Prompt, Operational Boundaries và cấu trúc đầu ra JSON.
- Hỗ trợ xây dựng và hoàn thiện mã nguồn Python kết nối với Gemini API.
- Phân tích và khắc phục các vấn đề kỹ thuật liên quan đến kết nối API và khả năng truy cập mô hình.
- Xây dựng các tình huống kiểm thử đối kháng (Adversarial Testing) và đánh giá kết quả hoạt động của prototype.

## 2. Những điểm AI hỗ trợ hiệu quả

AI giúp tôi tiết kiệm thời gian trong quá trình tìm kiếm ý tưởng, hệ thống hóa thông tin và chuyển đổi một vấn đề nghiệp vụ thành giải pháp kỹ thuật cụ thể. Thay vì phải tự xây dựng toàn bộ nội dung từ đầu, tôi có thể sử dụng AI để tham khảo các phương án, phân tích ưu nhược điểm và từng bước hoàn thiện giải pháp.

Đặc biệt, trong quá trình phát triển prototype phân loại khiếu nại cư dân tại Vinhomes, AI hỗ trợ tôi thiết kế các quy tắc hoạt động, xác định phạm vi xử lý và xây dựng cơ chế Human-in-the-loop. Nhờ đó, hệ thống được định hướng theo nguyên tắc AI chỉ đưa ra đề xuất phân loại, mức độ ưu tiên và bộ phận phụ trách, trong khi quyết định xử lý cuối cùng vẫn thuộc về nhân viên Chăm sóc khách hàng (CSKH).

Bên cạnh việc hỗ trợ xây dựng nội dung và mã nguồn, AI còn đóng vai trò như một công cụ hỗ trợ gỡ lỗi (Debugging). Trong quá trình kết nối Gemini API, tôi gặp vấn đề về khả năng cung cấp dịch vụ của mô hình ban đầu. Thông qua việc kiểm tra danh sách mô hình được hỗ trợ và thử nghiệm các phương án thay thế, tôi đã chuyển sang sử dụng Gemini 3.5 Flash và thực thi prototype thành công.

## 3. Những hạn chế và khó khăn gặp phải

Mặc dù mang lại nhiều lợi ích, quá trình phối hợp với AI vẫn tồn tại một số hạn chế và khó khăn:

- **Khả năng truy cập API:** Mô hình Gemini ban đầu gặp lỗi 503 UNAVAILABLE do tình trạng quá tải dịch vụ. Điều này khiến quá trình triển khai bị gián đoạn và đòi hỏi phải kiểm tra khả năng truy cập, lựa chọn mô hình thay thế phù hợp.
- **Tính nhất quán của bài toán:** Việc chuyển hướng từ bài toán điều phối xe điện tại Xanh SM sang phân loại khiếu nại cư dân tại Vinhomes đòi hỏi phải điều chỉnh lại System Prompt, Operational Boundaries, quy tắc nghiệp vụ và các tình huống kiểm thử để bảo đảm tính nhất quán.
- **Độ tin cậy của kết quả:** Một số đề xuất của AI chưa thực sự phù hợp với ngữ cảnh. Chẳng hạn, trong tình huống khiếu nại thiếu thông tin, mô hình vẫn đề xuất mức ưu tiên HIGH dù chưa có đủ căn cứ để xác định mức độ nghiêm trọng.
- **Hạn chế về dữ liệu kiểm thử:** Prototype mới được đánh giá thông qua ba tình huống giả lập, chưa có tập dữ liệu khiếu nại thực tế được gán nhãn. Do đó, kết quả 3/3 bài kiểm thử đạt yêu cầu chưa đủ cơ sở để khẳng định độ chính xác và độ tin cậy của hệ thống trong môi trường thực tế.

Để hạn chế vấn đề liên quan đến việc đánh giá mức độ ưu tiên, tôi xác định cần bổ sung quy tắc vào System Prompt: khi nội dung khiếu nại không cung cấp đủ bằng chứng về mức độ nghiêm trọng, AI không nên tự suy diễn mức ưu tiên HIGH mà cần nhận diện tình trạng thiếu thông tin và yêu cầu nhân viên CSKH xác minh trước khi đưa ra quyết định. Đây là hướng điều chỉnh cần được kiểm chứng thêm bằng các tình huống kiểm thử mới.

Những trải nghiệm trên cho thấy kết quả do AI tạo ra không phải lúc nào cũng chính xác hoặc phù hợp với ngữ cảnh. Vì vậy, việc kiểm tra, đối chiếu và đánh giá đầu ra là cần thiết trước khi sử dụng trong thực tế.

## 4. Những kiến thức và kinh nghiệm rút ra

Thông qua buổi Lab, tôi nhận thấy việc phát triển một sản phẩm AI không chỉ đơn thuần là lựa chọn mô hình hoặc xây dựng prompt, mà còn đòi hỏi sự kết hợp giữa tư duy nghiệp vụ, kỹ thuật và khả năng đánh giá rủi ro.

Một số bài học quan trọng tôi rút ra:

- **Xác định đúng vấn đề:** Cần hiểu rõ vấn đề nghiệp vụ trước khi lựa chọn công nghệ hoặc đề xuất giải pháp AI.
- **Phân tích quy trình:** Phải nắm được quy trình vận hành hiện tại để xác định chính xác điểm nghẽn cần cải thiện.
- **Thiết lập giới hạn hoạt động:** Cần xây dựng Operational Boundaries rõ ràng nhằm kiểm soát phạm vi và hành vi của mô hình.
- **Kiểm thử đối kháng:** Cần thiết kế các tình huống đầu vào bất thường hoặc có chủ đích gây sai lệch để đánh giá khả năng duy trì các quy tắc an toàn của AI.
- **Duy trì sự giám sát của con người:** Cơ chế Human-in-the-loop đóng vai trò quan trọng đối với các quyết định có thể ảnh hưởng trực tiếp đến người dùng.
- **Đánh giá khả năng triển khai:** Cần xem xét dữ liệu, chi phí, rủi ro và mức độ sẵn sàng của tổ chức trước khi đưa AI vào vận hành thực tế.

Đặc biệt, tôi hiểu rằng việc một prototype hoạt động thành công hoặc vượt qua một số tình huống kiểm thử không đồng nghĩa với việc hệ thống đã đủ độ tin cậy để triển khai trên quy mô thực tế.

## 5. Những điểm cần cải thiện trong các lần triển khai tiếp theo

Trong các lần phát triển tiếp theo, tôi sẽ ưu tiên thu thập tập dữ liệu khiếu nại thực tế có tính đại diện, đồng thời xây dựng bộ dữ liệu được gán nhãn để đánh giá khách quan hiệu quả phân loại của mô hình.

Bên cạnh đó, tôi sẽ so sánh hiệu quả giữa phương pháp phân loại thủ công, Rule-based và LLM-based nhằm xác định liệu việc ứng dụng mô hình ngôn ngữ lớn có thực sự mang lại giá trị vượt trội về thời gian xử lý, độ chính xác và hiệu quả vận hành hay không.

Tôi cũng sẽ tiếp tục hoàn thiện System Prompt để xử lý tốt hơn các trường hợp khiếu nại thiếu thông tin, đặc biệt là việc xác định mức độ ưu tiên. Đồng thời, cần mở rộng số lượng và tính đa dạng của các tình huống kiểm thử đối kháng để đánh giá khả năng duy trì Operational Boundaries trong những trường hợp phức tạp hơn.

Ngoài ra, việc đánh giá chi phí sử dụng API, bảo mật dữ liệu cư dân và khả năng tích hợp với quy trình CSKH hiện tại cũng cần được xem xét trước khi triển khai thực tế.

## 6. Phản ánh cá nhân

Nhìn chung, buổi Lab mang lại cho tôi trải nghiệm thực tiễn trong việc sử dụng AI như một công cụ hỗ trợ giải quyết vấn đề và phát triển sản phẩm kỹ thuật. Thông qua quá trình thực hiện, tôi nhận ra rằng giá trị của AI không chỉ nằm ở khả năng tạo ra câu trả lời, đề xuất ý tưởng hoặc sinh mã nguồn, mà còn phụ thuộc vào cách con người xác định bài toán, định hướng mô hình, kiểm chứng kết quả và kiểm soát các quyết định cuối cùng.

Một điểm đáng chú ý là quá trình làm việc với AI không phải lúc nào cũng diễn ra suôn sẻ. Việc gặp lỗi API, điều chỉnh bài toán và phát hiện những đề xuất chưa phù hợp từ mô hình giúp tôi hiểu rõ hơn về giới hạn của công nghệ này, đồng thời rèn luyện khả năng đánh giá và xử lý vấn đề thay vì phụ thuộc hoàn toàn vào kết quả do AI cung cấp.

**Bài học quan trọng nhất tôi rút ra là AI nên đóng vai trò tăng cường năng lực của con người thay vì thay thế hoàn toàn khả năng đánh giá và ra quyết định của con người. Việc ứng dụng AI chỉ thực sự có giá trị khi giải pháp được xây dựng dựa trên nhu cầu thực tế, có cơ chế kiểm soát phù hợp và mang lại hiệu quả có thể kiểm chứng, đặc biệt trong những môi trường vận hành mà sai sót có thể ảnh hưởng trực tiếp đến khách hàng và chất lượng dịch vụ.**