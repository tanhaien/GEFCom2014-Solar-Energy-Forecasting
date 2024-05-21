# GEFCom2014 Data Set

Tập dữ liệu này bao gồm 15 task. Mỗi task gồm 3 file:

- **Benchmark**: Dữ liệu không rõ
- **Predictors**: Dữ liệu từ các trang trại năng lượng mặt trời trong bài báo
- **Train**: Nhãn của dữ liệu

File **Train** bao gồm khoảng 75% dữ liệu đã được gán nhãn - ánh xạ với dữ liệu trong **Predictors**, phần còn lại của dữ liệu trong **Predictors** chưa được gán nhãn.

## Nhiệm vụ

1. **Nhiệm vụ 1**: Chia 25% dữ liệu không gán nhãn ra file test.csv (output)
2. **Nhiệm vụ 2**: Áp dụng XGBoost
   - Áp dụng trên từng dữ liệu trong mỗi task
   - Áp dụng trên toàn bộ dữ liệu các task

## Sơ đồ khối code xử lý

1. **Bước 1**: Đọc dataframe từ trang trại năng lượng mặt trời
2. **Bước 2**: Đọc nhãn cho dữ liệu của trang trại năng lượng mặt trời từ file train.csv
3. **Bước 3**: Tìm kiếm vị trí mà dữ liệu bắt đầu không được gán nhãn. Biến "slice_index" chính là vị trí để chia dữ liệu
4. **Bước cuối cùng**: Chia dữ liệu bắt đầu từ "slice_index" trở đi, lưu lại vào "test.csv"
