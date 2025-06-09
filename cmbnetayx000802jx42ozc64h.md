---
title: "Đề 15 Ngân hàng NMCNPM"
datePublished: Sun Jun 08 2025 08:36:59 GMT+0000 (Coordinated Universal Time)
cuid: cmbnetayx000802jx42ozc64h
slug: de-15-ngan-hang-nmcnpm
tags: software-engineering

---

### Viết một scenario chuẩn cho use case này

* Kịch bản: Khách hàng hủy bỏ đặt tour
    
* Actor(s): Nhân viên, khách hàng
    
* Pre condition: Nhân viên có tài khoản đúng kiểu của nhân viên
    
* Post condition: Nhân viên hủy vé của khách hàng thành công
    
* Main events:
    
    1. Khách hàng B báo với nhân viên A rằng muốn trả vé, hủy bỏ đặt tour
        
    2. nhân viên A đăng nhập vào hệ thống với username =a , password=123456 và nhấn vào nút đăng nhập
        
    3. hệ thống hiển thị giao diện chính dành cho nhân viên có lựa chọn: “trả vé theo yêu cầu của khách”
        
    4. nhân viên chọn chức năng “trả vé theo yêu cầu của khách”
        
    5. Hệ thống hiển thị giao diện trả vé theo yêu cầu của khách:
        
        * ô nhập mã vé
            
        * nút tìm kiếm
            
        * nút hủy vé
            
    6. nhân viên hỏi khách hàng B mã vé muốn hủy
        
    7. khách hàng trả lời mã vé là 1
        
    8. nhân viên nhập mã vé 1 và nhấn vào nút tìm kiếm
        
    9. Giao diện hiển thị kết quả tìm kiếm:
        
        * ô nhập mã vé: 1
            
        * nút tìm kiếm
            
        * nút hủy vé
            
        * kết quả tìm kiếm:Thông tin chi tiết của vé:
            
            * tên tour: Tour Mộc Châu
                
            * nơi đi: Thanh Xuân, Hà Nội
                
            * nơi đến: Mộc Châu
                
            * ngày đi:4/5/2025
                
            * tên khách đại diện đoàn: Nguyễn Văn B
                
            * số ID: 0123456789
                
            * kiểu ID: căn cước
                
            * địa chỉ khách: Hà Đông, Hà Nội
                
            * số điện thoại: 123123123
                
            * email: nguyenvanb@gmail.com
                
            * số lượng khách: 5
                
            * giá vé: 5,000,000
                
    10. Nhân viên nhấn vào nút hủy vé
        
    11. Hệ thống hiển thị giao diện hóa đơn phạt:
        
        * ngày lập: 3/5/2025
            
        * nhân viên lập: A
            
        * ô chọn kiểu thanh toán: có các lựa chọn: tiền mặt, thẻ, chuyển khoản
            
        * thông tin chi tiết của vé:
            
            * tên tour: Tour Mộc Châu
                
            * nơi đi: Thanh Xuân, Hà Nội
                
            * nơi đến: Mộc Châu
                
            * ngày đi:4/5/2025
                
            * tên khách đại diện đoàn: Nguyễn Văn B
                
            * số ID: 0123456789
                
            * kiểu ID: căn cước
                
            * địa chỉ khách: Hà Đông, Hà Nội
                
            * số điện thoại: 123123123
                
            * email: nguyenvanb@gmail.com
                
            * số lượng khách: 5
                
            * giá vé: 5,000,000
                
        * tiền phạt: 5,000,000
            
        * nút ok
            
    12. Nhân viên thông báo cho khách hàng tiền phạt là 5,000,000
        
    13. khách hàng thanh toán tiền phạt cho nhân viên bằng hình thức chuyển khoản
        
    14. nhân viên chọn kiểu thanh toán là chuyển khoản và nhấn vào nút ok
        
    15. hệ thống hiển thị thông báo trả vé thành công
        
    16. nhân viên thông báo cho khách hàng trả vé thành công
        

### Trích và vẽ biểu đồ các lớp thực thể của toàn bộ hệ thống

các danh từ:

* tour: đề xuất làm lớp thực thể Tour
    
* Mã tour, tên, nơi xuất phát, nơi đến, mô tả → thuộc tính tour
    
* ngày xuất phát → lớp LichtrinhTour
    
* số lượng người mua tour cho mỗi đoàn
    
* giá vé: → thuộc tính lớp vé, thuộc tính lớp LichTrinhTour
    
* khách hàng → lớp thực thể KhachHang
    
* (Mã, tên, số ID, loại thẻ ID, số ĐT, email, địa chỉ) → thuộc tính lớp KhachHang
    
* vé → lớp thực thể Ve
    
* số lượng vé mua → thuộc tính lớp Ve
    
* hóa đơn mua → lớp thực thể HoaDonMua
    
* thông tin tour, ngày xuất phát, giá tour, số lượng khách, tên khách hàng đại diện, tổng số tiền thanh toán. → thuộc tính lớp HoaDonMua
    
* tiền phạt → thuộc tính lớp HoaDonPhat
    
* hóa đơn phạt → lớp thực thể HoaDonPhat
    
* tiền thừa → loại vì ngoài phạm vi hệ thống
    
* hệ thống → loại vì quá chung chung
    
* giao diện→ loại vì quá chung chung
    
* ô, nút→ loại vì ngoài phạm vi hệ thống
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749382110672/c0503965-329c-4e38-a84a-b609db6d2db8.jpeg align="center")

### Thiết kế tĩnh: thiết kế giao diện và vẽ biểu đồ lớp MVC chi tiết cho modul

* Thiết kế giao diện:
    
    * Giao diện đăng nhập
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749390460128/2d47fb16-c4ae-4dcc-bc08-92ad325b0ac6.png align="center")
        
        ![](https://powerpoint.officeapps.live.com/pods/GetClipboardImage.ashx?Id=5aa83e04-ed5d-4c58-be53-3c4ca787e1d4&DC=PSG3&pkey=efb70a7a-f8a5-4a3f-9ed5-3be6dd72f043&wdwaccluster=PSG3 align="left")
        
    * giao diện trang chủ cho nhân viên
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749390597543/9e43e2c3-f85d-45d0-9117-89d5ccf9a384.png align="center")
        
        ![](https://powerpoint.officeapps.live.com/pods/GetClipboardImage.ashx?Id=26c1ea5e-6f8e-49df-bf57-66dafd05321e&DC=PSG3&pkey=7850eb37-1570-43f4-beb8-5c2b0e2a888c&wdwaccluster=PSG3 align="left")
        
    * giao diện trả vé theo yêu cầu của khách:
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749428491325/1bf95659-4d50-4ccc-89b9-7c8df4b9ef92.png align="center")
    
    ![](https://powerpoint.officeapps.live.com/pods/GetClipboardImage.ashx?Id=9ca53505-5725-4d0f-a44b-3b8dff34fbec&DC=PSG3&pkey=17a55f36-267a-4d62-9c4b-3ab1fe1a16be&wdwaccluster=PSG3 align="left")
    
    * giao diện hóa đơn phạt
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749428512368/1746ff8c-937f-498f-ba14-e82c2ec25c51.png align="center")
        
        ![](https://powerpoint.officeapps.live.com/pods/GetClipboardImage.ashx?Id=50e111ee-ea08-4848-91f6-e3a608763e28&DC=PSG3&pkey=c48866a8-daa9-4cdc-b2bb-fc35b1c2edd1&wdwaccluster=PSG3 align="left")
        
* Thiết kế biểu đồ MVC chi tiết
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749393835405/a3c1fd57-3543-4d75-8b57-7299841068e9.jpeg align="center")

### Thiết kế động: vẽ biểu đồ tuần tự mô tả tuần tự hoạt động của modul

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749396061670/065613bc-a845-45b5-b016-8d86c98b045d.jpeg align="center")

### Viết một test case chuẩn cho modul này

* CSDL trước khi test:
    
    * tblUser
        

| id | username | password | role | name |
| --- | --- | --- | --- | --- |
| 1 | a | 123456 | Nhân viên | A |

* tblKhachHang
    

| id | ten | so\_id | loai\_id | so\_dt | email | dia\_chi |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Nguyễn Văn B | 0123456789 | Căn cước | 123123123 | nguyenvana@gmail.com | Hà Đông |

* tblTour
    

| id | ten | noi\_xuat\_phat | noi\_den | mo\_ta |
| --- | --- | --- | --- | --- |
| 1 | Tour Mộc Châu | Thanh Xuân, Hà Nội | Mộc Châu |  |

* tblLichTrinhTour
    

| id | ngay\_xuat\_phat | ngay\_ket\_thuc | so\_ve\_toi\_da | gia\_ve | mo\_ta | tbTtour\_id |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 4/5/2025 | 6/5/2025 | 50 | 1,000,000 |  |  |

* tblHoaDonMua
    

| id | ngay\_thanh\_toan | giam\_gia | kieu\_thanh\_toan | ghi\_chu | user\_id | khach\_hang\_id |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 26/4/2025 | 0 | Chuyển khoản |  | 1 | 1 |

* tblVe
    

| id | so\_khach | giam\_gia | ghi\_chu | lich\_trinh\_tour\_id | hoa\_don\_mua\_id |
| --- | --- | --- | --- | --- | --- |
| 1 | 5 | 0 |  | 1 | 1 |

* tblHoaDonPhat
    

| id | hoa\_don\_mua\_id | user\_id | ngay\_thanh\_toan | kieu\_thanh\_toan |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

* Kịch bản và kết quả mong đợi
    
    * 1. Nhân viên đăng nhập vào hệ thống với username=a, password=123456 và nhấn vào nút đăng nhập
            
    * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749428232809/65666251-b77d-470b-881c-a3f190bdfc12.png align="center")
        
        2\. Nhân viên nhấn vào nút “Trả vé theo yêu cầu của khách”
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749428307551/c35d199f-50e6-4448-93fd-f0bc09ffdf76.png align="center")
        
    * 3. Nhân viên nhập mã vé là 1 và nhấn vào nút tìm kiếm
            
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749428384222/0152c62d-1640-49ab-8b8f-c96d6aabb6f1.png align="center")
    
    * 4. Nhân viên nhấn vào nút hủy vé
            
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749428529259/5b4b80e0-97af-4b27-8b7d-a933f4d5f42c.png align="center")
        
        5. Nhân viên nhấn OK
            
        
        Hệ thống hiển thị thông báo trả vé thành công
        
    

* CSDL sau khi test
    
    * tblHoaDonPhat
        

| id | hoa\_don\_mua\_id | user\_id | ngay\_thanh\_toan | kieu\_thanh\_toan |
| --- | --- | --- | --- | --- |
| 1 | 1 | 1 | 4/5/2025 | Chuyển khoản |