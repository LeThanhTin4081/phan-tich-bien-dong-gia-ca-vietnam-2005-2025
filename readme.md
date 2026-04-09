# :bar_chart: **Phân tích và Trực quan hóa Biến động Giá cả các Mặt hàng Thiết yếu tại Việt Nam 2005 - 2025 với Power BI**

## :mag_right: **1. Tổng quan dự án**

Dự án này là một bài phân tích toàn diện về sự biến động giá cả của các mặt hàng thiết yếu tại Việt Nam trong suốt gần hai thập kỷ (2005 - 2025). Thay vì tập trung vào doanh thu của một doanh nghiệp, dự án tập trung báo cáo xu hướng giá cả và bóc tách thông tin qua nhiều chiều dữ gồm 3 nhóm chính:

- Nhóm 1: `Lương thực - thực phẩm`. Đại diện là `Gạo` (lương thực gốc tại Việt Nam) và `Thịt heo` (nguồn đạm động vật chủ yếu của người Việt)
- Nhóm 2: `Tài sản tích trữ`. Đại diện là `Vàng` và `Bạc` (kênh đầu tư truyền thống phổ biến tại Việt Nam)
- Nhóm 3: `Đi lại - sinh hoạt`. Đại diện là `Xăng`, `Điện sinh hoạt` và `Nước sinh hoạt` (những tiện ích cơ bản không thể thiếu, gắn liền với mọi hoạt động thường ngày của mọi hộ gia đình tại Việt Nam)

## :high_brightness: **2. Dự án thể hiện các kỹ năng phân tích dữ liệu trọng tâm:**

>1. **Thu thập và định nghĩa dữ liệu**
>2. **Tiền xử lý dữ liệu** 
>3. **Trực quan hóa dữ liệu bằng Power BI**
>4. **Phân tích dữ liệu** 

## :pushpin: **3. Phân tích và Thực hiện**

Dự án được triển khai nhằm bóc tách bản chất của từng nhóm mặt hàng. Tiến hành tìm kiếm thu thập dữ liệu lịch sử trong giai đoạn 20 năm (2005 – 2025) từ nhiều nguồn uy tín. Bạn có thể xem dữ liệu tại thư mục [data](./data/). Chi tiết như sau

### 1. Thu thập dữ liệu
* Dữ liệu Nhóm Lương thực, thực phẩm (Gạo, Thịt heo):
  > * Viện Chính sách và Chiến lược Phát triển Nông nghiệp Nông thôn (IPSARD). Trang web thường có báo cáo giá nông sản hàng ngày/tuần. Websitetruy cập: [IPSARD](agro.gov.vn)
  
* Dữ liệu Nhóm Đi lại, sinh hoạt (Xăng, Điện và Nước sinh hoạt):
  >* Petrolimex: Đây là nguồn tốt nhất cho dữ liệu lịch sử giá xăng. Website truy cập: [Petrolimex](petrolimex.com.vn)
  >* Tập đoàn Điện lực Việt Nam (EVN): EVN công bố công khai các biểu giá bán lẻ điện cho sinh hoạt và sản xuất theo từng thời kỳ. Website truy cập: [EVN](evn.com.vn)
      
* Dữ liệu Nhóm Tài sản tích trữ (Vàng, Bạc):
  > * được trích xuất từ nền tảng tài chính uy tín hàng đầu thế giới. Websitetruy cập: [Investing](investing.com)

### 2. Phân nhóm chiến lược theo nhu cầu đời sống
* Phân loại 7 mặt hàng vào 3 nhóm chính: Lương thực - Thực phẩm, Đi lại - Sinh hoạt và Tài sản tích trữ dễ dàng so sánh biên độ biến động giữa nhóm tiêu dùng thiết yếu và nhóm đầu tư

### 3. Xử lý dữ liệu 
* Sử dụng Excel để làm sạch, thống nhất đơn vị tính và chuẩn hóa mốc thời gian cho toàn bộ bộ dữ liệu
* Thực hiện các phép toán chuyển đổi phức tạp, điển hình là quy đổi giá kim loại quý từ đơn vị quốc tế (USD/oz) sang đơn vị nội địa (Triệu VNĐ/lượng)
* Xây dựng các cột tính toán bổ sung để đo lường biên độ dao động (%) và tốc độ tăng trưởng (%) qua từng năm nhằm phục vụ phân tích sâu.
* 
### 4. Trực quan hóa và phân tích chuyên sâu bằng Power BI

Hệ thống báo cáo được xây dựng không chỉ để hiển thị dữ liệu mà còn nhằm kể những câu chuyện đằng sau các con số (Data Storytelling). 

* **Mô hình dữ liệu (Model View):** Thiết lập cấu trúc dữ liệu tối ưu để liên kết 7 mặt hàng thiết yếu, đảm bảo tính đồng bộ và chính xác khi tương tác với các bộ lọc thời gian.

![Model View](https://drive.google.com/uc?export=view&id=1XVhOD6SrzxsBot-g7H5Dfdte2KSJVdKL)

* **Ứng dụng DAX nâng cao:** Triển khai các Measures phức tạp để bóc tách các chỉ số như: chênh lệch giá lợn sống/bán lẻ, biên độ dao động thực tế và tốc độ tăng trưởng lũy kế qua 20 năm.

👉 **Xem chi tiết phân tích chuyên sâu và các câu chuyện dữ liệu (Data Storytelling) cho từng trang Dashboard tại đây:** [Thư mục Visualisation](./visualisation/README_VISUALISATION.md)

## :pushpin: **4. Các kết quả phân tích chính**

* **Mặt hàng có sức tăng trưởng bền bỉ nhất:** Nước sinh hoạt dẫn đầu với mức tăng trưởng trung bình hàng năm khoảng **10.85%**
* **Mặt hàng biến động mạnh nhất:** Thịt heo ghi nhận biên độ dao động trung bình cao nhất (**40.45%**), cho thấy sự nhạy cảm cực lớn với các yếu tố thị trường và dịch bệnh
* **Đỉnh lịch sử của tài sản tích trữ:** Vàng thiết lập kỷ lục tại mức **131.77 triệu VNĐ/lượng**, phản ánh tâm lý tích trữ an toàn của người dân trong các giai đoạn lạm phát
* **Tác động của cú sốc năng lượng:** Giá xăng lập đỉnh tại **32.87K VNĐ/lít** vào năm 2022, minh chứng cho ảnh hưởng trực tiếp từ các xung đột địa chính trị toàn cầu đến kinh tế nội địa


  
## :link: 5. **Liên kết và Nguồn tham khảo**
* Link báo cáo Power BI link công khai:

