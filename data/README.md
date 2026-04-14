# :file_folder: Dữ liệu dự án (Data Sources & Processing)

Thư mục này chứa file dữ liệu tên `Dulieu_BienDongGia_ThietYeu_VN_2005-2025.xlsx` được lưu trữ, chuẩn hóa và tiền xử lý qua Excel, đảm bảo tính sẵn sàng trước khi nạp vào Power BI phục vụ cho việc xây dựng Dashboard. Dữ liệu bao quát giai đoạn 20 năm (2005 - 2025) tại thị trường Việt Nam cho 7 mặt hàng thiết yếu.

## :open_file_folder: 1. Cấu trúc các tệp dữ liệu

| Bảng| Nội dung | Đơn vị tính |
| :--- | :--- | :--- |
| `Gạo` | Biến động giá gạo thường qua các năm | VNĐ/kg |
| `Thịt Heo` | So sánh giá lợn nuôi và giá bán lẻ thực tế | VNĐ/kg |
| `Xăng` | Lịch sử giá xăng RON 95 | VNĐ/lít |
| `Điện` | Giá điện bán lẻ bình quân qua các thời kỳ | VNĐ/kWh |
| `Nước sinh hoạt` | Giá nước sạch định mức hộ gia đình | VNĐ/m³ |
| `Vàng` | Giá vàng (đã quy đổi từ giá quốc tế) | Triệu VNĐ/lượng |
| `Bạc` | Giá bạc (đã quy đổi từ giá quốc tế) | Triệu VNĐ/lượng |


## :page_with_curl: 2. Nguồn dữ liệu (Data Sources)

Toàn bộ dữ liệu được trích xuất từ các cổng thông tin chính thống và các nền tảng tài chính quốc tế, đảm bảo tính nhất quán và tính toàn vẹn trong suốt giai đoạn 2005-2025.

### :ear_of_rice: Nhóm Lương thực - Thực phẩm
>* **Gạo & Thịt heo:** Trích xuất dữ liệu từ **Viện Chính sách và Chiến lược Phát triển Nông nghiệp Nông thôn (IPSARD)**. Đây là nguồn tin cậy về giá nông sản hàng ngày/tuần. Website: [agro.gov.vn](https://agro.gov.vn)

### :car: Nhóm Đi lại - Sinh hoạt
>* **Xăng dầu:** * **Petrolimex:** Cung cấp dữ liệu lịch sử giá xăng dầu qua các kỳ điều hành. Website: [petrolimex.com.vn](https://www.petrolimex.com.vn)
  
>* **Điện sinh hoạt:** * **Tập đoàn Điện lực Việt Nam (EVN):** Biểu giá bán lẻ điện cho sinh hoạt công khai theo từng thời kỳ. Website: [evn.com.vn](https://www.evn.com.vn)

>* **Nước sinh hoạt:** Vì nước sinh hoạt không có một tập đoàn duy nhất quản lý toàn quốc như điện hay xăng dầu, nên dữ liệu được tổng hợp từ các Quyết định về biểu giá nước sạch sinh hoạt của UBND TP.HCM (hoặc địa phương tương ứng) qua các thời kỳ. Tra cứu tại **Thư viện Pháp luật**.  Website: [thuvienphapluat.vn](https://thuvienphapluat.vn)

### :moneybag: Nhóm Tài sản tích trữ
>* **Vàng & Bạc:** Dữ liệu được trích xuất từ nền tảng tài chính uy tín thế giới. Website: [investing.com](https://vn.investing.com/)


## :speaker: 3. Từ điển dữ liệu chi tiết (Data Dictionary)

Mỗi tệp dữ liệu được chuẩn hóa với các trường thông tin chi tiết như sau:

* **Năm:** Mốc thời gian từ 2005 đến 2025.
* **Giá thấp nhất / Giá cao nhất:** Biên độ giá ghi nhận trong năm.
* **Giá trung bình:** Giá trị đại diện dùng cho các phân tích xu hướng và biểu đồ đường.
* **Biên độ dao động (%):** Chỉ số đo lường mức độ biến động giá trong năm.
* **Tăng trưởng (%):** Tốc độ thay đổi giá so với năm liền kề trước đó.

Dưới đây là cấu trúc các trường thông tin (Columns) có trong tệp dữ liệu đã qua xử lý, được phân tách theo từng mặt hàng.

### :ear_of_rice: **Mặt hàng: Gạo**
*Dữ liệu phản ánh biến động giá bán lẻ gạo thường qua các năm.*

| Tên cột trong Excel | Ý nghĩa | Kiểu dữ liệu |
| :--- | :--- | :--- |
| **Năm** | Mốc thời gian từ 2005 đến 2025 | `Integer` |
| **Giá gạo thấp nhất (VNĐ/kg)** | Mức giá sàn thấp nhất ghi nhận trong năm | `Decimal` |
| **Giá gạo cao nhất (VNĐ/kg)** | Mức giá trần cao nhất ghi nhận trong năm | `Decimal` |
| **Giá trung bình gạo (VNĐ/kg)** | Giá trị đại diện phục vụ phân tích xu hướng | `Decimal` |
| **Biên độ dao động gạo (VNĐ/kg)** | Chênh lệch giá trị tuyệt đối (Max - Min) | `Decimal` |
| **Biên độ dao động gạo (%)** | Tỷ lệ phần trăm biến động trong năm | `Percentage` |
| **Tăng trưởng giá TB gạo (%)** | Tốc độ tăng trưởng so với năm trước (YoY) | `Percentage` |

### :pig: **Mặt hàng: Thịt Heo**
*Dữ liệu so sánh giữa giá lợn sống (nguyên liệu) và giá thịt lợn bán lẻ.*

| Tên cột trong Excel | Ý nghĩa | Kiểu dữ liệu |
| :--- | :--- | :--- |
| **Năm** | Mốc thời gian từ 2005 đến 2025 | `Integer` |
| **Giá lợn sống cao nhất (VNĐ/kg)** | Giá lợn hơi (giá xuất chuồng) cao nhất năm | `Decimal` |
| **Giá thịt lợn bán lẻ thấp nhất (VNĐ/kg)** | Mức giá bán lẻ thấp nhất tại thị trường | `Decimal` |
| **Giá thịt lợn bán lẻ cao nhất (VNĐ/kg)** | Mức giá bán lẻ cao nhất tại thị trường | `Decimal` |
| **Giá TB thịt lợn (VNĐ/kg)** | Giá trị trung bình bán lẻ trong năm | `Decimal` |
| **Biên độ dao động thịt lợn (VNĐ/kg)** | Chênh lệch giá bán lẻ tuyệt đối (Max - Min) | `Decimal` |
| **Biên độ dao động thịt lợn (%)** | Tỷ lệ phần trăm biến động giá bán lẻ | `Percentage` |
| **Tăng trưởng giá TB thịt lợn (%)** | Tốc độ tăng trưởng bán lẻ so với năm trước (YoY) | `Percentage` |

### :oil_drum: **Mặt hàng: Xăng dầu**
*Dữ liệu theo dõi biến động giá xăng RON 95 qua các kỳ điều chỉnh trong năm.*

| Tên cột trong Excel | Ý nghĩa | Kiểu dữ liệu |
| :--- | :--- | :--- |
| **Năm** | Mốc thời gian từ 2005 đến 2025 | `Integer` |
| **Giá thấp nhất (VNĐ/lít)** | Mức giá sàn thấp nhất trong năm | `Decimal` |
| **Giá cao nhất (VNĐ/lít)** | Mức giá trần cao nhất trong năm | `Decimal` |
| **Giá TB (VNĐ/lít)** | Giá trị trung bình phục vụ phân tích xu hướng | `Decimal` |
| **Biên độ dao động (VNĐ/lít)** | Chênh lệch giá tuyệt đối (Max - Min) | `Decimal` |
| **Biên độ dao động (%)** | Tỷ lệ phần trăm biến động giá trong năm | `Percentage` |
| **Tăng trưởng (%)** | Tốc độ tăng trưởng giá trung bình (YoY) | `Percentage` |

### :electric_plug: **Mặt hàng: Điện sinh hoạt**
*Dữ liệu dựa trên biểu giá bán lẻ điện bình quân qua các thời kỳ.*

| Tên cột trong Excel | Ý nghĩa | Kiểu dữ liệu |
| :--- | :--- | :--- |
| **Năm** | Mốc thời gian từ 2005 đến 2025 | `Integer` |
| **Giá (VNĐ/kWh)** | Mức giá bán lẻ điện bình quân | `Decimal` |
| **Tăng giá (VNĐ)** | Số tiền tăng tuyệt đối so với năm trước | `Decimal` |
| **Tăng trưởng (%)** | Tỷ lệ phần trăm tăng trưởng giá (YoY) | `Percentage` |

### :sweat_drops: **Mặt hàng: Nước sinh hoạt**
*Dữ liệu giá nước sạch định mức hộ gia đình theo từng giai đoạn.*

| Tên cột trong Excel | Ý nghĩa | Kiểu dữ liệu |
| :--- | :--- | :--- |
| **Năm** | Mốc thời gian từ 2005 đến 2025 | `Integer` |
| **Giá (VNĐ/m3)** | Đơn giá nước sạch theo định mức | `Decimal` |
| **Tăng giá (VNĐ/m3)** | Số tiền tăng tuyệt đối trên mỗi khối nước | `Decimal` |
| **Tăng trưởng (%)** | Tỷ lệ phần trăm tăng trưởng giá (YoY) | `Percentage` |

### :moneybag: **Mặt hàng: Vàng**
*Dữ liệu giá vàng miếng SJC đã được quy đổi từ giá quốc tế ($USD/oz$) về đơn vị nội địa.*

| Tên cột trong Excel | Ý nghĩa | Kiểu dữ liệu |
| :--- | :--- | :--- |
| **Năm** | Mốc thời gian báo cáo (2005 - 2025) | `Integer` |
| **Giá trung bình (Triệu VNĐ/lượng)** | Mức giá đại diện bình quân của năm | `Decimal` |
| **Giá đầu năm (Triệu VNĐ/lượng)** | Giá mở cửa phiên giao dịch đầu năm | `Decimal` |
| **Giá cao nhất (Triệu VNĐ/lượng)** | Mức giá trần ghi nhận trong năm | `Decimal` |
| **Giá thấp nhất (Triệu VNĐ/lượng)** | Mức giá sàn ghi nhận trong năm | `Decimal` |
| **Giá cuối năm (Triệu VNĐ/lượng)** | Giá chốt phiên giao dịch cuối năm | `Decimal` |
| **Thay đổi % TB** | Biến động % giá trung bình so với năm trước | `Percentage` |

### :moneybag: **Mặt hàng: Bạc**
*Dữ liệu giá bạc thế giới quy đổi về đơn vị Lượng tại Việt Nam.*

| Tên cột trong Excel | Ý nghĩa | Kiểu dữ liệu |
| :--- | :--- | :--- |
| **Năm** | Mốc thời gian báo cáo (2005 - 2025) | `Integer` |
| **Giá trung bình (Triệu VNĐ/lượng)** | Mức giá đại diện bình quân của năm | `Decimal` |
| **Giá đầu năm (Triệu VNĐ/lượng)** | Giá mở cửa phiên giao dịch đầu năm | `Decimal` |
| **Giá cao nhất (Triệu VNĐ/lượng)** | Mức giá trần ghi nhận trong năm | `Decimal` |
| **Giá thấp nhất (Triệu VNĐ/lượng)** | Mức giá sàn ghi nhận trong năm | `Decimal` |
| **Giá cuối năm (Triệu VNĐ/lượng)** | Giá chốt phiên giao dịch cuối năm | `Decimal` |
| **Thay đổi % cuối năm** | Biến động % giá chốt phiên so với cuối năm trước | `Percentage` |


## :pushpin: 4. Quy trình xử lý dữ liệu Excel 
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



