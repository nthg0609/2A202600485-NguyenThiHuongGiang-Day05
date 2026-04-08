# Phân tích UX/UI: Vietnam Airlines - Chatbot NEO

## 1. Khám phá: Kỳ vọng Marketing vs. Thực tế trải nghiệm
* **Kỳ vọng Marketing:** NEO được định vị là một trợ lý ảo thông minh, hỗ trợ giải đáp thắc mắc khách hàng mọi lúc, mọi nơi, từ việc tìm kiếm thông tin, đặt vé, kiểm tra chuyến bay đến giải đáp về hành lý.
* **Thực tế trải nghiệm:**
    * **Tốc độ:** Phản hồi tức thì với các truy vấn có cấu trúc rõ ràng. Tuy nhiên, khi cần chuyển sang nhân viên tư vấn, tốc độ phản hồi bị chậm lại.
    * **Phản ứng của AI:** Hoạt động rập khuôn và máy móc. Thay vì tóm tắt, khi người dùng hỏi về các quy định, AI thường ném ra một khối văn bản dài. 
    * **Giọng điệu:** Lịch sự nhưng thiếu cảm xúc (zero empathy).

## 2. Phân tích 4 Paths (Luồng trải nghiệm)
* **Path 1 - Khi AI đúng:**
    * **User thấy gì:** Kết quả hiển thị thông tin gọn gàng, chính xác ngay lập tức (VD: Trả về thông tin vé đi Hà Nội kèm giờ bay, mã số vé).
    * **Hệ thống confirm:** Xác nhận ngầm bằng cách đề xuất các hành động tiếp theo thông qua hệ thống nút bấm (Quick replies/Buttons).
* **Path 2 - Khi AI không chắc:**
    * **Hệ thống xử lý:** Đưa ra câu trả lời mang tính chất rộng nhất, bao hàm các trường hợp để bao phủ ý định của người dùng.
* **Path 3 - Khi AI sai:**
    * **Nhận biết:** Người dùng lướt qua kết quả và thấy nội dung không đúng với ý mình.
    * **Cách sửa:** Không có cơ chế sửa lỗi trực tiếp. Người dùng buộc phải tự suy nghĩ một câu lệnh/từ khóa khác và thực hiện lại từ đầu.
* **Path 4 - Khi User mất tin (Dead end):**
    * **Lối thoát (Fallback):** Có tính năng "Gặp nhân viên hỗ trợ".
    * **Trải nghiệm:** Tùy chọn này không dễ tìm, bị giấu đi khiến người dùng khó khăn trong việc tìm đường thoát khỏi vòng lặp của bot.

## 3. Tổng quan & Khoảng trống (The Gap)
* **Luồng xử lý tốt nhất (Path 1):** Hệ thống làm rất tốt khi truy vấn đúng từ khóa do bản chất kiến trúc là Rule-based kết hợp NLP cơ bản.
* **Luồng yếu nhất (Path 3):** Hệ thống dễ gây ức chế do **thiếu bộ nhớ ngữ cảnh** (không nhớ câu hỏi trước đó) và **thiếu vòng lặp phản hồi** (không có nút bấm để đánh giá câu trả lời sai).
* **Gap (Marketing vs. Thực tế):** Khoảng trống lớn nhất nằm ở **khả năng suy luận** và **tính đàm thoại (Conversational)**. Khác với một trợ lý thông minh thực thụ, NEO chưa biết cách "hỏi vặn lại", làm rõ ngữ cảnh khi người dùng nói sai hoặc nói tắt.
