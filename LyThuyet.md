**SHELL SCRIPT - Việt Hùng**

# 1. Shell script là gì ?
- Shell script là chương trình giao tiếp với người dùng, có thể thực thi nhiều lệnh lệnh trong file shell chỉ bằng một lệnh khởi chạy file shell đó.

- Định nghĩa: **shell script** là một chuỗi các lệnh được viết trong plain text file, nố gần giống batch file trong MS-DOS nhưng mạnh hơn.

- Lợi ích của shell script: 

  - Shell script có thể nhận input từ user, file hoặc output từ màn hình
  - Tiện lợi để tạo nhóm lệnh riêng
  - Tiết kiêm thời gian
  - Tự động làm vài công việc thường xuyên

- Cách tạo và thực thi một chương trình shell:

  - Bước 1: Tạo file viethung.sh trên Desktop bằng lệnh:
    - touch viethung.sh
  - Bước 2: Cấp quyền thực thi cho file đó:
    - sudo chmod +x viethung.sh
  - Bước 3: Sử dụng gedit để code lệnh cho file shell
    - gedit viethung.sh
    - Soạn thảo nội dung sau: 
      - #!/bin/bash
      - echo "Hello Viet Hung"
  - Bước 4: Thực thi file shell bằng một trong các lệnh sau: 
    - sh viethung.sh
    - ./viethung.sh
    - bash hello.sh

# 2. Biến trong shell
Trong shell có hai loại biến: 
- Biến hệ thống: 
  - Được tạo ra và quản lý bởi Linux
  - Tên biến là chữ viết IN HOA
- Biến do người dùng định nghĩa
## 1. Biếm hệ thống

Ví dụ: file hello.sh

- Tạo file bằng lệnh terminal
  - touch hello.sh
- Code bằng gedit, gõ lệnh trên termanal
  - gedit hello.sh
- Gõ các lệnh sau:

#!/bin/bash
echo "Xin chao Viet Hung nha!"
echo "Have a nice night!"
echo -n "BASH_VERSION: "	# -n: option khong xuong dong
echo $BASH_VERSION
echo -n "BASH: "
echo $BASH
echo -n "HOME: "
echo $HOME
echo -n "PATH: "
echo $PATH

Lưu và chạy bằng lệnh terminal sau

- ./hello.sh
- Kết quả thu được trên console:

Xin chao Viet Hung nha!
Have a nice night!
BASH_VERSION: 4.4.19(1)-release
BASH: /bin/bash
HOME: /home/viethung
PATH: /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin

## 2. Biến người dùng đặt

- Cú pháp:

  varible_name=value

- Tên biến phải bắt đầu bằng ký tự hoặc dấu gạch dưới '_'

- Không có dấu khoảng trắng bên toán tử bằng:

  - Đúng: value=9
  - Sai: value = 9

- Tên biến có phân biệt chữ hoa và chữ thường

- Một biến không khởi tạo thì nhận giá trị NULL

- Không được dùng dấu '?', '*' để đặt tên biến

- Lệnh echo để in ra giá trị của biến

## 3. Các phép toán
- Cú pháp:
  - expr Toán_Hạng_1 Toán_Tử Toán_Hạng_2
- Ví dụ:
  - Đúng: 

- Dấu ngoặc: tất cả các dấu ngoặc đều không có ý nghĩa toán trừ những ký tự '\\' hoặc '$'
- Dấu ngoặc `: yêu cầu thực thi câu lệnh
- Kiểm tra trạng thái thực hiện của một câu lệnh
  - echo $?
  - Nếu trả về 0: câu lệnh thực hiện thành công, không có lỗi
  - Nếu trả về khác 0: câu lệnh thực hiện có lỗi.
## 4. Cấu trúc điều khiển
### 1. Lệnh rẽ nhánh if else
if Điều_Kiện
​	then Câu_Lệnh_1
else
​	Câu_Lệnh_2
fi
### 2. Câu lệnh for

```Powershell
for { tên biến } in { danh sách }
do
# Khối lệnh
# Thực hiện từng mục trong danh sách cho đến cho đến hết
# (Và lặp lại tất cả các lệnh nằm trong "do" và "done")
done

#hoặc sử dụng for
for (( expr1; expr2; expr3 ))
do
# Lặp cho đến khi biểu thức expr2 trả về giá trị TRUE
done
```

### 3. Vòng lặp while
while [Điều_Kiện]
do 
	Câu_Lệnh_1
	Câu_Lệnh_2
	.........
done











Nguồn tìm hiểu: https://viblo.asia/p/tim-hieu-lap-trinh-shell-linux-p1-wjAM7ydbvmWe