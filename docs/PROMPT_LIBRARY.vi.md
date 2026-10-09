# Thư viện 12 prompt sử dụng Thesis Research Workflow

[Trang chủ](../README.vi.md) · [Hướng dẫn](USER_GUIDE.vi.md) · [Ví dụ tổng hợp](../examples/synthetic-context/README.md)

**Lưu ý:** Đây là câu lệnh minh họa cho người đã cài bộ Thesis Skill phù hợp, không phải bằng chứng bản suite đã có thể tải/cài từ repository này. Hãy sử dụng dữ liệu do mình sở hữu hoặc dữ liệu tổng hợp. Không gửi luận án, dữ liệu thử nghiệm bảo mật hoặc thông tin nghiên cứu nhạy cảm lên kho công khai.

## Bắt đầu và điều phối

**1. Chuẩn hóa nguồn nghiên cứu**

> Dùng Thesis Context Bootstrap. Đây là bộ tài liệu được phép sử dụng của một dự án nghiên cứu giả lập. Tách sự kiện, kế hoạch, giả thuyết và nguồn bằng chứng. Tạo đủ 5 file context chuẩn và Gap Assessment, không viết nội dung chương.

**2. Resume sau khi đổi phiên**

> @Thesis Lifecycle Orchestrator — Kết nối đúng repo nghiên cứu và khôi phục continuation state, Research Round đang mở, task active, phê duyệt của tác giả và blocker. Đối chiếu từ file canonical; không suy ra quyết định từ ký ức chat.

**3. Báo cáo tiến độ**

> Từ Context Pack và continuation state đã xác minh, tổng hợp phần hoàn thành, claim có bằng chứng, công việc đang chạy, các gap/STALE, quyết định cần tác giả và ba ưu tiên hợp lệ tiếp theo. Không thay đổi state.

**4. Thêm một câu hỏi nghiên cứu**

> Intake câu hỏi sau: [câu hỏi]. Kiểm tra sự trùng lặp với Round hiện có, xác định giả thuyết và phản chứng, giới hạn phạm vi và đề xuất charter. Không mở rộng luận án chỉ vì câu hỏi mới.

## Nguồn và bằng chứng

**5. Lập Research Round**

> Dựa trên Context/Profile đã duyệt, đề xuất Research Round cho [gap], liệt kê từng task, điều kiện đủ bằng chứng, điều kiện dừng và phần tác giả phải phê duyệt. Không tự nâng evidence ceiling.

**6. Tìm tài liệu**

> Dùng Literature Search để xây taxonomy, truy vấn theo chương, candidate/source pack và gap register cho [phạm vi]. Phân biệt kết quả tìm thấy với tài liệu đã audit.

**7. Kiểm định nguồn**

> Dùng Source Audit kiểm tra phiên bản, DOI/URL, metadata, quyền truy cập, độ mạnh bằng chứng và mâu thuẫn của các nguồn trong pack. Trả patch đề xuất và human-review register; không tự duyệt.

**8. Liên kết claim với tài liệu**

> Dùng Reference Library Manager từ các audit đã được duyệt. Chuẩn hóa work ID, source version, exact locator và claim revision; xây chapter slice và báo STALE khi nguồn đổi. Không kết luận tài liệu hỗ trợ một claim nếu chưa có evidence audit.

## Viết, kiểm chứng và xuất bản

**9. Kiểm tra lỗi mô hình khoa học**

> Scientific Debug chế độ DIAGNOSE_ONLY. Đóng băng baseline, liệt kê khác biệt PASS/FAIL, phân loại failure layer, đưa ra các giả thuyết có thể bác bỏ và thí nghiệm phân biệt ít tác động nhất. Không sửa mô hình được chấp nhận.

**10. Viết một đoạn có giới hạn**

> Dùng Chapter Context Freeze Pack đã duyệt cho [mục]. Viết đúng claim ceiling, nguồn/phiên bản, gap, cấu trúc, thuật ngữ và công thức. Chỉ ra mệnh đề nào thiếu evidence; không tạo trích dẫn giả.

**11. Kiểm tra nhất quán liên chương**

> Kiểm tra đồng bộ câu hỏi nghiên cứu, đóng góp, thuật ngữ, công thức, kết quả và citation ID giữa các chương. Đưa ra danh sách lỗi và phần cần RECHECK, chưa tự sửa khóa nội dung đã duyệt.

**12. Dịch và chuẩn bị bản xuất**

> Dựa trên Language Profile, giữ semantic lock của bản đã duyệt; dịch [đoạn] sang ngôn ngữ đích, giữ công thức, thứ tự mục và nghĩa khoa học. Tạo bảng so sánh ký hiệu; chưa kết luận bản thảo sẵn sàng nộp chỉ vì xuất file thành công.

## Quy trình làm việc hằng ngày

Mở phiên bằng báo cáo trạng thái canonical → chọn một gap hoặc task hợp lệ → đọc evidence → giao việc có phạm vi → kiểm tra kết quả → yêu cầu Human Round Review khi cần → ghi lại quyết định → tạo checkpoint. Không tạo lại Research Round trùng và không để một task tự đóng toàn bộ vòng nghiên cứu.

**Trạng thái cần phân biệt:** `COMPLETE` của task chỉ chứng minh task trả kết quả; `APPROVE` của Human mới có thể cho phép Knowledge Delta đi vào canonical thesis state; `PRINT_READY` còn đòi hỏi điều kiện học thuật, bằng chứng và trình bày riêng.

Tất cả prompt ở trên là hướng dẫn sử dụng, không phải bằng chứng đầu ra đã được chạy hay nghiệm thu.
