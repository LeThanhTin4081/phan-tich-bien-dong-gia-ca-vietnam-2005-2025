# :bar_chart: Trực quan hóa dữ liệu trên Power BI

## :link: Bạn có thể truy cập phiên bản công khai của báo cáo để tương tác trực tiếp với các biểu đồ tại liên kết sau: [Báo cáo Power BI](https://app.powerbi.com/view?r=eyJrIjoiMDJlNjAwZTEtNTVjOS00Njc3LWJlMTItNGYxM2FmZmM3YjhkIiwidCI6ImVkOGYxNjczLTM4OTAtNGRiNC1hM2YwLTk3YWQ5NDI3Yzc0ZiIsImMiOjEwfQ%3D%3D)

## :bulb: Cấu trúc Dashboard
Báo cáo được thiết kế gồm 4 phân mục chuyên biệt, giúp người dùng đi từ cái nhìn tổng thể đến chi tiết từng nhóm mặt hàng:

## 1. Tổng Quan Chung 
* **Mục tiêu:** Trang này cung cấp bức tranh toàn cảnh về sự tăng trưởng và độ biến động của 7 mặt hàng thiết yếu.
  
* **Thành phần chính:**
    * **KPI Cards:** `Nước sinh hoạt` là mặt hàng âm thầm tăng bền bỉ nhất, còn `Thịt heo` lại là kẻ gây "đau đầu" nhất vì giá cả thay đổi chóng mặt. Mốc giá vàng `131.77tr` và gạo `14.31K` được mình đặt làm "mỏ neo" để người xem dễ dàng hình dung giá trị đồng tiền qua các thời kỳ.
      
    * Nghịch lý của sự "Ổn định": > Qua biểu đồ % Tăng trưởng, dữ liệu phơi bày một thực tế: Các mặt hàng thiết yếu như Nước và Gạo có tốc độ tăng giá trung bình bền bỉ, đôi khi vượt xa Vàng trong một số giai đoạn. Điều này cho thấy áp lực chi phí sinh hoạt cơ bản thực sự nặng nề và tác động trực tiếp hơn nhiều so với việc đầu tư tài sản.
 
    * Kẻ giấu mặt mang tên "Biến động": > Trái với lầm tưởng về giá Xăng dầu, biểu đồ Biên độ dao động (%) chỉ ra rằng Thịt heo mới là "ông vua" về sốc giá (biến động trên 40%). Insight này chứng minh bữa cơm gia đình chịu ảnh hưởng cực lớn từ chuỗi cung ứng nội địa và dịch bệnh hơn là sự trồi sụt của thị trường dầu thế giới.
 
    * Bàn tay điều tiết của Nhà nước: > Sự đối lập giữa đường biểu đồ Xăng (nhảy ziczac theo giá thế giới) và Điện/Nước (tăng hình bậc thang) cho thấy vai trò "bộ giảm xóc" của Chính phủ, giúp huyết mạch sinh hoạt không bị sốc nhiệt theo thị trường tự do.

![Trang 1: Tổng Quan Chung](https://drive.google.com/uc?export=view&id=13K5AVyo27NO0LFe0x--ORsUqNElELBhj)


## 2. Nhóm Lương Thực - Thực Phẩm 

* Phần này tập trung bóc tách tương quan giữa giá sản xuất (lợn sống) và giá tiêu dùng cuối cùng.
* Mục tiêu: Xác định các điểm gãy cung-cầu và cấu trúc chi phí trung gian

* Hố sâu trung gian của Thịt heo: Khoảng cách giữa giá lợn hơi tại trại và bán lẻ đạt đỉnh điểm 52.00K VNĐ/kg (2022). Điều này cho thấy phần lớn giá trị gia tăng bị chiếm dụng bởi các khâu trung gian, đòi hỏi các chính sách tối ưu hóa chuỗi cung ứng để bình ổn CPI.

> Insight: Lợi nhuận trong chuỗi giá trị thịt heo không nằm ở người chăn nuôi mà tập trung ở các khâu trung gian và bán lẻ, đòi hỏi các chính sách tối ưu hóa logistics để bình ổn giá.
  
* Điểm gãy vĩ mô 2008: Biểu đồ Gạo ghi nhận "cú sốc" toàn cầu. Trong khi giá thực tế tăng vọt, đường % tăng trưởng cho thấy một đỉnh nhọn cực đại, phản ánh mức độ nhạy cảm của lương thực Việt Nam trước khủng hoảng thế giới dù chúng ta là nước xuất khẩu lớn.

> Insight: Sự ổn định của Gạo: Trái ngược với thịt heo, giá Gạo (trung bình 14.31K/kg) giữ được đà tăng trưởng ổn định hơn, đóng vai trò là "mỏ neo" tâm lý cho thị trường lương thực dù có cú sốc vĩ mô vào năm 2008.

![Trang 2: Nhóm Lương Thực - Thực Phẩm](https://drive.google.com/uc?export=view&id=1WR1N9xLOaMSF6huLU17BGqWGLjPNjZuq)


## 3. Nhóm Tài Sản Tích Trữ 

Sử dụng **Waterfall Chart** để theo dõi cách giá trị của Vàng và Bạc được "bồi đắp" qua hai thập kỷ.

* Vàng - "Hầm trú ẩn" kiên cố: Tổng mức tăng trưởng đạt 248.62%. Đường Waterfall cho thấy sự tăng trưởng đều đặn, ít chịu ảnh hưởng bởi các đợt giảm giá sâu, khẳng định vị thế tài sản bảo toàn vốn hàng đầu.

* Bạc - Lợi nhuận đột biến: Mặc dù giá trị thấp (chốt phiên 2.07 triệu/lượng), nhưng Bạc lại có tổng mức tăng ấn tượng hơn Vàng (379.20%). Tuy nhiên, các cột màu đỏ (giảm giá) xuất hiện dày đặc hơn, cho thấy tính chất đầu cơ và rủi ro cao hơn hẳn so với Vàng.****

![Trang 3: Nhóm Tài Sản Tích Trữ](https://drive.google.com/uc?export=view&id=1LscKwfkVTRG0kl42ten3SBy_Mfny8nKA)


## 4. Nhóm Đi Lại & Sinh Hoạt

Phân tích các mặt hàng là chi phí đầu vào của toàn bộ nền kinh tế: Xăng, Điện và Nước.

* Xăng dầu - Nhịp thở thế giới: Biểu đồ vùng (Area Chart) của Xăng RON 95 cho thấy những đợt "sóng" cực mạnh, đạt đỉnh 32.87K/lít (2022). Đây là mặt hàng duy nhất có các giai đoạn giảm giá sâu (âm % tăng trưởng), phản ánh sự nhạy cảm tuyệt đối với giá dầu thô toàn cầu.

* Điện & Nước - Sự tăng trưởng có kiểm soát: Biểu đồ lịch sử giá cho thấy đường thẳng đi lên theo hình bậc thang.

> Insight: Trái với Xăng dầu nhảy múa theo thị trường, Điện và Nước thể hiện rõ vai trò điều tiết của Chính phủ trong việc giữ ổn định "huyết mạch" sinh hoạt, chỉ điều chỉnh theo lộ trình để tránh gây sốc cho nền kinh tế

![Trang 4: Nhóm Đi Lại & Sinh Hoạt](https://drive.google.com/uc?export=view&id=1YpXTXINBH5vzKTTJ7wLt9wrL5YsSwIBH)


## :rocket: Kỹ thuật xử lý trong Power BI (Technical Highlights)
Để đạt được các Insight trên, Dashboard đã áp dụng các kỹ thuật:

* Sử dụng các hàm DAX để tính toán % Tăng trưởng trung bình và Biên độ dao động qua các năm.

* Data Modeling: Thiết lập mối quan hệ chặt chẽ giữa bảng Dim_Time và các bảng Fact_Commodity để đồng bộ hóa bộ lọc (Slicers).

* Custom Visualization: Kết hợp biểu đồ Stacked Bar và Line Chart để so sánh đồng thời giá trị tuyệt đối và tốc độ tăng trưởng trên cùng một khung hình.

## :high_brightness: **Đánh giá cá nhân**

Dữ liệu 20 năm đã phác họa rõ nét "thế chân kiềng" của kinh tế dân sinh Việt Nam:

* Trạng thái Biến động (Xăng & Thịt heo): Phản ánh sự nhạy cảm tuyệt đối của thị trường nội địa trước các cú sốc cung ứng và giá năng lượng toàn cầu. Đây là nhóm trực tiếp gây ra các đợt "bão giá" ngắn hạn.

* Trạng thái Điều tiết (Điện & Nước): Thể hiện vai trò "bộ giảm xóc" của Nhà nước. Dù tăng giá theo hình bậc thang, nhưng sự lầm lũi tiến bước của nhóm này chính là áp lực chi phí cố định nặng nề nhất đối với túi tiền người dân trong dài hạn.

* Trạng thái Bảo toàn (Vàng & Bạc): Đây là câu trả lời của người dân trước áp lực trượt giá. Dữ liệu cho thấy khi các nhóm trên biến động, dòng tiền có xu hướng đổ dồn vào Vàng như một "hầm trú ẩn" kiên cố, trong khi Bạc nổi lên như một công cụ đầu cơ mang lại lợi nhuận đột biến nhưng đi kèm rủi ro cực lớn.

Kết luận: Hiểu được sự tương quan giữa 3 nhóm này chính là chìa khóa để giải mã bức tranh lạm phát thực tế. Không chỉ là nhìn vào con số tăng giá, mà là nhìn thấy cách người dân đang phải "vật lộn" để cân bằng giữa chi phí sinh hoạt và nhu cầu bảo toàn tài sản trong suốt hai thập kỷ qua.
