# Bài 7

- **Phần 1: Thiết kế Prompt 3 Thành phần Chuẩn hóa**
  1. *Nguyên nhân AI Hallucination:* Do câu hỏi quá cụt ngủn ("phần mềm trạm sạc của tôi bị hỏng"), AI hoàn toàn mù tịt về hệ điều hành, tên phần mềm hay mã lỗi thực tế. Do đó, AI buộc phải đoán mò và đưa ra các lời khuyên chung chung, vô căn cứ như tháo vỏ thiết bị phần cứng.
  2. *Prompt 3 Thành phần chuẩn hóa:*
     > **[Context]**: Tôi là kỹ thuật viên đang vận hành phần mềm VoltCharge Controller trên máy tính chạy hệ điều hành Windows 11 tại trạm sạc.
     > **[Raw Error]**: `System.UnauthorizedAccessException: Access to the path 'C:\Program Files\VoltCharge\data\session.log' is denied. Process terminated with exit code 5 (0x00000005).`
     > **[Instruction]**: Hãy dịch lỗi này sang tiếng Việt dễ hiểu và đưa ra 3 bước khắc phục cụ thể tại chỗ để cấp quyền cho phần mềm chạy bình thường.

- **Phần 2: Giải mã Lỗi & Kịch bản Khắc phục**
  3. *Giải mã lỗi:* Lỗi `UnauthorizedAccessException` nghĩa là "Không được phép truy cập". Ứng dụng đang cố gắng ghi file nhật ký (`session.log`) vào thư mục được bảo vệ của hệ thống (`C:\Program Files\...`) nhưng tài khoản hiện tại không có đủ quyền ghi, dẫn đến việc tiến trình bị dừng đột ngột (Mã lỗi 5).
  4. *3 bước xử lý tại chỗ:*
     - Bước 1: Đóng hẳn ứng dụng hoặc tiến trình đang chạy ngầm của VoltCharge Controller.
     - Bước 2: Nhấp chuột phải vào biểu tượng phần mềm, chọn **Run as administrator** để chạy với quyền Quản trị viên cao nhất.
     - Bước 3: Truy cập vào thư mục `C:\Program Files\VoltCharge`, nhấp chuột phải vào thư mục `data` ➔ chọn **Properties** ➔ chuyển sang tab **Security** ➔ cấp quyền **Full Control / Modify** cho tài khoản người dùng hiện tại.
  5. *Xử lý bẫy an ninh (API Key):* Kỹ thuật viên **tuyệt đối phải xóa bỏ hoặc thay thế chuỗi mã bí mật** (`API_KEY: volt_secret_token_889922`) bằng các ký tự che giấu chung chung (như `API_KEY: [REDACTED]` hoặc `API_KEY: ***`) trước khi dán vào khung chat AI. Lý do là để bảo mật thông tin doanh nghiệp, tránh rò rỉ mã khóa bí mật lên các hệ thống máy chủ bên ngoài có thể bị lợi dụng tấn công hệ thống trạm sạc.
