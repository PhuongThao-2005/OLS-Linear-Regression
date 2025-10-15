# 📚 Phân tích và Dự đoán Chỉ số Thành tích Học tập của Sinh viên (Student Performance Index)

## 🎯 Mục tiêu Đồ án

Đồ án này tập trung vào việc xây dựng và tối ưu hóa **mô hình Hồi quy Tuyến tính (Linear Regression)** để phân tích các yếu tố ảnh hưởng và dự đoán **Chỉ số Thành tích Học tập (Performance Index)** của sinh viên.

Mục tiêu cụ thể:
1.  **Phân tích Ảnh hưởng:** Xác định và đánh giá mức độ tác động của từng yếu tố đầu vào (giờ học, điểm trước đó, hoạt động ngoại khóa, v.v.) lên Performance Index.
2.  **Kỹ thuật Đặc trưng (Feature Engineering):** Tạo ra các đặc trưng mới từ dữ liệu gốc để nâng cao khả năng dự đoán của mô hình.
3.  **Xây dựng Mô hình Tối ưu:** Xây dựng và so sánh các phiên bản mô hình hồi quy tuyến tính (ví dụ: Hồi quy Đa biến, Ridge, Lasso) để chọn ra mô hình có hiệu suất dự đoán cao nhất.
4.  **Đánh giá Hiệu quả:** Đánh giá các mô hình bằng kỹ thuật Cross-validation (CV) để tránh overfitting và sử dụng MAE (Mean Absolute Error) trên tập kiểm tra (test set) để đo lường độ chính xác cuối cùng.

---

## 💾 Dữ liệu (Input / Output)

### Input
Bộ dữ liệu **Student Performance** bao gồm **10.000** dòng dữ liệu.
| STT | Tên Cột | Mô tả | Loại Dữ liệu |
| :---: | :--- | :--- | :---: |
| 1 | `Hours Studied` | Tổng số giờ học của sinh viên. | Số |
| 2 | `Previous Scores` | Điểm số sinh viên đạt được trong các bài kiểm tra trước đó. | Số |
| 3 | `Extracurricular Activities` | Sinh viên có tham gia hoạt động ngoại khóa (`Yes`/`No`). | Phân loại |
| 4 | `Sleep Hours` | Số giờ ngủ trung bình mỗi ngày của sinh viên. | Số |
| 5 | `Sample Question Papers Practiced` | Số lượng đề thi mẫu đã luyện tập. | Số |
| **6** | **`Performance Index`** | **Chỉ số thành tích học tập (Biến Mục tiêu - Target Variable).** | Số |

*Dữ liệu được chia theo tỉ lệ **9:1** (90% cho tập huấn luyện/train và 10% cho tập kiểm tra/test).*

### Output
-   Báo cáo chi tiết về **tầm quan trọng** và **ảnh hưởng** của từng đặc trưng đầu vào.
-   Mô hình Hồi quy Tuyến tính tối ưu cho việc dự đoán `Performance Index`.
-   Bảng đánh giá hiệu suất mô hình, bao gồm:
    -   Kết quả **Cross-validation** trên tập huấn luyện.
    -   Chỉ số **MAE (Mean Absolute Error)** trên tập kiểm tra.

---

## ⚙️ Công nghệ & Thư viện Sử dụng

-   **Ngôn ngữ:** Python
-   **Phân tích Dữ liệu (EDA):** `Pandas`, `NumPy`
-   **Trực quan hóa:** `Matplotlib`, `Seaborn`
-   **Xây dựng Mô hình:** `Scikit-learn` (Linear Regression, Ridge, Lasso)
-   **Đánh giá:** `Scikit-learn` (cross_val_score, mean_absolute_error)

---

## 🛠️ Hướng dẫn Cài đặt & Chạy Đồ án

### 1. Cài đặt Môi trường
```bash
# Tạo môi trường ảo (khuyến khích)
python -m venv venv
source venv/bin/activate  # Trên Linux/macOS
.\venv\Scripts\activate   # Trên Windows
