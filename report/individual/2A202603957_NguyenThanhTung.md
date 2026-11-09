# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Nguyễn Thanh Tùng
- MSSV: 2A202603957
- Tên nhóm: VietnamAirline
- Link repo nhóm:

---

## 2. Scan problem (CP1)

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | **Lặp lại** | Khi khởi tạo một dự án hoặc tính năng mới trên Jira, tôi muốn tự động sinh ra sẵn bộ sub-task chuẩn, để không phải tạo thủ công từng task cho mỗi đầu việc lặp lại | PM | Tạo thủ công hàng loạt sub-task (15-20 phút/lần) |
| 2 | **Tốn thời gian** | Khi cần làm báo cáo tiến độ dự án hằng tuần cho CEO, tôi muốn các biểu đồ từ Power BI và số liệu Jira gom chung 1 chỗ, để không phải mở luân phiên nhiều tab, chụp màn hình và căn chỉnh lại slide | PM | Tổng hợp và formatting thủ công (45 phút/lần) |
| 3 | **Pain từ người khác** | Khi các bạn Dev chuẩn bị bắt đầu sprint mới, tôi muốn các ticket có sẵn Acceptance Criteria rõ ràng từ BA/PO, để không phải liên tục ping PM hỏi lại yêu cầu | Dev, PM, BA/PO | Làm rõ yêu cầu chưa chuẩn chỉnh (3-5 lần hỏi/sprint) |
| 4 | **Đọc tổng hợp** | Khi có quá nhiều task cùng hạn, tôi muốn biết nên làm việc nào trước, để không trễ việc quan trọng | PM, team | Gần như task nào cũng ưu tiên, đã xảy ra trễ 3 task |
| 5 | **Lặp lại** | Khi cập nhật báo cáo plan hàng tuần, tôi muốn có sẵn các thông tin về sản phẩm như thời gian hoàn thành 1 sản phẩm, số người cần..., để không phải copy tay từ Power BI | PM | Mỗi tuần 2 lần, mất khoảng 40 phút/lần|

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- AI gợi ý bỏ ý 1 vì do có nhiều công cụ hỗ trợ tính năng đó.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | **Pain từ người khác** Sinh Acceptance Criteria rõ ràng cho Dev trước Sprint | Động tới nỗi đau thật của nhiều vai trò (Dev, PM, BA/PO), tần suất lặp lại theo mỗi sprint và có thể ứng dụng AI/Agent để hỗ trợ tự động hóa việc rà soát/sinh tiêu chí nghiệm thu | Chưa chắc context đầu vào từ PM/BA có đủ sâu để AI sinh AC chuẩn nghiệp vụ SaaS mà không bị ảo giác |
| 2 | **Tốn thời gian** Gom biểu đồ Power BI và số liệu Jira làm báo cáo tuần cho CEO | Thời gian nghẽn lớn nhất trong 3 bài toán (45 phút/lần), xảy ra định kỳ hằng tuần và tác động trực tiếp tới giao tiếp với C-level | Chưa chắc CEO chỉ cần nhìn dashboard chung hay vẫn bắt buộc phải có văn bản nhận định (narrative) đi kèm |
| 3 | **Lặp lại*** Tự động sinh bộ sub-task chuẩn khi tạo dự án/tính năng mới trên Jira | Tác động trực tiếp đến công việc thao tác lặp lại của PM, dễ định hình workflow giải quyết ngay | Chưa chắc giải pháp Rule đơn giản (Jira Automation có sẵn) đã đủ để thay thế việc PM phải rà soát và assign thủ công từng task |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi khởi tạo một dự án hoặc tính năng mới trên Jira, tôi muốn tự động sinh ra sẵn bộ sub-task chuẩn, để không phải tạo thủ công từng task cho mỗi đầu việc lặp lại. |
| Actor | Product Manager (PM) |
| Thời điểm / bối cảnh | Đầu dự án mới hoặc khi bắt đầu triển khai một feature mới trong sprint planning. |
| Quy trình hiện tại (3–7 bước) | [1] Tạo Epic/Story chính trên Jira → [2] Mở danh mục template/checklist mẫu → [3] Tạo thủ công từng sub-task và gán thông tin → [4] Chỉnh sửa chi tiết nội dung và assign cho team. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước [3] Tạo thủ công hàng loạt sub-task (mất 15–20 phút/lần). |
| Impact (nếu không giải thì sao) | Lãng phí thời gian thao tác lặp lại của PM, dễ bỏ sót các đầu việc chuẩn (checklist) quan trọng trong quy trình triển khai. |
| Success metric (baseline → target) | Thời gian tạo bộ sub-task chuẩn: Baseline ~20 phút → Target ≤ 5 phút/lần. |
| Phương án không dùng AI | Sử dụng tính năng Jira Automation tích hợp sẵn (Rule Trigger: Khi Epic được tạo → Auto create issue/sub-tasks theo checklist cố định). |
| Giả thuyết về AI (nếu có) | AI phân tích mô tả Epic để tự động đề xuất và điều chỉnh danh sách sub-task linh hoạt theo ngữ cảnh kỹ thuật của từng tính năng. |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:
```text
[1 Tạo Epic/Story] 
→ [2 Mở template mẫu] 
→ [3 Tạo thủ công từng sub-task: 15-20'] ← BOTTLENECK 
→ [4 Review & assign: 5']
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story | Khi cần làm báo cáo tiến độ dự án hằng tuần cho các bên CEO, tôi muốn các biểu đồ từ Power BI và số liệu Jira gom chung 1 chỗ, để không phải mở luân phiên nhiều tab, chụp màn hình và căn chỉnh lại slide. |
| Actor | Product Manager (PM) |
| Thời điểm / bối cảnh | Chiều thứ Sáu hàng tuần hoặc trước buổi họp giao ban tiến độ với Ban giám đốc (CEO/C-level). |
| Quy trình hiện tại (3–7 bước) | [1] Mở Power BI lấy biểu đồ progress → [2] Mở Jira lấy số liệu task/sprint → [3] Chụp ảnh màn hình từng phần → [4] Cân chỉnh hình ảnh và số liệu vào slide PowerPoint/Excel → [5] Review và gửi báo cáo qua email/Slack. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước [3] & [4] Tổng hợp và formatting thủ công từ nhiều nguồn (mất ~45 phút/lần). |
| Impact (nếu không giải thì sao) | Mất thời gian vận hành hàng tuần, dễ dẫn đến sai sót khi chép tay/chụp số liệu cũ, báo cáo bị chậm trễ so với giờ họp. |
| Success metric (baseline → target) | Thời gian tổng hợp và làm báo cáo tuần: Baseline ~45 phút → Target < 10 phút/lần. |
| Phương án không dùng AI | Dùng nhúng iframe/connector tích hợp trực tiếp Power BI và Jira API vào chung một Looker Studio / Notion Dashboard để tự đồng bộ số liệu tự động (Rule/Integration). |
| Giả thuyết về AI (nếu có) | AI đọc dữ liệu biến động từ Power BI và Jira để tự động tạo phần tóm tắt nhận định (narrative highlight) về tiến độ và rủi ro chính trong tuần. |
| Cảm nhận nhanh | Rule |

Quy trình nháp hiện tại:

```text
[1 Mở Power BI: 5']
→ [2 Mở Jira lấy số: 5']
→ [3 Chụp màn hình: 10']
→ [4 Format slide: 25'] ← BOTTLENECK
→ [5 Review & gửi: 5']
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi các bạn lập trình viên chuẩn bị bắt đầu sprint mới, tôi muốn các ticket có sẵn Acceptance Criteria (AC) rõ ràng từ BA/PO, để không phải liên tục ping PM hỏi lại yêu cầu làm gián đoạn tập trung. |
| Actor | Dev, PM, BA/PO |
| Thời điểm / bối cảnh | Giai đoạn Refinement / Sprint Planning hoặc ngay khi ticket được giao cho Dev bắt đầu code. |
| Quy trình hiện tại (3–7 bước) | [1] Dev nhận ticket trên Jira → [2] Đọc phần mô tả yêu cầu sơ khai → [3] Phát hiện thiếu điều kiện nghiệm thu/gặp case mờ hờ → [4] Nhắn tin/ping PM trên Slack để hỏi làm rõ → [5] PM/BA trả lời và bổ sung lại mô tả. |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước [3] & [4] Đọc hiểu và làm rõ yêu cầu chưa chuẩn chỉnh (mất 3–5 lần ping hỏi lại/sprint). |
| Impact (nếu không giải thì sao) | Gián đoạn luồng làm việc (context switching) của cả Dev lẫn PM, dễ phát sinh bug ở khâu Test/QC do hiểu sai spec, kéo dài thời gian hoàn thành sprint. |
| Success metric (baseline → target) | Tần suất Dev phải ping hỏi lại PM về AC: Baseline 3–5 lần/sprint → Target 1–2 lần/sprint. |
| Phương án không dùng AI | Bắt buộc áp dụng DoD (Definition of Done) / Template chuẩn: Ticket không có mục AC đầy đủ theo tiêu chuẩn Given-When-Then sẽ không được kéo vào Sprint. |
| Giả thuyết về AI (nếu có) | AI đóng vai trò Agent tự động rà soát mô tả tính năng (PRD thô) để tự động sinh sẵn bộ draft Acceptance Criteria theo chuẩn Given-When-Then và cảnh báo các edge case còn thiếu. |
| Cảm nhận nhanh | Agent |

Quy trình nháp hiện tại:

```text
[1 Nhận ticket: 2']
→ [2 Đọc mô tả sơ khai: 5']
→ [3 Thắc mắc yêu cầu: 15']
→ [4 Ping hỏi PM: 3-5 lần/sprint] ← BOTTLENECK
→ [5 Cập nhật lại spec]
```

### Card muốn pitch nhất

- Card số: #2
- Vì sao: Đây là bài toán có thời gian nghẽn rõ ràng và lớn nhất hàng tuần (45 phút/lần). Việc tổng hợp thủ công từ Power BI và Jira sang slide không chỉ tốn thời gian mà còn dễ sai sót số liệu khi gửi lên cấp C-level. Bài toán này có thể giải quyết dứt điểm bằng phương pháp Rule/Integration kết hợp AI hỗ trợ sinh phần nhận định, mang lại hiệu quả trực quan và đo lường được ngay.
- Câu hỏi muốn nhóm phản biện: Nếu dữ liệu trên Power BI và Jira liên tục được cập nhật theo real-time, liệu báo cáo tự động có làm mất đi góc nhìn nhận định chủ quan, mang tính chiến lược mà CEO thường kỳ vọng từ một Product Manager hay không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Việc chụp màn hình và dán vào slide có thể mang tính thói quen cá nhân của C-level thay vì thực sự do thiếu dashboard chung | Đồng ý | Bổ sung thêm tiêu chí kiểm chứng trong kế hoạch pilot: Xác thực trực tiếp với CEO xem việc chuyển đổi sang dùng khung nhìn dashboard tích hợp trực tiếp có đáp ứng đủ nhu cầu thông tin hay họ vẫn yêu cầu file slide tĩnh. |
| Chưa tính đến rủi ro lệch múi giờ dữ liệu (data sync delay) giữa Jira và Power BI khi báo cáo gấp vào phút chót | Đồng ý | Thêm bước rà soát và đồng bộ dữ liệu chủ động vào quy trình tương lai trước thời điểm họp 30 phút để đảm bảo số liệu khớp hoàn toàn. |

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Tôi pitch card của tôi và cùng vote lựa chọn | Đóng góp 3 bài toán vào danh sách chung để nhóm lựa chọn |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: "Có yếu tố gì cải thiện hay khác biệt đối với tính năng trên Discord đang sử dụng?" | Có thể cải thiện ở hiểu ngữ nghĩa lỗi để tìm đúng thread và tóm tắt các tin nhắn thử–sai thành hướng dẫn ngắn gọn kèm link nguồn, giúp học viên không phải mở đọc từng thread rải rác trên Discord. |
| Nhận phản biện | Câu hỏi tôi nhận được: "Đây thuần túy là sự cố tích hợp dữ liệu và thiết kế dashboard kém, chỉ cần nhúng connector/embed link là xong chứ không cần quy trình phức tạp hay AI."| Tôi đã sửa gì: chỉ nên chỉ ứng dụng AI ở bước cuối để tự động viết bản nháp tóm tắt nhận định. |
| Gom cluster / cây OST | Tôi tổng hợp và cluster lại | Tôi nhận ra pattern chung và từ đó phân tích thêm về ý kiến nổi bật |
| Chọn candidate problem | Tôi bần luận với nhóm và vote| Theo problem lấy thông tin qua Discord|
| Kiểm chứng / research | Tôi đóng góp ý kiến và format survey và nhưng gì nên điền trong research | |
| Quy trình nhóm | Tôi cùng phân tích quy trình hiện tại và đề xuất hướng cảu thiện quy trình mói| Giảm thiểu các bước cần thủ công |
| Problem Statement | Đóng góp ý kiến và phân tích các vấn đề gốc | |
| Mức can thiệp AI | Phân tích kỹ về các mức độ can thiệp và xác định hướng đi | Nhóm thống nhất chọn mức Workflow |
| Quyết định | Bàn về quyết định Go với pilot nhỏ để giám sát | Nhóm quyết định hướng Go|

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Phản biện lại ý kiến | Làm rõ hơn problem đang nằm ở đâu | Ban đầu còn khá chung chưa cụ thể về các giải quyết | Phân tích lại problem và các yếu tố có thể làm phức tạp thêm |
| CP2 Problem Card | Hỗ trợ phân tích, cluster các nhóm | Giải thích các problem và hướng có thể tiếp cận | Hay bị nhầm các loại Problem | Review lại và đối chiếu |
| CP4 Research | Không dùng | | | |
| CP5 Quy trình | Không dùng | | | |
| CP5–6 Problem Statement | Không dùng | | | |
| CP6 Mức can thiệp / quyết định | Không dùng | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Tôi cảm thấy scope problem của các bạn phản ánh rõ nét góc nhìn chuyên môn, background và ưu tiên vận hành riêng của từng người và tôi hiểu sâu hơn cách nhận diện điểm nghẽn thực tế, đồng thời rút kinh nghiệm trong việc định hình lại scope bài toán của mình.
**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Đôi lúc nhóm có suy nghĩ luôn về Chatbot trước khi phân tích rõ problem, khi đó tôi hiểu chatbot và agent hiện nay khá phổ biến nên hành vi đi theo xu hướng hiện tại khá rõ, và khi đó cũng đã dần tập trung lại về problem và tiếp tục phân tích mở rộng khi solution đang khá mở nhạt, chung chung.
**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Ý kiến của tôi không thay đổi nhiều về việc sử dụng AI để giải quyết vấn đề làm báo cáo dashboard từ nhiều nguồn cho CEO, tuy nhiên có hiểu thêm về mức độ can thiệp của AI cho problem đó.
**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Kết quả kiểm chứng đó không quá bất ngờ vì problem đó mỗi thành viên đều trải nghiệm
**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Khó nhất khi phân tích xem thật sự bottle neck nằm ở đâu, từ đó còn có thể phân tích rõ hướng cải thiện
**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Nếu làm lại tôi sẽ kiểm soát hơn về dữ liệu đầu vào, và phản biện nhiều hơn về thực tế của học viên xem họ có chịu dùng bot thay vì ping thẳng cho coach hay không.
**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
Khởi đầu từ problem, điểm nghẽn là học viên mất ~15 phút mò mẫm đọc từng thread Discord cũ để tìm lại cách sửa lỗi lặp. Quy trình tương lai rút ngắn còn 3 bước: gom thread thô, AI tóm tắt hướng dẫn có dẫn nguồn, và học viên tự kiểm chứng áp dụng. Metric đo lường bằng việc hạ thời gian tìm xuống < 3 phút, số lần hỏi coach không tăng và tỷ lệ AI tóm tắt sai <= 30%. Về boundary, AI tuyệt đối không tự trả lời thay coach, không chạy lệnh hộ và bắt buộc phải kèm link thread gốc. Nhóm chọn mức can thiệp AI là Workflow để tránh ảo giác rộng như Agent. Cuối cùng, quyết định chọn Go để chạy pilot 2 tuần trên 1 lớp nhằm kiểm chứng thực tế.

---

## 7. Tài liệu tham khảo

-
