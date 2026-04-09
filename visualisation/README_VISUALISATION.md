# :bar_chart: Trực quan hóa dữ liệu trên Power BI

## :link: Bạn có thể truy cập phiên bản công khai của báo cáo tại liên kết sau: [Báo cáo Power BI](https://app.powerbi.com/view?r=eyJrIjoiMDJlNjAwZTEtNTVjOS00Njc3LWJlMTItNGYxM2FmZmM3YjhkIiwidCI6ImVkOGYxNjczLTM4OTAtNGRiNC1hM2YwLTk3YWQ5NDI3Yzc0ZiIsImMiOjEwfQ%3D%3D)

## :bulb: Cấu trúc Dashboard
Báo cáo được thiết kế gồm 4 phân mục (pages) chuyên biệt, giúp người dùng đi từ cái nhìn tổng thể đến chi tiết từng nhóm mặt hàng:

### 1. Tổng Quan Chung (Overview)
* **Mục tiêu:** Cung cấp bức tranh toàn cảnh về sự tăng trưởng và độ biến động của thị trường
* **Thành phần chính:**
    * **KPI Cards:** Hiển thị mặt hàng tăng trưởng mạnh nhất (Nước sinh hoạt) và mặt hàng dao động mạnh nhất (Thịt heo).
    * **Biểu đồ so sánh:** So sánh trực diện biên độ dao động trung bình (%) giữa các ngành hàng để xác định mức độ rủi ro.
    * **Bộ lọc (Slicers):** Cho phép tùy chỉnh mốc thời gian từ 2005 đến 2025 để quan sát biến động theo từng giai đoạn kinh tế

### 2. Nhóm Lương Thực - Thực Phẩm
* **Mục tiêu:** Phân tích sâu về hai mặt hàng thiết yếu nhất là Gạo và Thịt heo
* **Kỹ thuật Visualisation:** * **Biểu đồ chênh lệch:** Làm nổi bật khoảng cách giữa giá lợn sống và giá bán lẻ (lên tới **52.00K VNĐ**), bóc tách ảnh hưởng của chi phí trung gian
    * **Line & Clustered Column Chart:** Kết hợp giữa giá trị tuyệt đối và tỷ lệ tăng trưởng qua từng năm để thấy rõ các cú sốc giá (ví dụ: năm 2008 của Gạo).

### 3. Nhóm Tài Sản Tích Trữ (Vàng & Bạc)
* **Mục tiêu:** Theo dõi hành trình giá trị của các kênh trú ẩn an toàn
* **Kỹ thuật Visualisation:**
    * **Waterfall Chart (Biểu đồ thác nước):** Thể hiện sự bồi đắp giá trị của Vàng và Bạc qua từng năm, làm rõ những năm có sự bùng nổ giá.
    * **Dấu ấn dữ liệu:** Ghi nhận đỉnh lịch sử của Vàng tại mức **131.77 triệu VNĐ/lượng**

### 4. Nhóm Đi Lại & Sinh Hoạt (Xăng, Điện, Nước)
* **Mục tiêu:** Phân tích các mặt hàng đầu vào của nền kinh tế và chi phí cố định của hộ gia đình.
* **Kỹ thuật Visualisation:**
    * **Area Chart (Biểu đồ vùng):** Thể hiện rõ vùng biến động của giá xăng dầu, đặc biệt là giai đoạn sụt giảm sâu năm 2020 và bật tăng mạnh năm 2022.
    * **Combined Chart:** So sánh lộ trình tăng giá hình bậc thang của Điện và Nước sinh hoạt dưới sự điều tiết của Nhà nước

