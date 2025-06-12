---
title: "Đề 40 Ngân hàng NMCNPM"
datePublished: Thu Jun 12 2025 10:39:00 GMT+0000 (Coordinated Universal Time)
cuid: cmbt8xm3r000r02l46kecfswm
slug: de-40-ngan-hang-nmcnpm
tags: software-engineering

---

### Viết một scenario chuẩn cho use case này

* kịch bản: “Xem BXH các đội đua”
    
* actor(s): nhân viên
    
* pre condition: Nhân viên có tài khoản đúng kiểu của nhân viên
    
* post condition: BTC xem bxh các đội đua thành công
    
* Main events:
    

1. Nhân viên A đăng nhập vào hệ thống với username = a, password=123456 và nhấn vào nút đăng nhập
    
2. hệ thống hiển thị giao diện trang chủ dành cho nhân viên có chức năng “Xem BXH các đội đua”
    
3. hệ thống hiển thị giao diện danh sách các đội đua theo dạng bảng
    

| STT | Tên đội đua | Hãng | Tổng điểm các tay đua đội sau các chặng | tổng thời gian sau các chặng |
| --- | --- | --- | --- | --- |
| 1 | Đội đua 1 | Mercedes | 86 | 10 giờ 20 phút |
| 2 | Đội đua 2 | Ferrari | 54 | 12 giờ 45 phút |

4. nhân viên nhấn vào dòng số 1
    
5. hệ thống hiển thị giao diện kết quả chi tiết cho từng chặng đua của đội đua 1:
    

| STT | Tên chặng | Tổng số điểm | Tổng thời gian của 2 tay đua trong đội |
| --- | --- | --- | --- |
| 1 | Chặng 1 | 43 | 5 giờ |
| 2 | Chặng 2 | 43 | 5 giờ 20 phút |

### Trích và vẽ biểu đồ các lớp thực thể của toàn bộ hệ thống

* chặng đua → lớp thực thể
    
* Mã chặng, tên, số vòng đua, địa điểm, thời gian, mô tả → thuộc tính lớp chặng đua
    
* đội đua → lớp thực thể
    
* (Mã, tên, hãng, mô tả). → thuộc tính lớp đội đua
    
* tay đua → lớp thực thể
    
* (mã, tên, ngày sinh, quốc tịch, tiểu sử). → thuộc tính lớp tay đua
    
* kết quả → lớp thực thể KetQuaChang
    
* thứ tự về đích, thời gian về đích, điểm số → thuộc tính lớp KetQuaChang
    
* bảng xếp hạng đội đua → là số nhiều của lớp thống kê kết quả đội đua - DoiDuaStat
    

Biểu đồ lớp thực thể của toàn bộ hệ thống

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749719895364/8c3b8581-e91c-439d-9981-c834596ad18e.jpeg align="center")

### Thiết kế tĩnh: thiết kế giao diện và vẽ biểu đồ lớp MVC chi tiết cho modul

* thiết kế giao diện
    
    * giao diện đăng nhập
        
    * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749720079321/80103d66-c47c-4a6b-9f13-a415505b120f.png align="center")
        
        giao diện trang chủ cho nhân viên
        
    * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749720141751/25dd000a-d527-413d-a230-e418abb10e94.png align="center")
        
        giao diện xem bảng xếp hạng các đội đua
        
    * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749720358289/86a5b21f-842e-4c15-bed1-7d7f8767a7e5.png align="center")
        
        giao diện chi tiết cho từng chặng đua
        
    * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749720577714/37a61172-704d-48a6-9dfc-d55ca7b77e7f.png align="center")
        
* thiết kế biểu đồ lớp MVC chi tiết cho module
    

### Thiết kế động: vẽ biểu đồ tuần tự mô tả tuần tự hoạt động của modul

### Viết một test case chuẩn cho modul này