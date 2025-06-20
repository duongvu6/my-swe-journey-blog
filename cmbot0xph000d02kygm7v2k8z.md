---
title: "Đề 27 Ngân hàng NMCNPM"
datePublished: Mon Jun 09 2025 08:02:36 GMT+0000 (Coordinated Universal Time)
cuid: cmbot0xph000d02kygm7v2k8z
slug: de-27-ngan-hang-nmcnpm
tags: software-engineering

---

### Viết một scenario chuẩn cho use case này

* Kịch bản: “Lập phiếu xuất hàng”
    
* Actor(s): Nhân viên, đại lý con
    
* Pre condition: Nhân viên có tài khoản đúng kiểu của nhân viên
    
* Post condition: Nhân viên xuất hàng thành công cho đại lý con
    
* Main events:
    
    * 1. Đại lý con B có yêu cầu xuất hàng từ kho
            
        2. Nhân viên A bắt đầu việc xuất hàng bằng việc đăng nhập vào hệ thống với username=a,password=123456 và nhấn vào nút đăng nhập
            
        3. Hệ thống hiển thị giao diện trang chủ dành cho nhân viên có lựa chọn “xuất hàng”
            
        4. Nhân viên nhấn vào nút xuất hàng
            
        5. Hệ thống hiển thị giao diện tìm kiếm đại lý con:
            
            * ô nhập tên đại lý con
                
            * nút tìm kiếm
                
            * nút hủy
                
        6. nhân viên hỏi đại lý con thông tin của đại lý con
            
        7. đại lý con trả lời thông tin của mình:
            
            * tên: B
                
            * địa chỉ: Đống Đa, Hà Nội
                
            * số điện thoại: 0123456789
                
        8. nhân viên nhập tên đại lý con vào ô nhập tên đại lý con và nhấn vào nút tìm kiếm
            
        9. hệ thống hiển thị giao diện kết quả tìm kiếm đại lý con:
            
            * ô tên đại lý con: B
                
            * nút tìm kiếm, hủy
                
            * kết quả tìm kiếm:
                

| STT | Mã đại lý | tên đại lý | địa chỉ | số điện thoại |
| --- | --- | --- | --- | --- |
| 1 | 1 | B | Đống Đa, Hà Nội | 0123456789 |
| 2 | 2 | Bình An | Hà Đông, Hà Nội | 0987654321 |
| 3 | 3 | B | Thanh Xuân, Hà Nội | 0123123123 |

* 10. Nhân viên nhấn vào dòng số 1
        
    11. Hệ thống hiển thị giao diện tìm hàng xuất:
        
        * ô nhập tên hàng:
            
        * nút tìm kiếm, hủy
            
    12. nhân viên hỏi đại lý con thông tin hàng hóa muốn xuất
        
    13. đại lý con trả lời thông tin hàng hóa muốn xuất:
        
        * tên: Kem đánh răng PS
            
    14. nhân viên nhập “Kem đánh răng PS” vào ô nhập tên hàng và nhấn vào nút tìm kiếm
        
    15. hệ thống hiển thị giao diện kết quả tìm kiếm hàng xuất:
        
        * ô tên hàng: Kem đánh răng PS
            
        * nút tìm kiếm, hủy
            
        * kết quả tìm kiếm
            

| STT | mã hàng | tên hàng | mô tả | số lượng |
| --- | --- | --- | --- | --- |
| 1 | 1 | Kem đánh răng PS |  | 50 |
| 2 | 2 | Kem đánh răng PS loại đặc biệt | Loại đặc biệt | 30 |
| 3 | 3 | Kem đánh răng PS hương Dứa | Hương dứa | 20 |

* 16. nhân viên nhấn vào dòng số 1
        
    17. hệ thống hiển thị giao diện nhập số lượng và đơn giá:
        
* mã hàng: 1
    
* tên hàng: Kem đánh răng PS
    
* ô nhập số lượng
    
* ô nhập đơn giá
    
* nút xác nhận, reset
    
* 16. nhân viên hỏi đại lý con số lượng muốn xuất
        
    17. đại lý con trả lời số lượng muốn xuất là 30
        
    18. nhân viên nhập số lượng = 30, đơn giá = 40000 và nhấn vào nút xác nhận
        
    19. hệ thống hiển thị giao diện hóa đơn xuất:
        
        * ngày lập: 4/5/2025
            
        * tên nhân viên lập: A
            
        * thông tin đại lý con
            

| Mã đại lý | tên đại lý | địa chỉ | số điện thoại |
| --- | --- | --- | --- |
| 1 | B | Đống Đa, Hà Nội | 0123456789 |

* danh sách các mặt hàng xuất đi:
    

| STT | mã hàng | tên hàng | mô tả | số lượng | đơn giá | thành tiền |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 1 | Kem đánh răng PS |  | 30 | 40,000 | 1,200,000 |

* tổng tiền: 1,200,000
    
* ô nhập giảm giá:
    
* ô chọn kiểu thanh toán
    
* nút xác nhận
    
    20. nhân viên thông báo số tiền thanh toán cho đại lý con là 1,200,000 và yêu cầu đại lý con thanh toán
        
    21. đại lý con thanh toán số tiền 1,200,000 bằng hình thức chuyển khoản
        
    22. nhân viên nhập ô giảm giá = 0, chọn kiểu thanh toán = chuyển khoản và nhấn vào nút xác nhận
        
    23. hệ thống thông báo xuất thành công và in ra hóa đơn xuất:
        
        * ngày lập: 4/5/2025
            
        * tên nhân viên lập: A
            
        * thông tin đại lý con
            

| Mã đại lý | tên đại lý | địa chỉ | số điện thoại |
| --- | --- | --- | --- |
| 1 | B | Đống Đa, Hà Nội | 0123456789 |

* danh sách các mặt hàng xuất đi:
    

| STT | mã hàng | tên hàng | mô tả | số lượng | đơn giá | thành tiền |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 1 | Kem đánh răng PS |  | 30 | 40,000 | 1,200,000 |

* tổng tiền: 1,200,000
    
* giảm giá: 0
    
* kiểu thanh toán: chuyển khoản
    

### Trích và vẽ biểu đồ các lớp thực thể của toàn bộ hệ thống

* các danh từ:
    
    * nhân viên → lớp thực thể User
        
    * username, password → thuộc tính lớp User
        
    * hàng hóa → lớp thực thể HangHoa
        
    * (Mã hàng, tên, mô tả, số lượng tồn) → thuộc tính lớp HangHoa
        
    * số lượng nhập, giá nhập → thuộc tính lớp HangNhap
        
    * nhà cung cấp → lớp thực thể NhaCungCap
        
    * (mã NCC, tên NCC, địa chỉ, số ĐT) → thuộc tính lớp NhaCungCap
        
    * mặt hàng nhập → lớp thực thể HangNhap
        
    * hóa đơn nhập → lớp thực thể HoaDonNhap
        
    * số lượng, đơn giá, thành tiền → thuộc tính lớp HangNhap
        
    * tổng tiền của hóa đơn nhập → thuộc tính HoaDonNhap
        
    * đại lý con → lớp thực thể DaiLy
        
    * (mã ĐL, tên ĐL, địa chỉ, số ĐT) → thuộc tính lớp DaiLy
        
    * hóa đơn xuất → lớp thực thể HoaDonXuat
        
    * mặt hàng xuất → lớp thực thể HangXuat
        
    * số lượng, đơn giá, thành tiền → thuộc tính lớp HangXuat
        
    * tổng tiền của hóa đơn xuất → thuộc tính HoaDonXuat
        
* biểu đồ lớp thực thể hệ thống
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749436560453/b96251fe-c520-466c-a3e2-69ea41deccd3.jpeg align="center")

### Thiết kế tĩnh: thiết kế giao diện và vẽ biểu đồ lớp MVC chi tiết cho modul

* thiết kế giao diện
    
    * giao diện đăng nhập
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749436647573/aaaf3c21-05dc-4295-b9d2-b4442d7409bc.png align="center")
    
    * giao diện trang chủ cho nhân viên
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749436764928/ee86b793-8ae3-4598-8491-390f9e084101.png align="center")
    
    * giao diện tìm kiếm đại lý con
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749437066893/6d37f77d-5b06-4a37-b2b6-900cb43b66d7.png align="center")
    
    * giao diện thêm mới đại lý
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749437173966/8dc8a951-9def-4104-8a71-a7f04cbf92b0.png align="center")
    
    * giao diện tìm kiếm hàng
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749437373801/25b7fc80-e5a5-4403-b8ed-7b6f57e275cc.png align="center")
    
    * giao diện nhập số lượng, đơn giá hàng xuất
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749438856639/7e9e1822-7877-4989-bafd-9635ea07ec6d.png align="center")
    
    * giao diện hóa đơn xuất
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749456038107/5a628743-98be-4184-9566-4f1adaa4f616.png align="center")

* thiết kế biểu đồ lớp chi tiết MVC module
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749456094655/2466dc0e-f0ec-43db-8151-bc673edeb4d0.jpeg align="center")

### Thiết kế động: vẽ biểu đồ tuần tự mô tả tuần tự hoạt động của modul

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749452688681/52d42c01-1048-426c-8619-1f11a93f25c6.jpeg align="center")

### Viết một test case chuẩn cho modul này

* csdl trước khi test
    
    * tblUser
        

| id | vai\_tro | ten | username | password |
| --- | --- | --- | --- | --- |
| 1 | Nhân viên | A | a | 123456 |

* tblDaiLy
    

| id | dia\_chi | so\_dt | ten |
| --- | --- | --- | --- |
| 1 | Đống Đa, Hà Nội | 0123456789 | B |
| 2 | Hà Đông, Hà Nội | 0987654321 | Bình An |
| 3 | Thanh Xuân, Hà Nội | 0123123123 | B |

* tblHangHoa
    

| id | so\_luong\_ton | mo\_ta | ten |
| --- | --- | --- | --- |
| 1 | 50 |  | Kem đánh răng PS |
| 2 | 30 | loại đặc biệt | Kem đánh răng PS loại đặc biệt |
| 3 | 20 | hương dứa | Kem đánh răng PS hương dứa |

* tblHoaDonXuat
    

| id | ngay\_lap | kieu\_thanh\_toan | giam\_gia | user\_id | dai\_ly\_id |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

* tblHangXuat
    

| id | don\_gia | so\_luong | hang\_hoa\_id | hoa\_don\_xuat\_id |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

* kịch bản và kết quả mong đợi
    
    * 1. nhân viên đăng nhập vào hệ thống với username=a, password=123456 và nhấn vào nút đăng nhập
            
    * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749455705808/1fa4a7d6-a668-4061-8586-9306ca56eed3.png align="center")
        
        2\. nhân viên nhấn vào nút xuất hàng
        

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749455751244/94fc8ec6-d7cc-4f7b-8425-54d59f064902.png align="center")

3. nhân viên nhập tên đại lý = B và nhấn vào nút tìm kiếm
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749455821346/bdda7c0a-1d45-430a-8257-79bf8300c0b6.png align="center")

4. nhân viên nhấn vào dòng số 1
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749455870715/f91a4105-be1f-43e7-a56f-0444168cda36.png align="center")

5. nhân viên nhập tên hàng hóa = “Kem đánh răng PS” và nhấn vào nút tìm kiếm
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749455901068/440392c4-a98a-4867-afd9-f0bd25f68278.png align="center")

6. nhân viên nhấn vào dòng số 1
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749455929821/fa0cbbbe-a7fb-4894-bd3c-c13db155aaec.png align="center")

7. nhân viên nhập số lượng =30, đơn giá = 40 và nhấn vào nút xác nhận
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749456044968/ebfaebb3-5151-4c55-b2a3-a3dfb533465e.png align="center")

8. nhân viên nhấn nút xác nhận
    
    hệ thống hiển thị thông báo xuất thành công + in hóa đơn
    

* csdl sau khi test
    
* tblHoaDonXuat
    

| id | ngay\_lap | kieu\_thanh\_toan | giam\_gia | user\_id | dai\_ly\_id |
| --- | --- | --- | --- | --- | --- |
| 1 | 4/5/2025 | chuyển khoản | 0 | 1 | 1 |

* tblHangXuat
    

| id | don\_gia | so\_luong | hang\_hoa\_id | hoa\_don\_xuat\_id |
| --- | --- | --- | --- | --- |
| 1 | 40,000 | 30 | 1 | 1 |