# 01 — Individual Problem Scan

**Học viên:** Vũ Tú Quỳnh  
**Mã học viên:** 2A202601239  
**Repo:** `Day02_2A202601239_VuTuQuynh`

> **Lưu ý về dữ liệu:** Các vấn đề dưới đây được tổng hợp từ trải nghiệm học tập, công việc kỹ thuật và vận hành bán hàng. Những con số thời gian là baseline ước tính ban đầu từ quan sát cá nhân, cần được kiểm chứng thêm bằng log, khảo sát hoặc phỏng vấn nếu vấn đề được nhóm chọn để đào sâu.

---

## Phase 1 — Scan rộng các vấn đề

Tôi scan các vấn đề theo bốn lăng kính: công việc lặp lại, công việc tốn thời gian, bước AI có thể hỗ trợ tốt hơn và pain point được quan sát từ người khác.

| # | Lĩnh vực / lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật / cách đo ban đầu |
|---:|---|---|---|---|
| 1 | Fintech / pain từ người khác | Khách hàng gọi tổng đài ngân hàng để xử lý giao dịch nhưng đường dây liên tục bận, có trường hợp phải gọi lại khoảng 10 lần mới kết nối được. | Khách hàng ngân hàng, tổng đài viên | Số lần gọi lại; thời gian từ lần gọi đầu đến khi được tiếp nhận; tỷ lệ bỏ cuộc |
| 2 | Doanh nghiệp sản xuất / tốn thời gian | CBNV phải tìm quy trình nội bộ nằm rải rác theo từng phòng ban và thường phải nhớ đúng tên quy trình hoặc đúng thư mục mới tìm thấy. | CBNV, quản lý phòng ban, nhân sự mới | Ước tính 15–30 phút/lần tìm; phải hỏi đồng nghiệp; có nguy cơ dùng nhầm phiên bản |
| 3 | E-commerce / lặp lại | Khi có khiếu nại hoàn hàng, shop phải tự thu thập thông tin đơn, video đóng gói, tin nhắn, xác nhận vận chuyển và giấy tờ chất lượng từ nhiều nơi. | Chủ shop, nhân viên vận hành, khách hàng | Ước tính 20–45 phút/case; dễ thiếu bằng chứng; có deadline phản hồi từ nền tảng |
| 4 | E-commerce / lặp lại | Shop phải trả lời nhiều câu hỏi giống nhau về kích thước, màu sắc, phí ship, thêu logo và chính sách đổi hàng trên nhiều kênh. | Nhân viên CSKH, khách mua hàng | Câu hỏi lặp lại hằng ngày; phản hồi chậm ngoài giờ; thông tin có thể không đồng nhất |
| 5 | E-commerce / tốn thời gian | Báo giá và hóa đơn bán hàng được tính thủ công từ giá sản phẩm, số lượng, phí thêu, phí ship, hoa hồng và biên lợi nhuận. | Chủ shop, nhân viên chốt đơn | Dễ nhập sai đơn giá hoặc tổng tiền; phải sửa hóa đơn; mất 5–15 phút/đơn |
| 6 | Giáo dục / AI có thể hỗ trợ | Học viên phải đọc nhiều file hướng dẫn, rubric và ví dụ để xác định chính xác yêu cầu nộp bài và nguyên nhân bị trừ điểm. | Học viên, trợ giảng | Mất thời gian đối chiếu nhiều file; bỏ sót tên file hoặc tiêu chí chấm |
| 7 | Giáo dục / tốn thời gian | Người học có nhiều tài liệu nhưng khó xác định nội dung nào cần học trước theo mục tiêu, thời gian còn lại và lỗ hổng kiến thức. | Học viên khóa ngắn hạn | Ôn lan man; học lại phần đã biết; bỏ sót kiến thức nền quan trọng |
| 8 | DevOps / tốn thời gian | Khi tiếp quản máy chủ NGINX cũ, kỹ sư khó biết reverse proxy đang phục vụ domain nào vì cấu hình thiếu tài liệu và nằm rải rác trong container/server. | DevOps, SRE, đội ứng dụng | Phải SSH, đọc nhiều file config và đối chiếu DNS; rủi ro bỏ sót domain |
| 9 | DevOps / lặp lại | Chứng chỉ TLS được gia hạn và cập nhật thủ công, phụ thuộc vào một người nhớ ngày hết hạn và thao tác đúng trên server/Kubernetes. | DevOps, người dùng hệ thống | Có ngày hết hạn rõ; thao tác lặp lại; rủi ro downtime nếu quên hoặc cập nhật sai |
| 10 | DevOps / AI có thể hỗ trợ | Khi có sự cố, kỹ sư phải đọc log từ nhiều service, metric và deployment history để tìm nguyên nhân, trong khi dữ liệu nằm ở nhiều công cụ. | DevOps, developer, người dùng hệ thống | Thời gian điều tra kéo dài; lặp lại truy vấn; khó nối chuỗi sự kiện giữa các hệ thống |
| 11 | Knowledge management / pain từ người khác | Nhân viên mới thường hỏi lại các bước onboarding, quyền truy cập và quy trình triển khai vì tài liệu phân tán hoặc không biết từ khóa chính xác. | Nhân viên mới, mentor, DevOps | Cùng câu hỏi xuất hiện nhiều lần; mentor bị gián đoạn; onboarding kéo dài |
| 12 | Team collaboration / tốn thời gian | Quyết định kỹ thuật cũ nằm trong Slack, ticket, email và tài liệu; thành viên khó tìm lại lý do vì sao một phương án đã được chọn. | Developer, DevOps, PM | Mất 10–20 phút/lần tìm; có thể lặp lại tranh luận hoặc đưa ra quyết định trái ngược |
| 13 | Robotics / AI có thể hỗ trợ | Robot trong phòng đông người thu nhiều giọng nói nhưng khó xác định ai đang trực tiếp nói với robot trước khi chuyển âm thanh sang STT. | Người dùng robot, đội AI | STT ghi cả tiếng nền; phản hồi nhầm người; độ chính xác giảm trong môi trường ồn |
| 14 | Robotics / workflow | Robot biết tọa độ đồ vật nhưng hướng dẫn người dùng đi đến đồ vật chưa tính tốt vật cản, hướng nhìn và cách diễn đạt theo từng bước. | Người dùng, đội robot | Chỉ báo khoảng cách không đủ; người dùng có thể đi sai hướng hoặc va vào vật cản |
| 15 | Tuyển dụng / tốn thời gian | Ứng viên phải đọc JD, đối chiếu kỹ năng và chỉnh CV/cover letter thủ công cho từng vị trí. | Ứng viên, nhà tuyển dụng | Mất 30–60 phút/JD; dễ bỏ sót keyword; nội dung ứng tuyển thiếu nhất quán |

### Nhận xét sau khi scan

- Các vấn đề có workflow rõ nhất tập trung ở **chăm sóc khách hàng**, **tìm kiếm tri thức nội bộ** và **xử lý khiếu nại e-commerce**.
- Một số bài toán nghe phù hợp với AI nhưng thực tế có thể giải quyết phần lớn bằng rule, checklist, template hoặc cải tiến quy trình.
- Tôi ưu tiên những vấn đề có actor cụ thể, tần suất lặp lại, bottleneck nhìn thấy được và có thể đo trước/sau.

---

## Phase 2 — Chọn Top 3 Problem Cards

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Khách hàng không kết nối được tổng đài ngân hàng | Pain rõ, xảy ra đúng lúc khách hàng cần hỗ trợ; workflow có thể vẽ; impact về thời gian và trải nghiệm có thể đo | Chưa có dữ liệu chính thức về tỷ lệ cuộc gọi bận, thời gian chờ và phân bố loại yêu cầu |
| 2 | CBNV khó tìm quy trình nội bộ | Có actor rõ, dữ liệu tài liệu sẵn có, semantic search có điểm can thiệp cụ thể; impact lan rộng toàn công ty | Chất lượng và quyền truy cập tài liệu có đồng nhất không; tài liệu cũ đã được đánh dấu chưa |
| 3 | Shop thu thập bằng chứng khiếu nại hoàn hàng thủ công | Là pain thật trong vận hành; workflow lặp lại; có deadline; dễ đo thời gian và tỷ lệ hồ sơ thiếu | Mỗi nền tảng có rule khác nhau; khó đo mức tăng tỷ lệ khiếu nại thành công chỉ trong pilot ngắn |

---

# Problem Card #1 — Khách hàng không kết nối được tổng đài ngân hàng

## Problem 1 câu

Khi gặp vấn đề về giao dịch hoặc tài khoản, khách hàng phải gọi lại tổng đài ngân hàng nhiều lần vì đường dây bận, có trường hợp tới khoảng 10 cuộc vẫn chưa được tiếp nhận, khiến việc xử lý bị chậm và tạo cảm giác không được hỗ trợ.

## Actor

- **Actor chính:** Khách hàng cá nhân đang cần hỗ trợ về giao dịch, tài khoản hoặc thẻ.
- **Actor liên quan:** Tổng đài viên, bộ phận vận hành chăm sóc khách hàng và bộ phận xử lý nghiệp vụ.

## Thời điểm / bối cảnh

- Khách hàng phát hiện giao dịch bất thường, chuyển khoản chưa tới, thẻ bị khóa, cần tra soát hoặc cần giải đáp gấp.
- Nhu cầu thường có tính khẩn cấp và khách hàng không biết khi nào đường dây sẽ hết bận.

## Current workflow

1. Khách hàng phát hiện vấn đề.
2. Tự tìm số hotline hoặc mở ứng dụng ngân hàng.
3. Gọi tổng đài.
4. Nếu báo bận, khách hàng ngắt máy và tự gọi lại.
5. Sau khi kết nối, nghe IVR và chọn nhánh.
6. Chờ tổng đài viên.
7. Xác minh danh tính và kể lại toàn bộ vấn đề.
8. Tổng đài viên giải đáp, chuyển bộ phận hoặc tạo yêu cầu tra soát.
9. Khách hàng tiếp tục chờ kết quả nếu chưa giải quyết ngay.

## Bottleneck

**Bước 3–4: gọi tổng đài và tự gọi lại khi đường dây bận.**

- Khách hàng không biết vị trí trong hàng đợi.
- Không có cơ chế giữ chỗ hoặc hẹn gọi lại.
- Các yêu cầu đơn giản và yêu cầu khẩn cấp cùng tranh chấp một kênh hỗ trợ.
- Thời gian ước tính: 10 lần gọi lại có thể làm khách hàng mất khoảng 10–30 phút trước cả khi được tiếp nhận.

## Impact

- Chậm khóa thẻ hoặc báo giao dịch bất thường có thể làm tăng rủi ro cho khách hàng.
- Khách hàng mất thời gian và giảm niềm tin vào dịch vụ.
- Số cuộc gọi lặp lại làm tăng tải cho chính tổng đài.
- Tổng đài viên phải nghe khách hàng kể lại thông tin từ đầu, kéo dài thời gian xử lý.
- Khi khách hàng bỏ cuộc, vấn đề vẫn tồn tại và có thể chuyển thành khiếu nại nghiêm trọng hơn.

## Success metric

Các target dưới đây là giả thuyết ban đầu để pilot:

- Giảm số lần khách hàng phải chủ động gọi lại từ **tối đa khoảng 10 lần xuống không quá 1 lần**.
- Ít nhất **80% yêu cầu được hệ thống ghi nhận trong vòng 1 phút**, dù chưa có tổng đài viên rảnh.
- Với yêu cầu cần người xử lý, cung cấp callback hoặc lịch hẹn rõ ràng thay vì bắt khách hàng gọi lại.
- Giảm **50% số cuộc gọi lặp lại của cùng một khách hàng cho cùng một vấn đề**.
- Không tăng tỷ lệ chuyển sai bộ phận hoặc số lần khách hàng phải mô tả lại vấn đề.

## Non-AI alternative

- Tăng số lượng tổng đài viên vào giờ cao điểm.
- Dùng **virtual queue/callback** để giữ lượt và gọi lại cho khách hàng.
- Cải tiến IVR, tách hotline khẩn cấp và hotline thông tin chung.
- Hiển thị thời gian chờ dự kiến trong ứng dụng.
- Đưa các tác vụ đơn giản như khóa thẻ, tra cứu trạng thái tra soát vào self-service có rule rõ ràng.

Phần lớn bottleneck kết nối có thể được cải thiện bằng **workflow và hệ thống hàng đợi**, chưa bắt buộc phải dùng AI.

## AI hypothesis

AI có thể hỗ trợ ở một số bước có ngôn ngữ tự nhiên:

- Nhận diện nhanh ý định từ câu mô tả của khách hàng.
- Gợi ý self-service cho câu hỏi phổ biến.
- Tóm tắt vấn đề và dữ liệu khách đã cung cấp để tổng đài viên không phải hỏi lại từ đầu.
- Ưu tiên chuyển người thật với dấu hiệu rủi ro như mất thẻ, giao dịch nghi ngờ hoặc tài khoản bị chiếm quyền.

AI **không được** tự thực hiện giao dịch tài chính, tự kết luận gian lận hoặc bỏ qua bước xác minh danh tính.

## Quick gut

- [ ] No AI / process fix
- [ ] Rule
- [x] Workflow
- [ ] Agent
- [ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — ước tính 15–40+ phút trước khi xử lý xong

[Phát hiện vấn đề]
→ [Tìm hotline/app: 1–3']
→ [Gọi tổng đài: 1–2']
→ [Đường dây bận]
→ [Tự gọi lại nhiều lần: 10–30']  <-- bottleneck
→ [Nghe IVR + chờ: 3–10']
→ [Xác minh + kể lại vấn đề: 3–7']
→ [Giải đáp / chuyển bộ phận / tạo tra soát]

Failure:
Khách hàng bỏ cuộc hoặc chuyển sang kênh khác nhưng phải kể lại từ đầu.
```

### Draft future workflow

```text
FUTURE STATE — tiếp nhận yêu cầu trong dưới 1 phút

[Khách mở app hoặc gọi hotline]
→ [Nhập/nói vấn đề]
→ [Rule kiểm tra danh tính và dấu hiệu khẩn cấp]
→ [Hệ thống ghi nhận ticket + giữ vị trí trong hàng đợi]
→ ┌─ Yêu cầu đơn giản → [Self-service / FAQ có nguồn]
  └─ Cần nghiệp vụ → [Đặt callback + thời gian dự kiến]
→ [AI tạo tóm tắt cho tổng đài viên]
→ [Tổng đài viên xác minh, kiểm tra và xử lý]  <-- human boundary
→ [Khách nhận trạng thái và mã yêu cầu]

Fallback:
AI không hiểu hoặc confidence thấp → chuyển thẳng sang người thật,
giữ nguyên toàn bộ thông tin khách đã cung cấp.
```

## Vì sao bài toán này có impact

Đây không chỉ là vấn đề “chờ lâu” mà là điểm nghẽn ngay tại cửa vào của quy trình hỗ trợ. Khi chưa được ghi nhận yêu cầu, khách hàng phải tự chịu toàn bộ chi phí chờ và gọi lại. Một workflow callback kết hợp phân loại yêu cầu có thể giảm cuộc gọi lặp, giúp tổng đài viên nhận context sẵn và ưu tiên các trường hợp rủi ro cao.

---

# Problem Card #2 — CBNV khó tìm quy trình nội bộ

## Problem 1 câu

CBNV trong công ty sản xuất phải tìm thủ công quy trình của nhiều phòng ban và thường phải nhớ đúng tên tài liệu hoặc đường dẫn, nên mất thời gian, phải hỏi đồng nghiệp và có nguy cơ dùng nhầm quy trình hoặc phiên bản cũ.

## Actor

- **Actor chính:** CBNV cần tra cứu quy trình để thực hiện công việc.
- **Actor liên quan:** Nhân viên mới, quản lý phòng ban, QA/compliance và người phụ trách cập nhật tài liệu.

## Thời điểm / bối cảnh

- Khi nhân viên cần thực hiện một nghiệp vụ không thường xuyên.
- Khi có quy trình liên phòng ban.
- Khi nhân viên mới onboarding.
- Khi cần viết quy trình mới và phải tìm các quy trình liên quan để tham khảo.

## Current workflow

1. Nhân viên xác định nhu cầu bằng ngôn ngữ tự nhiên.
2. Đoán tên quy trình hoặc phòng ban sở hữu.
3. Mở từng thư mục, portal, Drive hoặc hệ thống quản lý tài liệu.
4. Search bằng keyword chính xác.
5. Mở nhiều file để kiểm tra nội dung.
6. Nếu không tìm thấy, hỏi đồng nghiệp hoặc quản lý.
7. Kiểm tra phiên bản và áp dụng quy trình.
8. Khi viết tài liệu mới, copy cấu trúc từ một file gần giống.

## Bottleneck

**Bước 2–5: người dùng phải chuyển nhu cầu thực tế thành đúng từ khóa/tên tài liệu và tự đọc nhiều kết quả.**

- Cùng một nhu cầu có thể được gọi bằng nhiều cách.
- Tài liệu được tổ chức theo phòng ban, trong khi công việc thực tế có thể liên phòng ban.
- Search keyword không hiểu ngữ nghĩa.
- Metadata, trạng thái hiệu lực và phiên bản có thể không đồng nhất.
- Baseline ước tính: **15–30 phút/lần tìm**, chưa tính thời gian chờ người khác trả lời.

## Impact

- Mất thời gian của cả người hỏi và người được hỏi.
- Nhân viên mới phụ thuộc nhiều vào mentor.
- Có nguy cơ dùng quy trình hết hiệu lực hoặc bỏ sót bước kiểm soát.
- Viết quy trình mới bị trùng lặp hoặc không nhất quán với quy định liên quan.
- Nếu mỗi nhân viên mất 20 phút và có 50 lượt tra cứu/ngày, tổng effort có thể vượt 16 giờ công/ngày; con số này cần được validate bằng log thực tế.

## Success metric

- Giảm median thời gian tìm đúng quy trình từ **15–30 phút xuống dưới 3 phút**.
- Ít nhất **80% lượt tìm kiếm có tài liệu phù hợp trong Top 3 kết quả**.
- Giảm **50% số câu hỏi lặp lại gửi cho quản lý/mentor**.
- 100% kết quả phải hiển thị **nguồn, phòng ban sở hữu, phiên bản và ngày hiệu lực** nếu dữ liệu có sẵn.
- Không hiển thị tài liệu ngoài quyền truy cập của người dùng.
- Tỷ lệ người dùng đánh dấu “kết quả không phù hợp” dưới 10% trong pilot.

## Non-AI alternative

- Chuẩn hóa tên file, taxonomy và metadata.
- Tạo một cổng tài liệu tập trung.
- Bắt buộc có owner, trạng thái hiệu lực, ngày cập nhật và phiên bản.
- Dùng tag theo nghiệp vụ thay vì chỉ theo phòng ban.
- Tạo FAQ và danh mục quy trình phổ biến.
- Cải thiện search keyword và filter.

Các bước quản trị dữ liệu này là điều kiện bắt buộc; semantic search không thể sửa tài liệu sai, thiếu hoặc không có owner.

## AI hypothesis

- Dùng embedding/semantic retrieval để hiểu câu hỏi theo nghĩa thay vì yêu cầu đúng tên tài liệu.
- Có thể tạo câu trả lời ngắn từ nội dung truy xuất, nhưng bắt buộc kèm citation tới đoạn nguồn.
- Khi viết quy trình mới, hệ thống chỉ gợi ý quy trình liên quan, template và các điểm có thể xung đột; người phụ trách vẫn chịu trách nhiệm nội dung cuối.
- Áp dụng access control trước retrieval và filter theo phiên bản hiệu lực.

## Quick gut

- [ ] No AI / process fix
- [ ] Rule
- [x] Workflow
- [ ] Agent
- [ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — 15–30+ phút/lần

[Có nhu cầu nghiệp vụ]
→ [Đoán phòng ban/tên quy trình: 2–5']
→ [Mở nhiều thư mục/portal: 3–5']
→ [Search keyword chính xác: 3–10']  <-- bottleneck
→ [Mở và đọc nhiều file: 5–10']
→ [Hỏi đồng nghiệp nếu chưa thấy: thời gian không xác định]
→ [Kiểm tra phiên bản]
→ [Áp dụng quy trình]

Failure:
Không tìm thấy, dùng file cũ hoặc bỏ qua một quy trình liên quan.
```

### Draft future workflow

```text
FUTURE STATE — mục tiêu dưới 3 phút

[Nhân viên mô tả nhu cầu bằng ngôn ngữ tự nhiên]
→ [Kiểm tra danh tính + quyền truy cập]
→ [Semantic retrieval trên tài liệu được phép xem]
→ [Trả Top 3 quy trình + đoạn liên quan + metadata]
→ [Người dùng mở nguồn và xác nhận]  <-- human boundary
→ ┌─ Đúng → [Áp dụng / lưu feedback]
  └─ Sai → [Đổi câu hỏi / filter / gửi yêu cầu cho document owner]

Khi cần viết quy trình mới:
[Nhập mục tiêu]
→ [Gợi ý template + quy trình liên quan]
→ [Người phụ trách soạn và phê duyệt]

Fallback:
Không có kết quả đủ tin cậy → không tự trả lời;
chuyển yêu cầu đến đúng phòng ban hoặc document owner.
```

## Vì sao bài toán này có impact

Đây là pain point có tần suất cao và ảnh hưởng nhiều phòng ban. Giá trị không chỉ nằm ở việc tìm nhanh hơn mà còn ở khả năng giảm dùng sai phiên bản, giảm gián đoạn mentor và làm rõ nguồn chịu trách nhiệm. AI chỉ phù hợp sau khi quyền truy cập, metadata và lifecycle tài liệu được quản trị tốt.

---

# Problem Card #3 — Thu thập bằng chứng khiếu nại hoàn hàng thủ công

## Problem 1 câu

Khi khách khiếu nại hoặc yêu cầu hoàn tiền, shop phải tự tìm và ghép bằng chứng từ nhiều nguồn để phản hồi nền tảng trong thời hạn ngắn, nên mất thời gian, dễ thiếu tài liệu và có nguy cơ thua khiếu nại dù shop có bằng chứng hợp lệ.

## Actor

- **Actor chính:** Chủ shop hoặc nhân viên vận hành đơn hàng.
- **Actor liên quan:** Khách hàng, đơn vị vận chuyển và bộ phận xử lý tranh chấp của nền tảng.

## Thời điểm / bối cảnh

- Khách chọn lý do như hàng giả, hàng không giống mô tả, sai màu, thiếu hàng hoặc chỉ hoàn tiền.
- Trạng thái hệ thống ghi “trả hàng thành công” nhưng shop chưa nhận được hàng.
- Nền tảng yêu cầu phản hồi trong một khoảng thời gian nhất định và có giới hạn ký tự hoặc định dạng bằng chứng.

## Current workflow

1. Nhận thông báo khiếu nại.
2. Đọc lý do và trạng thái đơn.
3. Tìm thông tin sản phẩm, đơn hàng và vận chuyển.
4. Tìm video đóng gói theo mã đơn.
5. Tìm tin nhắn thương lượng với khách hàng.
6. Xin hoặc tìm xác nhận từ đơn vị vận chuyển.
7. Tìm hóa đơn, phiếu kiểm định hoặc chính sách liên quan.
8. Chọn các ảnh/video phù hợp.
9. Viết mô tả theo giới hạn của nền tảng.
10. Gửi phản hồi và theo dõi kết quả.

## Bottleneck

**Bước 3–8: thu thập và kiểm tra bằng chứng nằm rải rác ở nhiều hệ thống và thư mục.**

- File có thể đặt tên không nhất quán.
- Nhân viên khó biết case này cần những loại bằng chứng nào.
- Có nguy cơ bỏ sót bằng chứng quan trọng hoặc gửi tài liệu không liên quan.
- Việc viết mô tả chỉ là bước cuối; pain lớn hơn nằm ở khâu chuẩn bị hồ sơ.
- Baseline ước tính: **20–45 phút/case**.

## Impact

- Tốn thời gian vận hành, đặc biệt khi có nhiều case cùng lúc.
- Dễ bỏ lỡ deadline phản hồi.
- Hồ sơ thiếu hoặc diễn đạt không rõ có thể làm shop mất doanh thu và hàng hóa.
- Nhân viên xử lý không nhất quán giữa các case.
- Khách hàng phải chờ lâu hơn để nhận phương án giải quyết.

## Success metric

- Giảm thời gian chuẩn bị hồ sơ từ **20–45 phút xuống dưới 10 phút/case**.
- Ít nhất **95% hồ sơ có đủ các bằng chứng bắt buộc theo checklist** trước khi submit.
- Giảm số case bị yêu cầu bổ sung bằng chứng ít nhất 50%.
- Không gửi nhầm dữ liệu của đơn hàng khác.
- 100% nội dung khiếu nại phải được người phụ trách kiểm tra trước khi gửi.
- Tỷ lệ thắng khiếu nại chỉ là metric thứ cấp vì còn phụ thuộc chính sách và quyết định của nền tảng.

## Non-AI alternative

- Tạo checklist riêng theo từng nhóm lý do khiếu nại.
- Chuẩn hóa tên file theo mã đơn hàng.
- Tạo folder tự động ngay khi đơn được đóng gói.
- Lưu video, ảnh, xác nhận vận chuyển và chat theo cùng một order ID.
- Dùng các mẫu câu phản hồi theo giới hạn ký tự của từng nền tảng.
- Cài cảnh báo deadline.

Các bước này có thể giải quyết phần lớn vấn đề dữ liệu phân tán mà chưa cần AI.

## AI hypothesis

- Phân loại lý do khiếu nại vào nhóm case.
- Đọc thông tin case và kiểm tra checklist bằng chứng.
- Tóm tắt sự kiện theo timeline.
- Gợi ý bằng chứng nào còn thiếu.
- Draft mô tả ngắn theo giới hạn ký tự và giữ giọng điệu trung lập.
- Không tự submit, không tự làm giả bằng chứng và không khẳng định điều không có trong hồ sơ.

## Quick gut

- [ ] No AI / process fix
- [ ] Rule
- [x] Workflow
- [ ] Agent
- [ ] Chưa biết

### Draft current workflow

```text
CURRENT STATE — 20–45 phút/case

[Nhận thông báo khiếu nại]
→ [Đọc lý do + deadline: 2–5']
→ [Tìm thông tin đơn: 3–5']
→ [Tìm video/ảnh đóng gói: 5–15']  <-- bottleneck
→ [Tìm chat + xác nhận vận chuyển: 5–10']
→ [Tìm giấy tờ/chính sách: 3–10']
→ [Chọn bằng chứng]
→ [Viết mô tả: 5–10']
→ [Submit]
→ [Theo dõi kết quả]

Failure:
Thiếu bằng chứng, nhầm file, quá deadline hoặc mô tả không khớp hồ sơ.
```

### Draft future workflow

```text
FUTURE STATE — mục tiêu dưới 10 phút/case

[Nhận khiếu nại]
→ [Tạo case theo order ID]
→ [Rule kéo thông tin đơn + deadline]
→ [Hệ thống tập hợp file có cùng order ID]
→ [AI phân loại case + kiểm checklist]
→ [Hiển thị timeline, bằng chứng có/thiếu]
→ [AI draft mô tả theo dữ liệu thật]
→ [Nhân viên kiểm chứng và chọn file]  <-- human boundary
→ [Nhân viên submit]
→ [Lưu kết quả để cải thiện checklist]

Fallback:
Không tìm được file hoặc dữ liệu mâu thuẫn → dừng draft,
yêu cầu nhân viên kiểm tra thủ công; không tự suy diễn.
```

## Vì sao bài toán này có impact

Bài toán có workflow rõ, xuất hiện lặp lại và có deadline cụ thể. Tuy nhiên, giải pháp tốt không nên bắt đầu bằng một agent tự khiếu nại. Nền tảng dữ liệu theo order ID, checklist và template cần được làm trước; AI chỉ nên hỗ trợ phân loại, kiểm tra thiếu sót và soạn bản nháp có căn cứ.

---

# So sánh nhanh ba Problem Cards

| Tiêu chí | Tổng đài ngân hàng | Tìm quy trình nội bộ | Khiếu nại hoàn hàng |
|---|---:|---:|---:|
| Actor rõ | 5/5 | 5/5 | 5/5 |
| Workflow hiện tại rõ | 5/5 | 5/5 | 5/5 |
| Bottleneck cụ thể | 5/5 | 5/5 | 5/5 |
| Impact đo được | 4/5 | 4/5 | 4/5 |
| Có thể pilot nhỏ | 3/5 | 5/5 | 5/5 |
| Data dễ tiếp cận | 2/5 | 4/5 | 4/5 |
| Rủi ro nếu AI sai | Cao | Trung bình | Trung bình |
| Non-AI alternative rõ | Có | Có | Có |
| Quick gut | Workflow | Workflow | Workflow |
| Tổng | **29/40** | **33/40** | **33/40** |

## Card tôi muốn pitch nhất

**Problem Card #2 — CBNV khó tìm quy trình nội bộ.**

## Vì sao chọn để pitch

- Có thể tiếp cận dữ liệu tài liệu nội bộ dễ hơn dữ liệu vận hành tổng đài ngân hàng.
- Workflow và intervention point rõ: sau khi người dùng nhập nhu cầu, trước khi họ phải tự mở nhiều thư mục và file.
- Có thể làm pilot nhỏ với một phòng ban, một tập tài liệu và một nhóm người dùng.
- Có thể đo thời gian tìm kiếm, Top-3 relevance, tỷ lệ hỏi lại và feedback của người dùng.
- Có non-AI foundation rõ: chuẩn hóa metadata, quyền truy cập, version và document owner.
- Không cần agent tự trị; một workflow semantic search/RAG có citation và human verification là scope hợp lý hơn.

## Câu hỏi tôi muốn nhóm challenge

1. Pain chính là search kém hay dữ liệu/taxonomy đang được quản trị kém?
2. Người dùng hiện mất bao lâu để tìm một quy trình và số lượt tìm mỗi ngày là bao nhiêu?
3. Làm sao xác định tài liệu nào còn hiệu lực và ai chịu trách nhiệm cập nhật?
4. Những tài liệu nào người dùng không được phép tìm thấy?
5. Top-3 relevance bao nhiêu là đủ để pilot được coi là thành công?
6. Khi không có nguồn đủ tin cậy, hệ thống nên fallback sang ai hoặc quy trình nào?
7. Một portal tập trung và search keyword tốt hơn có đủ giải quyết trước khi dùng AI không?

---

# Kết luận cá nhân

Sau khi scan và phản biện, tôi nhận thấy cả ba bài toán top đầu đều không nên bắt đầu bằng một “AI Agent tự làm tất cả”.

- Với tổng đài ngân hàng, cải tiến quan trọng nhất là virtual queue, callback, triage và giữ context.
- Với tìm quy trình nội bộ, cần data governance và access control trước khi dùng semantic search/RAG.
- Với khiếu nại hoàn hàng, cần chuẩn hóa dữ liệu theo order ID, checklist và template trước khi dùng AI draft.

Vì vậy, mức phù hợp ban đầu của cả ba là **Workflow**: kết hợp rule ở các bước xác định, AI ở bước đọc/hiểu/tóm tắt ngôn ngữ và người thật ở điểm phê duyệt hoặc xử lý nghiệp vụ có rủi ro.
