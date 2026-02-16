# ANN1
## 1. Công nghệ sử dụng
- PyTorch để xây dựng và huấn luyện mô hình.
- scikit-learn, chia tập train và test và đánh giá độ chính xác.
- Matplotlib để trực quan hóa quá trình huấn luyện.
## 2. Cách hoạt động
### 2.1 Dữ liệu
- Dữ liệu được tạo bằng hàm make_circles.  
- Mỗi mẫu dữ liệu gồm 2 đặc trưng đầu vào và 1 nhãn đầu ra.  
- Dữ liệu được chia thành 80% cho huấn luyện và 20% cho kiểm tra.
### 2.2 Mô hình ANN
- Mô hình gốc: 2–4–1  
- Tăng số nút ẩn: 2–8–1  
- Thêm lớp ẩn: 2–8–6–1  
### 2.3 Huấn luyện
- Hai hàm mất mát: BCELoss và BCEWithLogitsLoss.
- Hai bộ tối ưu hóa: Adam và SGD (learning rate = 0.01).
## 3. Kết quả
- Việc tăng số nút ẩn và thêm lớp ẩn giúp mô hình giảm loss và cải thiện độ chính xác.
- Mô hình 2–8–6–1 cho kết quả tốt nhất nhờ khả năng biểu diễn phi tuyến mạnh hơn.
- BCEWithLogitsLoss giúp quá trình huấn luyện ổn định hơn so với BCELoss.
- Adam hội tụ nhanh và ổn định hơn, trong khi SGD giảm loss chậm và có hiện tượng dao động.
## 4. Kết luận
Kết quả chạy : cấu trúc mạng và bộ tối ưu hóa ảnh hưởng đáng kể đến hiệu quả của ANN; mạng sâu hơn và Adam giúp mô hình học tốt hơn trên dữ liệu phi tuyến, trong khi đồ thị loss cho phép đánh giá trực quan tốc độ hội tụ và độ ổn định khi huấn luyện.
# ANN2
### Nhận xét : MNIST
Mô hình ANN đạt độ chính xác khoảng 95–97% trên tập MNIST.
Do ảnh có kích thước nhỏ và đặc trưng rõ ràng,
ANN nhiều lớp có thể học tốt sau khi flatten ảnh.
Adam giúp mô hình hội tụ nhanh và ổn định.
### Nhận xét : Cat & Dog
Mô hình ANN đạt độ chính xác ở mức trung bình trên bài toán Cat & Dog.
Do ANN không khai thác được đặc trưng không gian của ảnh như CNN,
khả năng phân loại bị hạn chế.
Việc flatten ảnh làm mất cấu trúc không gian, ảnh hưởng đến hiệu suất mô hình.
