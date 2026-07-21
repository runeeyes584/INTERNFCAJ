---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

- Thực hành giới hạn quyền hạn IAM Policy, cấu hình Switch Role ràng buộc điều kiện và gán IAM Role cho EC2.
- Thực hành bảo vệ và giám sát dữ liệu: mã hoá S3 bằng KMS, ghi nhật ký bằng CloudTrail và truy vấn log qua Amazon Athena.
- Tìm hiểu lý thuyết về cơ sở dữ liệu trên AWS gồm RDS, Aurora, Redshift và ElastiCache.
- Thực hành triển khai ứng dụng Multi-Tier kết nối EC2 và RDS trong mạng VPC tùy chỉnh.

### Các công việc cần triển khai trong tuần này:

<table>
  <thead>
    <tr>
      <th style="text-align:center;">Thứ</th>
      <th style="text-align:center;">Ngày tháng</th>
      <th style="text-align:center;">Công việc</th>
      <th style="text-align:center;">Nguồn tài liệu</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center;">2</td>
      <td style="text-align:center;">11/05/2026</td>
      <td>
        <ul>
          <li> <strong>Giới hạn quyền IAM:</strong> Thực hành tạo chính sách giới hạn quyền hạn (Restriction Policy) và kiểm tra truy cập của IAM User bị giới hạn. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">3</td>
      <td style="text-align:center;">12/05/2026</td>
      <td>
        <ul>
          <li> <strong>Giám sát bảo mật:</strong> Cấu hình mã hóa KMS cho S3 bucket, tạo trail trên CloudTrail và thực hiện truy vấn nhật ký hoạt động bằng Amazon Athena. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">4</td>
      <td style="text-align:center;">13/05/2026</td>
      <td>
        <ul>
          <li> <strong>Cấu hình Switch Role:</strong> Thiết lập vai trò chuyển đổi và tạo các điều kiện giới hạn theo IP nguồn và thời gian. </li>
          <li> <strong>Xác thực EC2:</strong> So sánh việc sử dụng Access Key với việc gắn IAM Role trực tiếp cho EC2 khi truy cập S3. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">5</td>
      <td style="text-align:center;">14/05/2026</td>
      <td>
        <ul>
          <li> <strong>Cơ sở dữ liệu AWS:</strong> Tìm hiểu lý thuyết về các dịch vụ cơ sở dữ liệu trên AWS gồm RDS, Aurora, Redshift và ElastiCache. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">6</td>
      <td style="text-align:center;">15/05/2026</td>
      <td>
        <ul>
          <li> <strong>Thực hành Lab RDS:</strong> Xây dựng mạng Multi-Tier VPC, tạo Subnet Group, khởi tạo EC2 app server và RDS instance, chạy thử ứng dụng và kiểm tra backup/restore database. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://cloudjourney.awsstudygroup.com/">Thảo luận nhóm & Tài liệu AWS</a> </li>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Kết quả đạt được tuần 4:

- **Phân quyền & Bảo mật IAM**: Thực hành thiết lập chính sách giới hạn quyền hạn và kiểm tra các giới hạn truy cập đối với IAM User. Thiết lập Switch Role kèm ràng buộc điều kiện theo địa chỉ IP nguồn và khung giờ truy cập cụ thể. Thực hành gắn IAM Role cho EC2 instance thay thế việc lưu trữ thủ công Access Key.

- **Mã hóa, Ghi log & Truy vấn dữ liệu**: Thực hành tạo khóa KMS mã hóa S3 bucket, kích hoạt CloudTrail để ghi nhật ký hoạt động và sử dụng Amazon Athena truy vấn lịch sử truy cập.

- **Cơ sở dữ liệu & Ứng dụng Multi-Tier**: Tìm hiểu tổng quan các dịch vụ cơ sở dữ liệu AWS (RDS, Aurora, Redshift, ElastiCache). Thực hành triển khai ứng dụng Multi-Tier kết nối EC2 với RDS database trong mạng VPC và kiểm tra tính năng backup/restore cơ sở dữ liệu.

- **Tiến độ học tập**: Đã hoàn thành theo dõi và học toàn bộ từ video 187 đến 228 trong series _First Cloud Journey Bootcamp 2025_ của AWS Study Group.
