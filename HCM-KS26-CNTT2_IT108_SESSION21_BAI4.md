# Bài 4

- **Bảng so sánh Ưu/Nhược điểm:**

| Tiêu chí | Google Search | AI Assistant (ChatGPT / Gemini) |
| :--- | :--- | :--- |
| **Độ chính xác** | Cao nếu chọn đúng nguồn (StackOverflow, tài liệu chính hãng), nhưng dễ bị lạc vào web quảng cáo nếu tìm kém. | Khá tốt với lỗi phổ biến, nhưng đôi khi đưa ra mã lệnh giả định (Hallucination) nếu lỗi quá mới. |
| **Tính cập nhật** | Cực kỳ cập nhật, lấy trực tiếp các bài thảo luận mới nhất trên mạng theo thời gian thực. | Phụ thuộc vào dữ liệu huấn luyện hoặc khả năng duyệt web thời gian thực của mô hình. |
| **Khả năng giải thích** | Thấp (chỉ đưa ra danh sách các bài viết, người dùng phải tự đọc, tự dịch tiếng Anh và tự hiểu). | Rất cao (có thể dịch nghĩa, phân tích chi tiết từng dòng lỗi và giải thích cặn kẽ bằng tiếng Việt). |
| **Rủi ro (Hallucination)** | Thấp hơn (hiển thị nguyên văn bài viết của người khác, rủi ro nằm ở việc người dùng chọn nhầm bài viết cũ). | Có thể xảy ra hiện tượng "ảo giác", tự bịa ra câu lệnh hoặc tên hàm không có thật nếu không kiểm tra kỹ. |

- **Lựa chọn an toàn:**
  - Trong trường hợp liên quan đến các lệnh hệ thống cấp thấp có nguy cơ xóa dữ liệu ổ cứng, thay đổi cấu hình mạng cốt lõi (như `diskpart`, `format`, `regedit`), **bắt buộc phải sử dụng Google Search** để tìm đọc kỹ các thảo luận gốc từ trang chủ Microsoft hoặc các kỹ sư trưởng trên StackOverflow nhằm đảm bảo không chạy nhầm lệnh phá hoại máy tính do AI tự bịa ra.
