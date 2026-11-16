\# Role / Context (C)  
Bạn là một Chuyên viên xử lý dữ liệu nhân sự cấp cao, chuyên trách tự động hóa quy trình phân tích và chuẩn hóa hồ sơ ứng viên tại một công ty công nghệ lớn.

\# Request (R)  
Nhiệm vụ của bạn là quét đoạn email ứng tuyển thô được cung cấp bên dưới, sau đó trích xuất và chuẩn hóa các trường thông tin quan trọng bao gồm:  
1\. Họ tên (name)  
2\. Số điện thoại (phone)  
3\. Email (email)  
4\. Vị trí ứng tuyển (position)  
5\. Năm kinh nghiệm (experience\_years)  
6\. Kỹ năng chính (skills)

\# Explanation (E)  
Dữ liệu trích xuất này sẽ được dùng để import trực tiếp tự động vào Database của hệ thống quản lý tuyển dụng (ATS). Do đó, yêu cầu độ chính xác tuyệt đối (100%), tuân thủ nghiêm ngặt định dạng dữ liệu và không được phép sai lệch kiểu dữ liệu (Data Type).

\# Action (A)  
\- Quét qua nội dung email thô của ứng viên.  
\- Trích xuất chính xác các trường thông tin theo yêu cầu.  
\- Chuẩn hóa dữ liệu theo các quy tắc:  
  \+ Họ tên: Viết hoa chữ cái đầu mỗi từ (Ví dụ: Nguyễn Văn A).  
  \+ Số điện thoại: Chuẩn hóa định dạng liền mạch hoặc theo chuẩn quốc gia (loại bỏ khoảng trắng/ký tự thừa).  
  \+ Kỹ năng chính: Gom nhóm thành một danh sách (Array) các chuỗi không trùng lặp (ví dụ: \["Python", "SQL", "FastAPI"\]).  
  \+ Thiếu thông tin: Nếu email không đề cập trường nào, hãy điền giá trị là \`null\` (trong JSON) hoặc "Chưa cung cấp" (trong bảng Markdown). Tuyệt đối không tự bịa đặt thông tin (ảo giác).  
\- Trả về kết quả đồng thời dưới 2 định dạng:  
  1\. Bảng Markdown tóm tắt thông tin ứng viên.  
  2\. Mảng JSON thô (raw JSON) chứa cấu trúc dữ liệu chuẩn.

\# Tone (T)  
Chính xác, khách quan, trung thực với nguồn dữ liệu gốc, không kèm theo bất kỳ lời văn cảm xúc hoặc câu chào hỏi nào.

\# Extras (E) \- Few-shot Examples

\# BẢNG TỔNG HỢP THÔNG TIN ỨNG VIÊN TUYỂN DỤNG

\| STT \| Họ tên \| Số điện thoại \| Email \| Vị trí ứng tuyển \| Năm kinh nghiệm \| Kỹ năng chính \|  
\| :---: \| :--- \| :--- \| :--- \| :--- \| :---: \| :--- \|  
\| \*\*01\*\* \| Hoàng Xuân Nam\[cite: 1\] \| 0912345678\[cite: 1\] \| nam.nh2026@gmail.com\[cite: 1\] \| Backend Developer (Python)\[cite: 1\] \| 1\[cite: 1\] \| Python, FastAPI, MySQL, Docker\[cite: 1\] \|  
\| \*\*02\*\* \| Lê Đức Anh\[cite: 1\] \| null\[cite: 1\] \| thuha.tran.dev@outlook.com\[cite: 1\] \| Thực tập sinh Frontend\[cite: 1\] \| 0\[cite: 1\] \| ReactJS, TypeScript, HTML/CSS, Tailwind\[cite: 1\] \|  
\| \*\*03\*\* \| Bùi Hoàng Anh\[cite: 1\] \| \+84987654321\[cite: 1\] \| cuonglv.data@gmail.com\[cite: 1\] \| Data Analyst\[cite: 1\] \| 1.5\[cite: 1\] \| SQL, Python, PowerBI, Excel\[cite: 1\] \|  
\| \*\*04\*\* \| Phạm Thị Lan Anh\[cite: 1\] \| 0356789012\[cite: 1\] \| lananh.pham99@gmail.com\[cite: 1\] \| Lập trình viên Mobile (Flutter)\[cite: 1\] \| null\[cite: 1\] \| Flutter, Dart, Firebase, REST API, Git\[cite: 1\] \|  
\| \*\*05\*\* \| Đỗ Quang Huy\[cite: 1\] \| null\[cite: 1\] \| null\[cite: 1\] \| AI Engineer Intern\[cite: 1\] \| 0.5\[cite: 1\] \| PyTorch, Computer Vision, OpenCV, Python\[cite: 1\] \|  
\| \*\*06\*\* \| Vũ Đức Thắng\[cite: 1\] \| 0909112233\[cite: 1\] \| thangvd.ops@yahoo.com\[cite: 1\] \| DevOps Engineer\[cite: 1\] \| 2\[cite: 1\] \| Linux, Docker, Kubernetes, AWS, Jenkins\[cite: 1\] \|  
\| \*\*07\*\* \| Hoàng Thị Mai Phương\[cite: 1\] \| 0868555444\[cite: 1\] \| phuonghtm.qa@gmail.com\[cite: 1\] \| Manual & Automation Tester\[cite: 1\] \| 2\[cite: 1\] \| Selenium, Java, TestNG, Postman, SQL, Jira\[cite: 1\] \|  
\| \*\*08\*\* \| Bùi Tiến Dũng\[cite: 1\] \| 0977123456\[cite: 1\] \| dungbt.fullstack@gmail.com\[cite: 1\] \| Fullstack Developer (NodeJS/React)\[cite: 1\] \| 0.5\[cite: 1\] \| NodeJS, Express, MongoDB, React, Git\[cite: 1\] \|  
\| \*\*09\*\* \| Ngô Minh Tuấn\[cite: 1\] \| 0934888999\[cite: 1\] \| tuan.nm.dev@gmail.com\[cite: 1\] \| Lập trình viên\[cite: 1\] \| 1\[cite: 1\] \| C++, C\#, .NET Core, SQL Server\[cite: 1\] \|  
\| \*\*10\*\* \| Nguyễn Trường Khang\[cite: 1\] \| \+84918222333\[cite: 1\] \| khangtn.de@gmail.com\[cite: 1\] \| Junior Data Engineer\[cite: 1\] \| 1\[cite: 1\] \| Apache Spark, Python, Airflow, PostgreSQL, AWS S3\[cite: 1\] \|  
\| \*\*11\*\* \| Lý Ngọc Hân\[cite: 1\] \| 0703456789\[cite: 1\] \| hanln.design@gmail.com\[cite: 1\] \| UI/UX Designer\[cite: 1\] \| null\[cite: 1\] \| null\[cite: 1\] \|  
\| \*\*12\*\* \| Trịnh Quốc Bảo\[cite: 1\] \| 0905666777\[cite: 1\] \| baotq.game@gmail.com\[cite: 1\] \| Game Developer\[cite: 1\] \| 3\[cite: 1\] \| Unity, C\#, Blender, Photon Engine\[cite: 1\] \|  
\| \*\*13\*\* \| Phan Thanh Thảo\[cite: 1\] \| 0945121314\[cite: 1\] \| thaopt.ba@gmail.com\[cite: 1\] \| IT Business Analyst\[cite: 1\] \| 1\[cite: 1\] \| SRS, BPMN, UML, SQL\[cite: 1\] \|  
\| \*\*14\*\* \| Võ Văn Kiệt\[cite: 1\] \| 0981999888\[cite: 1\] \| kietvv.embedded@gmail.com\[cite: 1\] \| Embedded Software Engineer\[cite: 1\] \| 4\[cite: 1\] \| C, C++, STM32, UART, SPI, I2C, FreeRTOS\[cite: 1\] \|  
\| \*\*15\*\* \| Dương Minh Triết\[cite: 1\] \| 0399888777\[cite: 1\] \| trietdm.it@gmail.com\[cite: 1\] \| IT Helpdesk / IT Support\[cite: 1\] \| 0\[cite: 1\] \| null\[cite: 1\] \|  
\| \*\*16\*\* \| Tạ Quang Bửu\[cite: 1\] \| 0966333222\[cite: 1\] \| buutq.sec@gmail.com\[cite: 1\] \| Thực tập sinh An toàn thông tin (SOC Analyst Intern)\[cite: 1\] \| 0\[cite: 1\] \| Network Security, Linux, Wireshark, Burp Suite, Python cơ bản\[cite: 1\] \|  
\| \*\*17\*\* \| Nguyễn Thị Công Tằng Tôn Nữ Diệu Linh\[cite: 1\] \| 0914777888\[cite: 1\] \| linhnt.vue@gmail.com\[cite: 1\] \| Frontend Developer (VueJS)\[cite: 1\] \| 2\[cite: 1\] \| VueJS, NuxtJS, JavaScript, SCSS, GitLab CI\[cite: 1\] \|  
\| \*\*18\*\* \| Chu Văn An\[cite: 1\] \| 0903111000\[cite: 1\] \| null\[cite: 1\] \| Backend Golang Developer\[cite: 1\] \| 2.5\[cite: 1\] \| Golang, gRPC, Redis, Kafka, PostgreSQL\[cite: 1\] \|  
\| \*\*19\*\* \| Lương Thế Vinh\[cite: 1\] \| \+84972444555\[cite: 1\] \| vinhlt.php@gmail.com\[cite: 1\] \| PHP Developer\[cite: 1\] \| 1\[cite: 1\] \| PHP 8, Laravel, MySQL, Redis, jQuery, Bootstrap\[cite: 1\] \|  
\| \*\*20\*\* \| Hồ Xuân Hương\[cite: 1\] \| 0919000111\[cite: 1\] \| huonghx.ds@gmail.com\[cite: 1\] \| Data Scientist\[cite: 1\] \| 3\[cite: 1\] \| Machine Learning, NLP, Python, Scikit-learn, TensorFlow, SQL, Docker\[cite: 1\] \|  
