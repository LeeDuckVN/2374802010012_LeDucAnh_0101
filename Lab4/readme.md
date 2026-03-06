## ann1
công nghệ sử dụng pytorch scikit learn matplotlib
cách hoạt động tạo dữ liệu bằng make circles mỗi mẫu có 2 đặc trưng đầu vào và 1 nhãn dữ liệu được chia 80 phần trăm train và 20 phần trăm test
mô hình ann thử các cấu trúc 2 4 1 2 8 1 và 2 8 6 1
huấn luyện sử dụng hai hàm mất mát bce loss và bce with logits loss cùng hai bộ tối ưu adam và sgd với learning rate 0.01
kết quả tăng số nút ẩn và thêm lớp ẩn giúp giảm loss và tăng độ chính xác mô hình 2 8 6 1 cho kết quả tốt nhất adam hội tụ nhanh và ổn định hơn sgd
kết luận cấu trúc mạng và bộ tối ưu ảnh hưởng lớn đến hiệu quả ann mạng sâu hơn và adam giúp mô hình học tốt hơn trên dữ liệu phi tuyến
## ann2
nhận xét mnist mô hình ann đạt độ chính xác khoảng 95 đến 97 phần trăm do ảnh nhỏ và đặc trưng rõ ràng ann nhiều lớp vẫn học tốt sau khi flatten ảnh adam giúp hội tụ nhanh và ổn định
nhận xét cat dog mô hình ann đạt độ chính xác trung bình do ann không khai thác được đặc trưng không gian của ảnh như cnn việc flatten ảnh làm mất cấu trúc không gian nên hiệu suất bị giảm
