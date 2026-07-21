---
title: "Worklog tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

- Deploy trang web lên Amazon S3 & CloudFront và nâng cấp giao diện UI.

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
      <td style="text-align:center;">22/06/2026</td>
      <td>
        <ul>
          <li> <strong>Deploy Web tĩnh lên S3 & CloudFront:</strong> Triển khai bản build ứng dụng web lên Amazon S3 Bucket và cấu hình mạng phân phối nội dung CloudFront (CDN) để tối ưu hóa tốc độ tải trang. </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">3</td>
      <td style="text-align:center;">23/06/2026</td>
      <td>
        <ul>
          <li> <strong>Cấu hình Domain & Bảo mật HTTPS:</strong> Thiết lập tên miền (domain) tùy chỉnh và tích hợp chứng chỉ bảo mật SSL/HTTPS thông qua AWS Certificate Manager (ACM) để bảo đảm an toàn dữ liệu. </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">4</td>
      <td style="text-align:center;">24/06/2026</td>
      <td>
        <ul>
          <li> <strong>Hoàn thiện Giao diện & Sửa lỗi UI:</strong> Rà soát tổng thể, hoàn thiện thiết kế giao diện mới và xử lý dứt điểm các lỗi hiển thị (UI bugs) còn tồn đọng. </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">5</td>
      <td style="text-align:center;">25/06/2026</td>
      <td>
        <ul>
          <li> <strong>Tối ưu hóa Tài nguyên (Assets):</strong> Thực hiện nén, tối ưu hóa dung lượng hình ảnh, icon và các tài nguyên tĩnh khác nhằm nâng cao tối đa hiệu năng của trang web. </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">6</td>
      <td style="text-align:center;">26/06/2026</td>
      <td>
        <ul>
          <li> <strong>Kiểm thử Quy trình CI/CD:</strong> Kiểm tra, đánh giá toàn bộ luồng tích hợp và triển khai liên tục (CI/CD), đảm bảo quy trình deploy tự động hoạt động trơn tru cho các bản cập nhật sau này. </li>
        </ul>
      </td>
      <td></td>
    </tr>
  </tbody>
</table>

### Kết quả đạt được:

- Ứng dụng web được phân phối toàn cầu với tốc độ cao nhờ S3 và CloudFront.
- Khắc phục hoàn toàn các lỗi về giao diện UI, đem lại trải nghiệm mượt mà cho người chơi.
- Hiệu năng tải trang được cải thiện đáng kể thông qua việc tối ưu asset.
