# Bài tập 1
Công nghệ : Tensor scalar: torch.tensor 

Cách hoạt động : 
Tạo tensor x 1 giá trị 
bài kêu tính hàm đa thức y theo đề bài
gọi y.backward()  PyTorch là thư viện tự đạo hàm 
Kết quả : 
y'(3) = 1462.0
Điểm dốc=0: x≈+0.3736, y' = -0.0005713701248168945
Điểm dốc=0: x≈-0.3736, y' = -0.0005713701248168945
# Bài tập 2
Công nghệ : Autograd: requires_grad=True, backward(), grad

Cách hoạt động : 
Khởi tạo x = 2, alpha = 0.1, bật requires_grad=True ( đùng để tính (đạo hàm) khi train model.
Lặp 10 lần tính y = x^3 + 2x^2 + 5x + 1 và cập nhật x = x - alpha * x.grad
In ra x và dy/dx sau mỗi vòng

Kết quả : 
Ban đầu: x = 2.0 | dy/dx = 25.0
Vòng 01: x = -3.000000 | dy/dx = 50.000000
Vòng 02: x = -5.000000 | dy/dx = 20.000000
Vòng 03: x = -11.000000 | dy/dx = 60.000000
Vòng 04: x = -43.400002 | dy/dx = 324.000000
Vòng 05: x = -591.608093 | dy/dx = 5482.080566
Vòng 06: x = -105355.507812 | dy/dx = 1047638.937500
Vòng 07: x = -3329998336.000000 | dy/dx = 33298927616.000000
Vòng 08: x = -3326666712958369792.000000 | dy/dx = 33266667679339511808.000000
Vòng 09: x = -3320013366952489364115158725096898560.000000 | dy/dx = 33200134303350193755266287999320588288.000000
Vòng 10: x = -inf | dy/dx = inf

# Bài tập 3
Công nghệ : Tạo dữ liệu ngẫu nhiên: torch.randint, torch.randn

Cách hoạt động 
x ngẫu nhiên
y = 3x + 5 + noise
tạo tham số w và b ngẫu nhiên Train 100 vòng lặp 
Dự đoán 
In loss và giá trị w, b theo epoch ( kết quả tóm tắc lại thành 11 vòng do em prinrt theo mốc )

Kết quả : 
Epoch 001 | MSE=743.8687 | w=2.8037 | b=-0.0630
Epoch 010 | MSE=5.0757 | w=3.6921 | b=0.2473
Epoch 020 | MSE=4.7027 | w=3.6646 | b=0.4379
Epoch 030 | MSE=4.3583 | w=3.6381 | b=0.6210
Epoch 040 | MSE=4.0403 | w=3.6127 | b=0.7969
Epoch 050 | MSE=3.7468 | w=3.5882 | b=0.9660
Epoch 060 | MSE=3.4758 | w=3.5648 | b=1.1284
Epoch 070 | MSE=3.2257 | w=3.5422 | b=1.2844
Epoch 080 | MSE=2.9948 | w=3.5206 | b=1.4344
Epoch 090 | MSE=2.7816 | w=3.4997 | b=1.5784
Epoch 100 | MSE=2.5848 | w=3.4797 | b=1.7168

Kết quả cuối: w ~ 3.4797468185424805  | b ~ 1.7168469429016113
# Bài tập 4
Công nghê : Chuyển NumPy - Tensor: torch.from_numpy()

Cách hoạt động : 
Tạo mảng NumPy arr
x = torch.from_numpy(arr) dùng chung bộ nhớ và x = torch.tensor(arr)  copy dữ liệu
Thay đổi arr[0] = 99 rồi quan sát tensor đổi hay không

Kết quả :
Trong trường hợp 1 khi dùng hàm torch.from_numpy(arr) với mục đích là tạo ra một Tensor đống vai trò như một lớp vỏ bao bọc vùng bộ nhớ của mảng Numpy. Khác với trường hợp 2 khi dùng hàm torch.tensor(arr) là tạo một vùng bộ nhớ hoàn toàn mới và sao chép toàn bộ giá trị từ mảng Numpy sang vùng bộ nhớ đó

Nên khi thực hiện arr[0] 99 với 2 trường hợp cho ra kết quả khác nhau, với trường hợp 1 là đang dùng chung một bộ nhớ, trường hợp 2 là đang dùng tensor cũ.
# Bài tập 5
Công nghệ : Tạo tensor

Cách hoạt động : 
Tạo các tensor 
Đổi shape :
reshape theo kích thước mình muốn ,reshape giống shape của tensor khác không giống với ban đầu rồi In kết quả ra 

Kết quả : 
empty:
 tensor([[0., 0., 0.],
        [0., 0., 0.]])

zeros:
 tensor([[0., 0., 0.],
        [0., 0., 0.]])

ones:
 tensor([[1., 1., 1.],
        [1., 1., 1.]])

random:
 tensor([[0.5699, 0.5677, 0.5848],
        [0.7786, 0.6291, 0.6111]])

view(3,4):
 tensor([[ 1,  2,  3,  4],
        [ 5,  6,  7,  8],
        [ 9, 10, 11, 12]])

view_as(2,6):
 tensor([[ 1,  2,  3,  4,  5,  6],

        [ 7,  8,  9, 10, 11, 12]])
