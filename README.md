# Churn Prediction Project

## Mục tiêu
Dự án này nhằm xây dựng mô hình dự đoán khách hàng rời bỏ ngân hàng (churn) dựa trên dữ liệu thực tế. Mục tiêu là phân tích dữ liệu, xử lý đặc trưng, xây dựng và đánh giá các mô hình học máy để xác định các yếu tố ảnh hưởng đến churn và dự đoán chính xác khách hàng có khả năng rời đi.

## Dữ liệu
- File dữ liệu: `Churn_Modelling.csv`
- Các thuộc tính chính:
  - RowNumber, CustomerId, Surname
  - CreditScore, Geography, Gender, Age, Tenure, Balance
  - NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary
  - Exited (biến mục tiêu: 1 là churn, 0 là không churn)

## Quy trình thực hiện
1. **Khám phá dữ liệu**: Thống kê, trực quan hóa phân phối các thuộc tính, kiểm tra mất cân bằng lớp.
2. **Tiền xử lý**:
   - Mã hóa biến phân loại (LabelEncoder, OneHotEncoder)
   - Loại bỏ các cột không cần thiết
   - Chuẩn hóa dữ liệu
3. **Xây dựng mô hình**:
   - Chia tập dữ liệu thành train/test
   - Sử dụng nhiều thuật toán: Random Forest, Gradient Boosting, AdaBoost, SVC, Naive Bayes, KNN, XGBoost, Logistic Regression
   - Áp dụng mô hình stacking với meta-learner là mạng nơ-ron nhân tạo (ANN)
   - Cross-validation để đánh giá mô hình
4. **Đánh giá mô hình**:
   - Tính toán các chỉ số: Accuracy, F1-Score, AUC-ROC
   - Phân tích ma trận nhầm lẫn, classification report, ROC curve, Precision-Recall curve
   - So sánh hiệu suất các mô hình
   - Phân tích feature importance và lỗi dự đoán

## Yêu cầu môi trường
- Python >= 3.8
- Các thư viện: pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, tensorflow
- Cài đặt bằng lệnh:
  ```bash
  pip install -r requirements.txt
  ```

## Sử dụng
1. Chuẩn bị dữ liệu `Churn_Modelling.csv` trong thư mục dự án.
2. Chạy notebook `final.ipynb` để thực hiện toàn bộ quy trình từ phân tích đến đánh giá mô hình.
3. Kết quả sẽ được hiển thị trực tiếp trên notebook, bao gồm các biểu đồ, bảng so sánh và phân tích chi tiết.