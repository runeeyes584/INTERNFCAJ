---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---
### Mục tiêu tuần 3:

- Thực hành AWS Storage Gateway và Amazon FSx (SSD/HDD Multi‑AZ).
- Thực hành Amazon S3 Static Website Hosting, CloudFront, S3 Versioning và Replication đa vùng.
- Tìm hiểu lý thuyết về Bảo mật & Định danh trên AWS: IAM, Cognito, AWS Organizations, Identity Center và KMS.
- Thực hành tự động hoá thao tác trên EC2 bằng AWS Lambda và gửi cảnh báo qua Slack Incoming Webhooks.
- Tìm hiểu cách quản lý tag tài nguyên, Resource Groups và cấu hình phân quyền IAM dựa trên tag (Tag‑based access control).

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
      <td style="text-align:center;">04/05/2026</td>
      <td>
        <ul>
          <li> <strong>Storage Gateway:</strong> Tạo Storage Gateway, File Share và mount File Share vào máy local. </li>
          <li> <strong>Amazon FSx:</strong> Tạo SSD/HDD Multi‑AZ file system, cấu hình quotas, shadow copies, co giãn throughput/storage. </li>
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
      <td style="text-align:center;">05/05/2026</td>
      <td>
        <ul>
          <li> <strong>Amazon S3 & CloudFront:</strong> Cấu hình Static Website, chặn public access và tích hợp CloudFront CDN, cấu hình Versioning, di chuyển object, Replication đa vùng (CRR). </li>
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
      <td style="text-align:center;">06/05/2026</td>
      <td>
        <ul>
          <li> <strong>Bảo mật & Định danh:</strong> Tìm hiểu Mô hình trách nhiệm chung, IAM, Cognito, AWS Organizations, Identity Center, KMS. </li>
          <li> <strong>Security Hub:</strong> Kích hoạt và theo dõi điểm tiêu chuẩn bảo mật trên AWS. </li>
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
      <td style="text-align:center;">07/05/2026</td>
      <td>
        <ul>
          <li> <strong>Tích hợp Slack & Lambda:</strong> Tạo VPC, Security Group, EC2 Instance; cấu hình Slack Incoming Webhooks. </li>
          <li> <strong>Tự động hóa:</strong> Tạo Lambda Role, viết script Lambda bật/tắt EC2 tự động. </li>
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
      <td style="text-align:center;">08/05/2026</td>
      <td>
        <ul>
          <li> <strong>Quản lý tag & Resource Groups:</strong> Lọc tài nguyên bằng tag qua Console và CLI, quản lý Resource Groups. </li>
          <li> <strong>IAM nâng cao:</strong> Tạo IAM User, Policy, Role, thực hành Switch Role và cấu hình chính sách phân quyền dựa trên tag (Tag‑based access control) cho EC2 tại Tokyo và North Virginia. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://cloudjourney.awsstudygroup.com/">Tài liệu của FCAJ</a> </li>
          <li> <a href="https://www.youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i">AWS Study Group Playlist</a> </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Kết quả đạt được tuần 3:

- **Lưu trữ mạng Storage Gateway & Amazon FSx**: Thực hành thiết lập Storage Gateway, tạo File Share và mount thành công lên thiết bị local. Thực hành tạo hệ thống tệp Amazon FSx (SSD/HDD Multi‑AZ), thử nghiệm cấu hình quotas, shadow copies, data deduplication và kiểm tra co giãn dung lượng/băng thông.

- **Tối ưu lưu trữ S3 & Phân phối nội dung CloudFront**: Thực hành lưu trữ web tĩnh trên S3, quản lý chặn truy cập công khai, tích hợp CloudFront Distribution, quản lý phiên bản (Versioning), di chuyển object và thiết lập Replication đa vùng (CRR).

- **Bảo mật & Quản lý định danh trên AWS**: Tìm hiểu Mô hình trách nhiệm chung, IAM, Cognito, AWS Organizations, Identity Center, KMS và thực hành theo dõi các tiêu chuẩn bảo mật trên AWS Security Hub.

- **Tự động hóa & Phân quyền nâng cao**: Thực hành viết hàm Lambda bật/tắt EC2 tự động và nhận thông báo qua Slack Incoming Webhooks. Thực hành quản lý tag tài nguyên qua Console/CLI, tạo Resource Group, cấu hình Switch Role và kiểm tra phân quyền IAM dựa trên tag (Tag-based access control).

- **Tiến độ học tập**: Đã hoàn thành theo dõi và học toàn bộ từ video 121 đến 186 trong series *First Cloud Journey Bootcamp 2025* của AWS Study Group.






