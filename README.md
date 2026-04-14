# :bar_chart: **Phân tích và Trực quan hóa Biến động Giá cả các Mặt hàng Thiết yếu tại Việt Nam 2005 - 2025 với Power BI**
![vst](https://drive.google.com/thumbnail?id=1gRj-l1Nu3AQYSNrnMqz9t81jka7zkS_u&sz=w1200)

# :mag_right: **1. Tổng quan dự án**

Dự án này là một bài phân tích toàn diện về sự biến động giá cả của các mặt hàng thiết yếu tại Việt Nam trong suốt gần hai thập kỷ (2005 - 2025). Thay vì tập trung vào doanh thu của một doanh nghiệp, dự án tập trung vào 4 trang báo cáo xu hướng giá cả và bóc tách thông tin qua nhiều chiều dữ gồm 3 nhóm chính:

- Nhóm 1: `Lương thực - thực phẩm`. Đại diện là `Gạo` (lương thực gốc tại Việt Nam) và `Thịt heo` (nguồn đạm động vật chủ yếu của người Việt)
- Nhóm 2: `Tài sản tích trữ`. Đại diện là `Vàng` và `Bạc` (kênh đầu tư truyền thống phổ biến tại Việt Nam)
- Nhóm 3: `Đi lại - sinh hoạt`. Đại diện là `Xăng`, `Điện sinh hoạt` và `Nước sinh hoạt` (những tiện ích cơ bản không thể thiếu, gắn liền với mọi hoạt động thường ngày của mọi hộ gia đình tại Việt Nam)


# :high_brightness: **2. Dự án thể hiện các kỹ năng phân tích dữ liệu trọng tâm:**

>1. **Thu thập và định nghĩa dữ liệu**
>2. **Tiền xử lý dữ liệu** 
>3. **Trực quan hóa dữ liệu bằng Power BI**
>4. **Phân tích dữ liệu** 


# :pushpin: **3. Phân tích và Thực hiện**

Dự án được triển khai nhằm bóc tách bản chất của từng nhóm mặt hàng. Tiến hành tìm kiếm thu thập dữ liệu lịch sử trong giai đoạn 20 năm (2005 – 2025) từ nhiều nguồn uy tín. Phân loại 7 mặt hàng vào 3 nhóm chính: Lương thực - Thực phẩm, Đi lại - Sinh hoạt và Tài sản tích trữ để dễ dàng so sánh biên độ biến động giữa nhóm tiêu dùng thiết yếu và nhóm đầu tư

> :file_folder: **Quản lý dữ liệu:** Toàn bộ dữ liệu và file tài liệu giải thích chi tiết về quy trình xử lý dữ liệu được lưu trữ tại thư mục **[data](./data/)**

Tóm tắt thực hiện như sau:

## 1. Thu thập dữ liệu
* **Nhóm Lương thực, thực phẩm (Gạo, Thịt heo):**
  > Trích xuất dữ liệu từ **Viện Chính sách và Chiến lược Phát triển Nông nghiệp Nông thôn (IPSARD)**. Đây là nguồn tin cậy về giá nông sản hàng ngày/tuần. Website: [agro.gov.vn](https://agro.gov.vn)
  
* **Nhóm Đi lại, sinh hoạt (Xăng, Điện và Nước sinh hoạt):**
  > * **Petrolimex:** Cung cấp dữ liệu lịch sử giá xăng dầu qua các kỳ điều hành. Website: [petrolimex.com.vn](https://www.petrolimex.com.vn)
  > * **Tập đoàn Điện lực Việt Nam (EVN):** Biểu giá bán lẻ điện cho sinh hoạt công khai theo từng thời kỳ. Website: [evn.com.vn](https://www.evn.com.vn)
  > * **Nước sinh hoạt:** Vì nước sinh hoạt không có một tập đoàn duy nhất quản lý toàn quốc như điện hay xăng dầu, nên dữ liệu được tổng hợp từ các Quyết định về biểu giá nước sạch sinh hoạt của UBND TP.HCM (hoặc địa phương tương ứng) qua các thời kỳ. Tra cứu tại **Thư viện Pháp luật**.  Website: [thuvienphapluat.vn](https://thuvienphapluat.vn)
      
* **Nhóm Tài sản tích trữ (Vàng, Bạc):**
  > Dữ liệu được trích xuất từ nền tảng tài chính uy tín thế giới. Website: [investing.com](https://vn.investing.com/)

## 2. Xử lý dữ liệu 
* Sử dụng **Excel & Power Query** để làm sạch, thống nhất đơn vị tính và chuẩn hóa mốc thời gian.
* Thực hiện các phép toán chuyển đổi phức tạp, điển hình là quy đổi giá kim loại quý từ đơn vị quốc tế (USD/oz) sang đơn vị nội địa (Triệu VNĐ/lượng)
* Xây dựng các cột tính toán bổ sung để đo lường biên độ dao động (%) và tốc độ tăng trưởng (%) qua từng năm nhằm phục vụ phân tích sâu.
* **Chi tiết quy trình xử lý dữ liệu xem tại thư mục** [data](./data/)
  
## 3. Trực quan hóa và phân tích chuyên sâu bằng Power BI

Hệ thống báo cáo được xây dựng không chỉ để hiển thị dữ liệu mà còn nhằm kể những câu chuyện đằng sau các con số (Data Storytelling). 

* **Mô hình dữ liệu (Model View):** Thiết lập cấu trúc dữ liệu tối ưu để liên kết 7 mặt hàng thiết yếu, đảm bảo tính đồng bộ và chính xác khi tương tác với các bộ lọc thời gian.

![Model View](https://drive.google.com/uc?export=view&id=1XVhOD6SrzxsBot-g7H5Dfdte2KSJVdKL)

* **Ứng dụng DAX nâng cao:** Triển khai các Measures phức tạp để bóc tách các chỉ số như: chênh lệch giá lợn sống/bán lẻ, biên độ dao động thực tế và tốc độ tăng trưởng lũy kế qua 20 năm.


# :pushpin: 4. **Các kết quả phân tích chính (Key Insights)**

Báo cáo bóc tách các điểm xoay chiều của thị trường gắn liền với các biến động vĩ mô và địa chính trị trong suốt 20 năm qua tại Việt Nam:

## :chart_with_upwards_trend: **Tác động từ các cuộc khủng hoảng kinh tế**
  * **Khủng hoảng tài chính 2008:** Ghi nhận sự bùng nổ của **Gạo** và **Xăng** (đạt đỉnh tăng trưởng). Lạm phát toàn cầu thời điểm này đã đẩy giá lương thực và năng lượng lên mức chưa từng có tiền lệ.
  * **Đại dịch COVID-19 (2019 - 2021):**
      >* **Xăng dầu:** Giá giảm sâu kỷ lục (đặc biệt là năm 2020) do các lệnh phong tỏa diện rộng do bệnh dịch COVID 19, nhu cầu di chuyển gần như bằng không.
      >* **Lương thực (Gạo, Thịt heo):** Tăng mạnh do tâm lý tích trữ đồ ăn do bệnh dịch. Riêng Thịt heo chịu tác động kép sau dịch tả lợn châu Phi, đẩy giá bán lẻ lên mức cao nhất lịch sử.

## :meat_on_bone: **Insight về chuỗi cung ứng thực phẩm**
  * **Nghịch lý giá Thịt heo:** Khoảng cách giữa giá lợn hơi tại trại và giá bán lẻ ngày càng giãn rộng (đỉnh điểm chênh lệch lên đến **52.00K VNĐ/kg** vào năm 2022). Điều này cho thấy rủi ro và lợi nhuận thị trường chủ yếu nằm ở khâu trung gian và người bán chứ không phải người chăn nuôi.

## :bank: **Tài sản tích trữ & Vai trò điều tiết**
  * **Vàng:** Luôn tăng vọt trong mọi giai đoạn bất ổn (2008, 2020, 2022). Mức đỉnh **131.77 triệu VNĐ/lượng** phản ánh rõ áp lực lạm phát và tâm lý bảo toàn vốn của người dân Việt Nam.
  * **Bàn tay điều tiết của Nhà nước:** Sự đối lập hoàn toàn giữa biến động "ziczac" theo giá thế giới của **Xăng** và biểu đồ hình bậc thang của **Điện/Nước** minh chứng cho vai trò giữ ổn định an sinh xã hội của Chính phủ trước các cú sốc thị trường tự do.

## :rocket: **Sức tăng trưởng "âm thầm"**
  * **Nước sinh hoạt:** Dù không gây sốc như Vàng hay Xăng trong ngắn hạn, nhưng đây lại là mặt hàng có sức tăng bền bỉ nhất (**~11%/năm**), tạo áp lực chi phí sinh hoạt dài hạn cực lớn cho các hộ gia đình qua hai thập kỷ.

:books: **Xem chi tiết phân tích chuyên sâu và Data Storytelling cho từng Dashboard tại thư mục** [Visualisation](./visualisation/)


# :link: 5. **Liên kết chính**

Để thuận tiện cho việc theo dõi, dự án được chia thành các phân khu tài liệu chi tiết sau:

* **Báo cáo Power BI (Bản công khai):** [Truy cập trực tiếp tại đây](https://app.powerbi.com/view?r=eyJrIjoiMDJlNjAwZTEtNTVjOS00Njc3LWJlMTItNGYxM2FmZmM3YjhkIiwidCI6ImVkOGYxNjczLTM4OTAtNGRiNC1hM2YwLTk3YWQ5NDI3Yzc0ZiIsImMiOjEwfQ%3D%3D). Bạn có thể tương tác trực tiếp với các biểu đồ và bộ lọc thời gian.

* **Tài liệu Dữ liệu & Quy trình ETL:** [Chi tiết tại thư mục data](./data/). Chứa toàn bộ dữ liệu, nguồn gốc và các công thức xử lý từ Excel sang Power BI.

* **Tài liệu Trực quan hóa & Data Storytelling:** [Chi tiết tại thư mục visualisation](./visualisation/). Phân tích chuyên sâu về ý nghĩa các chỉ số và các câu chuyện kinh tế đằng sau mỗi Dashboard.



