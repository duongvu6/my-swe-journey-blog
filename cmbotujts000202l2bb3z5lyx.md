---
title: "Analysis workflow"
datePublished: Mon Jun 09 2025 08:25:38 GMT+0000 (Coordinated Universal Time)
cuid: cmbotujts000202l2bb3z5lyx
slug: analysis-workflow
tags: software-engineering

---

5. ### **Kịch bản chuẩn và ngoại lệ**
    

| Scenario | Nhập truyện từ nhà cung cấp |
| --- | --- |
| Actor(s) | Nhân viên kho, nhà cung cấp |
| Pre-condition | Nhân viên kho có tài khoản đúng kiểu của nhân viên kho |
| Post-condition | Nhập truyện từ nhà cung cấp thành công |

* main events:
    
    * 1\. Nhân viên kho A đăng nhập vào hệ thống với username = a, password = 123456 để nhập truyện từ nhà cung cấp B
        
        2\. Hệ thống hiện giao diện chính của nhân viên kho có lựa chọn nhập truyện từ nhà cung cấp
        
        3\. Nhân viên kho chọn chức năng nhập truyện từ nhà cung cấp
        
        4\. Hệ thống hiện giao diện tìm kiếm nhà cung cấp:
        
        \- Ô nhập: tên nhà cung cấp
        
        \- Nút tìm kiếm
        
        \- Nút thêm mới nhà cung cấp
        
        5\. Nhân viên kho hỏi nhà cung cấp các thông tin của nhà cung cấp: tên, địa chỉ, email, điện thoại
        
        6\. Nhà cung cấp trả lời các thông tin của nhà cung cấp:
        
        \-tên: B
        
        \-địa chỉ: Hà Đông, Hà Nội
        
        \-email: [nccb@gmail.com](mailto:nccb@gmail.com)
        
        \-điện thoại: 0123456789
        
        7\. Nhân viên kho nhập: tên nhà cung cấp: B và click vào nút tìm kiếm
        
        8\. Hệ thống hiện kết quả tìm kiếm nhà cung cấp
        
        \- Ô nhập tên nhà cung cấp: B
        
        \- Nút tìm kiếm
        
        \- Nút thêm mới nhà cung cấp
        
        \- Kết quả tìm kiếm:
        
    * | STT | Mã | Tên | Địa chỉ | Email | Điện thoại | Mô tả |
        | --- | --- | --- | --- | --- | --- | --- |
        | 1 | 1 | B | Hà Đông, Hà Nội | [nccb@gmail.com](mailto:nccb@gmail.com) | 0123456789 | Chuyên cung cấp truyện thiếu nhi |
        | 2 | 2 | B | Sài Gòn | [sgb@gmail.com](mailto:sgb@gmail.com) | 9876543210 | Chuyên cung cấp truyện ngôn tình |
        | 3 | 3 | Bình An | Đà Nẵng | [binhan@gmail.com](mailto:binhan@gmail.com) | 1231231231 | Chuyên cung cấp truyện trinh thám |
        
        9\. Nhân viên kho chọn dòng số 1
        
        10\. Hệ thống hiện giao diện tìm đầu truyện:
        
        \- Ô nhập: tên đầu truyện
        
        \- Nút tìm kiếm
        
        \- Nút thêm mới đầu truyện
        
        11\. Nhân viên kho hỏi nhà cung cấp thông tin về đầu truyện cần nhập: tên, tác giả, nhà xuất bản, năm xuất bản, đơn giá
        
        12\. Nhà cung cấp trả lời nhân viên kho thông tin đầu truyện cần nhập:
        
        \-tên:7 viên ngọc rồng tập 6
        
        \-tác giả: Akira Toriyama
        
        \-nhà xuất bản: Kim Đồng
        
        \-năm xuất bản: 2023
        
        \-đơn giá: 30000
        
        13\. Nhân viên kho nhập vào ô nhập tên đầu truyện: 7 viên ngọc rồng tập 6 rồi nhấn nút tìm kiếm
        
        14\. Hệ thống hiện giao diện kết quả tìm kiếm đầu truyện:
        
        \- Ô nhập: tên đầu truyện: 7 viên ngọc rồng tập 6
        
        \- Nút tìm kiếm
        
        \- Nút thêm mới đầu truyện
        
        \- Kết quả tìm kiếm:
        
    * | STT | Mã | Tên | Tác giả | Nhà xuất bản | Năm xuất bản | Đơn giá |
        | --- | --- | --- | --- | --- | --- | --- |
        | 1 | 1 | 7 viên ngọc rồng tập 61 | Akira Toriyama | Kim Đồng | 2023 | 30,000 |
        | 2 | 2 | 7 viên ngọc | Akira Toriyama | Kim Đồng | 2023 | 30,000 |
        | 3 | 3 | 7 viên ngọc rồng tập 6 | Akira Toriyama | Kim Đồng | 2023 | 30,000 |
        
        15\. Nhân viên kho chọn dòng số 3
        
        16\. Hệ thống hiện giao diện nhập số lượng truyện:
        
        \- Thông tin đầu truyện:
        
        +Mã: 3
        
        +tên: 7 viên ngọc rồng tập 6
        
        +tác giả: Akira Toriyama
        
        +nhà xuất bản: Kim Đồng
        
        +năm xuất bản: 2023
        
        +đơn giá: 30000
        
        \- Ô nhập số lượng truyện
        
        \- Nút xác nhận, huỷ
        
        17\. Nhân viên kho hỏi nhà cung cấp số lượng truyện của đầu truyện
        
        18\. Nhà cung cấp trả lời nhân viên kho số lượng truyện của đầu truyện: 7 viên ngọc rồng tập 6 là 15
        
        19\. Nhân viên kho nhập vào ô số lượng truyện=15 và nhấn vào nút xác nhận
        
        20\. Hệ thống hiển thị giao diện danh sách các truyện nhập:
        
        \- Nút xác nhận, huỷ
        
        \- Nút thêm truyện khác(nhân viên kho có thể tiếp tục nhập các đầu truyện khác)
        
        \- Danh sách các đầu truyện nhập:
        
    * | STT | Mã | Tên | Đơn giá | Số lượng | Thành tiền |
        | --- | --- | --- | --- | --- | --- |
        | 1 | 3 | 7 viên ngọc rồng tập 6 | 30,000 | 15 | 450,000 |
        
        21\. Nhân viên kho đọc lại thông tin các truyện được nhập và yêu cầu nhà cung cấp đối chiếu
        
        22\. Nhà cung cấp xác nhận đúng thông tin
        
        23\. Nhân viên kho nhấn vào nút xác nhận
        
        24\. Hệ thống hiển thị giao diện xác nhận nhập truyện:
        
        \- Nút in, huỷ
        
        \- Tên nhân viên kho nhập truyện: A
        
        \- Ngày nhập truyện: 11/4/2025
        
        \- Thông tin nhà cung cấp:
        
    * | Mã | Tên | Địa chỉ | Email | Điện thoại | Mô tả |
        | --- | --- | --- | --- | --- | --- |
        | 1 | B | Hà Đông, Hà Nội | [nccb@gmail.com](mailto:nccb@gmail.com) | 0123456789 | Chuyên cung cấp truyện thiếu nhi |
        
        \- Danh sách các truyện được nhập:
        
        | STT | Mã | Tên | Đơn giá | Số lượng | Thành tiền |
        | --- | --- | --- | --- | --- | --- |
        | 1 | 3 | 7 viên ngọc rồng tập 6 | 30,000 | 15 | 450,000 |
        | Giảm giá | 0 |  |  |  |  |
        | Tổng tiền | 450,000 |  |  |  |  |
        | Phương thức thanh toán | Chuyển khoản |  |  |  |  |
        | Ghi chú |  |  |  |  |  |
        
    
    25\. Nhân viên kho hỏi nhà cung cấp số tiền giảm giá trong lần nhập này
    
    26\. Nhà cung cấp trả lời nhân viên kho số tiền giảm giá trong lần nhập này là 0 đồng
    
    27\. Nhân viên kho nhập 0 vào ô giảm giá, chọn phương thức thanh toán là chuyển khoản và nhấn vào nút in
    
    28\. Hệ thống báo nhập truyện thành công và in ra hoá đơn nhập truyện. Hoá đơn nhập truyện gồm các thông tin:
    
    \- Tên nhân viên kho nhập truyện: A
    
    \- Ngày nhập truyện: 11/4/2025
    
    \- Thông tin nhà cung cấp:
    
* | Mã | Tên | Địa chỉ | Email | Điện thoại | Mô tả |
    | --- | --- | --- | --- | --- | --- |
    | 1 | B | Hà Đông, Hà Nội | [nccb@gmail.com](mailto:nccb@gmail.com) | 0123456789 | Chuyên cung cấp truyện thiếu nhi |
    

\- Danh sách các đầu truyện được nhập:

| STT | Mã | Tên | Đơn giá | Số lượng | Thành tiền |
| --- | --- | --- | --- | --- | --- |
| 1 | 3 | 7 viên ngọc rồng tập 6 | 30,000 | 15 | 450,000 |
| Giảm giá | 0 |  |  |  |  |
| Tổng tiền | 450,000 |  |  |  |  |
| Phương thức thanh toán | Chuyển khoản |  |  |  |  |
| Ghi chú |  |  |  |  |  |

29\. Nhân viên kho nhận hoá đơn nhập truyện và đưa cho nhà cung cấp ký xác nhận

30\. Nhà cung cấp ký xác nhận nhập truyện thành công

31\. Nhân viên kho báo nhập truyện từ nhà cung cấp thành công cho nhà cung cấp

* exceptions:
    
    * 2\. Hệ thống báo sai username/password
        
        2.1 Nhân viên kho click nút OK của thông báo
        
        2.2 Hệ thống hiển thị lại giao diện đăng nhập với username=a, password=123456
        
        2.3 Nhân viên kho sửa lại password=1234567 và nhấn vào nút đăng nhập
        
        2.4 Hệ thống hiển thị giao diện chính của nhân viên kho có lựa chọn nhập truyện từ nhà cung cấp
        
        8\. Hệ thống hiện kết quả tìm kiếm nhà cung cấp
        
        \- Tên nhà cung cấp: B
        
        \- Nút tìm kiếm
        
        \- Nút thêm mới nhà cung cấp
        
        \- Kết quả tìm kiếm:
        
        | STT | Mã | Tên | Địa chỉ | Email | Điện thoại | Mô tả |
        | --- | --- | --- | --- | --- | --- | --- |
        | 1 | 2 | B | Sài Gòn | [sgb@gmail.com](mailto:sgb@gmail.com) | 9876543210 | Chuyên cung cấp truyện ngôn tình |
        | 2 | 3 | Bình An | Đà Nẵng | [binhan@gmail.com](mailto:binhan@gmail.com) | 1231231231 | Chuyên cung cấp truyện trinh thám |
        
* 8.1 Nhân viên kho nhấn vào nút thêm mới nhà cung cấp
    
    8.2 Hệ thống hiển thị giao diện thêm mới nhà cung cấp:
    
    \- Ô nhập: tên, địa chỉ, email, điện thoại, mô tả
    
    \- Nút thêm, huỷ
    
    8.3 Nhân viên kho hỏi thêm thông tin mô tả của nhà cung cấp do trước đó nhà cung cấp đã trả lời thông tin về tên, địa chỉ, email, điện thoại
    
    8.4 Nhà cung cấp trả lời nhân viên kho về mô tả: chuyên cung cấp truyện thiếu nhi
    
    8.5 Nhân viên kho nhập thông tin nhà cung cấp như đã được trả lời trước đó vào các ô nhập tương ứng:
    
    \- Tên: B
    
    \- Địa chỉ: Hà Đông, Hà Nội
    
    \- Điện thoại: 0123456789
    
    \- Mô tả: chuyên cung cấp truyện thiếu nhi
    
    và nhấn nút thêm
    
    8.6 Hệ thống hiện thông báo thêm thành công
    
    8.7 Nhân viên kho nhấn nút OK của thông báo
    
    8.8 Hệ thống hiện giao diện tìm đầu truyện theo tên
    
    \- Ô nhập: tên đầu truyện
    
    \- Nút tìm kiếm
    
    \- Nút thêm mới đầu truyện
    
    14\. Hệ thống hiện giao diện kết quả tìm kiếm đầu truyện:
    
    \- Ô nhập: tên đầu truyện: 7 viên ngọc rồng tập 6
    
    \- Nút tìm kiếm
    
    \- Nút thêm mới đầu truyện
    
    \- Kết quả tìm kiếm:
    

| STT | Mã | Tên | Tác giả | Nhà xuất bản | Năm xuất bản | Đơn giá |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 1 | 7 viên ngọc rồng tập 60 | Akira Toriyama | Kim Đồng | 2023 | 30,000 |
| 2 | 2 | 7 viên ngọc | Akira Toriyama | Kim Đồng | 2023 | 30,000 |

14.1 Nhân viên kho nhấn nút thêm mới đầu truyện

14.2 Hệ thống hiển thị giao diện thêm mới đầu truyện:

\- Ô nhập: tên, tác giả, nhà xuất bản, năm xuất bản, đơn giá

\- Nút: thêm, huỷ

14.3 Nhân viên kho dựa vào thông tin nhà cung cấp vừa trả lời để nhập thông tin đầu truyện và các ô tương ứng:

\- Tên: 7 viên ngọc rồng tập 6

\- Tác giả: Akira Toriyama

\- Nhà xuất bản: Kim Đồng

\- Năm xuất bản: 2023

\- Đơn giá: 30000

và nhấn vào nút thêm

14.4 Hệ thống hiển thị thông báo thêm đầu truyện thành công

14.5 Nhân viên kho nhấn vào nút OK của thông báo

14.6 Hệ thống hiện giao diện nhập số lượng truyện:

\- Thông tin đầu truyện:

+Mã: 3

+tên: 7 viên ngọc rồng tập 6

+tác giả: Akira Toriyama

+nhà xuất bản: Kim Đồng

+năm xuất bản: 2023

+đơn giá: 30000

\- Ô nhập số lượng truyện

\- Nút xác nhận, huỷ

22\. Nhà cung cấp báo sai thông tin, số lượng truyện là 20 chứ không phải 15

22.1 Nhân viên kho nhấn vào đầu truyện ở dòng số 1 để sửa thông tin số lượng truyện

22.2 Hệ thống hiện giao diện nhập số lượng truyện:

\- Thông tin đầu truyện:

+Mã: 3

+tên: 7 viên ngọc rồng tập 6

+tác giả: Akira Toriyama

+nhà xuất bản: Kim Đồng

+năm xuất bản: 2023

+đơn giá: 30000

\- Ô nhập số lượng truyện=15

\- Nút xác nhận, huỷ

22.3 Nhân viên kho thay đổi giá trị nhập trong ô nhập số lượng truyện = 20 và nhấn vào nút xác nhận

22.4 Hệ thống hiển thị giao diện danh sách các truyện nhập:

\- Nút xác nhận, huỷ

\- Nút nhập truyện khác(nhân viên kho có thể tiếp tục nhập các đầu truyện khác)

\- Danh sách các đầu truyện nhập:

| STT | Mã | Tên | Đơn giá | Số lượng | Thành tiền |
| --- | --- | --- | --- | --- | --- |
| 1 | 3 | 7 viên ngọc rồng tập 6 | 30,000 | 20 | 600,000 |

6. ### **Diễn giải và vẽ biểu đồ lớp thực thể của module “Quản lý nhập truyện từ nhà cung cấp”**
    

* **Bước 1+2+3**: Mô tả module trong 1 đoạn văn ngắn(có thể thay thế bằng cách duyệt tất cả kịch bản của module tương ứng). Trích tất cả các danh từ xuất hiện và đánh giá các danh từ (3 loại: bị loại – quá chung chung, trừu tượng, ngoài phạm vi module; làm thuộc tính – chỉ thuộc tính của vật như thời gian, tiền bạc,…; làm lớp thực thể-phần còn lại)
    

Các danh từ:

* Nhân viên kho: lớp thực thể số 1: User
    
* Hệ thống: loại vì quá chung chung
    
* Username: thuộc tính của lớp User
    
* Password: thuộc tính của lớp User
    
* Đầu truyện: là đối tượng xử lý của hệ thống nên là lớp thực thể số 2: BookTitle
    
* Nhà cung cấp: là đối tượng xử lý của hệ thống nên là lớp thực thể số 3: Provider
    
* Giao diện: loại vì quá chung chung
    
* Chức năng: loại vì quá chung chung
    
* Ô nhập: loại vì quá chung chung
    
* Nút: loại vì quá chung chung
    
* Thông tin: loại vì quá chung chung
    
* Mã (nhà cung cấp): thuộc tính của lớp Provider
    
* Tên (nhà cung cấp): thuộc tính của lớp Provider
    
* Địa chỉ (nhà cung cấp): thuộc tính của lớp Provider
    
* Email (của nhà cung cấp): thuộc tính của lớp Provider
    
* Điện thoại (của nhà cung cấp): thuộc tính của lớp Provider
    
* Mô tả nhà cung cấp: thuộc tính của lớp Provider
    
* Kết quả: loại vì quá chung chung
    
* Truyện thiếu nhi: loại vì ngoài phạm vi hệ thống/module
    
* Mã đầu truyện: thuộc tính của lớp BookTitle
    
* Tên đầu truyện: thuộc tính của lớp BookTitle
    
* Tác giả: thuộc tính của lớp BookTitle
    
* Nhà xuất bản: thuộc tính của lớp BookTitle
    
* Năm xuất bản: thuộc tính của lớp BookTitle
    
* Đơn giá: thuộc tính của lớp BookTitle
    
* Danh sách các truyện nhập: đề xuất tạo một lớp thực thể cho truyện nhập – lớp thực thể số 4: ImportedBookTitle
    
* Số lượng: thuộc tính của lớp ImportedBookTitle
    
* Thành tiền: thuộc tính của lớp ImportedBookTitle
    
* Hoá đơn nhập truyện: đề xuất tạo lớp thực thể số 5: ImportBill
    
* Tổng tiền: thuộc tính của lớp ImportBill
    
* Phương thức thanh toán: thuộc tính của lớp ImportBill
    
* Số tiền giảm giá: thuộc tính của lớp ImportBill
    
* Ngày nhập truyện: thuộc tính của lớp ImportBill
    
* Bước: loại vì ngoài phạm vi hệ thống/module
    
* **Bước 4: Xét quan hệ số lượng giữa các lớp**
    
* BookTitle và ImportedBookTitle: 1-n do 1 đầu truyện có thể được nhập nhiều lần nhưng với mỗi đầu truyện được nhập chỉ ứng với duy nhất 1 đầu truyện
    
* Provider và ImportBill: 1-n do một nhà cung cấp có thể có nhiều hoá đơn nhập truyện nhưng 1 hoá đơn nhập truyện cụ thể chỉ thuộc về 1 nhà cung cấp duy nhất
    
* ImportBill và ImportedBookTitle: 1-n do một hoá đơn nhập truyện sẽ có thể có nhiều đầu truyện được nhập và mỗi một đầu truyện được nhập chỉ thuộc về duy nhất 1 hoá đơn nhập truyện
    
* User và ImportBill: 1-n do một nhân viên kho có thể tạo nhiều hoá đơn nhập trong nhiều lần nhập nhưng mỗi hoá đơn nhập chỉ được tạo bởi duy nhất 1 nhân viên kho cụ thể.
    
* Provider và BookTitle: có thể nhập nhiều đầu truyện từ một nhà cung cấp trong một lần nhập và một đầu truyện có thể xuất hiện trong nhiều lần nhập khác nhau nên quan hệ giữa Provider và BookTitle là n-n
    

Thực hiện việc tách quan hệ n-n của Provider và BookTitle:

* Ta thấy xung quanh Provider có Provider và ImportBill thoả mãn quan hệ 1-n. Do đó ta xét quan hệ giữa BookTitle và ImportBill, đây là quan hệ n-n khi một hoá đơn nhập truyện có thể gồm nhiều đầu truyện và một đầu truyện cụ thể có thể nằm trong nhiều hoá đơn nhập truyện.
    
* Lặp lại đệ quy: ta thấy xung quanh lớp ImportBill có lớp ImportedBookTitle thoả mãn quan hệ giữa ImportBill và ImportedBookTitle là 1-n. Do đó ta xét quan hệ giữa BookTitle và ImportedBookTitle, đây là quan hệ 1-n và ta dừng việc đệ quy, hoàn thành việc tách quan hệ n-n của Provider và BookTitle.
    
* **Bước 5: Bổ sung quan hệ đối tượng giữa các lớp**
    
* User và ImportBill: quan hệ 1-n nên ưu tiên quan hệ thành phần, ta thấy trong hoá đơn nhập truyện có thông tin của 1 nhân viên kho lập hoá đơn, và nhân viên kho lẫn hoá đơn nhập truyện có thể tồn tại độc lập với nhau. Do vậy, ta bổ sung quan hệ aggregation cho quan hệ này
    
* Provider và ImportBill: quan hệ 1-n nên ưu tiên quan hệ thành phần, ta thấy thông tin nhà cung cấp là một thành phần trong hoá đơn nhập truyện và nhà cung cấp độc lập với hoá đơn nhập truyện nên ta bổ sung quan hệ aggregation cho quan hệ này
    
* ImportBill và BookTitle: quan hệ n-n nên ưu tiên quan hệ liên kết(association class), ta xét 2 điều kiện cần thoả mãn:
    
* Quan hệ giữa ImportBill và ImportedBookTitle là 1-n. Quan hệ giữa BookTitle và ImportedBookTitle là 1-n
    
* 1 ImportBill và 1 BookTitle có tồn tại duy nhất 1 class ImportedBookTitle không? Ta thấy với một đầu truyện đã được nhập thì sẽ chỉ có duy nhất, không thể có 2 lần nhập được. Do đó thoả mãn điều kiện này.
    

Từ đó ta có thể chuyển quan hệ thành liên kết

![](data:image/png;base64,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 align="left")

7. ### **Diễn giải và vẽ biểu đồ lớp bao gồm lớp giao diện cho module “Quản lý nhập truyện từ nhà cung cấp”**
    

* * **Bước 1: Mỗi giao diện chính đề xuất thành 1 lớp biên**
        
        Các giao diện chính:
        
        * Giao diện đăng nhập
            
        * Ô nhập username → inUsername
            
        * Ô nhập password → inPassword
            
        * Nút đăng nhập → subLogin
            
        * Giao diện chính của nhân viên kho:
            
        * Nút chọn chức năng nhập truyện từ nhà cung cấp à subImport
            
        * Giao diện tìm kiếm nhà cung cấp + hiển thị kết quả
            
        * Ô nhập tên nhà cung cấp → inName
            
        * Nút thêm mới nhà cung cấp → subAddProvider
            
        * Nút tìm kiếm → subSearchProvider
            
        * Một bảng hiển thị kết quả có thể nhấn vào một dòng trong bảng để chọn 1 nhà cung cấp→ outSubListProvider
            
        * Giao diện tìm kiếm đầu truyện + hiển thị kết quả
            
        * Ô nhập tên đầu truyện → inName
            
        * Nút tìm kiếm đầu truyện → subSearchBookTitle
            
        * Nút thêm mới đầu truyện → subAddBookTitle
            
        * Một bảng hiển thị kết quả có thể nhấn vào một dòng trong bảng để chọn 1 đầu truyện → outSubListBookTitle
            
        * Giao diện thêm nhà cung cấp mới
            
        * Ô nhập tên nhà cung cấp → inName
            
        * Ô nhập địa chỉ nhà cung cấp → inAddress
            
        * Ô nhập email nhà cung cấp → inEmail
            
        * Ô nhập điện thoại nhà cung cấp → inPhoneNumber
            
        * Ô nhập mô tả nhà cung cấp → inNote
            
        * Nút thêm nhà cung cấp → subAdd
            
        * Nút huỷ → subCancel
            
        * Giao diện thêm đầu truyện mới
            
        * Ô nhập tên đầu truyện → inName
            
        * Ô nhập tác giả → inAuthor
            
        * Ô nhập nhà xuất bản → inPublisher
            
        * Ô nhập năm xuất bản → inPublicationYear
            
        * Ô nhập đơn giá→ inUnitPrice
            
        * Nút thêm đầu truyện→ subAdd
            
        * Nút huỷ → subCancel
            
        * Giao diện nhập số lượng truyện
            
        * Ô hiển thị tên đầu truyện → outName
            
        * Ô hiển thị mã đầu truyện → outId
            
        * Ô hiển thị tác giả→ outAuthor
            
        * Ô hiển thị nhà xuất bản → outPublisher
            
        * Ô hiển thị năm xuất bản → outPublicationYear
            
        * Ô hiển thị đơn giá→ outUnitPrice
            
        * Nút xác nhận → subConfirm
            
        * Nút huỷ → subCancel
            
        * Ô nhập số lượng truyện → inQuantity
            
        * Giao diện danh sách các truyện nhập
            
        * Nút nhập thêm đầu truyện → subImportBookTitle
            
        * Nút xác nhận → subConfirm
            
        * Nút huỷ→ subCancel
            
        * Một bảng gồm danh sách các đầu truyện nhập và có thể nhấn vào từng dòng để sửa thông tin nếu sai→outSubListImportedBookTitle
            
        * Giao diện xác nhận nhập truyện
            
        * Nút in → subPrint
            
        * Nút huỷ →subCancel
            
        * Một bảng (1 dòng) gồm các thông tin của nhà cung cấp →outProvider
            
        * Một bảng gồm danh sách các đầu truyện nhập → outListImportedBookTitle
            
        * Ô hiển thị tổng tiền → outTotalAmount
            
        * Ô hiển thị tên của nhân viên kho lập hoá đơn → outWarehouseStaffName
            
        * Ô hiển thị ngày lập hoá đơn nhập truyện → outImportDate
            
        * Ô hiển thị phương thức thanh toán dưới dạng combobox , gồm các giá trị có thể lựa chọn: tiền mặt, chuyển khoản, thẻ tín dụng → outInPaymentMethod
            
        * Ô nhập số tiền giảm giá →inSaleOff
            
        * Ô để nhập ghi chú → inNote
            
        * **Bước 2: Mỗi hoạt động vào/ra dữ liệu với hệ thống thì đề xuất 1 hàm xử lý**
            
        * Kiểm tra đăng nhập:
            
        * Tên: checkLogin()
            
        * Input: username, password (User)
            
        * Output: boolean
            
        * Lớp chủ thể: User
            
        * Tìm kiếm nhà cung cấp
            
        * Tên: searchProviderByName()
            
        * Input: name(Provider)
            
        * Output: List&lt;Provider&gt;
            
        * Lớp chủ thể: Provider
            
        * Tìm kiếm đầu truyện:
            
        * Tên: searchBookTitleByName()
            
        * Input: name(BookTitle)
            
        * Output: List&lt;BookTitle&gt;
            
        * Lớp chủ thể: BookTitle
            
        * Xác nhận nhập truyện
            
        * Tên: confirmImportBookTitle()
            
        * Input: ImportBill
            
        * Output: boolean
            
        * Lớp chủ thể: ImportBill
            
        * Thêm mới nhà cung cấp:
            
        * Tên: addNewProvider()
            
        * Input: name, address, email, phoneNumber, note(Provider)
            
        * Output: boolean
            
        * Lớp chủ thể: Provider
            
        * Thêm mới đầu truyện
            
        * Tên: addNewBookTitle()
            
        * Input: name, author, publisher, publicationYear, unitPrice(BookTitle)
            
        * Output: boolean
            
        * Lớp chủ thể: BookTitle
            
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749457121707/57ab3693-5199-4e7e-ae70-edd9a4154f10.jpeg align="center")
        
        8. ### **Kịch bản chuẩn v2**
            
        9. 1. Nhà cung cấp nhập một số lượng truyện(cũ hoặc mới) cho cửa hàng
                
            2. Nhân viên kho bắt đầu quá trình nhập truyện từ nhà cung cấp bằng việc đăng nhập trên giao diện LoginView
                
            3. Lớp LoginView gọi lớp User để xử lý
                
            4. Lớp User thực hiện hàm checkLogin()
                
            5. Lớp User trả kết quả về cho lớp LoginView
                
            6. Lớp LoginView gọi lớp WarehouseStaffView
                
            7. Lớp WarehouseStaffView hiển thị cho nhân viên kho
                
            8. Nhân viên kho chọn chức năng nhập truyện từ lớp WarehouseStaffView
                
            9. Lớp WarehouseStaffView gọi lớp SearchProviderView
                
            10. Lớp SearchProviderView hiển thị cho nhân viên kho
                
            11. Nhân viên kho hỏi nhà cung cấp thông tin của nhà cung cấp
                
            12. Nhà cung cấp cung cấp thông tin cho nhân viên kho
                
            13. Nhân viên kho nhập tên nhà cung cấp và nhấn nút tìm kiếm trên giao diện SearchProviderView
                
            14. Lớp SearchProviderView gọi lớp Provider
                
            15. Lớp Provider thực hiện hàm searchProviderByName()
                
            16. Lớp Provider trả kết quả về cho lớp SearchProviderView
                
            17. Lớp SearchProviderView hiển thị kết quả cho nhân viên kho
                
            18. Nhân viên kho chọn đúng dòng của thông tin nhà cung cấp
                
            19. Lớp SearchProviderView gọi lớp SearchBookTitleView
                
            20. Lớp SearchBookTitleView hiển thị cho nhân viên kho
                
            21. Nhân viên kho hỏi nhà cung cấp thông tin về đầu truyện cần nhập
                
            22. Nhà cung cấp trả lời nhân viên kho về thông tin đầu truyện cần nhập
                
            23. Nhân viên kho nhập tên đầu truyện và nhấn nút tìm kiếm
                
            24. Lớp SearchBookTitleView gọi lớp BookTitle
                
            25. Lớp BookTitle thực hiện hàm searchBookTitleByName()
                
            26. Lớp BookTitle trả kết quả về cho lớp SearchBookTitleView
                
            27. Lớp SearchBookTitleView hiển thị kết quả cho nhân viên kho
                
            28. Nhân viên kho chọn dòng có thông tin đầu truyện đúng
                
            29. Lớp SearchBookTitleView gọi lớp EnterQuantityView
                
            30. Lớp EnterQuantityView hiển thị cho nhân viên kho
                
            31. Nhân viên kho hỏi nhà cung cấp số lượng truyện của đầu truyện
                
            32. Nhà cung cấp trả lời nhân viên kho số lượng truyện của đầu truyện
                
            33. Nhân viên kho nhập số lượng truyện và nhấn vào nút xác nhận
                
            34. Lớp EnterQuantityView gọi lớp ImportedBookTitleListView
                
            35. Lớp ImportedBookTitleListView hiển thị cho nhân viên kho
                
            36. Nhân viên kho đọc lại thông tin các đầu truyện được nhập và yêu cầu nhà cung cấp đối chiếu xác nhận
                
            37. Nhà cung cấp xác nhận đúng thông tin
                
            38. Nhân viên kho nhấn nút xác nhận
                
            39. Lớp ImportedBookTitleListView gọi lớp ConfirmView
                
            40. Lớp ConfirmView hiển thị cho nhân viên kho
                
            41. Nhân viên kho hỏi nhà cung cấp số tiền giảm giá trong lần nhập này
                
            42. Nhà cung cấp trả lời nhân viên kho số tiền giảm giá trong lần nhập này
                
            43. Nhân viên kho nhập số tiền giảm giá, chọn phương thức thanh toán và nhấn vào nút In
                
            44. Lớp ConfirmView gọi cho lớp ImportBill
                
            45. Lớp ImportBill thực hiện hàm confirmImportBookTitle()
                
            46. Lớp ImportBill trả kết quả về cho lớp ConfirmView
                
            47. Lớp ConfirmView hiển thị thông báo nhập truyện thành công cho nhân viên kho và in ra hoá đơn nhập truyện
                
            48. Nhân viên kho nhận hoá đơn nhập truyện và đưa cho nhà cung cấp ký xác nhận
                
            49. Nhà cung cấp ký xác nhận nhập truyện thành công
                
            50. Nhân viên kho báo với nhà cung cấp nhập truyện từ nhà cung cấp thành công
                
        10. 9. ### **Vẽ biểu đồ tuần tự cho kịch bản chuẩn v2**
                
            
            ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749458679662/575fdfaf-6949-467e-b0fc-44833deeb6e0.jpeg align="center")