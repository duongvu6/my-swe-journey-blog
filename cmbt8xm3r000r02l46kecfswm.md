---
title: "Đề 40 Ngân hàng NMCNPM"
datePublished: Thu Jun 12 2025 10:39:00 GMT+0000 (Coordinated Universal Time)
cuid: cmbt8xm3r000r02l46kecfswm
slug: de-40-ngan-hang-nmcnpm
tags: software-engineering

---

### Viết một scenario chuẩn cho use case này

* kịch bản: “Xem BXH các đội đua”
    
* actor(s): BTC
    
* pre condition: BTC có tài khoản đúng kiểu của BTC
    
* post condition: BTC xem bxh các đội đua thành công
    
* Main events:
    

1. BTC A đăng nhập vào hệ thống với username = a, password=123456 và nhấn vào nút đăng nhập
    
2. hệ thống hiển thị giao diện trang chủ dành cho BTC có chức năng “Xem BXH các đội đua”
    
3. hệ thống hiển thị giao diện danh sách các đội đua theo dạng bảng
    

| STT | Tên đội đua | Hãng | Tổng điểm các tay đua đội sau các chặng | tổng thời gian sau các chặng |
| --- | --- | --- | --- | --- |
| 1 | Đội đua 1 | Mercedes | 86 | 10 giờ 20 phút |
| 2 | Đội đua 2 | Ferrari | 54 | 12 giờ 45 phút |

4. BTCf nhấn vào dòng số 1
    
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

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1750121060083/ad2bdcae-32a7-4457-b084-08c793e79eba.jpeg align="center")

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
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1750123356021/ddd9f3c1-03f6-40a7-87b1-fe77ab2b68be.jpeg align="center")

### Thiết kế động: vẽ biểu đồ tuần tự mô tả tuần tự hoạt động của modul

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1750125341442/d463344a-612e-4d0f-adf6-e8618454b5b5.jpeg align="center")

### Viết một test case chuẩn cho modul này

\- csdl trước khi test

\+ tblUser

| Id | Username | Password | Role | Full\_name |
| --- | --- | --- | --- | --- |
| 1 | a | 123456 | BTC | A |

\+ tblSeason\`

| Id | Name | Start\_date | End\_date |
| --- | --- | --- | --- |
| 1 | Mùa giải 2025 | 1/1/2025 | 31/12/2026 |

\+ tblRacer

| Id | Name | Dob | Nationality | bio |
| --- | --- | --- | --- | --- |
| 1 | Nguyễn Văn B | 24/09/2000 | Việt Nam |  |
| 2 | Trần Văn C | 23/09/2001 | Việt Nam |  |
| 3 | Hoàng Văn D | 24/04/2000 | Việt Nam |  |
| 4 | Đinh Văn E | 25/6/1999 | Việt Nam |  |

+tblTeam

| Id | Name | Brand | des |
| --- | --- | --- | --- |
| 1 | Đội đua 1 | Mercedes |  |
| 2 | Đội đua 2 | Ferrari |  |

\+ tblRaceTrack

| Id | Name | location | Num\_of\_laps | time | des | Season\_id |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Chặng trung quốc | Thượng Hải | 50 | 19/06/2025 |  | 1 |
| 2 | Chặng monaco | Monaco | 60 | 19/07/2025 |  | 1 |

\+ tblTeamRacer

| Id | Start\_time | End\_time | Team\_id | Racer\_id |
| --- | --- | --- | --- | --- |
| 1 | 1/1/2025 | 31/12/2026 | 1 | 1 |
| 2 | 1/1/2025 | 31/12/2026 | 1 | 2 |
| 3 | 1/1/2025 | 31/12/2026 | 2 | 3 |
| 4 | 1/1/2025 | 31/12/2026 | 2 | 4 |

+tblRaceResult

| Id | Order | Score | Completion\_time | Completed\_laps | Race\_track\_id | Team\_racer\_id |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 1 | 25 | 2h25’ | 50 | 1 | 1 |
| 2 | 2 | 18 | 2h35’ | 50 | 1 | 2 |
| 3 | 3 | 15 | 2h40’ | 50 | 1 | 3 |
| 4 | 4 | 12 | 2h45’ | 50 | 1 | 4 |
| 5 | 1 | 25 | 2h30’ | 60 | 2 | 1 |
| 6 | 2 | 18 | 2h50’ | 60 | 2 | 2 |
| 7 | 3 | 15 | 3h | 60 | 2 | 3 |
| 8 | 4 | 12 | 4h20’ | 60 | 2 | 4 |

+tblRaceTeamTrackDetail

| Id | Team\_id | Race\_track\_id |
| --- | --- | --- |
| 1 | 1 | 1 |
| 2 | 2 | 2 |

\[if !supportLists\]-        \[endif\]Kịch bản và kết quả mong đợi

| Kịch bản | Kết quả mong đợi |
| --- | --- |
| 1.btc đăng nhập với username=a, password=123456 |  |
| 2.btc nhấn vào nút xem bxh các đội đua |  |
| 3.btc nhấn vào dòng số 1 |  |

\[if !supportLists\]-        \[endif\]Csdl sau test (không có thay đổi)