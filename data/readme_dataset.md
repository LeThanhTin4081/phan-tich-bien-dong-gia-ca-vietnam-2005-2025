# :file_folder: Dữ liệu dự án (Data Sources & Processing)

Thư mục này chứa file dữ liệu tên `Dulieu_BienDongGia_ThietYeu_VN_2005-2025.xlsx` đã qua xử lý phục vụ cho việc xây dựng Dashboard Power BI. Dữ liệu bao quát giai đoạn 20 năm (2005 - 2025) tại thị trường Việt Nam cho 7 mặt hàng thiết yếu.

## :page_with_curl: 1. Nguồn dữ liệu (Data Sources)

Dữ liệu được tổng hợp và trích xuất từ các nguồn uy tín để đảm bảo tính xác thực:

### :ear_of_rice: Nhóm Lương thực - Thực phẩm
* **Gạo & Thịt heo:** Số liệu từ Viện Chính sách và Chiến lược Phát triển Nông nghiệp Nông thôn (IPSARD).

### :car: Nhóm Đi lại - Sinh hoạt
* **Xăng dầu:** Lịch sử giá từ Tập đoàn Xăng dầu Việt Nam (Petrolimex).
* **Điện sinh hoạt:** Biểu giá bán lẻ điện từ Tập đoàn Điện lực Việt Nam (EVN).
* **Nước sinh hoạt:** Dữ liệu từ các đơn vị cấp nước và bảng giá niêm yết của địa phương.

### :moneybag: Nhóm Tài sản tích trữ
* **Vàng & Bạc:** Trích xuất từ nền tảng tài chính Investing.com và quy đổi theo tỷ giá nội địa Việt Nam.

---

## :open_file_folder: 2. Cấu trúc các tệp dữ liệu

| Tên file | Nội dung | Đơn vị tính |
| :--- | :--- | :--- |
| `Gạo` | Biến động giá gạo thường qua các năm | VNĐ/kg |
| `Thịt Heo` | So sánh giá lợn hơi và giá bán lẻ thực tế | VNĐ/kg |
| `Xăng` | Lịch sử giá xăng RON 95 | VNĐ/lít |
| `Điện` | Giá điện bán lẻ bình quân qua các thời kỳ | VNĐ/kWh |
| `Nước sinh hoạt` | Giá nước sạch định mức hộ gia đình | VNĐ/m³ |
| `Vàng` | Giá vàng miếng SJC (đã quy đổi) | Triệu VNĐ/lượng |
| `Bạc` | Giá bạc (quy đổi từ giá quốc tế) | Triệu VNĐ/lượng |

---

## :speaker: 3. Từ điển dữ liệu (Data Dictionary)

Mỗi tệp dữ liệu được chuẩn hóa với các trường thông tin sau:

* **Năm:** Mốc thời gian từ 2005 đến 2025.
* **Giá thấp nhất / Giá cao nhất:** Biên độ giá ghi nhận trong năm.
* **Giá trung bình:** Giá trị đại diện dùng cho các phân tích xu hướng và biểu đồ đường.
* **Biên độ dao động (%):** Chỉ số đo lường mức độ biến động giá trong năm.
* **Tăng trưởng (%):** Tốc độ thay đổi giá so với năm liền kề trước đó.

---

## :pushpin: 4. Quy trình xử lý dữ liệu (ETL Process)

### Sử dụng công thức Excel 
Thực hiện tính toán các chỉ số bổ sung trực tiếp trong file dữ liệu để làm rõ bản chất biến động của thị trường:

* **Tốc độ tăng trưởng hàng năm (YoY):**
  Dùng để đo lường mức độ trượt giá hoặc tăng giá của mặt hàng so với năm trước.

$$\text{Tốc độ tăng trưởng (\%)} = \frac{\text{Giá}_{\text{Năm } n} - \text{Giá}_{\text{Năm } n-1}}{\text{Giá}_{\text{Năm } n-1}} \times 100$$

* **Biên độ dao động giá trong năm:**
  Xác định khoảng cách chênh lệch giữa giá trần và giá sàn, phản ánh mức độ ổn định của mặt hàng.

$$\text{Biên độ dao động (VNĐ)} = \text{Giá}_{\text{Cao nhất}} - \text{Giá}_{\text{Thấp nhất}}$$

* **Quy đổi giá kim loại quý (Vàng & Bạc):**
  Quy đổi từ đơn vị quốc tế ($USD/oz$) về đơn vị phổ biến tại Việt Nam ($Triệu\ VNĐ/lượng$).

$$\text{Giá}_{\text{Lượng}} = \frac{\text{Giá}_{\text{Ounce}} \times 1.205 \times \text{Tỷ giá USD/VND}}{1,000,000}$$

*(Trong đó 1.205 là hệ số quy đổi chuẩn từ Ounce sang Lượng)*

