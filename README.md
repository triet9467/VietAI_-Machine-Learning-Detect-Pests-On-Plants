<src="https://github.com/user-attachments/assets/e997ce85-01ba-4dee-a320-19f64f750b1d" /># VietAI_-Machine-Learning-Detect-Pests-On-Plants
Báo cáo cuối khóa F0ML-09
# Machine Learning phát hiện côn trùng gây hại

Dự án này tập trung vào việc nhận diện các loại côn trùng gây hại trên cây trồng bằng cách sử dụng các đặc trưng hình ảnh và mô hình học máy.

## 📌 Tổng quan dự án
Dự án được triển khai dưới dạng một Pipeline toàn diện (End-to-End) trong một file Notebook duy nhất, bao gồm từ bước xử lý dữ liệu thô đến giao diện demo thực tế.

## 📂 Cấu trúc mã nguồn
Do tính chất thực nghiệm liên tục, mã nguồn được tổ chức tập trung tại:
- **/notebooks/VietAI.ipynb**: File mã nguồn chính chứa:
    - **Tải dữ liệu**: Tải dữ liệu từ Kaggle.
    - **Tiền xử lí ảnh**: Resize, mã hóa, kiểm định dữ liệu, SimpleImputer, StandardScaler
    - **Trích xuất đặc trưng**: Phân tích 19 chỉ số về màu sắc, kết cấu và hình thái.
    - **Huấn luyện mô hình**: Logistic Regression, Random Forest, SVM, KNN, LightBGM, Ensemble.
    - **Đánh giá**: Bảng so sánh giữa các mô hình -> Chọn Random Forest, đánh giá Confusion Matrix, Classification Report và Feature Importance.
    - **Ứng dụng (App)**: Giao diện demo tương tác trực tiếp bằng **Gradio**.

## 📊 Kết quả thực nghiệm
- **Độ chính xác (Accuracy)**: 96.37%
- **Recall (Lớp Pest)**: 99.2% (Ưu tiên giảm thiểu việc bỏ sót côn trùng).
- **Đặc trưng quan trọng nhất**: Kết cấu ($f_7$) đóng vai trò quyết định trong việc phân loại.

## 🛠 Hướng dẫn sử dụng
1. Mở file `VietAI.ipynb` trong thư mục `notebooks`.
2. Nhấn nút "Open in Colab".
3. Chạy các cell từ trên xuống dưới.
