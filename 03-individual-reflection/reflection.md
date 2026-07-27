 # Individual Reflection — Day 02

**Họ và tên:** Vũ Tú Quỳnh
**Mã học viên:** 2A202601239
**Chủ đề nhóm:** Trợ lý tuyển sinh AI cho Trường X

---

## 1. Tôi đã tham gia vào phần nào?

| Hảnh hưởng |
|---|---|---|
| Scan cá nhân | Tôi phân tích nhiều vấn đề từ công việc và trải nghiệm thực tế, nổi bật là tìm kiếm quy trình nội bộ, tổng đài ngân hàng quá tải và xử lý khiếu nại hoàn hàng. | Giúp tôi có nhiều candidate problem để so sánh thay vì bắt đầu ngay từ một giải pháp AI. |
| Pitch Problem Card | Tôi trình bày vấn đề khách hàng phải gọi lại tổng đài ngân hàng nhiều lần và vấn đề nhân viên khó tìm quy trình nội bộ. | Nhóm có thêm góc nhìn về bottleneck chờ đợi, tìm kiếm thông tin và các phương án không nhất thiết phải dùng AI. |
| Challenge bài của thành viên khác | Với ý tưởng trợ lý tuyển sinh, tôi tập trung đặt câu hỏi về nguồn dữ liệu chính thức, việc cập nhật thông tin theo từng năm, cách đo hiệu quả và trường hợp nào phải chuyển cho cán bộ. | Ý tưởng được thu hẹp từ một chatbot tư vấn tổng quát thành workflow trả lời từ nguồn đã được phê duyệt, có citation và human handoff. |
| Gom trùng / cluster | Tôi hỗ trợ nhóm các bài toán thành những nhóm như hỏi đáp thông tin, hỗ trợ người dùng quá tải, recommendation và tổng hợp báo cáo. | Giúp nhóm nhận ra nhiều ý tưởng có cùng pattern, từ đó so sánh candidate problem công bằng hơn. |
| Chọn candidate problem | Tôi cùng nhóm so sánh các vấn đề theo actor, workflow, impact, khả năng tiếp cận dữ liệu, mức rủi ro và khả năng pilot. | Nhóm chọn trợ lý tuyển sinh vì actor và workflow rõ, dữ liệu có thể giới hạn trong tài liệu chính thức và có thể thử nghiệm ở scope nhỏ. |
| Validation / research | Tôi hỗ trợ xác định những thông tin nào đang là giả định, tìm các mô hình chatbot tuyển sinh đã tồn tại và phân tích rủi ro khi tài liệu thay đổi hoặc AI trả lời không có nguồn. | Nhóm không sử dụng các con số chưa được kiểm chứng như dữ liệu thật và bổ sung yêu cầu đo baseline trước pilot. |
| Workflow nhóm | Tôi hỗ trợ phân tích current workflow và future workflow, xác định bottleneck ở bước người dùng chờ phản hồi và cán bộ phải tra cứu, viết lại câu trả lời. | AI được đặt vào một intervention point rõ ràng, không bao phủ toàn bộ quy trình. |
| Problem Statement | Tôi hỗ trợ làm rõ actor, bottleneck, impact, success metric, boundary và các giả định chưa được validate. | Problem Statement v1 cụ thể hơn v0 và có thể dùng để thiết kế pilot, thay vì chỉ mô tả chung chung rằng chatbot sẽ giúp trả lời nhanh hơn. |
| Rule / Workflow / Agent | Tôi phân tích rằng rule có thể dùng để kiểm tra scope và các trường hợp cố định, AI dùng cho semantic retrieval và diễn giải, còn cán bộ xử lý những trường hợp phức tạp. | Nhóm chọn mức Workflow thay vì Agent. |
| Decision | Tôi ủng hộ quyết định Go cho pilot nhỏ nhưng Not Yet cho production vì nhóm chưa có baseline, log thực tế và content owner của Trường X. | Quyết định cuối có điều kiện, quality gate, rollback và các trường hợp No-Go rõ ràng. |

---

## 2. Tôi đã sử dụng AI như thế nào?

| Phase                   | Tôi dùng AI để làm gì?                                                               | AI hữu ích ở đâu?                                                                                                                                | AI sai hoặc hời hợt ở đâu?                                                                                    | Tôi sửa gì bằng nhận định của mình?                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Scan                    | Tôi dùng AI để mở rộng các góc nhìn từ những vấn đề ban đầu của mình.                | AI giúp gợi ý thêm actor, dấu hiệu có thể đo và các vấn đề liên quan đến công việc, học tập, DevOps và vận hành.                                 | Một số gợi ý quá rộng, giống một ý tưởng sản phẩm hơn là một problem có workflow thật.                        | Tôi chỉ giữ những vấn đề gần với trải nghiệm của mình và có thể mô tả actor, bước làm hiện tại và bottleneck.     |
| Problem Card            | Tôi nhờ AI phản biện Problem Card và gợi ý current/future workflow.                  | AI giúp tôi nhìn rõ hơn sự khác nhau giữa pain, bottleneck, impact và solution.                                                                  | AI có xu hướng thêm nhiều chức năng vào future workflow và đôi khi biến giải pháp thành một trợ lý toàn năng. | Tôi thu hẹp phạm vi và giữ AI ở một số bước cụ thể, đồng thời bổ sung non-AI alternative.                         |
| Workflow                | Tôi dùng AI để cấu trúc lại workflow và chuyển thành bảng hoặc Mermaid.              | AI giúp trình bày các bước, handoff và fallback rõ ràng hơn.                                                                                     | Ban đầu AI gộp nhiều bước với nhau và chưa tách rõ đâu là rule, đâu là AI, đâu là người thật.                 | Tôi tách scope check, retrieval, answer generation, validation và human handoff thành các bước riêng.             |
| Research                | Tôi dùng AI và công cụ tìm kiếm để tìm các chatbot tuyển sinh và tài liệu liên quan. | AI giúp xác định nhanh các nhóm giải pháp đã tồn tại và các vấn đề cần research như citation, source freshness và content governance.            | Một số kết quả có claim về hiệu quả nhưng không có số liệu hoặc nguồn đủ mạnh.                                | Tôi không dùng các claim không kiểm chứng và chỉ xem các case đó là bằng chứng rằng pattern giải pháp đã tồn tại. |
| Problem Statement       | Tôi nhờ AI kiểm tra các field còn mơ hồ và đề xuất metric.                           | AI giúp nhận ra các cụm từ như “nhanh hơn”, “chính xác hơn” hoặc “giảm tải” chưa đủ để đo.                                                       | AI có thể đề xuất target như 70%, 95% hoặc dưới 15 giây dù chưa có baseline thật.                             | Tôi ghi rõ đây là target giả định cho pilot và yêu cầu đo log thực tế trước khi triển khai production.            |
| Rule / Workflow / Agent | Tôi dùng AI để lập bảng so sánh các mức giải pháp.                                   | AI giúp chỉ ra rule phù hợp với điều kiện cố định, workflow phù hợp với chuỗi bước rõ và agent chỉ cần khi AI phải tự quyết định bước tiếp theo. | AI đôi khi đề xuất agent quá sớm vì agent nghe có vẻ mạnh và hiện đại hơn.                                    | Tôi cùng nhóm chọn Workflow vì bài toán không yêu cầu AI tự lập kế hoạch hoặc tự thực hiện hành động tuyển sinh.  |
| Decision                | Tôi nhờ AI kiểm tra các rủi ro, quality gate và điều kiện rollback.                  | AI giúp mở rộng các rủi ro như hallucination, tài liệu hết hiệu lực, citation sai và lộ dữ liệu cá nhân.                                         | AI có thể viết quyết định rất thuyết phục dù nhóm chưa có validation với người dùng thật.                     | Tôi giữ quyết định ở mức Go cho pilot nhỏ, chưa Go production và ghi rõ những dữ liệu còn thiếu.                  |

---

## 3. Tôi học được gì khi nghe các vấn đề của thành viên khác?

Khi nghe các thành viên trình bày, tôi nhận thấy một vấn đề có impact lớn chưa chắc đã là vấn đề phù hợp nhất để làm trong lab. Ví dụ, hỗ trợ thông tin thuốc hoặc theo dõi dinh dưỡng bệnh nhân có ý nghĩa lớn nhưng hậu quả khi AI sai rất cao, cần chuyên gia và dữ liệu y tế được kiểm soát. Bài toán tổng đài ngân hàng cũng có pain rõ nhưng bottleneck chính có thể được giải bằng hàng đợi và callback, chưa chắc cần AI.

Ngược lại, trợ lý tuyển sinh có phạm vi dễ thu hẹp hơn. Nội dung trả lời phần lớn có thể lấy từ một tập tài liệu chính thức, actor và workflow rõ, đồng thời có thể pilot mà không cần cho AI quyền thực hiện hành động nhạy cảm.

Tôi học được rằng việc chọn bài toán không nên dựa vào việc ý tưởng nào nghe hấp dẫn nhất, mà phải dựa vào khả năng mô tả workflow, đo impact, tiếp cận dữ liệu và kiểm soát hậu quả khi AI sai.

---

## 4. Nhóm có lúc nào bị solution-first không?

Có. Khi nghe ý tưởng “Trợ lý tuyển sinh AI”, phản ứng ban đầu của nhóm là nghĩ ngay tới chatbot, RAG, cá nhân hóa và agent tư vấn.

Sau khi vẽ current workflow, nhóm nhận ra vấn đề thật không phải là “Trường X chưa có chatbot”. Vấn đề là học sinh và phụ huynh phải tự tìm nhiều nguồn hoặc chờ cán bộ, trong khi cán bộ phải tra cứu và trả lời lặp lại cùng một tập thông tin.

Việc quay lại actor, workflow và bottleneck giúp nhóm nhận ra rằng một số phần nên được giải bằng cách chuẩn hóa tài liệu, FAQ, rule và content governance. AI chỉ nên hỗ trợ hiểu cách hỏi, tìm đúng đoạn thông tin và diễn giải câu trả lời.

---

## 5. Tôi có thay đổi ý kiến sau khi bị challenge không?

Ban đầu tôi có xu hướng cho rằng một hệ thống AI có thể tự động trả lời phần lớn vấn đề nếu sử dụng RAG và tài liệu chính thức.

Sau khi phân tích kỹ hơn, tôi nhận ra RAG không tự bảo đảm câu trả lời đúng. Nếu retriever lấy nhầm tài liệu, trộn tài liệu của nhiều năm hoặc nguồn đã hết hiệu lực, LLM vẫn có thể tạo ra một câu trả lời hợp lý nhưng sai.

Vì vậy, tôi thay đổi quan điểm từ “chỉ cần xây chatbot RAG” thành “cần xây một workflow có quản trị nguồn, metadata, citation, kiểm tra confidence và human handoff”. Tôi cũng đồng ý rằng production chưa thể Go khi chưa có content owner và bộ dữ liệu evaluation.

---

## 6. Tôi đóng góp gì thật sự vào artifact cuối?

Đóng góp chính của tôi là hỗ trợ chuyển ý tưởng ban đầu thành một problem statement có cấu trúc và có thể đo:

* Xác định current workflow và bottleneck.
* Phân tích future workflow.
* Làm rõ intervention point của AI.
* Đề xuất metric gồm baseline, target và cách đo.
* Phân biệt phần có thể dùng rule, AI và phần bắt buộc phải có cán bộ.
* Bổ sung boundary, fallback, quality gate và rollback.
* Tổng hợp các nội dung thành file `group-report.md`.

Tôi cũng cố gắng không trình bày các con số giả định như dữ liệu thực tế. Những target trong report được ghi là mục tiêu pilot và cần được xác nhận bằng log hoặc phỏng vấn.

---

## 7. Điều khó nhất khi viết Problem Statement là gì?

Điều khó nhất là viết đủ cụ thể nhưng không biến Problem Statement thành mô tả giải pháp.

Ban đầu rất dễ viết theo hướng:

> Xây dựng chatbot AI giúp tư vấn tuyển sinh nhanh chóng và chính xác.

Câu này chưa nói rõ ai đang gặp vấn đề, họ làm gì hiện tại, bước nào bị nghẽn, hậu quả là gì và “nhanh, chính xác” được đo như thế nào.

Sau khi chỉnh sửa, Problem Statement cần thể hiện được mạch:

```text
Actor
→ Current workflow
→ Bottleneck
→ Impact
→ Baseline
→ Target
→ Boundary
→ AI intervention point
```

Tôi cũng nhận ra metric không chỉ cần target mà phải có baseline và cách thu thập dữ liệu. Nếu chưa có baseline thì phải ghi rõ là chưa có, thay vì tự tạo một con số có vẻ hợp lý.

---

## 8. Vì sao nhóm chọn Workflow thay vì Rule hoặc Agent?

Rule phù hợp với các câu hỏi cố định và các điều kiện rõ ràng, chẳng hạn kiểm tra câu hỏi có thuộc phạm vi tuyển sinh hay không, nhận diện thông tin cá nhân hoặc chuyển các từ khóa khẩn cấp cho cán bộ. Tuy nhiên, chỉ dùng rule sẽ khó xử lý nhiều cách diễn đạt và các câu hỏi kết hợp.

Workflow phù hợp hơn vì quy trình có các bước tương đối cố định:

```text
Nhận câu hỏi
→ Kiểm tra scope
→ Tìm trong nguồn chính thức
→ Tạo câu trả lời có citation
→ Kiểm tra độ tin cậy
→ Trả lời hoặc chuyển cán bộ
```

Agent chưa cần thiết vì AI không cần tự đặt mục tiêu, tự lập kế hoạch hoặc tự lựa chọn nhiều hành động. Cho agent quyền truy cập hồ sơ, thanh toán hoặc tự đưa ra quyết định tuyển sinh sẽ làm tăng rủi ro mà không giải quyết thêm bottleneck cốt lõi.

---

## 9. Tôi hiểu mạch problem → workflow → metric → boundary → AI fit như thế nào?

* **Problem:** Học sinh và phụ huynh khó nhận thông tin tuyển sinh nhanh và đáng tin cậy; cán bộ bị quá tải bởi câu hỏi lặp lại.
* **Workflow:** Người dùng tự tìm nhiều nguồn, gửi câu hỏi, chờ cán bộ; cán bộ đọc, tra cứu, trả lời và xử lý follow-up.
* **Bottleneck:** Thời gian chờ cán bộ và bước cán bộ phải tìm, viết lại thông tin đã tồn tại.
* **Metric:** Thời gian phản hồi, tỷ lệ self-service, factual accuracy, citation correctness, thời gian cán bộ xử lý và mức hài lòng.
* **Boundary:** AI chỉ trả lời từ nguồn được duyệt, không dự đoán đỗ, không phê duyệt hoặc nộp hồ sơ và phải chuyển người thật khi không chắc.
* **AI fit:** AI phù hợp ở bước hiểu ngôn ngữ, semantic retrieval và diễn giải; rule phù hợp với guardrail; con người phù hợp với case ngoại lệ và quyết định có hậu quả cao.
* **Decision:** Go cho pilot read-only, chưa Go production.

---

## 10. Nếu làm lại, tôi sẽ thay đổi gì?

Nếu làm lại, tôi sẽ dành nhiều thời gian hơn cho validation trước khi viết metric và thiết kế future workflow.

Cụ thể, tôi sẽ:

1. Phỏng vấn ít nhất một cán bộ tuyển sinh để xác định số lượng câu hỏi, thời gian xử lý và các nhóm câu hỏi phổ biến.
2. Hỏi một số học sinh hoặc phụ huynh về cách họ đang tìm thông tin và trường hợp nào khiến họ không tin kết quả tìm kiếm.
3. Thu thập một tập câu hỏi thật đã được ẩn thông tin cá nhân để xây evaluation set.
4. Xác định source of truth và content owner trước khi thiết kế RAG.
5. Challenge mạnh hơn về việc FAQ hoặc search thông thường có thể giải quyết bao nhiêu phần trăm vấn đề.
6. Không đặt target cố định trước khi đo baseline.
7. Chia rõ nhiệm vụ của từng thành viên từ đầu để tránh một người phải tổng hợp quá nhiều phần vào cuối buổi.

Bài học quan trọng nhất của tôi sau Day 02 là:

> Một sản phẩm AI tốt không bắt đầu từ việc chọn mô hình hoặc chọn Agent. Nó bắt đầu từ một vấn đề thật, một workflow có thể quan sát, một bottleneck cụ thể, metric đo được và boundary đủ rõ để kiểm soát khi AI sai.
