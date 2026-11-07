# Bài 1

- **Tại sao truy vấn trên là "Bad Query" (gây nhiễu):**
  - Câu truy vấn của bạn sinh viên chứa toàn bộ các từ ngữ cảm thán, văn nói tự nhiên ("thầy ơi cho em xin...", "với ạ"). Các cỗ máy tìm kiếm như Google hoạt động dựa trên việc khớp từ khóa (keyword matching), chúng không hiểu được các từ đệm xã giao này và sẽ tìm kiếm mọi trang web có chứa các cụm từ đó, dẫn đến việc trả về vô số diễn đàn thảo luận, bài viết chia sẻ chung chung không chính thống.
  - Ngoài ra, cụm từ "tài liệu học html cơ bản của trang mozilla" quá dài và không chuẩn xác theo cấu trúc URL hay tên gọi chính thức của tài liệu Mozilla (MDN Web Docs), khiến thuật toán bị loãng.

- **Viết lại truy vấn sử dụng toán tử:**
  - `site:developer.mozilla.org HTML cơ bản` hoặc `site:mozilla.org "HTML tutorials" -forum -ads`

- **Ý nghĩa của việc sử dụng các toán tử:**
  - `site:developer.mozilla.org`: Giúp ép Google chỉ quét và trả kết quả nằm trong tên miền chính thức của Mozilla, loại bỏ hoàn toàn các trang web rác, blog cá nhân hay diễn đàn linh tinh bên ngoài, giúp tiết kiệm 90% thời gian lọc tin.
  - Toán tử `-` (loại trừ): Giúp lọc bỏ các từ khóa không mong muốn như `-forum` hay `-ads`, tránh việc click nhầm vào các nội dung quảng cáo độc hại hoặc thảo luận dài dòng vô ích.
