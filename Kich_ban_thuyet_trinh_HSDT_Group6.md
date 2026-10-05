# KỊCH BẢN THUYẾT TRÌNH HỒ SƠ DỰ THẦU

**Gói thầu:** Cung cấp dịch vụ thiết kế, phát triển và triển khai website thương mại điện tử cho ABC Wear
**Nhà thầu:** Công ty TNHH Group 6
**Căn cứ số liệu:** HSDT v6 (đã cập nhật năng lực, giá và kế hoạch sprint)
**Thời lượng:** 15 phút trình bày + 5–7 phút hỏi đáp · 3 người trình bày · 18 slide

---

## Số phải thuộc lòng

| Nội dung | Con số |
|---|---|
| Giá dự thầu | 1.300.000.000 đ |
| Giá sau giảm 5% | 1.235.000.000 đ |
| Ký hợp đồng (T0) | 25/03 |
| Go-live | 01/07 |
| Sprint | 7 sprint × 2 tuần, 67 ngày làm việc |
| Khối lượng | 429 ngày công, bình quân 6,4 người toàn thời gian |
| Nhân công / bảo hành / dự phòng | 1.101,9 / 75 / 123,1 triệu |
| Bảo hành | 12 tháng từ biên bản nghiệm thu triển khai |

---

## Phân vai và mốc thời gian

| Mốc | Phần | Slide | Người nói |
|---|---|---|---|
| 0:00 | Mở đầu | 1–2 | Quản lý dự án |
| 0:45 | 1. Cách chúng tôi đọc đề bài | 3 | Quản lý dự án |
| 2:00 | 2. Phạm vi và ranh giới | 4 | Quản lý dự án |
| 3:30 | 3. Kiến trúc hệ thống | 5 | Technical Lead |
| 5:15 | 4. Mô hình dữ liệu Selling DB | 6 | Technical Lead |
| 6:30 | 5. Cam kết chất lượng | 7–8 | Technical Lead |
| 8:30 | 6. Tiến độ theo sprint | 9 | Quản lý dự án |
| 10:00 | 7. Tổ chức và năng lực | 10 | Quản lý dự án |
| 11:00 | 8. Bàn giao, nghiệm thu, bảo hành | 11–12 | Business Analyst |
| 12:15 | 9. Giá và cơ sở tính giá | 13–14 | Business Analyst |
| 13:45 | 10. Điều kiện hợp đồng | 15 | Business Analyst |
| 14:30 | 11. Rủi ro và đề nghị | 16 | Quản lý dự án |
| 15:00 | Kết | 17–18 | Quản lý dự án |

---

## Mở đầu (0:00 → 0:45) · Slide 1–2

> Gioi thieu Công ty TNHH Group 6.
>
> Đề xuất của chúng tôi cho gói phát triển website thương mại điện tử ABC Wear: giá dự thầu 1.300.000.000 đồng, sau giảm giá 5% còn 1.235.000.000 đồng. Thời gian thực hiện từ ngày ký hợp đồng đến cutover ngày 01 tháng 7. Bảo hành 12 tháng.
>
> Trong mười lăm phút, chúng tôi trình bày mười một nội dung, bám đúng mười mục mà RFP yêu cầu. Xin bắt đầu bằng cách chúng tôi hiểu đề bài, vì đó là chỗ quyết định mọi con số phía sau.

---

## 1. Cách chúng tôi đọc đề bài (0:45 → 2:00) · Slide 3

**Thông điệp:** chúng tôi đọc kỹ, kể cả những dòng dễ bỏ qua.

> RFP của ABC Wear dài năm trang. Chúng tôi tách ra hai mươi hai yêu cầu, đánh mã từ R01 đến R22 khớp đúng mã trong hồ sơ mời thầu, rồi lập ma trận đối chiếu từng yêu cầu với vị trí đáp ứng trong hồ sơ dự thầu.
>
> Ma trận đó cho kết quả trung thực: mười chín yêu cầu chúng tôi đáp ứng, ba yêu cầu chưa thể khẳng định trọn vẹn. R10 về cách nộp hồ sơ, R13 về tên bên B, và R22 về bốn khung đặc tả còn trống ở trang bốn và trang năm của RFP. Ba điểm này chúng tôi ghi là đề nghị làm rõ, không ghi là đã đáp ứng.
>
> Chúng tôi chọn cách làm này vì một hồ sơ nói đáp ứng mọi thứ thường là hồ sơ chưa đọc kỹ.

*Nếu tổ chuyên gia quan tâm:* "Ma trận đầy đủ nằm ở mục XI.9 của hồ sơ."

---

## 2. Phạm vi và ranh giới (2:00 → 3:30) · Slide 4

**Thông điệp:** chúng tôi chào đúng thứ RFP yêu cầu, không nhiều hơn.

> Sơ đồ trong RFP vẽ rất rõ: hệ thống mới gồm ba nhóm chức năng Product Search, Member Administration và Order, cùng cơ sở dữ liệu Selling DB, kết nối với Main System hiện hữu. Chúng tôi chào đúng ba nhóm đó, cộng một hạng mục riêng cho phần tích hợp.
>
> Có một dòng nhỏ ở trang bốn mà chúng tôi coi là quan trọng: các chức năng quản trị nội bộ nằm ngoài phạm vi dự án. Nghĩa là quản lý sản phẩm, tồn kho, khuyến mại, cấu hình và báo cáo quản trị tiếp tục do Main System đảm nhiệm. Chúng tôi không đưa những thứ đó vào bảng giá.
>
> Những tính năng hấp dẫn nhưng RFP không nêu, như gợi ý sản phẩm theo hành vi, so sánh sản phẩm, hóa đơn điện tử, kết nối trực tiếp đơn vị giao hàng, chúng tôi tách thành phạm vi tùy chọn với báo giá riêng. ABC Wear quyết định có đưa vào hợp đồng hay không, và giá gói cơ sở không thay đổi.
>
> Chúng tôi làm vậy để tổ chuyên gia so sánh được các hồ sơ trên cùng một mặt bằng.

---

## 3. Kiến trúc hệ thống (3:30 → 5:15) · Slide 5

*Chỉ vào sơ đồ sáu tầng.*

> Hệ thống chia thành sáu tầng.
>
> Tầng truy cập là trình duyệt trên máy tính và thiết bị di động, thiết kế responsive.
>
> Toàn bộ lưu lượng từ Internet đi qua cân bằng tải, nơi kết thúc kết nối SSL. Cân bằng tải chạy cặp chủ động và chờ, nên một máy hỏng không làm gián đoạn dịch vụ.
>
> Tiếp đến là cổng API kèm dịch vụ xác thực riêng, lo việc định tuyến, giới hạn tần suất và cấp mã phiên.
>
> Tầng nghiệp vụ tách thành ba dịch vụ độc lập đúng theo ba nhóm chức năng của RFP. Khi lưu lượng tìm kiếm tăng vào mùa cao điểm, chúng tôi nhân bản riêng dịch vụ tìm kiếm mà không phải nhân bản cả hệ thống.
>
> Tầng dữ liệu gồm Selling DB, cache và chỉ mục tìm kiếm. Cơ sở dữ liệu có bản sao đọc và chuyển đổi dự phòng. Cache và chỉ mục đều dựng lại được từ dữ liệu gốc, nên mất chúng không làm mất dữ liệu.
>
> Cuối cùng là adapter tích hợp, nơi duy nhất trao đổi với Main System. Dữ liệu sản phẩm và tồn kho đi vào, đơn hàng đi ra, và mọi lần trao đổi đều được ghi nhật ký để đối soát khi có chênh lệch số liệu.
>
> Các sản phẩm nền tảng nêu trong hồ sơ đều đã được định giá và có phương án tương đương, không ràng buộc ABC Wear vào một nhà cung cấp.

---

## 4. Mô hình dữ liệu Selling DB (5:15 → 6:30) · Slide 6

*Chỉ vào sơ đồ ERD.*

> Đây là một trong bốn khung mà RFP để trống. Chúng tôi vẽ luôn thay vì chờ ký hợp đồng mới làm.
>
> Selling DB có mười thực thể. Xin nêu ba quyết định thiết kế đáng chú ý.
>
> Thứ nhất, đơn hàng lưu bản chụp địa chỉ giao hàng và giá tại thời điểm mua, chứ không chỉ trỏ tới sổ địa chỉ và bảng giá. Khách sửa địa chỉ hay cửa hàng đổi giá về sau thì đơn cũ vẫn giữ nguyên dữ liệu gốc. Nhiều hệ thống thương mại điện tử làm sai chỗ này và chỉ phát hiện ra khi đối soát.
>
> Thứ hai, chúng tôi cho phép đặt hàng không cần đăng nhập. Trường thành viên trong đơn được để trống, và đơn lưu kèm email, số điện thoại của khách vãng lai.
>
> Thứ ba, một đơn hàng có thể có nhiều bản ghi thanh toán. Thanh toán trực tuyến thất bại rồi thử lại là chuyện bình thường, và mô hình phải chịu được điều đó. Hoàn tiền cũng có thực thể riêng.
>
> Mô hình logic, mô hình vật lý và từ điển dữ liệu nằm trong sản phẩm bàn giao D03, được ABC Wear phê duyệt trước khi chúng tôi viết dòng mã đầu tiên.

---

## 5. Cam kết chất lượng (6:30 → 8:30) · Slide 7–8

**Thông điệp:** giữ nguyên hai chỉ tiêu gốc, và nói trước cách đo.

*Slide 7 – Phản hồi 2 giây*

> RFP đặt hai chỉ tiêu phi chức năng: phản hồi trong hai giây, và dùng được hai mươi bốn giờ mỗi ngày, ba trăm sáu mươi lăm ngày mỗi năm. Chúng tôi giữ nguyên cả hai.
>
> Hai giây chỉ có nghĩa khi nói rõ đo ở đâu và ở mức tải nào. Chúng tôi đề xuất trọn bộ thông số: đo tại trình duyệt, ở mức bốn trăm phiên hoạt động thực tế, tăng tải mười phút, giữ tải sáu mươi phút, lặp ba lần. Cơ cấu thao tác gồm bốn mươi phần trăm tìm kiếm, ba mươi phần trăm xem chi tiết, hai mươi phần trăm thao tác tài khoản, mười phần trăm đặt hàng.
>
> Có ba điểm chúng tôi tự ràng buộc chặt hơn mức thông thường. Một, từng mẫu hợp lệ phải đạt, không lấy trung bình và không thay bằng giá trị phân vị. Hai, giao dịch lỗi hoặc quá thời gian được tính là không đạt và vẫn nằm trong tập mẫu. Ba, bằng chứng nghiệm thu là lần chạy đầy đủ trên môi trường vận hành trước go-live, không ngoại suy từ môi trường thử quy mô nhỏ hơn.

*Slide 8 – Vận hành 24/365*

> Về chỉ tiêu 24/365, chúng tôi thiết kế để bảo trì thông thường thực hiện luân phiên, không làm gián đoạn dịch vụ. Chúng tôi không đề nghị bất kỳ khoản miễn trừ mặc định nào. Mọi khoảng dừng đều được ghi đầy đủ trong báo cáo khả dụng hằng tháng.
>
> Ngoài hai chỉ tiêu gốc, chúng tôi bổ sung những cam kết RFP chưa nêu nhưng một hệ thống lưu hồ sơ thành viên và đơn hàng bắt buộc phải có: kiểm thử theo ma trận OWASP ASVS mức hai, cấu hình máy chủ theo chuẩn CIS, thiết kế theo nguyên tắc quyền tối thiểu, sao lưu hằng ngày, khôi phục dịch vụ trong bốn giờ và mất dữ liệu tối đa mười lăm phút.

---

## 6. Tiến độ theo sprint (8:30 → 10:00) · Slide 9

> Chúng tôi lập lịch ngược từ cutover ngày 01 tháng 7, chia thành bảy sprint, mỗi sprint hai tuần.
>
> Từ ngày ký hợp đồng 25 tháng 3 đến hết 30 tháng 6 là đúng 98 ngày, tức bảy sprint. Trừ cuối tuần và ba ngày lễ Giỗ Tổ, 30 tháng 4, 1 tháng 5, còn 67 ngày làm việc.
>
> Sprint 0 dùng để khởi động, khảo sát và dựng môi trường. Sprint 1 chốt đặc tả vào ngày 10 tháng 4 và thiết kế vào ngày 18 tháng 4. Ba sprint tiếp theo là phát triển, ba module chạy song song. Tích hợp với Main System xong ngày 28 tháng 5, cũng là ngày đóng băng tính năng. Sprint 5 dành cho đo hiệu năng ngày 4 tháng 6 và kiểm thử bảo mật ngày 10 tháng 6. Sprint 6 hoàn tất nghiệm thu người dùng ngày 18 tháng 6, đào tạo ngày 22 tháng 6, diễn tập chuyển đổi ngày 27 tháng 6 và họp go/no-go ngày 30 tháng 6.
>
> Cuối mỗi sprint có buổi demo với ABC Wear, thay cho buổi họp tiến độ tuần đó. Như vậy ABC Wear được thấy sản phẩm chạy thật bảy lần trước go-live, không chỉ đọc báo cáo.
>
> Hai hạng mục đầu muộn hơn mốc tham chiếu trong hồ sơ mời thầu lần lượt mười ngày và ba ngày, vì chúng tôi tính từ sau ngày đóng thầu. Nếu ABC Wear ký sớm hơn, chúng tôi trả lại đúng mốc gốc. Chúng tôi ghi rõ sai khác này thay vì lặng lẽ chỉnh số cho khớp.

**Bảng tra nhanh cho người nói:**

| Sprint | Thời gian | Trọng tâm | Mốc |
|---|---|---|---|
| S0 | 25/03 – 07/04 | Khởi động, khảo sát, dựng môi trường | D01; T0 25/03 |
| S1 | 08/04 – 21/04 | Đặc tả, thiết kế, khung hệ thống | D02 10/04; D03 18/04 |
| S2 | 22/04 – 05/05 | Tìm kiếm, tài khoản, giỏ hàng | Nghỉ lễ 30/4–1/5 |
| S3 | 06/05 – 19/05 | Danh mục, địa chỉ, đặt hàng, API tích hợp | Hai module xong kiểm thử 16/05 |
| S4 | 20/05 – 02/06 | Thanh toán, hủy, hoàn tiền, đồng bộ hai chiều | Xong tích hợp 28/05; D04 |
| S5 | 03/06 – 16/06 | Thử tải trên PRD, kiểm thử bảo mật | Hiệu năng 04/06; bảo mật 10/06 |
| S6 | 17/06 – 30/06 | UAT, đào tạo, diễn tập, go/no-go | UAT 18/06; D06 22/06; diễn tập 27/06; go/no-go 30/06 |
| — | 01/07 | Go-live, smoke test, nghiệm thu | D07; bắt đầu bảo hành |

---

## 7. Tổ chức và năng lực (10:00 → 11:00) · Slide 10

> Chín nhân sự chủ chốt. Chúng tôi không kê tỷ lệ phần trăm chung chung mà kê số ngày công của từng người trong từng sprint, và không ô nào vượt số ngày làm việc của sprint đó.
>
> Tổng khối lượng là 429 ngày công. Chia cho 67 ngày làm việc thì bình quân cần 6,4 người toàn thời gian. Đội chín người có năng lực tối đa khoảng 600 ngày công, nên còn dư khoảng 174 ngày công làm vùng đệm nếu phần tích hợp gặp sự cố.
>
> Quản lý dự án tham gia toàn thời gian từ đầu đến hết nghiệm thu và là đầu mối duy nhất của chúng tôi với ABC Wear. Trưởng nhóm kiểm thử báo cáo độc lập về chất lượng, không nằm dưới trưởng nhóm phát triển, để tránh xung đột lợi ích. Mỗi vai trò đều có người thay thế được chỉ định.
>
> Về họp: họp nội bộ hằng ngày mười lăm phút, demo với ABC Wear cuối mỗi sprint, họp rà soát cuối mỗi giai đoạn, và họp đột xuất khi có sự cố ảnh hưởng tiến độ.

---

## 8. Bàn giao, nghiệm thu và bảo hành (11:00 → 12:15) · Slide 11–12

*Slide 11 – Bàn giao và nghiệm thu*

> Tám sản phẩm bàn giao, đánh mã D01 đến D08 đúng theo hồ sơ mời thầu: kế hoạch triển khai, đặc tả yêu cầu, tài liệu thiết kế, phần mềm và mã nguồn, hồ sơ kiểm thử, tài liệu và chuyển giao, hồ sơ cutover và nghiệm thu, và cuối cùng là hồ sơ sửa lỗi trong năm bảo hành.
>
> Xin làm rõ một điểm hay bị hiểu nhầm. Chúng tôi tách hai văn bản ở hai thời điểm khác nhau. Biên bản go/no-go ký trước ngày 01 tháng 7, làm điều kiện để chuyển đổi. Biên bản nghiệm thu triển khai ký tại hoặc sau cutover, sau khi kiểm thử nhanh trên môi trường thật. Chính biên bản thứ hai mới là mốc bắt đầu mười hai tháng bảo hành và mốc thanh toán mười phần trăm cuối.
>
> Sản phẩm D08 là hồ sơ sửa lỗi cả năm, nên chỉ đóng sau khi hết mười hai tháng, không phải hoàn thành tại ngày go-live.

*Slide 12 – Bảo hành 12 tháng*

> Trong năm bảo hành, chúng tôi cam kết bốn mức hỗ trợ. Sự cố nghiêm trọng là khi hệ thống dừng, không đặt được hàng, hoặc có dấu hiệu mất hay rò rỉ dữ liệu khách hàng. Với loại sự cố này, chúng tôi phản hồi trong một giờ, khôi phục dịch vụ trong bốn giờ và sửa dứt điểm nguyên nhân trong mười sáu giờ.
>
> Đồng hồ tính từ lúc yêu cầu được ghi nhận trên kênh tiếp nhận, không tính từ lúc chúng tôi xác nhận. Đội trực ba ca luân phiên, chi phí đã nằm trong giá.

---

## 9. Giá và cơ sở tính giá (12:15 → 13:45) · Slide 13–14

*Slide 13 – Giá*

> Giá được tính từ dưới lên, từ năng lực thật của đội.
>
> Chúng tôi lấy ngày công của từng vai trò nhân với đơn giá của vai trò đó. Quản lý dự án và Technical Lead là 3 triệu một ngày công, lập trình viên 2,4 triệu, kiểm thử và triển khai 2,2 triệu. Đơn giá đã gồm chi phí quản lý, lợi nhuận và thuế. Tổng 429 ngày công ra 1 tỷ 102 triệu đồng tiền nhân công.
>
> Cộng 75 triệu cho bảo hành mười hai tháng. Cộng 123 triệu dự phòng, chủ yếu cho rủi ro tích hợp Main System, tương đương khoảng 48 ngày công, đủ bù một sprint chậm mà không phải dời cutover. Tổng là đúng 1 tỷ 300 triệu, giảm giá năm phần trăm còn 1 tỷ 235 triệu.
>
> Phân theo sáu hạng mục của hồ sơ mời thầu: phân tích và đặc tả 197 triệu, thiết kế 103 triệu, phát triển và tích hợp 580 triệu, đã gồm toàn bộ dự phòng, kiểm thử và nghiệm thu người dùng 201 triệu, chuẩn bị vận hành và cutover 144 triệu, bảo hành 75 triệu.

**Bảng tra nhanh cho người nói:**

| Cấu thành | Triệu đồng |
|---|---|
| Nhân công (429 ngày công) | 1.101,9 |
| Bảo hành 12 tháng | 75,0 |
| Dự phòng rủi ro tích hợp | 123,1 |
| **Giá dự thầu** | **1.300,0** |
| Giảm giá 5% | − 65,0 |
| **Giá sau giảm** | **1.235,0** |

*Slide 14 – Chi phí ngoài giá*

> Một điểm chúng tôi muốn nói thẳng: giá này không phải toàn bộ chi phí vận hành của ABC Wear. Thuê máy chủ, băng thông, chứng thư số, phí cổng thanh toán và dịch vụ gửi tin nhắn là chi phí định kỳ thuộc chủ đầu tư. Chúng tôi liệt kê đủ chín khoản trong hồ sơ, kèm bên chịu chi phí, để ABC Wear lập dự toán vận hành ngay từ bây giờ thay vì phát hiện ra sau go-live.

---

## 10. Điều kiện hợp đồng (13:45 → 14:30) · Slide 15

> Chúng tôi chấp thuận các điều kiện chính của hồ sơ mời thầu.
>
> Hợp đồng trọn gói, không tạm ứng, thanh toán bốn đợt hai mươi, ba mươi, bốn mươi và mười phần trăm, gắn với đầu ra.
>
> Mười phần trăm cuối được trả sau nghiệm thu triển khai, đổi lấy bảo lãnh bảo hành bằng mười phần trăm giá trị hợp đồng do ngân hàng thương mại phát hành, hiệu lực đến ba mươi ngày sau khi hết thời hạn bảo hành. Phí bảo lãnh do chúng tôi chịu và đã tính trong giá.
>
> Chúng tôi chấp thuận biên độ tăng giảm khối lượng năm phần trăm tại thời điểm trao hợp đồng, định giá theo đơn giá của hạng mục tương ứng.
>
> Về quyền sở hữu: phần mã nguồn và tài liệu viết riêng cho ABC Wear thuộc về ABC Wear. Với thư viện nguồn mở và thành phần bên thứ ba, chúng tôi không cam kết chuyển giao quyền mà mình không sở hữu, nhưng bàn giao đầy đủ danh mục thành phần, phiên bản và giấy phép, kèm hướng dẫn để ABC Wear tự dựng lại hệ thống từ mã nguồn.
>
> Chúng tôi không sử dụng nhà thầu phụ khi chưa có văn bản chấp thuận của ABC Wear.

---

## 11. Rủi ro và đề nghị (14:30 → 15:00) · Slide 16

> Rủi ro lớn nhất của dự án này không nằm ở phần chúng tôi viết mới, mà ở chỗ nối với Main System. RFP chỉ vẽ một mũi tên, không mô tả giao thức, chiều truyền, tần suất hay định dạng dữ liệu.
>
> Chúng tôi đề nghị ABC Wear cung cấp đặc tả giao diện, dữ liệu mẫu và môi trường thử trong mười ngày làm việc kể từ ngày ký. Nếu chậm, chúng tôi vẫn chạy bằng môi trường mô phỏng để không dừng tiến độ. Nhưng mô phỏng không thay được kiểm thử trên giao diện thật, và nghiệm thu bắt buộc phải làm trên giao diện thật.
>
> Hồ sơ của chúng tôi có mười bốn đề nghị làm rõ. Ba đề nghị quan trọng nhất là: chức năng Order có bao gồm thanh toán trực tuyến hay không, đơn vị nào thuê và vận hành hạ tầng sau cutover, và thông số chính thức để đo tiêu chí hai giây.

---

## Kết (15:00) · Slide 17–18

> Xin tóm tắt bằng năm điểm.
>
> Một, đúng phạm vi: không chào thừa để đẩy giá, cũng không cắt bớt để hạ giá.
>
> Hai, hai chỉ tiêu gốc của RFP được giữ nguyên, kèm cách đo cụ thể đến mức có thể tranh luận ngay bây giờ.
>
> Ba, lịch về đúng ngày 01 tháng 7 qua bảy sprint, mọi điều kiện quyết định nằm trước cutover.
>
> Bốn, giá được bóc tách đến từng ngày công của từng người, và phần chi phí không thuộc chúng tôi cũng được nói rõ.
>
> Năm, những gì chưa chắc chắn, chúng tôi ghi thành đề nghị làm rõ thay vì giấu vào giá rồi tính sau.
>
> Xin cảm ơn tổ chuyên gia. Chúng tôi sẵn sàng trả lời câu hỏi.

---

## Chuẩn bị hỏi đáp

| Câu hỏi có thể gặp | Trả lời ngắn |
|---|---|
| 1,3 tỷ có quá thấp để làm đủ? | 429 ngày công được tính theo từng người, từng sprint, và không vượt năng lực của đội. Chúng tôi còn khoảng 174 ngày công dư và 123 triệu dự phòng. |
| 1,3 tỷ có quá cao? | Phần nhân công là 1,1 tỷ, đơn giá bình quân khoảng 2,57 triệu một ngày công, đã gồm quản lý, lợi nhuận và thuế. Phần còn lại là bảo hành và dự phòng, cả hai đều có con số riêng. |
| Vì sao dự phòng nằm trong hạng mục phát triển? | Vì rủi ro lớn nhất là tích hợp Main System, và hạng mục đó là nơi rủi ro xảy ra. Chúng tôi ghi riêng con số 123,1 triệu chứ không trộn vào đơn giá. |
| Đội có thật sự làm kịp 01/07? | 429 ngày công chia 67 ngày là 6,4 người toàn thời gian, trong khi đội có 9 người. Mỗi sprint có demo, ABC Wear thấy tiến độ thật sau mỗi hai tuần. |
| Nếu một sprint bị trễ? | Dùng vùng đệm năng lực và dự phòng để bù trong sprint kế tiếp. Nếu trễ do chậm cấp API hoặc chậm phê duyệt quá năm ngày làm việc, chúng tôi lập biên bản và trình ABC Wear quyết định. Chúng tôi không tự dời cutover. |
| Vì sao hai hạng mục đầu muộn hơn mốc trong hồ sơ mời thầu? | Vì chúng tôi tính từ sau ngày đóng thầu. Ký sớm hơn thì trả lại đúng mốc gốc. |
| Vì sao không chào thanh toán online rõ ràng? | Có chào, nằm trong hạng mục Order. RFP không nêu rõ nên chúng tôi ghi thành giả định GĐ-03: nếu ABC Wear xác nhận không cần, giảm 60 triệu trước khi áp giảm giá. |
| Chỉ có một hợp đồng tương tự? | Đúng, và chúng tôi kê khai thêm một hợp đồng không hoàn thành thay vì giấu. Xin trình bày nguyên nhân và biện pháp đã khắc phục. |
| Cam kết 24/365 thế nào khi hạ tầng do ABC Wear thuê? | Chúng tôi chịu trách nhiệm phần mềm và cấu hình ứng dụng. Phần hạ tầng được tính theo thời gian chúng tôi kiểm soát được. Ranh giới này ghi rõ trong hồ sơ. |
| Ba yêu cầu chưa đáp ứng trọn vẹn có phải điểm yếu? | Đó là ba điểm hồ sơ mời thầu còn để mở, không phải chúng tôi thiếu năng lực. Chúng tôi nêu ra để hai bên chốt trước khi ký. |
| Tại sao không dùng công nghệ X? | Các phương án chúng tôi nêu đều đã định giá và có sản phẩm tương đương. Nếu ABC Wear có chuẩn riêng nằm trong danh sách tương đương, chúng tôi áp dụng ở giai đoạn thiết kế mà không đổi giá. |
| Đội ngũ có đang làm dự án khác không? | Bảng ngày công theo từng sprint nằm ở mục XI.8, kèm người thay thế cho từng vai trò. |

---

## Ba điều không làm tại buổi thuyết trình

1. Không hứa thêm tính năng tại chỗ.
2. Không giảm giá tại chỗ.
3. Không trả lời "để sau". Thay bằng: *"Nội dung đó chúng tôi đã ghi thành đề nghị số … trong hồ sơ, xin ABC Wear xác nhận khi làm rõ E-HSDT."*

---

## Nếu bị cắt thời gian còn 10 phút

- Bỏ mục 10 (điều kiện hợp đồng), để dành cho phần hỏi đáp.
- Gộp mục 7 vào mục 6, chỉ giữ một câu: *"429 ngày công, bình quân 6,4 người trên đội 9 người."*
- Rút mục 4 xuống một câu về ba quyết định thiết kế.
- Bỏ slide 14, chỉ nói một câu: *"Giá chưa gồm chi phí vận hành định kỳ của ABC Wear, đã liệt kê đủ trong hồ sơ."*
