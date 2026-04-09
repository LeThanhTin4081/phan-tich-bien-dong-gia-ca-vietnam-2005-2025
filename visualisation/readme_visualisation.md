# :bar_chart: Trực quan hóa dữ liệu trên Power BI

## :link: Bạn có thể truy cập phiên bản công khai của báo cáo để tương tác trực tiếp với các biểu đồ tại liên kết sau: [Báo cáo Power BI](https://app.powerbi.com/view?r=eyJrIjoiMDJlNjAwZTEtNTVjOS00Njc3LWJlMTItNGYxM2FmZmM3YjhkIiwidCI6ImVkOGYxNjczLTM4OTAtNGRiNC1hM2YwLTk3YWQ5NDI3Yzc0ZiIsImMiOjEwfQ%3D%3D)

## :bulb: Cấu trúc Dashboard
Báo cáo được thiết kế gồm 4 phân mục chuyên biệt, giúp người dùng đi từ cái nhìn tổng thể đến chi tiết từng nhóm mặt hàng:

### 1. Tổng Quan Chung (Overview)
* **Mục tiêu:** Cung cấp bức tranh toàn cảnh về sự tăng trưởng và độ biến động của thị trường.
  
* **Thành phần chính:**
    * **KPI Cards:** Nước sinh hoạt là mặt hàng âm thầm tăng bền bỉ nhất, còn Thịt heo lại là kẻ gây "đau đầu" nhất vì giá cả thay đổi chóng mặt. Mốc giá vàng 131.77tr và gạo 14.31K được mình đặt làm "mỏ neo" để người xem dễ dàng hình dung giá trị đồng tiền qua các thời kỳ.
      
* **Data Storytelling - Những câu chuyện đằng sau biểu đồ:**

> **Nghịch lý mặt hàng "ổn định":** Nhìn vào biểu đồ cột % Tăng trưởng trung bình, có một sự thật khá "phũ phàng" là các mặt hàng thiết yếu như Nước và Gạo đôi khi lại có tốc độ tăng giá tổng thể vượt xa cả Vàng trong một số giai đoạn. Điều này cho thấy áp lực chi phí sinh hoạt cơ bản thực sự nặng nề hơn nhiều so với việc đầu tư tài sản.

> **Kẻ giấu mặt mang tên "Biến động":** Mọi người thường than phiền về giá Xăng dầu, nhưng biểu đồ Biên độ dao động (%) lại chỉ ra rằng Thịt heo mới là "ông vua" về sốc giá (biến động trên 40%). Điều này chứng tỏ bữa cơm của người dân chịu ảnh hưởng cực lớn từ chuỗi cung ứng và dịch bệnh, hơn là sự trồi sụt của giá dầu thế giới.

> **Bàn tay điều tiết của Nhà nước:** Sự đối lập hoàn toàn giữa biểu đồ vùng của Xăng (nhảy ziczac theo giá thế giới) và đường biểu đồ của Điện/Nước (tăng theo hình bậc thang) cho thấy vai trò cực lớn của Chính phủ trong việc giữ cho "huyết mạch" sinh hoạt không bị sốc nhiệt theo thị trường tự do.

> **Trải nghiệm tương tác:** Mình đã đồng bộ hóa Bộ lọc thời gian (Slicers). Khi bạn chọn một giai đoạn khủng hoảng (ví dụ 2008 hay 2020), toàn bộ 6 biểu đồ sẽ cùng "nhảy" để cho thấy tại thời điểm đó, túi tiền của người dân đã bị tác động đa chiều như thế nào.

![Trang 1: Tổng Quan Chung](https://drive.google.com/uc?export=view&id=13K5AVyo27NO0LFe0x--ORsUqNElELBhj)

---

### 2. Nhóm Lương Thực - Thực Phẩm (Food & Staples Analysis)

Phần này tập trung bóc tách biến động của hai mặt hàng có tỷ trọng lớn nhất và tác động trực tiếp nhất đến rổ lạm phát (CPI) của hộ gia đình: Gạo và Thịt heo. Mục tiêu là phân tích sự tương quan giữa giá đầu vào (sản xuất) và giá đầu ra (tiêu dùng).

* **Mục tiêu phân tích:** Xác định các điểm sốc giá do cung-cầu và phân tích cấu trúc chi phí trung gian ảnh hưởng đến người tiêu dùng cuối cùng.

* **Hệ thống Visualization (Visual Techniques):**
    * **Biểu đồ Cột Chênh lệch Giá (Price Spread Bar Chart):** Tập trung vào khoảng cách giá trị (Spread) giữa lợn sống tại trại (Live Pig Price) và giá bán lẻ (Retail Price) hàng năm.
    * **Biểu đồ Kết hợp (Line & Clustered Column Chart):** Tích hợp giữa "Giá trị tuyệt đối" (Giá Gạo thực tế/kg - Column) và "Tốc độ tăng trưởng lũy kế (%)" (Growth Rate - Line) trên cùng một trục thời gian.

#### 🎙 Data Storytelling - Những câu chuyện đằng sau biểu đồ

> **Câu chuyện Chuỗi Cung ứng qua "Chênh lệch Giá" Thịt heo**
> Biểu đồ chênh lệch giá (bên trái) đã phơi bày một Insight chiến lược về hiệu quả chuỗi cung ứng. Ta thấy một khoảng cách cực lớn giữa giá lợn hơi tại trại và giá thịt bán lẻ đến tay người tiêu dùng, có năm lên tới đỉnh điểm **52.00K VNĐ/kg** (năm 2022). Số liệu này là minh chứng rõ nét cho thấy, phần lớn giá trị gia tăng của mặt hàng này không nằm ở người chăn nuôi hay người tiêu dùng, mà bị chiếm dụng bởi các chi phí trung gian, logistics, khâu giết mổ và thương lái, đòi hỏi các chính sách tối ưu hóa chuỗi cung ứng để bình ổn CPI.

> **Cú sốc lương thực vĩ mô qua biểu đồ Gạo**
> Biểu đồ kết hợp bên phải đã ghi nhận lại một "cú sốc" vĩ mô thực sự vào khoảng năm **2008**. Trong khi cột giá thực tế bắt đầu tăng vọt, **đường tốc độ tăng trưởng (%)** (Line chart) cho thấy một đỉnh nhọn "chóng mặt", phản ánh chính xác tác động của cuộc Khủng hoảng lương thực toàn cầu thời điểm đó đối với Việt Nam - dù là một nước xuất khẩu gạo lớn. Dữ liệu cho thấy đường tăng trưởng (%) thường phản ứng nhanh và gắt hơn nhiều so với đường giá tuyệt đối trước các sự kiện vĩ mô.

> **Đặc trưng biến động: "Sốc ngắn hạn" vs. "Tăng trưởng dài hạn"**
> Phân tích tương quan dữ liệu chỉ ra rằng mặc dù cả hai là mặt hàng thiết yếu, Gạo có xu hướng tăng trưởng ổn định hơn sau các cú sốc vĩ mô (tăng trưởng đều qua các năm gần đây). Ngược lại, Thịt heo lại thường xuyên "nhảy múa" thất thường trước các tác động sinh học (như dịch bệnh) và chi phí trung gian, đòi hỏi Chính phủ có các chiến lược bình ổn thị trường hoàn toàn khác nhau cho hai nhóm hàng này: một bên cần theo dõi tăng trưởng CAGR, một bên cần quản lý biên độ dao động ngắn hạn.

![Trang 2: Nhóm Lương Thực - Thực Phẩm](https://drive.google.com/uc?export=view&id=1WR1N9xLOaMSF6huLU17BGqWGLjPNjZuq)

---

### 3. Nhóm Tài Sản Tích Trữ (Safe Haven Assets)

Sử dụng **Waterfall Chart** để theo dõi cách giá trị của Vàng và Bạc được "bồi đắp" qua từng năm.

#### 🎙 Data Storytelling - Những câu chuyện đằng sau biểu đồ

> **Vàng: "Hầm trú ẩn" kiên cố**
> Với tổng mức tăng lũy kế lên tới **248.62%**, Vàng khẳng định vị thế tài sản bảo toàn giá trị tốt nhất mỗi khi kinh tế có biến động.

> **Bạc: Lợi nhuận cao đi kèm rủi ro lớn**
> Một bất ngờ từ dữ liệu: Bạc tăng trưởng tới **379.20%** (cao hơn Vàng), nhưng biên độ dao động cực gắt (có năm giảm sâu 35%), cho thấy đây là kênh đầu tư mang tính đầu cơ cao hơn.

![Trang 3: Nhóm Tài Sản Tích Trữ](https://drive.google.com/uc?export=view&id=1LscKwfkVTRG0kl42ten3SBy_Mfny8nKA)

---

### 4. Nhóm Đi Lại & Sinh Hoạt (Utilities & Fuel)

Phân tích các mặt hàng là chi phí đầu vào của toàn bộ nền kinh tế: Xăng, Điện và Nước.

#### 🎙 Data Storytelling - Những câu chuyện đằng sau biểu đồ

> **Xăng dầu và áp lực năng lượng toàn cầu**
> Biểu đồ vùng (Area Chart) cho thấy giá Xăng nhạy cảm tuyệt đối với thị trường thế giới, đạt đỉnh **32.87K/lít** vào năm 2022.

> **Điện và Nước: Sự ổn định có tính toán**
> Trái ngược với Xăng, Điện và Nước có lộ trình tăng giá hình bậc thang. Tuy nhiên, dữ liệu Matrix (bảng tra cứu) cho thấy từ mức 700đ/kWh (2005) lên 2150đ/kWh (2024) là một áp lực chi phí không hề nhỏ cho sản xuất công nghiệp.

![Trang 4: Nhóm Đi Lại & Sinh Hoạt](https://drive.google.com/uc?export=view&id=1YpXTXINBH5vzKTTJ7wLt9wrL5YsSwIBH)


