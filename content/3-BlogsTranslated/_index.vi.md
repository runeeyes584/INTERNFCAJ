---
title: "Các bài blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Trong quá trình thực tập tại FCAJ, em và nhóm **Lacrimosa** đã đăng 3 bài Blog theo quy định của FCAJ. Đại diện của nhóm là bạn **Tường Vi** đảm nhiệm đại diện nhóm đăng blog. Những bài blogs này bao gồm:

### [Blog 1 - TỐI ƯU HÓA KIẾN TRÚC LAKEHOUSE VỚI AMAZON SAGEMAKER](3.1-Blog1/)

Blog này giới thiệu về Kiến trúc Lakehouse với Amazon SageMaker. Kiến trúc Lakehouse với Amazon SageMaker cung cấp giải pháp thống nhất cho các tổ chức, kết hợp tính linh hoạt của Data Lake với hiệu suất của Data Warehouse trên một nền tảng mở. Hệ thống được xây dựng trên bốn thành phần cốt lõi: lưu trữ linh hoạt, danh mục kỹ thuật tập trung (AWS Glue), quản trị quyền truy cập chi tiết (AWS Lake Formation), và khung API mở dựa trên Apache Iceberg. Doanh nghiệp có thể chọn từ ba phương thức tích hợp dữ liệu—ETL truyền thống, Zero-ETL tự động, hay Data Federation không di chuyển dữ liệu—cùng với các lựa chọn lưu trữ tối ưu (S3 + Iceberg, S3 Tables, hay Redshift Managed Storage) tùy theo yêu cầu độ trễ và hiệu suất. Cách tiếp cận này cho phép các tổ chức xây dựng hệ thống dữ liệu có khả năng mở rộng cao, sẵn sàng cho AI/ML, mà không cần đánh đổi giữa linh hoạt và tối ưu hóa chi phí.

### [Blog 2 - XÂY DỰNG ỨNG DỤNG CHATBOT THEO NGỮ CẢNH BẰNG AMAZON BEDROCK KNOWLEDGE BASES](3.2-Blog2/)

Blog này nói về xây dựng chatbot thông minh bằng cách kết hợp LLM với kiến trúc RAG (Retrieval Augmented Generation) để cung cấp câu trả lời dựa trên dữ liệu độc quyền của tổ chức. Thay vì tự xây dựng hệ thống RAG phức tạp (đòi hỏi quản lý vector embeddings, database, tìm kiếm semantic, v.v.), Amazon Bedrock Knowledge Bases cung cấp giải pháp serverless tự động hóa toàn bộ quy trình: từ đưa dữ liệu (StartIngestionJob chia nhỏ tài liệu, tạo embeddings bằng Amazon Titan, lưu vào OpenSearch Serverless) đến truy vấn và tạo phản hồi (RetrieveAndGenerate kết hợp Titan embeddings với Claude Instant 1.2). Kiến trúc sử dụng S3 làm nguồn dữ liệu, Lambda để tự động hóa quy trình, API Gateway cho giao diện người dùng, và Infrastructure as Code (AWS CDK) để dễ dàng triển khai và mở rộng—giúp đội kỹ thuật tập trung vào giá trị thay vì vận hành phức tạp.

### [Blog 3 - XÂY DỰNG GAME ĐA NGƯỜI CHƠI VỚI KIẾN TRÚC AWS SERVERLESS](3.3-Blog3/)

Blog này nói về xây dựng game web đa người chơi bằng kiến trúc AWS Serverless để tối ưu thời gian phát triển, chi phí và khả năng mở rộng tự động. Dự án Simple Trivia Service minh chứng cách các dịch vụ serverless (Lambda, API Gateway, DynamoDB, SNS) kết hợp với các công cụ hỗ trợ (Cognito, ElastiCache, AWS IoT) để xây dựng game hoàn chỉnh có chế độ chơi đơn và nhiều người. Tùy theo yêu cầu của từng chế độ chơi: chế độ đơn dùng HTTP API + SNS để cập nhật điểm bất đồng bộ; chế độ nhiều người chơi thường sử dụng API Gateway WebSockets với trạng thái quản lý từ máy khách; còn chế độ bảng điểm trực tiếp (yêu cầu độ trễ cực thấp) sử dụng AWS IoT + ElastiCache for Redis để lưu trữ trạng thái backend và cập nhật realtime cho toàn bộ người chơi. Kiến trúc này không chỉ tiết kiệm chi phí vận hành mà còn giải phóng đội ngũ phát triển khỏi gánh nặng cấu hình máy chủ, cho phép tập trung vào sáng tạo nội dung và trải nghiệm người chơi.
