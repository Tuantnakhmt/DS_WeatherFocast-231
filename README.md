# 🌤️ Dự báo thời tiết Hà Nội (IT4991-Nhập môn Khoa học dữ liệu)
Dự đoán điều kiện thời tiết tại Hà Nội dựa trên dữ liệu lịch sử 10 năm từ Weatherbit. Nhóm sử dụng kỹ thuật xử lý chuỗi thời gian, phân tích đặc trưng và mô hình học máy để dự báo các yếu tố khí tượng như nhiệt độ, độ ẩm và phân loại tình trạng thời tiết.

## ✅ Các bước chính
- Thu thập dữ liệu: Crawl dữ liệu thời tiết từ Weatherbit (giới hạn 1500 requests/ngày).

- Tiền xử lý: Loại bỏ cột không cần thiết, chuyển đổi thời gian, chuẩn hóa dữ liệu.

- Phân tích dữ liệu (EDA):

+ Trực quan hóa biến động các đặc trưng theo thời gian.

+ Phân tích tương quan giữa các đặc trưng và nhãn thời tiết.

- Xây dựng mô hình:

+ 📈 LSTM cho bài toán chuỗi thời gian (nhiệt độ, độ ẩm).

+ 🌧️ Random Forest để phân loại nhãn thời tiết (mưa, nắng...).

+ Tối ưu kiến trúc LSTM: 5 layers, 32 hidden units, dropout 20%.

## 🛠️ Hệ thống tự động
+ Dùng Apache Airflow để tự động:

+ Crawl dữ liệu mỗi ngày.

+ Retrain mô hình mỗi tuần với dữ liệu mới.

## 📊 Kết quả
- MAE (LSTM): ~0.0971 (train) và ~0.2660 (val)

- Accuracy (RandomForest): ~91.1% khi giữ đặc trưng precip.

## 📌 Hướng phát triển
- Giải quyết mất cân bằng dữ liệu nhãn.

- Thu thập dữ liệu phong phú hơn.

- Triển khai mô hình trên hệ thống trực tuyến.
