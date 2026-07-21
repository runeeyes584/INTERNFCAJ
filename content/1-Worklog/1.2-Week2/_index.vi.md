---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
### Mục tiêu tuần 2:

- Hoàn thành các bài lab AWS Transit Gateway để kết thúc Module 02 về mạng.
- Tìm hiểu sâu về Amazon EC2 (Instance Type, AMI, EBS, Instance Store, User Data, Metadata và Auto Scaling).
- Thực hành AWS Backup cho EC2 và nắm vững quy trình backup/restore.
- Tìm hiểu và thực hành triển khai AWS Storage Gateway và cấu hình File Share.
- Nắm vững các tính năng Amazon S3 (Static Website Hosting, tích hợp CloudFront, Bucket Versioning và Cross-Region Replication).
- Nắm tổng quan các dịch vụ Storage AWS và bắt đầu quy trình migrate máy ảo (VM) từ On-premises lên AWS.

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
      <td style="text-align:center;">27/04/2026</td>
      <td>
        <ul>
          <li> <strong>EC2 cơ bản:</strong> Tìm hiểu Instance Type, AMI, Key Pair. </li>
          <li> <strong>EC2 nâng cao (Phần 1):</strong> Thực hành Elastic Block Store (EBS), Instance Store, User Data (bootstrap script), EC2 Metadata Service. </li>
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
      <td style="text-align:center;">28/04/2026</td>
      <td>
        <ul>
          <li> <strong>EC2 nâng cao (Phần 2):</strong> Thực hành EC2 Auto Scaling, EFS, FSx, Lightsail, MGN. </li>
          <li> <strong>Transit Gateway:</strong> Tạo Transit Gateway, tạo Attachment và Route Table, cập nhật Route Table cho VPC. </li>
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
      <td style="text-align:center;">29/04/2026</td>
      <td>
        <ul>
          <li> <strong>Storage Gateway (Trọn gói):</strong> Tạo S3 Bucket, tạo EC2 cho Storage Gateway, tạo và cấu hình Storage Gateway, cấu hình File Share. </li>
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
      <td style="text-align:center;">30/04/2026</td>
      <td>
        <ul>
          <li> <strong>AWS Backup:</strong> Triển khai hạ tầng Backup, tạo Backup Plan, kiểm tra Restore từ Recovery Point, cấu hình thông báo cho Backup. </li>
          <li> <strong>S3 Static Website Hosting:</strong> Tạo bucket, cấu hình Public Access và Bucket Policy, cấu hình CloudFront và kiểm tra phân phối nội dung. </li>
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
      <td style="text-align:center;">01/05/2026</td>
      <td>
        <ul>
          <li> <strong>S3 nâng cao:</strong> Thực hành Bucket Versioning, Lifecycle Object và Cross-Region Replication. </li>
          <li> <strong>Ôn tập lý thuyết:</strong> Tổng quan Module 04 Storage (S3 nâng cao, Snow Family, Storage Gateway, Backup). </li>
          <li> <strong>Migration:</strong> Bắt đầu quy trình migrate VM (VMware Workstation, Export VM, Upload và Import lên AWS). </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://cloudjourney.awsstudygroup.com/vi/2-migrate/">Tài liệu của FCAJ</a> </li>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Kết quả đạt được tuần 2:

- **Hạ tầng mạng & Máy chủ EC2**: Hoàn thành thiết lập AWS Transit Gateway (Attachment nhiều VPC, Route Table liên VPC). Tìm hiểu các kiến thức về EC2 (Instance Type, AMI, Key Pair, EBS, Instance Store, User Data, Metadata, Auto Scaling) cùng các dịch vụ liên quan (EFS, FSx, Lightsail, AWS MGN).

- **Lưu trữ, Backup & Storage Gateway**: Tìm hiểu các dịch vụ lưu trữ AWS (S3, Glacier, Snow Family, Storage Gateway, AWS Backup). Thực hành triển khai hạ tầng AWS Backup (Backup Plan, Recovery Point, restore EC2) và cấu hình AWS Storage Gateway File Share với Amazon S3.

- **Amazon S3 & Phân phối nội dung CloudFront**: Tìm hiểu cơ chế quản lý dữ liệu S3 (Bucket Policy, Public Access, Storage Class, Access Point, Versioning, Lifecycle, CRR). Thực hành triển khai S3 Static Website Hosting kết hợp với CloudFront Distribution.

- **Dịch chuyển máy ảo (Migration) & Troubleshooting**: Thực hành quy trình migrate VM từ On-premises lên AWS (export VM từ VMware Workstation, upload S3, import AMI và launch EC2). Học hỏi và rèn luyện xử lý các sự cố thực tế (Transit Gateway Attachment, EBS, Bucket Policy, CloudFront origin, S3 Replication, VM Import).

- **Tiến độ học tập**: Đã hoàn thành theo dõi và học toàn bộ từ video 65 đến 120 trong series *First Cloud Journey Bootcamp 2025* của AWS Study Group.


