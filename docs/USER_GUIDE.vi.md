# Hướng dẫn sử dụng Thesis Research Workflow (ứng viên công khai)

[README](../README.md) · [Danh mục chức năng](FEATURES.md) · [Tính di động và bảo mật](PORTABILITY.md) · [Trạng thái phát hành](RELEASE_STATUS.md)

**Lưu ý:** Repository là **PUBLIC DOCS PREVIEW**, chỉ có tài liệu và dữ liệu giả lập, **không có ZIP Skill Suite có thể cài độc lập**. RC6 đã được đối chiếu với bản cài, nhưng vẫn thiếu quyền phân phối, kiểm định an toàn và canary tài khoản mới.

## 1. Triết lý sử dụng

Hệ quản lý một luận án theo câu hỏi nghiên cứu, luận điểm, nguồn chứng cứ, kết quả khoa học, mâu thuẫn và quyết định được người nghiên cứu duyệt. Nó không chỉ là công cụ viết nội dung; nó giúp tránh việc AI lấy một đoạn hội thoại cũ hoặc một tài liệu chưa xác minh làm chân lý học thuật.

Mỗi lần chỉ có **một parent cursor** cho toàn luận án. Task chuyên môn có thể chạy riêng, nhưng chỉ parent `thesis-lifecycle-orchestrator` sở hữu quyết định nghiên cứu cấp luận án và vòng Research Round. Agent không thể tự phê duyệt Knowledge Delta.

## 2. Chuẩn bị đầu vào

Cần tài liệu nguồn thuộc quyền sử dụng của tác giả, ví dụ đề cương, mục lục, bài báo đã công bố, ghi chú phương pháp, dữ liệu thử nghiệm được phép xử lý và quy định trình bày.

Không đưa thông tin nhận dạng cá nhân, thư từ nội bộ, mật khẩu, dữ liệu bench chưa được phép công bố hoặc toàn bộ bản thảo luận án vào một repo GitHub công khai. Với AI cloud, hãy cân nhắc riêng quyền gửi dữ liệu đến nhà cung cấp.

Dùng Context Bootstrap để chuẩn hóa:

```text
00-THESIS-INTAKE-MASTER.md
01-TOC-MAP.md
02-CONTRIBUTION-AND-EVIDENCE.md
03-MODEL-METHOD-DATA-PACK.md
04-WRITING-POLICY.md
05-CONTEXT-GAP-ASSESSMENT.md
```

Năm file đầu là nền tảng context; file thứ sáu liệt kê thiếu hụt cần làm rõ. Sau đó binding `thesis-context-profile/1.0` xác định luận án, hồ sơ ngôn ngữ và miền khoa học. Không mặc định luận án luôn có bốn chương, dùng tiếng Việt/Nga hoặc dùng một mô hình cụ thể.

## 3. Khởi động một Research Round

Ví dụ nghiên cứu **giả lập hoàn toàn**, không phải kết quả khoa học:

> “Đây là Context Pack đã duyệt của một nghiên cứu đồ chơi về độ bền vật liệu với dữ liệu giả lập. Hãy tạo intake cho câu hỏi liệu hai phương pháp nội suy cho kết quả khác nhau có ý nghĩa không. Chỉ dùng số liệu tổng hợp. Tách rõ giả thuyết, bằng chứng, phản chứng, điều chưa biết.”

Thesis Lifecycle parent nên sinh `research-intake/1.0`, đối chiếu với câu hỏi/gap có sẵn, sau đó định hướng `research-round-charter/1.0` với mục tiêu, giới hạn, tiêu chí đủ/chưa đủ bằng chứng và task nhỏ.

Yêu cầu “tiếp tục” không có nghĩa tự nâng quyền, thay câu hỏi khoa học hoặc duyệt một kết quả.

## 4. Giao việc có giới hạn

Parent phát `thesis-task-execution/1.0` cho một việc cụ thể: tìm tài liệu, audit nguồn, so sánh kết quả, kiểm chứng bằng chứng, viết một đoạn đã đóng băng nguồn, hoặc chuyển ngữ được phép.

Mỗi task phải ghi định danh luận án/round/task, đầu vào được phép, trạng thái chứng cứ, giới hạn thao tác, tiêu chí nghiệm thu và điểm dừng.

Task Controller và chuyên gia trả `thesis-task-return/1.0`: COMPLETE, PARTIAL, BLOCKED hoặc FAILED cùng bằng chứng, gap và next action. **COMPLETE của một task không đóng Research Round.** Khi bằng chứng chưa đủ, không suy diễn hoặc “điền cho tròn”.

## 5. Tìm và kiểm toán tài liệu

Quy trình nguồn thông thường:

1. Tạo bộ truy vấn và danh sách nguồn theo chương/phạm vi bằng Literature Search.
2. Ghi nguồn gốc, metadata, URL/DOI, phiên bản, trạng thái truy cập và khoảng trống.
3. Dùng Source Audit để soát nguồn trước khi viết; nguồn “có liên quan” chưa chắc hỗ trợ một luận điểm.
4. Sau quyết định audit được chấp nhận, dùng Reference Library Manager duy trì B-ID ổn định (như `B0001`), phiên bản và liên kết claim → source.
5. Chỉ sau khi bộ nguồn của chương được đóng băng và khóa bằng chứng mới dùng Batch Writer soạn các đoạn có giới hạn.

Không sao chép nội dung có bản quyền vào kho chia sẻ, không dùng tài liệu đã rút lại làm bằng chứng hợp lệ, không tạo trích dẫn giả.

## 6. Kiểm tra bất thường kết quả khoa học

Nếu mô hình hoặc thử nghiệm cho kết quả khác kỳ vọng:

> “Khóa baseline, so sánh trường hợp PASS/FAIL, kiểm tra provenance của file nguồn, solver/phiên bản công cụ, đơn vị, cấu hình và điều kiện đầu. Chỉ điều tra read-only, đưa ra các giả thuyết có thể bác bỏ và thí nghiệm tối thiểu để phân biệt.”

Scientific Debug tách **chẩn đoán** khỏi **sửa**. Không được sửa golden model hoặc dữ liệu thô trong giai đoạn xác định nguyên nhân. Chỉ khi có căn cứ `ROOT_CAUSE_LOCKED` và một phạm vi sửa độc lập đã được cho phép mới có thể giao nhiệm vụ repair riêng.

## 7. Tổng hợp Round và duyệt của tác giả

Sau khi task trả kết quả, parent xây `research-round-synthesis/1.0` và ứng viên `knowledge-delta/1.0`. Tác giả quyết định APPROVE / PATCH / CONTINUE / REJECT dựa vào đúng bản synthesis.

APPROVE chỉ nâng những thay đổi khoa học được duyệt, sau đó tính tác động đến luận điểm, chương, công thức, kết quả, nguồn và các bản export. Những phần bị ảnh hưởng cần gắn STALE hoặc RECHECK_REQUIRED trước khi tiếp tục phát hành.

## 8. Viết, dịch và xuất bản thảo

- Batch Writer dùng Context Freeze Pack theo chương/phần nhỏ, giữ khóa luận điểm, phiên bản nguồn, thuật ngữ, công thức và giới hạn mạnh/yếu của bằng chứng.
- Math/Word Export đọc Language Profile đã duyệt, giữ nghĩa khoa học trong chuyển ngữ; không tự thêm kết quả mới khi đã khóa nội dung.
- PASS kiểm tra hình thức không chứng minh lập luận khoa học đúng. Bản Word/PDF chỉ nên coi là sẵn sàng nộp khi cả tiêu chí khoa học, bằng chứng và trình bày đạt.

## 9. Khi đổi chat/máy hoặc mất ngữ cảnh

Khởi động lại từ canonical repository và continuation state, không dựa hoàn toàn vào trí nhớ cuộc trò chuyện. Repo-local-memory chỉ định vị trạng thái, task, nguồn và checkpoint; sự thật khoa học vẫn nằm ở kết quả/nguồn chuẩn cùng quyết định của tác giả.

## 10. Checklist trước phát hành bộ Skill

- [ ] Tách toàn bộ tài liệu luận án và dữ liệu cá nhân khỏi Skill công khai.
- [ ] Xác minh quyền/license của từng Skill và phụ thuộc.
- [ ] Có bản mô tả tính năng, cài đặt, ví dụ, schema và phiên bản rõ.
- [ ] Đóng gói và kiểm tra cấu trúc từng Skill.
- [ ] Thử trên tài khoản mới với dữ liệu nghiên cứu tổng hợp.
- [ ] Kiểm chứng các Gate, Human approval, Round synthesis, nguồn sai và Scientific Debug không sửa trái phép.
- [ ] Kiểm tra lịch sử Git mới sạch và các path staging/private không public.

Đây là **hướng dẫn quy trình hiện tại**, không phải giấy chứng nhận tính đúng đắn học thuật hay bằng chứng đã cài đặt được từ repo nháp.
