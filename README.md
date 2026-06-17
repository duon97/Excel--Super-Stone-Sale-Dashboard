# 📊 Excel - Sales Performance Analysis Dashboard

## I. Giới thiệu

### Tổng quan dự án

Dự án được thực hiện nhằm phân tích hiệu quả kinh doanh dựa trên bộ dữ liệu Superstore bằng Microsoft Excel. Thông qua việc làm sạch dữ liệu, phân tích và xây dựng Dashboard trực quan, dự án giúp theo dõi doanh thu, lợi nhuận, hiệu suất sản phẩm và hiệu quả hoạt động tại các khu vực khác nhau.

Kết quả phân tích hỗ trợ doanh nghiệp xác định các cơ hội tăng trưởng, tối ưu danh mục sản phẩm và đưa ra quyết định kinh doanh dựa trên dữ liệu.

---

## II. Mục tiêu dự án

Dự án được xây dựng nhằm trả lời các câu hỏi kinh doanh sau:

- Doanh thu và lợi nhuận đang được tạo ra từ đâu?
- Khu vực nào mang lại hiệu quả kinh doanh tốt nhất?
- Danh mục sản phẩm nào đóng góp nhiều doanh thu và lợi nhuận nhất?
- Chiết khấu có ảnh hưởng như thế nào đến lợi nhuận?
- Doanh nghiệp nên tập trung nguồn lực vào đâu để cải thiện hiệu quả kinh doanh?

---

## III. Mô tả dữ liệu

### Bộ dữ liệu Superstore

Bộ dữ liệu chứa thông tin chi tiết về các giao dịch bán hàng, khách hàng, sản phẩm và hiệu quả kinh doanh.

| Tên cột | Mô tả |
|----------|--------|
| Row ID | Mã định danh của từng dòng dữ liệu |
| Order ID | Mã đơn hàng |
| Order Date | Ngày đặt hàng |
| Ship Date | Ngày giao hàng |
| Ship Mode | Phương thức giao hàng |
| Customer ID | Mã khách hàng |
| Customer Name | Tên khách hàng |
| Segment | Phân khúc khách hàng |
| Country | Quốc gia |
| City | Thành phố |
| State | Bang/Tỉnh |
| Postal Code | Mã bưu chính |
| Region | Khu vực bán hàng |
| Product ID | Mã sản phẩm |
| Category | Danh mục sản phẩm |
| Sub-Category | Danh mục con |
| Product Name | Tên sản phẩm |
| Sales | Doanh thu |
| Quantity | Số lượng bán |
| Discount | Mức chiết khấu |
| Profit | Lợi nhuận |

---

## IV. Quy trình thực hiện

### 1. Làm sạch dữ liệu

- Kiểm tra dữ liệu thiếu
- Kiểm tra định dạng dữ liệu
- Chuẩn hóa dữ liệu ngày tháng
- Kiểm tra dữ liệu bất thường

### 2. Phân tích dữ liệu

- Phân tích doanh thu
- Phân tích lợi nhuận
- Phân tích theo khu vực
- Phân tích theo danh mục sản phẩm
- Phân tích ảnh hưởng của chiết khấu

### 3. Xây dựng Dashboard

Sử dụng Excel để xây dựng Dashboard tương tác nhằm hỗ trợ người dùng theo dõi hiệu quả kinh doanh thông qua:

- KPI Cards
- Pivot Tables
- Pivot Charts
- Slicers
- Conditional Formatting

---

## V. Dashboard

### Dashboard Tổng Quan

<img width="1516" height="625" alt="image" src="https://github.com/user-attachments/assets/8161ec32-935d-44b6-9ff4-bd9218c8ed08" />


---

## VI. Các Insight Chính
Năm 2017:
## Margin đang bị bào mòn bởi discount. 
Profit margin thực tế = 93,439.27 / 733,215.26 ≈ 12,75%, trong khi Avg. Discount lại là 15,65%. Mức chiết khấu trung bình cao hơn cả margin cuối cùng cho thấy chính sách discount đang ăn sâu vào lợi nhuận. Đây là một insight cần đào sâu hơn: nên xem discount có phân bổ đều across category/segment hay tập trung ở một vài nhóm sản phẩm cụ thể, vì nếu một category nào gánh discount cao mà margin gốc thấp thì có thể đang lỗ.

## Tính nhanh hai chỉ số phụ: 
AOV (giá trị đơn hàng trung bình) = 733,215.26 / 1608 ≈ $456/đơn. Doanh số trung bình/khách hàng = 733,215.26 / 216 ≈ $3,394/khách. Với chỉ 216 khách mà tạo ra hơn 1600 đơn, trung bình mỗi khách đặt khoảng 7,4 đơn/năm — tần suất mua khá cao, gợi ý đây là nhóm khách hàng lặp lại (repeat customer) nhiều hơn là khách mua một lần.

## Technology, cụ thể là Phones, đang dẫn đầu doanh số theo category con. 
Trong chart Product Sales by Category, cột Phones (thuộc Technology) đạt khoảng $105K, cao nhất trong toàn bộ các category con, vượt xa Bookcases hay Storage. Điều này khớp với Top 10 Products khi sản phẩm như Samsung Galaxy Mega 6.3 lọt vào top 5.

## Top 10 Products bị chi phối bởi thiết bị giá trị đơn vị cao, không phải số lượng lớn. 
Canon imageCLASS 2200 Advanced Copier dẫn đầu với gần $40K, gấp đôi sản phẩm thứ hai. Phần lớn top 10 là máy photocopy, máy in, máy đóng gáy — tức doanh số cao đến từ đơn giá cao chứ chưa chắc đến từ sales volume. Nếu muốn biết sản phẩm nào thực sự "bán chạy" (số lượng), cần thêm chart Quantity, vì chart hiện tại chỉ thể hiện Sales.

## Sales by State có một outlier rất đáng ngờ. 
Carlifornia đạt 146,388.34, cao gấp 1,5–10 lần hầu hết các bang khác (đa số dưới $30K, một vài bang như New Mexico ~$94K, Texas ~$65K). Cần kiểm tra xem có đơn hàng lỗi, double-counting, hay chỉ đơn giản là dữ liệu 2017 có một deal lớn bất thường tại đó. Trước khi đưa insight này vào báo cáo, nên trace lại transaction-level data của bang đó.

## Về region và segment: 
West (34%) và East (29%) gộp lại chiếm 63% doanh số, South chỉ 17% 

## Sales Trend 
Có pattern mùa rõ nhưng có một điểm gãy bất thường ở tháng 2 (giảm mạnh từ ~42K xuống ~25K rồi mới phục hồi tăng dần đến đỉnh tháng 11 ~125K). Nếu đây là pattern lặp lại qua các năm thì là seasonality bình thường (sau Tết/đầu năm chi tiêu thấp), nhưng nếu chỉ riêng 2017 thì cần xem có nguyên nhân vận hành cụ thể (ví dụ thiếu hàng, gián đoạn logistics).

---

## VII. Kết luận và Đề xuất

### Kết luận

Năm 2017, doanh nghiệp đạt $733K doanh thu và $93K lợi nhuận, tuy nhiên Discount trung bình (15.65%) cao hơn Profit Margin (12.75%), cho thấy chính sách giảm giá đang làm suy giảm lợi nhuận. Vì vậy, doanh nghiệp nên rà soát các nhóm sản phẩm và phân khúc khách hàng có mức chiết khấu cao để tối ưu hiệu quả kinh doanh.

Khách hàng có tần suất mua lặp lại cao với trung bình 7.4 đơn hàng/khách hàng/năm, cho thấy tiềm năng phát triển các chương trình giữ chân khách hàng và gia tăng giá trị vòng đời khách hàng.

Nhóm Technology, đặc biệt là Phones, đang dẫn đầu doanh số và nên được ưu tiên đầu tư. Đồng thời, cần theo dõi thêm sản lượng bán để đánh giá chính xác hiệu suất sản phẩm thay vì chỉ dựa trên doanh thu.

Về khu vực, West và East đóng góp 63% tổng doanh thu, trong khi California là thị trường nổi bật với doanh thu vượt trội. Doanh nghiệp nên tập trung nguồn lực vào các thị trường trọng điểm và nghiên cứu mô hình thành công để mở rộng sang các khu vực khác.

Ngoài ra, doanh số thể hiện xu hướng mùa vụ rõ rệt với đỉnh điểm vào cuối năm. Doanh nghiệp nên tận dụng các giai đoạn cao điểm để tối ưu tồn kho, hoạt động bán hàng và các chương trình khuyến mãi nhằm nâng cao hiệu quả kinh doanh.

---

## VIII. Công cụ sử dụng

- Microsoft Excel
  - Pivot Table
  - Pivot Chart
  - Slicer
  - Conditional Formatting
  - Data Cleaning

---


- LinkedIn: https://www.linkedin.com/in/duong-minh-nhat-4084091b8/
- GitHub: https://github.com/duon97
