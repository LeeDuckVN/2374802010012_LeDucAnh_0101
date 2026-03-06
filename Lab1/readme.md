## bài 1
dùng torch tensor và backward để tính đạo hàm
tính y tại x bằng 3 và tìm điểm có đạo hàm gần bằng 0
kết quả y phẩy tại 3 bằng 1462
điểm dốc gần 0 tại x gần bằng cộng trừ 0.3736

## bài 2
sử dụng autograd requires grad true và gradient descent
cập nhật x theo công thức x bằng x trừ alpha nhân gradient
kết quả gradient tăng nhanh làm x diverge dẫn đến inf

## bài 3
tạo dữ liệu ngẫu nhiên bằng torch randint và torch randn
train mô hình tuyến tính y bằng w nhân x cộng b bằng mse
kết quả cuối w gần bằng 3.48 và b gần bằng 1.72

## bài 4
so sánh torch from numpy và torch tensor
from numpy dùng chung bộ nhớ với numpy
torch tensor tạo bộ nhớ mới và copy dữ liệu

## bài 5
tạo tensor bằng empty zeros ones và random
đổi shape bằng view và view as
