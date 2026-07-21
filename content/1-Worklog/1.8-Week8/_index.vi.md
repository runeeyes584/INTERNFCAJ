---
title: "Worklog tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

- Phát triển WebSocket realtime, xây dựng hệ thống ghép trận đấu và ruling của game.

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
      <td style="text-align:center;">08/06/2026</td>
      <td>
        <ul>
          <li> <strong>Cấu hình WebSocket:</strong> Thiết lập kết nối socket và xây dựng chức năng truyền thông tin thời gian thực giữa hai người chơi. </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">3</td>
      <td style="text-align:center;">09/06/2026</td>
      <td>
        <ul>
          <li> <strong>Hệ thống ghép phòng PvP:</strong> Phát triển tính năng tạo phòng thi đấu và cơ chế ghép cặp ngẫu nhiên cho người chơi trong chế độ đối kháng (PvP). </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">4</td>
      <td style="text-align:center;">10/06/2026</td>
      <td>
        <ul>
          <li> <strong>Xử lý Logic Trò chơi:</strong> Thiết kế và lập trình các hàm xử lý logic nội tại, bao hàm toàn bộ các hành động có thể xảy ra trong quá trình diễn ra một trận đấu. </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">5</td>
      <td style="text-align:center;">11/06/2026</td>
      <td>
        <ul>
          <li> <strong>Cơ chế tính điểm Elo & Matching:</strong> Viết logic ghép cặp dựa trên điểm xếp hạng (Elo), đồng thời xây dựng công thức cộng/trừ điểm theo tiêu chuẩn thể thức Thụy Sĩ. </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td style="text-align:center;">6</td>
      <td style="text-align:center;">12/06/2026</td>
      <td>
        <ul>
          <li> <strong>Kiểm thử & Sửa lỗi (Bug Fixing):</strong> Tiến hành thử nghiệm toàn diện hệ thống, phát hiện và khắc phục các lỗi (bug) liên quan đến logic, luật chơi (ruling) và cơ chế cơ bản. </li>
        </ul>
      </td>
      <td></td>
    </tr>
  </tbody>
</table>

### Kết quả đạt được:

- Hệ thống WebSocket hoạt động ổn định, cho phép hai người chơi kết nối theo thời gian thực.
- Hoàn thiện hệ thống ghép phòng ngẫu nhiên và tính toán điểm Elo sau mỗi trận đấu.
- Các hàm logic cốt lõi của game (ruling) đã được triển khai và kiểm thử thành công.
