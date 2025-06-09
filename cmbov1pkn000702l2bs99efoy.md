---
title: "Design workflow"
datePublished: Mon Jun 09 2025 08:59:11 GMT+0000 (Coordinated Universal Time)
cuid: cmbov1pkn000702l2bs99efoy
slug: design-workflow
tags: software-engineering

---

10. ### **Thiết kế lớp thực thể cho module “Quản lý nhập truyện từ nhà cung cấp”** 
    

**Bước 1: Hoàn thiện lớp và thuộc tính** 

**Bước 2: Chuyển quan hệ association sang quan hệ aggregation/composition** 

Xét quan hệ của 3 lớp ImportBill – ImportedBookTitle – BookTitle: 

Ta xét quan hệ giữa lớp ImportedBookTitle và ImportBill: Trong hoá đơn nhập truyện có danh sách truyện nhập và mỗi một truyện nhập trong danh sách đó chính là thực thể lớp ImportedBookTitle. Do đó, quan hệ giữa ImportBill và ImportedBookTitle là quan hệ 1-n và ImportBill chứa ImportedBookTitle, quan hệ này là quan hệ thành phần chặt (composition) do khi truyện nhập phải nằm trong hoá đơn nhập truyện, mỗi 1 dòng của danh sách truyện nhập trong hoá đơn chính là một object của lớp truyện nhập(ImportedBookTitle) 

Từ đó ta có thể dễ dàng suy ra quan hệ giữa BookTitle và ImportedBookTitle là 1-n và là quan hệ thành phần lỏng (aggregation). 

**Bước 3: Bổ sung thuộc tính đối tượng tương ứng với các quan hệ aggregation/composition** 

* BookTitle – ImportedBookTitle(1-n) nên ta bổ sung thuộc tính đối tượng cho lớp ImportedBookTitle (bookTitle:BookTitle) 
    

* ImportBill – ImportedBookTitle(1-n) nên ta bổ sung thuộc tính đối tượng cho lớp ImportBill (importedBookTitleList: ImportedBookTitle\[\]) 
    

* ImportBill – Provider(n-1) nên ta bổ sung thuộc tính đối tượng cho lớp ImportBill (provider: Provder) 
    

* ImportBill – User(n-1) nên ta bổ sung thuộc tính đối tượng cho lớp ImportBill (user: User) 
    

**Bước 4: Thêm getter/setter cho các thuộc tính(mặc định, không cần vẽ vào trong biểu đồ cho đỡ rối)** 

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459513726/6b093901-0247-41e9-b040-4966039e7149.jpeg align="center")

11. ### **Thiết kế cơ sở dữ liệu cho module “Quản lý nhập truyện từ nhà cung cấp”** 
    

**Bước 1: Mỗi lớp thực thể tạo 1 bảng** 

**Bước 2: Các thuộc tính không đối tượng của lớp nào thì chuyển thành tên cột của bảng tương ứng** 

**Bước 3: Các quan hệ số lượng giữa các lớp chuyển thành quan hệ số lượng giữa các bảng tương ứng** 

* Xét quan hệ giữa bảng tblUser và bảng tblImportBill: 
    

* Trong biểu đồ lớp thực thể pha thiết kế: quan hệ là 1-n(User-ImportBill). Do đó khi sang bảng trong CSDL, quan hệ vẫn là 1-n. Ta xét tiếp liệu là 0..n hay 1..n 
    

* Ta thấy có thể có trường hợp 1 nhân viên kho chưa tạo hoá đơn nhập truyện nào. Do đó quan hệ là 1-n(0..n) 
    

* Xét quan hệ giữa bảng tblProvider và bảng tblImportBill: 
    

* Trong biểu đồ lớp thực thể pha thiết kế: quan hệ là 1-n(Provider-ImportBill). Do đó khi sang bảng trong CSDL, quan hệ vẫn là 1-n. Ta xét tiếp liệu là 0..n hay 1..n 
    

* Ta thấy có thể có trường hợp 1 nhà cung cấp chưa cung cấp truyện nhập nào. Do đó quan hệ là 1-n(0..n) 
    

* Xét quan hệ giữa bảng tblImportBill và bảng tblImportedBookTitle: 
    

* Trong biểu đồ lớp thực thể pha thiết kế: quan hệ là 1-n(ImportBill - ImportedBookTitle). Do đó khi sang bảng trong CSDL, quan hệ vẫn là 1-n. Ta xét tiếp liệu là 0..n hay 1..n 
    

* Ta thấy không thể có trường hợp nhập một đầu truyện mà không đưa vào trong hoá đơn nhập truyện cả. Do đó quan hệ là 1-n(1..n) 
    

* Xét quan hệ giữa bảng tblImportedBookTitle và bảng tblBookTitle: 
    

* Trong biểu đồ lớp thực thể pha thiết kế: quan hệ là 1-n(BookTitle-ImportedBookTitle). Do đó khi sang bảng trong CSDL, quan hệ vẫn là 1-n. Ta xét tiếp liệu là 0..n hay 1..n 
    

* Ta thấy với mỗi một đầu truyện thì có trường hợp ví dụ như lúc nhập một đầu truyện mới thì khi tìm kiếm không tìm thấy đầu truyện ta phải thêm đầu truyện mới. Trong trường hợp đó thì ta thấy khi đó bảng tblBookTitle có thêm 1 bản ghi mới và chưa có bản ghi tương ứng với đầu truyện này trong bảng tblImportedBookTitle. Do đó quan hệ là 1-n(0..n) 
    

**Bước 4: Khoá chính, khoá ngoại** 

Thêm khoá ngoại cho các bảng: 

* Bảng tblUser, tblProvider, tblBookTitle không có khoá ngoại 
    

* Bảng tblImportedBookTitle có 2 quan hệ 1-n trỏ vào nên ta sẽ thêm 2 khoá ngoại tương ứng: importBIllId và bookTitleId 
    

* Bảng tblImportBill có 2 quan hệ 1-n trỏ vào nên ta sẽ thêm 2 khoá ngoại tương ứng: userId và providerId 
    

**Bước 5: Loại bỏ các thuộc tính dư thừa:** 

* Trùng lặp: thuộc tính unitPrice ở bảng tblBookTitle và bảng tblImportedBookTitle trùng lặp nhưng không thể bỏ đi ở bảng tblImportedBookTitle vì sẽ có những trường hợp một đầu truyện sẽ có đơn giá nhập thay đổi theo thời gian 
    

* Dẫn xuất: 
    

* Thuộc tính totalAmount(tổng tiền) của bảng tblImportBill được tính bằng tổng thành tiền của các đầu truyện nhập trừ đi giảm giá 
    

* Thành tiền của một đầu truyện (thuộc tính amount của tblImportedBookTitle) được tính bằng đơn giá đầu truyện \* số lượng truyện nhập 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459423955/18a9422e-a318-4f21-82ce-3a717d44d062.jpeg align="center")

12. ### **Thiết kế các giao diện cho module “Quản lý nhập truyện từ nhà cung cấp”** 
    

* Giao diện đăng nhập: LoginFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459209502/395b64a8-1396-40db-bb76-6ce57dea826b.png align="center")

* Giao diện chính của nhân viên kho: WarehouseStaffHomeFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459214387/2f946d10-73c8-4b65-b67d-322e892be9d7.png align="center")

* Giao diện tìm kiếm nhà cung cấp: SearchProviderFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459220131/3be619a3-c5fe-4e97-aebb-8363d4d24a9e.png align="center")

* Giao diện thêm mới nhà cung cấp: AddProviderFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459224983/f95039e7-f2d4-4b1e-8d2d-35c0267222a3.png align="center")

* Giao diện tìm kiếm đầu truyện: SearchBookTitleFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459233703/071b1811-3d7a-4d07-b3c8-a3be9097d1ea.png align="center")

* Giao diện thêm mới đầu truyện: AddBookTitleFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459260534/77527f5c-5ec6-42e7-9dcf-7df7e71873b4.png align="center")

* Giao diện nhập số lượng truyện: EnterQuantityFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459260534/eaea3303-13de-4408-97e8-30cdeb3e3598.png align="center")

* Giao diện danh sách truyện nhập: ImportedBookTitleListFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459260549/2b01d7a7-2df4-4ed3-b022-854c6f3bdf17.png align="center")

* Giao diện xác nhận nhập truyện: ConfirmFrm 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459260530/4e653a42-3c5c-433e-9345-6dbdab81004d.png align="center")

13. ### **Thiết kế biểu đồ lớp chi tiết cho module “Quản lý nhập truyện từ nhà cung cấp”** 
    

Diễn giải, phân tích thuộc tính ẩn và các hàm của các lớp giao diện: 

* LoginFrm: 
    

* Hàm kiểm tra thông tin đăng nhập: 
    

* Tên: checkLogin() 
    

* Input: username, password(User) 
    

* Output: boolean/fullname/id/role(User) 
    

* Lớp chủ thể: UserDAO 
    

* Thuộc tính ẩn: Không có 
    

Ta xét các lựa chọn cho tham số đầu vào: 

1. checkLogin() 
    

2. checkLogin(u: string, p: string) 
    

3. checkLogin(u: User) 
    

4. checkLogin(lu: ArrayList&lt;User&gt;) 
    

Đầu tiên, dễ thấy lựa chọn số 1 bị loại ngay từ đầu do không có tham số đầu vào thì không thể kiểm tra đăng nhập được. Tiếp theo dễ thấy lựa chọn số 4 với việc cho tham số đầu vào là cả một danh sách User là việc lãng phí nên lựa chọn số 4 bị loại. Xét lựa chọn số 2 và lựa chọn số 3: lựa chọn số 2 không tuân theo nguyên tắc hướng đối tượng: 2 thuộc tính username và password của cùng một lớp thực thể User không được phép truyền cùng nhau trong hàm checkLogin. Do đó lựa chọn số 3 là hợp lý hơn cả và tuân theo nguyên tắc hướng đối tượng 

Ta xét các lựa chọn cho kết quả trả về: 

1. checkLogin(u: User): boolean 
    

2. checkLogin(u:User): int 
    

3. checkLogin(u: User): void 
    

4. checkLogin(u: User): string 
    

5. checkLogin(u: User): User 
    

6. checkLogin(u: User): ArrayList&lt;User&gt; 
    

Đầu tiên, với lựa chọn số 3 thì hoàn toàn khả thi, nhưng cần phải giải thích rõ ràng, ví dụ với tham số User là null khi thông tin đăng nhập sai và tham số User khác null khi thông tin đăng nhập đúng. Lựa chọn số 1 thì không cần phải giải thích do bản thân kiểu dữ liệu boolean đã có giá trị mặc định là True/False nên lựa chọn số 1 khả thi. Lựa chọn số 2, 4 xử lý giống nhau, đều khả thi nhưng phải giải thích rõ ràng kết quả với các trường hợp liên quan. Lựa chọn số 5,6 bị loại do lãng phí không cần thiết, không cần thiết phải đưa tham số đầu vào User và nhận kết quả trả về là User/List các User(2 hay nhiều instance của lớp User). Xét tiếp tính tối ưu các lựa chọn khả thi, dễ thấy lựa chọn 1 ít phải giải thích nhất, do đó tối ưu nhất nên ta sẽ chọn lựa chọn số 1. Vậy hàm kiểm tra thông tin đăng nhập sẽ là: checkLogin(u: User): boolean 

* WarehouseStaffHomeFrm: 
    

* Thuộc tính ẩn: u:User vì cần phải hiển thị tên nhân viên kho trên giao diện chính của nhân viên kho và cần điều hướng sang đúng giao diện chính cho nhân viên kho 
    

* SearchProviderFrm 
    

* Hàm tìm kiếm nhà cung cấp: 
    

* Tên: searchProviderByName 
    

* Input: name(Provider) 
    

* Output: ArrayList&lt;Provider&gt; 
    

* Lớp chủ thể: ProviderDAO 
    

* Thuộc tính ẩn: u:User 
    

Xét 3 lựa chọn cho tham số đầu vào: 

1. searchProviderByName(name: string) 
    

2. searchProviderByName(p: Provider) 
    

3. searchProviderByName(lp: ArrayList&lt;Provider&gt;) 
    

Dễ thấy lựa chọn số 3 không tối ưu do truyền hẳn một danh sách làm tham số nên bị loại. Còn lại lựa chọn số 1 và lựa chọn số 2. Do đây là hàm tìm kiếm và chỉ truyền vào 1 tham số đầu vào là thuộc tính name của thực thể Provider nên ta không cần thiết phải truyền vào 1 object là tham số. Do đó ta chọn lựa chọn số 1 

Tóm lại: hàm sẽ như sau: searchProviderByName(name: string): ArrayList&lt;Provider&gt; 

* AddProviderFrm 
    

* Hàm thêm mới nhà cung cấp 
    

* Tên: addNewProvider 
    

* Input: p: Provider 
    

* Output: void/boolean 
    

* Lớp chủ thể: ProviderDAO 
    

* Hàm đầy đủ: addNewProvider(p: Provider): boolean 
    

* Thuộc tính ẩn: u:User 
    

Lập luận tương tự hàm checkLogin, ta thấy input nên truyền cả object Provider làm tham số đầu vào theo nguyên tắc hướng đối tượng và trả về kiểu dữ liệu boolean để tối ưu do với kiểu trả về boolean thì sẽ có được nhiều thông tin cần thiết hơn void – True nếu thành công và False nếu ngược lại. Vậy hàm đầy đủ thông tin sẽ được viết là: addNewProvider(p: Provider): boolean 

* SearchBookTitleFrm 
    

* Hàm tìm kiếm đầu truyện 
    

* Tên: searchBookTitleByName 
    

* Input: name(BookTitle) 
    

* Output: ArrayList&lt;BookTitle&gt; 
    

* Lớp chủ thể: BookTitleDAO 
    

* Thuộc tính ẩn: importBill: ImportBill do cần truyền 2 thuộc tính ẩn là User và Provider, mà đây là 2 thuộc tính của lớp thực thể ImportBill nên theo nguyên tắc hướng đối tượng ta truyền thuộc tính ẩn là object của lớp ImportBill 
    

Lập luận tương tự hàm searchProviderByName, hàm đầy đủ thông tin sẽ được viết là: searchBookTitleByName(name: String): ArrayList&lt;BookTitle&gt; 

* AddBookTitleFrm 
    

* Hàm thêm mới đầu truyện 
    

* Tên: addNewBookTitle 
    

* Input: BookTitle 
    

* Output: void/boolean 
    

* Lớp chủ thể: BookTitleDAO 
    

* Thuộc tính ẩn: importBill: ImportBill vì phải cần truyền 2 thuộc tính ẩn User và Provider là thuộc tính của 1 lớp thực thể là ImportBill nên áp dụng nguyên tắc hướng đối tượng, cần truyền luôn object lớp ImportBill 
    

Lập luận tương tự hàm checkLogin và hàm addNewProvider, ta thấy input nên truyền cả object BookTitle làm tham số đầu vào theo nguyên tắc hướng đối tượng và trả về kiểu dữ liệu boolean để tối ưu. Vậy hàm đầy đủ thông tin sẽ được viết là: addNewBookTitle(bookTitle: BookTitle): boolean 

* EnterQuantityFrm 
    

* Thuộc tính ẩn: importBill: ImportBill và bookTitle: BookTitle 
    

* ImportedBookTitleListFrm 
    

* Thuộc tính ẩn: importBill: ImportBill 
    

* ConfirmFrm 
    

* Hàm xác nhận nhập truyện: 
    

* Tên: confirmImportBookTitle 
    

* Input: ImportBill 
    

* Output: void/boolean 
    

* Lớp chủ thể: ImportBillDAO 
    

* Thuộc tính ẩn: importBill: ImportBill vì phải cần truyền 3 thuộc tính ẩn User, Provider và ArrayList&lt;ImportedBookTitle&gt; là thuộc tính của 1 lớp thực thể là ImportBill nên áp dụng nguyên tắc hướng đối tượng, cần truyền luôn object lớp ImportBill 
    

Lập luận tương tự hàm addNewProvider ta sẽ chọn output cho hàm là boolean để tối ưu thông tin nhận được. Do đó, hàm đầy đủ thông tin sẽ được viết là: confirmImportBookTitle(importBill: ImportBill): boolean. 

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459094904/81402fe3-db03-4691-8d0c-01ffeb7d5aaa.jpeg align="center")

14. ### **Kịch bản chuẩn V3** 
    

1. Nhà cung cấp nhập một số lượng truyện (cũ hoặc mới) cho cửa hàng 
    

2. Nhân viên kho bắt đầu quá trình nhập truyện từ nhà cung cấp bằng việc nhập username, password và nhấn nút đăng nhập trên giao diện LoginFrm 
    

3. Lớp LoginFrm thực hiện hàm actionPerformed() 
    

4. Hàm actionPerformed() gọi lớp User 
    

5. Lớp User thực hiện hàm khởi tạo User(), setUsername(), setPassword(), đóng gói các thuộc tính thành object của lớp User 
    

6. Lớp User trả kết quả là object lớp User về cho hàm actionPerformed() 
    

7. Hàm actionPerformed() gọi lớp UserDAO 
    

8. Lớp UserDAO thực hiện hàm checkLogin() 
    

9. Lớp UserDAO gọi lớp User 
    

10. Lớp User thực hiện hàm setId(), setFullName(), setRole() 
    

11. Lớp User trả kết quả là object lớp User về cho lớp UserDAO 
    

12. Lớp UserDAO trả kết quả về cho hàm actionPerformed() 
    

13. Hàm actionPerformed() gọi lớp WarehouseStaffHomeFrm 
    

14. Lớp WarehouseStaffHomeFrm thực hiện hàm khởi tạo WarehouseStaffHomeFrm(u: User) 
    

15. Lớp WarehouseStaffHomeFrm hiển thị cho nhân viên kho 
    

16. Nhân viên kho chọn chức năng nhập truyện từ lớp WarehouseStaffHomeFrm 
    

17. Lớp WarehouseStaffHomeFrm thực hiện hàm actionPerformed() 
    

18. Hàm actionPerformed() gọi lớp SearchProviderFrm 
    

19. Lớp SearchProviderFrm thực hiện hàm khởi tạo SearchProviderFrm(u: User) 
    

20. Lớp SearchProviderFrm hiển thị cho nhân viên kho 
    

21. Nhân viên kho hỏi nhà cung cấp thông tin của nhà cung cấp 
    

22. Nhà cung cấp cung cấp thông tin cho nhân viên kho 
    

23. Nhân viên kho nhập tên nhà cung cấp và nhấn nút tìm kiếm trên giao diện lớp SearchProviderFrm 
    

24. Lớp SearchProviderFrm thực hiện hàm actionPerformed() 
    

25. Hàm actionPerformed() gọi lớp ProviderDAO 
    

26. Lớp ProviderDAO thực hiện hàm searchProviderByName(name: String) 
    

27. Lớp ProviderDAO gọi lớp Provider 
    

28. Lớp Provider thực hiện hàm khởi tạo Provider(), các hàm setter() và đóng gói các thuộc tính thành object của lớp Provider 
    

29. Lớp Provider trả kết quả là object của lớp Provider về cho lớp ProviderDAO 
    

30. Lớp ProviderDAO trả kết quả về cho hàm actionPerformed() 
    

31. Lớp SearchProviderFrm hiển thị kết quả cho nhân viên kho 
    

32. Nhân viên kho chọn đúng dòng của thông tin nhà cung cấp 
    

33. Lớp SearchProviderFrm thực hiện hàm actionPerformed() 
    

34. Hàm actionPerformed() gọi lớp ImportBill 
    

35. Lớp ImportBill thực hiện hàm khởi tạo ImportBill(), setUser(), setProvider() và đóng gói các thuộc tính thành object của lớp ImportBill 
    

36. Lớp ImportBill trả kết quả là object lớp ImportBill về cho hàm actionPerformed() 
    

37. Hàm actionPerformed() gọi lớp SearchBookTitleFrm 
    

38. Lớp SearchBookTitleFrm thực hiện hàm khởi tạo SearchBookTitleFrm(importBill: ImportBill) 
    

39. Lớp SearchBookTitleFrm hiển thị cho nhân viên kho 
    

40. Nhân viên kho hỏi nhà cung cấp thông tin về đầu truyện cần nhập 
    

41. Nhà cung cấp trả lời nhân viên kho về thông tin đầu truyện cần nhập 
    

42. Nhân viên kho nhập tên đầu truyện và nhấn nút tìm kiếm 
    

43. Lớp SearchBookTitleFrm thực hiện hàm actionPerformed() 
    

44. Hàm actionPerformed() gọi lớp BookTitleDAO 
    

45. Lớp BookTitleDAO thực hiện hàm searchBookTitleByName(name: String) 
    

46. Lớp BookTitleDAO gọi lớp BookTitle 
    

47. Lớp BookTitle thực hiện hàm khởi tạo BookTitle() và các hàm setter() và đóng gói các thuộc tính thành object lớp BookTitle 
    

48. Lớp BookTitle trả kết quả là object lớp BookTitle về cho lớp BookTitleDAO 
    

49. Lớp BookTitleDAO trả kết quả về cho hàm actionPerformed() 
    

50. Lớp SearchBookTitleFrm hiển thị kết quả cho nhân viên kho 
    

51. Nhân viên kho chọn dòng có thông tin đầu truyện đúng 
    

52. Lớp SearchBookTitleFrm thực hiện hàm actionPerformed() 
    

53. Hàm actionPerformed() gọi lớp EnterQuantityFrm 
    

54. Lớp EnterQuantityFrm thực hiện hàm khởi tạo EnterQuantityFrm(importBill: ImportBill, bookTitle: BookTitle) 
    

55. Lớp EnterQuantityFrm hiển thị cho nhân viên kho 
    

56. Nhân viên kho hỏi nhà cung cấp số lượng truyện của đầu truyện 
    

57. Nhà cung cấp trả lời nhân viên kho số lượng truyện của đầu truyện 
    

58. Nhân viên kho nhập số lượng truyện và nhấn vào nút xác nhận 
    

59. Lớp EnterQuantityFrm thực hiện hàm actionPerformed() 
    

60. Hàm actionPerformed() gọi lớp ImportedBookTitle 
    

61. Lớp ImportedBookTitle thực hiện hàm khởi tạo ImportedBookTitle(), setter(), setBookTitle(), setQuantity(), setUnitPrice() và đóng gói các thuộc tính thành các object lớp ImportedBookTitle 
    

62. Lớp ImportedBookTitle trả kết quả là object lớp ImportedBookTitle về cho hàm actionPerformed() 
    

63. Hàm actionPerformed() gọi lớp ImportBill 
    

64. Lớp ImportBill thực hiện hàm setImportedBookTitleList() 
    

65. Lớp ImportBill trả kết quả là object của lớp ImportBill cho hàm actionPerformed() 
    

66. Hàm actionPerformed() gọi lớp ImportedBookTitleListFrm 
    

67. Lớp ImportedBookTitleListFrm thực hiện hàm khởi tạo ImportedBookTitleListFrm(importBill: ImportBill) 
    

68. Lớp ImportedBookTitleListFrm hiển thị cho nhân viên kho 
    

69. Nhân viên kho đọc lại thông tin các đầu truyện được nhập và yêu cầu nhà cung cấp đối chiếu xác nhận 
    

70. Nhà cung cấp xác nhận đúng thông tin 
    

71. Nhân viên kho nhấn nút xác nhận 
    

72. Lớp ImportedBookTitleListFrm thực hiện hàm actionPerformed() 
    

73. Hàm actionPerformed() gọi lớp ConfirmFrm 
    

74. Lớp ConfirmFrm thực hiện hàm khởi tạo ConfirmFrm(importBill: ImportBill) 
    

75. Lớp ConfirmFrm hiển thị cho nhân viên kho 
    

76. Nhân viên kho hỏi nhà cung cấp số tiền giảm giá trong lần nhập này 
    

77. Nhà cung cấp trả lời nhân viên kho số tiền giảm giá trong lần nhập này 
    

78. Nhân viên kho nhập số tiền giảm giá, chọn phương thức thanh toán và nhấn vào nút in 
    

79. Lớp ConfirmFrm thực hiện hàm actionPerformed() 
    

80. Hàm actionPerformed() gọi lớp ImportBillDAO 
    

81. Lớp ImportBillDAO thực hiện hàm confirmImportBookTitle() 
    

82. Lớp ImportBillDAO trả kết quả về cho hàm actionPerformed() 
    

83. Lớp ConfirmFrm hiển thị thông báo nhập truyện thành công cho nhân viên kho và in ra hoá đơn nhập truyện 
    

84. Nhân viên kho nhận hoá đơn nhập truyện và đưa cho nhà cung cấp ký xác nhận 
    

85. Nhà cung cấp ký xác nhận nhập truyện thành công 
    

86. Nhân viên kho báo với nhà cung cấp nhập truyện từ nhà cung cấp thành công 
    

15. ### **Vẽ biểu đồ tuần tự chi tiết cho kịch bản chuẩn v3**
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749459162743/8bf86356-3156-47dd-ad91-29f75b0314ac.jpeg align="center")