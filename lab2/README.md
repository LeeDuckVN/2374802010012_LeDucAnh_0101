Bài tập 1 — Autograd tính đạo hàm đa thức
Công nghệ sử dụng

Python 3.x

PyTorch (torch) — Autograd (requires_grad, backward, grad)

Cách hoạt động

Tạo x là tensor 1 giá trị và bật requires_grad=True

Tính hàm đa thức y

Gọi y.backward() để PyTorch tự tính đạo hàm

Lấy đạo hàm tại điểm bằng x.grad

Kết quả

In ra đạo hàm tại x = 3

Kiểm tra độ dốc gần 0 của đa thức thứ 2 (tìm x sao cho gradient ≈ 0)

Bài tập 2 — Gradient Descent 10 vòng
Công nghệ sử dụng

Python 3.x

PyTorch (torch) — Autograd + cập nhật Gradient Descent

Cách hoạt động

Khởi tạo x = 2, alpha = 0.1, bật requires_grad=True

Với mỗi vòng lặp:

tính y

gọi backward() lấy gradient dy/dx

cập nhật x = x - alpha * gradient

reset gradient x.grad.zero_()

Kết quả

In ra x và dy/dx sau mỗi vòng (tổng 10 vòng)

Quan sát giá trị x thay đổi theo Gradient Descent

Bài tập 3 — Train hồi quy tuyến tính (w, b) với dữ liệu giả lập
Công nghệ sử dụng

Python 3.x

PyTorch (torch) — Tensor, Autograd, MSE Loss, Gradient Descent

Cách hoạt động

Sinh dữ liệu giả:

x là số giờ học

y = 3x + 5 + noise

Khởi tạo w và b ngẫu nhiên (requires_grad=True)

Dự đoán y_hat = w*x + b

Tính loss MSE

backward() lấy gradient

Cập nhật w, b bằng Gradient Descent trong 100 epoch

Reset gradient sau mỗi epoch

Kết quả

Loss giảm theo epoch

w tiến gần 3, b tiến gần 5

Bài tập 4 — So sánh torch.from_numpy() và torch.tensor()
Công nghệ sử dụng

Python 3.x

NumPy

PyTorch (torch)

Cách hoạt động

Tạo mảng NumPy arr

TH1: x = torch.from_numpy(arr) → dùng chung bộ nhớ

TH2: x = torch.tensor(arr) → copy dữ liệu

Thay đổi arr[0] = 99 để quan sát kết quả

Kết quả

from_numpy: arr đổi → tensor đổi theo ✅

torch.tensor: arr đổi → tensor không đổi ✅

Bài tập 5 — Tạo Tensor và Reshape
Công nghệ sử dụng

Python 3.x

PyTorch (torch)

Cách hoạt động

Tạo tensor bằng:

torch.empty()

torch.zeros()

torch.ones()

torch.rand()

Tạo dãy số bằng torch.arange()

Đổi shape bằng:

view()

view_as()

Kết quả

In ra tensor mẫu (empty/zeros/ones/random)

Reshape đúng kích thước theo yêu cầu bằng view và view_as