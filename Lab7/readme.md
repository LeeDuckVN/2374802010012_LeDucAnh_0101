# RNN
## Công nghệ sử dụng
Python, NumPy, Matplotlib, PyTorch, Scikit-learn.
## Cách hoạt động
- Chuẩn hóa dữ liệu để dễ xử lý  
- Dùng RNN để học dữ liệu theo thời gian  
- Huấn luyện mô hình để giảm sai số  
- Dự đoán và so sánh với dữ liệu thật  
- Thử thay đổi các tham số để xem ảnh hưởng  
## Kết quả
- Mô hình dự đoán khá tốt  
- Độ dài chuỗi vừa phải cho kết quả tốt nhất  
- Học nhiều lần giúp giảm lỗi nhưng có thể làm dự đoán kém hơn  
- Dự đoán nhiều bước thì càng về sau càng sai  
- Thêm dropout giúp mô hình ổn định hơn  
## Kết luận
- Mô hình hoạt động tốt nhưng cần chọn tham số phù hợp để tránh sai nhiều.
## Nhận xét 
- seq_length ở mức vừa phải khoảng 20 cho kết quả tốt nhất, quá ngắn thì thiếu dữ liệu, quá dài thì dễ bị sai.
- hidden_size lớn giúp mô hình học tốt hơn nhưng chạy chậm và dễ bị sai nhiều hơn ở dữ liệu mới.
- Tăng số lần học epoch giúp giảm lỗi lúc học, nhưng có thể làm mô hình học quá kỹ và dự đoán kém.
- Dự đoán nhiều bước liên tiếp thì càng về sau càng sai nhiều.
- Thêm dropout giúp mô hình bớt bị sai khi gặp dữ liệu mới.
- Learning rate lớn học nhanh nhưng dễ sai, nhỏ thì học chậm nhưng ổn định hơn.
- Lỗi dự đoán không đều, có lúc đúng nhiều, có lúc sai nhiều.
