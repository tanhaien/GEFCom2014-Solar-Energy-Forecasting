Trong data nay bao gom 15 task
Moi task gom 3 file

- Benchmark
- Predictors
- Train

- Benchmark: du lieu gi khong biet
- Predictors: du lieu tu cac farm solar trong paper
- Train: label cua du lieu

Train bao gom khoang 75% du lieu da duoc label - mapping voi data trong Predictors, con lai data trong Predictors chua dc label

Nhiem vu 1: Split 25% data khong label ra file test.csv (output)
Nhiem vu 2: Apply XGBoost nhu mr.Thang said la best => Xem output the nao?

Cac truong hop nhu sau:
- Apply tren tuong data trong moi task
- Apply tren toan bo data cac task 
-------------------

So do khoi code xu ly nhu sau:

Step 1: Doc dataframe tu solar farm
Step 2: Doc label cho data cua solar farm tu file train.csv
Step 3: Tim kiem vi tri ma data bat dau khong duoc gan nhan
Bien "slice_index" chinh la vi tri de Split

Final step: Split data bat dau tu slice_index tro di, luu lai vao "test.csv"