---
title: "Testing workflow"
datePublished: Mon Jun 09 2025 09:13:24 GMT+0000 (Coordinated Universal Time)
cuid: cmbovjznq000o02lb20q1eoub
slug: testing-workflow
tags: software-engineering

---

* ### **Test plan cho test hộp đen của module “Nhập truyện từ nhà cung cấp”** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>STT&nbsp;</p></td><td colspan="1" rowspan="1"><p>Module&nbsp;</p></td><td colspan="1" rowspan="1"><p>Test case&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="5"><p>Nhập truyện từ nhà cung cấp&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thêm 1 ImportBill: trong đó Provider đã tồn tại, Đầu truyện đã tồn tại&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thêm 1 ImportBill: trong đó Provider không tồn tại, Đầu truyện tồn tại&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thêm 1 ImportBill: trong đó Provider tồn tại, Đầu truyện không tồn tại&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thêm 1 ImportBill: trong đó Provider và Đầu truyện không tồn tại&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thêm 2 lần liên tục 1 ImportBill: trong đó Provider và Đầu truyện đã tồn tại&nbsp;</p></td></tr></tbody></table>

* ### **Test case chuẩn cho test hộp đen của module “nhập truyện từ nhà cung cấp”** 
    

**CSDL trước khi test** 

* **tblUser** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>id&nbsp;</p></td><td colspan="1" rowspan="1"><p>username&nbsp;</p></td><td colspan="1" rowspan="1"><p>password&nbsp;</p></td><td colspan="1" rowspan="1"><p>full_name&nbsp;</p></td><td colspan="1" rowspan="1"><p>role&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>a&nbsp;</p></td><td colspan="1" rowspan="1"><p>123456&nbsp;</p></td><td colspan="1" rowspan="1"><p>A&nbsp;</p></td><td colspan="1" rowspan="1"><p>Nhân viên kho&nbsp;</p></td></tr></tbody></table>

* **tblProvider** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>id&nbsp;</p></td><td colspan="1" rowspan="1"><p>name&nbsp;</p></td><td colspan="1" rowspan="1"><p>address&nbsp;</p></td><td colspan="1" rowspan="1"><p>email&nbsp;</p></td><td colspan="1" rowspan="1"><p>phone_number&nbsp;</p></td><td colspan="1" rowspan="1"><p>note&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>B&nbsp;</p></td><td colspan="1" rowspan="1"><p>Hà Đông, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccb@gmail.com" style="pointer-events: none">nccb@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0123456789&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện thiếu nhi&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>Bình An&nbsp;</p></td><td colspan="1" rowspan="1"><p>Hoàn Kiếm, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccbinhan@gmail.com" style="pointer-events: none">nccbinhan@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>123123123&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp tiểu thuyết&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>An Bình&nbsp;</p></td><td colspan="1" rowspan="1"><p>Đống Đa, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccanbinh@gmail.com" style="pointer-events: none">nccanbinh@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0129834122&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện Doraemon&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>An&nbsp;</p></td><td colspan="1" rowspan="1"><p>Quận 10, Sài Gòn&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccan@gmail.com" style="pointer-events: none">nccan@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0722645498&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện trinh thám&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>An B&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thanh Xuân, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccanb@gmail.com" style="pointer-events: none">nccanb@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0912834162&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện tranh&nbsp;</p></td></tr></tbody></table>

* **tblBookTitle** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>id&nbsp;</p></td><td colspan="1" rowspan="1"><p>name&nbsp;</p></td><td colspan="1" rowspan="1"><p>author&nbsp;</p></td><td colspan="1" rowspan="1"><p>publication_year&nbsp;</p></td><td colspan="1" rowspan="1"><p>publisher&nbsp;</p></td><td colspan="1" rowspan="1"><p>unit_price&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 6&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>2023&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>2023&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 7&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>2023&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>Ngoại truyện 7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>2024&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>Ngoại truyện 7 viên ngọc rồng tập 6&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>2024&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td></tr></tbody></table>

* **tblImportBill** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>id&nbsp;</p></td><td colspan="1" rowspan="1"><p>import_date&nbsp;</p></td><td colspan="1" rowspan="1"><p>sale_off&nbsp;</p></td><td colspan="1" rowspan="1"><p>payment_method&nbsp;</p></td><td colspan="1" rowspan="1"><p>note&nbsp;</p></td><td colspan="1" rowspan="1"><p>user_id&nbsp;</p></td><td colspan="1" rowspan="1"><p>provider_id&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-01&nbsp;</p></td><td colspan="1" rowspan="1"><p>1000000&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyển khoản&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giảm 100000 cho lần nhập đầu tiên&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-01&nbsp;</p></td><td colspan="1" rowspan="1"><p>1000000&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thẻ tín dụng&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giảm giá do thanh toán bằng thẻ tín dụng&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-02&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tiền mặt&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-02&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyển khoản&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-02&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tiền mặt&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td></tr></tbody></table>

* **tblImportedBookTitle** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>id&nbsp;</p></td><td colspan="1" rowspan="1"><p>quantity&nbsp;</p></td><td colspan="1" rowspan="1"><p>unit_price&nbsp;</p></td><td colspan="1" rowspan="1"><p>import_bill_id&nbsp;</p></td><td colspan="1" rowspan="1"><p>book_title_id&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>30&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>25&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>15&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>30&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>6&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>7&nbsp;</p></td><td colspan="1" rowspan="1"><p>15&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>8&nbsp;</p></td><td colspan="1" rowspan="1"><p>25&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>9&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>10&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td></tr></tbody></table>

**Kịch bản và kết quả mong đợi** 

<table><tbody><tr><td colspan="1" rowspan="1"><p>Kịch bản&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kết quả mong đợi&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1.Đăng nhập:&nbsp;Nhân viên kho nhập username= a, password = 123456 và nhấn vào nút Đăng nhập</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>2. Nhân viên kho chọn chức năng nhập truyện từ nhà cung cấp&nbsp;</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>3. Nhân viên kho nhập vào ô tên nhà cung cấp là: B và nhấn nút tìm kiếm&nbsp;</p></td><td colspan="1" rowspan="1"><p>- Giao diện tìm kiếm nhà cung cấp:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4. Nhân viên kho chọn dòng số 1 ứng với thông tin nhà cung cấp B của giao diện tìm kiếm nhà cung cấp&nbsp;</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>5. Nhân viên kho nhập vào ô tên đầu truyện là: bảy viên ngọc rồng tập 6 và nhấn nút tìm kiếm&nbsp;</p></td><td colspan="1" rowspan="1"><p>- Giao diện tìm kiếm đầu truyện:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>6. Nhân viên kho chọn dòng số 1 ứng với thông tin đầu truyện: 7 viên ngọc rổng tập 6 của giao diện tìm kiếm đầu truyện&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giao diện nhập số lượng truyện:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>7. Nhân viên kho nhập vào ô số lượng truyện là 20 và nhấn nút xác nhận&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giao diện danh sách các truyện nhập:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>8. Nhân viên kho nhấn vào nút nhập thêm truyện&nbsp;</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>9. Nhân viên kho nhập vào ô tên đầu truyện là: 7 viên ngọc rồng tập 60 và nhấn vào nút tìm kiếm&nbsp;</p></td><td colspan="1" rowspan="1"><p>- Giao diện tìm kiếm đầu truyện:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>10. Nhân viên kho chọn dòng số 1 ứng với thông tin đầu truyện: 7 viên ngọc rổng tập 60 của giao diện tìm kiếm đầu truyện&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giao diện nhập số lượng truyện:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>11. Nhân viên kho nhập vào ô số lượng truyện là 15 và nhấn nút xác nhận&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giao diện danh sách các truyện nhập:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>12. Nhân viên kho nhấn vào nút xác nhận&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giao diện xác nhận nhập truyện:&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>13. Nhân viên kho nhập vào ô giảm giá = 0, chọn phương thức thanh toán là chuyển khoản và nhấn in hoá đơn&nbsp;</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody></table>

 kết quả mong đợi

* 1:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749460022050/ea10abd2-f757-4641-9510-3f3eac8c4701.png align="center")
    
* 2
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749460081501/2571a5e9-9b61-4040-b732-ac5ba6adfc9b.png align="center")

* 3
    

Giao diện tìm kiếm nhà cung cấp: 

\+ ô tên nhà cung cấp: B 

\+ nút tìm kiếm 

\+ nút thêm mới nhà cung cấp 

\+ kết quả tìm kiếm: 

<table><tbody><tr><td colspan="1" rowspan="1"><p>STT&nbsp;</p></td><td colspan="1" rowspan="1"><p>Mã&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tên&nbsp;</p></td><td colspan="1" rowspan="1"><p>Địa chỉ&nbsp;</p></td><td colspan="1" rowspan="1"><p>email&nbsp;</p></td><td colspan="1" rowspan="1"><p>Số điện thoại&nbsp;</p></td><td colspan="1" rowspan="1"><p>Ghi chú&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>B&nbsp;</p></td><td colspan="1" rowspan="1"><p>Hà Đông, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccb@gmail.com" style="pointer-events: none">nccb@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0123456789&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện thiếu nhi&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>Bình An&nbsp;</p></td><td colspan="1" rowspan="1"><p>Hoàn Kiếm, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccbinhan@gmail.com" style="pointer-events: none">nccbinhan@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>123123123&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp tiểu thuyết&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>An Bình&nbsp;</p></td><td colspan="1" rowspan="1"><p>Đống Đa, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccanbinh@gmail.com" style="pointer-events: none">nccanbinh@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0129834122&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện Doraemon&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>An B&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thanh Xuân,Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccanb@gmail.com" style="pointer-events: none">nccanb@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0912834162&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện tranh&nbsp;</p></td></tr></tbody></table>

* 4
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749460129053/2dd8d7e7-b812-4ea2-9f9d-73caa071d5fa.png align="center")

* 5
    

\- Giao diện tìm kiếm đầu truyện: 

\+ ô tên đầu truyện: 7 viên ngọc rồng tập 6 

\+ nút tìm kiếm 

\+ nút thêm mới đầu truyện 

\+ kết quả tìm kiếm: 

<table><tbody><tr><td colspan="1" rowspan="1"><p>STT&nbsp;</p></td><td colspan="1" rowspan="1"><p>Mã&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tên&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tác giả&nbsp;</p></td><td colspan="1" rowspan="1"><p>Nhà xuất bản&nbsp;</p></td><td colspan="1" rowspan="1"><p>Năm xuất bản&nbsp;</p></td><td colspan="1" rowspan="1"><p>Đơn giá&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 6&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>2023&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>2023&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>Ngoại truyện 7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>2024&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>Ngoại truyện 7 viên ngọc rồng tập 6&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>2024&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td></tr></tbody></table>

* 6
    

Giao diện nhập số lượng truyện: 

* Thông tin đầu truyện: 
    

\+ Mã: 1 

\+ Tên: 7 viên ngọc rồng tập 6 

\+ Tác giả: Akira Toriyama 

\+ Nhà xuât bản: Kim Đồng 

\+ Năm xuất bản: 2023 

\+ Đơn giá: 30000 

* Ô nhập số lượng truyện 
    

* Nút xác nhận 
    

* Nút huỷ 
    

* 7
    

Giao diện danh sách các truyện nhập: 

\- Nút xác nhận, huỷ 

\- Nút nhập thêm truyện 

\- Danh sách các đầu truyện nhập: 

<table><tbody><tr><td colspan="1" rowspan="1"><p>STT&nbsp;</p></td><td colspan="1" rowspan="1"><p>Mã&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tên&nbsp;</p></td><td colspan="1" rowspan="1"><p>Đơn giá&nbsp;</p></td><td colspan="1" rowspan="1"><p>Số lượng&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thành tiền&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 6&nbsp;</p></td><td colspan="1" rowspan="1"><p>30,000&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>600,000&nbsp;</p></td></tr></tbody></table>

* 8
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749460206492/ad92baf8-c6fb-4328-8456-11e1d2b48631.png align="center")

* 9
    

\- Giao diện tìm kiếm đầu truyện: 

\+ ô tên đầu truyện: 7 viên ngọc rồng tập 60 

\+ nút tìm kiếm 

\+ nút thêm mới đầu truyện 

\+ kết quả tìm kiếm: 

<table><tbody><tr><td colspan="1" rowspan="1"><p>STT&nbsp;</p></td><td colspan="1" rowspan="1"><p>Mã&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tên&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tác giả&nbsp;</p></td><td colspan="1" rowspan="1"><p>Nhà xuất bản&nbsp;</p></td><td colspan="1" rowspan="1"><p>Năm xuất bản&nbsp;</p></td><td colspan="1" rowspan="1"><p>Đơn giá&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>2023&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>Ngoại truyện 7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>Akira Toriyama&nbsp;</p></td><td colspan="1" rowspan="1"><p>Kim Đồng&nbsp;</p></td><td colspan="1" rowspan="1"><p>2024&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td></tr></tbody></table>

* 10
    

Giao diện nhập số lượng truyện: 

* Thông tin đầu truyện: 
    

\+ Mã: 2 

\+ Tên: 7 viên ngọc rồng tập 60 

\+ Tác giả: Akira Toriyama 

\+ Nhà xuât bản: Kim Đồng 

\+ Năm xuất bản: 2023 

\+ Đơn giá: 30000 

* Ô nhập số lượng truyện 
    

* Nút xác nhận 
    

* Nút huỷ 
    

* 11
    

Giao diện danh sách các truyện nhập: 

\- Nút xác nhận, huỷ 

\- Nút nhập thêm truyện 

\- Danh sách các đầu truyện nhập: 

<table><tbody><tr><td colspan="1" rowspan="1"><p>STT&nbsp;</p></td><td colspan="1" rowspan="1"><p>Mã&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tên&nbsp;</p></td><td colspan="1" rowspan="1"><p>Đơn giá&nbsp;</p></td><td colspan="1" rowspan="1"><p>Số lượng&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thành tiền&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 6&nbsp;</p></td><td colspan="1" rowspan="1"><p>30,000&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>600,000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>30,000&nbsp;</p></td><td colspan="1" rowspan="1"><p>15&nbsp;</p></td><td colspan="1" rowspan="1"><p>450,000&nbsp;</p></td></tr></tbody></table>

* 12
    

Giao diện xác nhận nhập truyện: 

\- Nút in, huỷ 

\- Tên nhân viên kho nhập truyện: A 

\- Ngày nhập truyện: 14/5/2025 

\- Thông tin nhà cung cấp: 

<table><tbody><tr><td colspan="1" rowspan="1"><p>Mã&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tên&nbsp;</p></td><td colspan="1" rowspan="1"><p>Địa chỉ&nbsp;</p></td><td colspan="1" rowspan="1"><p>Email&nbsp;</p></td><td colspan="1" rowspan="1"><p>Điện thoại&nbsp;</p></td><td colspan="1" rowspan="1"><p>Mô tả&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>B&nbsp;</p></td><td colspan="1" rowspan="1"><p>Hà Đông, Hà Nội&nbsp;</p></td><td colspan="1" rowspan="1"><p><a target="_self" rel="noopener noreferrer nofollow" href="mailto:nccb@gmail.com" style="pointer-events: none">nccb@gmail.com</a>&nbsp;</p></td><td colspan="1" rowspan="1"><p>0123456789&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyên cung cấp truyện thiếu nhi&nbsp;</p></td></tr></tbody></table>

\- Danh sách các truyện được nhập: 

<table><tbody><tr><td colspan="1" rowspan="1"><p>STT&nbsp;</p></td><td colspan="1" rowspan="1"><p>Mã&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tên&nbsp;</p></td><td colspan="1" rowspan="1"><p>Đơn giá&nbsp;</p></td><td colspan="1" rowspan="1"><p>Số lượng&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thành tiền&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 6&nbsp;</p></td><td colspan="1" rowspan="1"><p>30,000&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>600,000&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>7 viên ngọc rồng tập 60&nbsp;</p></td><td colspan="1" rowspan="1"><p>30,000&nbsp;</p></td><td colspan="1" rowspan="1"><p>15&nbsp;</p></td><td colspan="1" rowspan="1"><p>450,000&nbsp;</p></td></tr><tr><td colspan="5" rowspan="1"><p>Giảm giá&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td></tr><tr><td colspan="5" rowspan="1"><p>Tổng tiền&nbsp;</p></td><td colspan="1" rowspan="1"><p>1,050,000&nbsp;</p></td></tr><tr><td colspan="5" rowspan="1"><p>Phương thức thanh toán&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyển khoản&nbsp;</p></td></tr><tr><td colspan="5" rowspan="1"><p>Ghi chú&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td></tr></tbody></table>

* 13
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749460281849/20051f77-2e87-4f5f-9f97-65cc37af43ab.png align="center")

**CSDL sau khi test** 

* **tblImportBill** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>id&nbsp;</p></td><td colspan="1" rowspan="1"><p>import_date&nbsp;</p></td><td colspan="1" rowspan="1"><p>sale_off&nbsp;</p></td><td colspan="1" rowspan="1"><p>payment_method&nbsp;</p></td><td colspan="1" rowspan="1"><p>note&nbsp;</p></td><td colspan="1" rowspan="1"><p>user_id&nbsp;</p></td><td colspan="1" rowspan="1"><p>provider_id&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-01&nbsp;</p></td><td colspan="1" rowspan="1"><p>1000000&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyển khoản&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giảm 100000 cho lần nhập đầu tiên&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-01&nbsp;</p></td><td colspan="1" rowspan="1"><p>1000000&nbsp;</p></td><td colspan="1" rowspan="1"><p>Thẻ tín dụng&nbsp;</p></td><td colspan="1" rowspan="1"><p>Giảm giá do thanh toán bằng thẻ tín dụng&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-02&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tiền mặt&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-02&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyển khoản&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-02&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td><td colspan="1" rowspan="1"><p>Tiền mặt&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>6&nbsp;</p></td><td colspan="1" rowspan="1"><p>2025-05-14&nbsp;</p></td><td colspan="1" rowspan="1"><p>0&nbsp;</p></td><td colspan="1" rowspan="1"><p>Chuyển khoản&nbsp;</p></td><td colspan="1" rowspan="1"><p>&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr></tbody></table>

* **tblImportedBookTitle** 
    

<table><tbody><tr><td colspan="1" rowspan="1"><p>id&nbsp;</p></td><td colspan="1" rowspan="1"><p>quantity&nbsp;</p></td><td colspan="1" rowspan="1"><p>unit_price&nbsp;</p></td><td colspan="1" rowspan="1"><p>import_bill_id&nbsp;</p></td><td colspan="1" rowspan="1"><p>book_title_id&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>30&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>25&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>15&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>30&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>6&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>7&nbsp;</p></td><td colspan="1" rowspan="1"><p>15&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>8&nbsp;</p></td><td colspan="1" rowspan="1"><p>25&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>3&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>9&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td><td colspan="1" rowspan="1"><p>4&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>10&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>40000&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td><td colspan="1" rowspan="1"><p>5&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>11&nbsp;</p></td><td colspan="1" rowspan="1"><p>20&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>6&nbsp;</p></td><td colspan="1" rowspan="1"><p>1&nbsp;</p></td></tr><tr><td colspan="1" rowspan="1"><p>12&nbsp;</p></td><td colspan="1" rowspan="1"><p>15&nbsp;</p></td><td colspan="1" rowspan="1"><p>30000&nbsp;</p></td><td colspan="1" rowspan="1"><p>6&nbsp;</p></td><td colspan="1" rowspan="1"><p>2&nbsp;</p></td></tr></tbody></table>