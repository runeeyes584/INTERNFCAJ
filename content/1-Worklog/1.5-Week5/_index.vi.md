---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

- Tạo và cấu hình tài khoản IAM User để chia sẻ môi trường làm việc AWS an toàn cho các thành viên trong nhóm dự án.
- Tìm hiểu và nghiên cứu dịch vụ AWS Cognito (User Pools & Identity Pools) chuẩn bị cho tính năng xác thực người dùng trong milestone project.

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
      <td style="text-align:center;">18/05/2026</td>
      <td>
        <ul>
          <li> <strong>IAM User & Phân quyền nhóm:</strong> Tạo và cấu hình các tài khoản IAM User, thiết lập IAM Group và phân quyền truy cập an toàn cho các thành viên trong nhóm dự án. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users.html">Tài liệu AWS IAM User Guide</a> </li>
          <li> <a href="https://cloudjourney.awsstudygroup.com/">Tài liệu của FCAJ</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">3</td>
      <td style="text-align:center;">19/05/2026</td>
      <td>
        <ul>
          <li> <strong>Quản lý quyền truy cập nhóm:</strong> Cấu hình chính sách bảo mật (MFA, Password Policy) cho tài khoản IAM User của nhóm và kiểm tra khả năng đăng nhập/làm việc chung trên Console. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html">AWS Password Policy Guide</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">4</td>
      <td style="text-align:center;">20/05/2026</td>
      <td>
        <ul>
          <li> <strong>Tìm hiểu AWS Cognito (Phần 1):</strong> Nghiên cứu tổng quan về dịch vụ AWS Cognito, khái niệm User Pools (quản lý người dùng, đăng ký, đăng nhập) cho dự án. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html">AWS Cognito User Pools Docs</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">5</td>
      <td style="text-align:center;">21/05/2026</td>
      <td>
        <ul>
          <li> <strong>Tìm hiểu AWS Cognito (Phần 2):</strong> Tìm hiểu khái niệm Identity Pools (xác thực và phân quyền truy cập tài nguyên AWS) và cơ chế tích hợp OAuth2/JWT. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-identity.html">AWS Cognito Identity Pools Docs</a> </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center;">6</td>
      <td style="text-align:center;">22/05/2026</td>
      <td>
        <ul>
          <li> <strong>Thử nghiệm Cognito:</strong> Lập tài liệu cấu hình Cognito User Pools mẫu và kiểm thử luồng xác thực người dùng ban đầu chuẩn bị cho milestone project. </li>
        </ul>
      </td>
      <td>
        <ul>
          <li> <a href="https://docs.aws.amazon.com/cognito/">AWS Cognito Developer Guide</a> </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Kết quả đạt được tuần 5:

- **Quản trị tài khoản & Phân quyền nhóm**: Cấu hình thành công các tài khoản IAM User và IAM Group với các chính sách bảo mật phù hợp, giúp các thành viên trong nhóm truy cập và làm việc chung hiệu quả trên môi trường AWS.

- **Nghiên cứu AWS Cognito**: Tìm hiểu cơ chế hoạt động của AWS Cognito bao gồm User Pools (đăng ký, đăng nhập, quản lý người dùng) và Identity Pools (cấp quyền truy cập tài nguyên), nắm rõ luồng xác thực chuẩn bị áp dụng cho dự án.





