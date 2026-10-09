# Thesis Research Workflow — Điều phối nghiên cứu luận án dựa trên bằng chứng

[English](README.md) · [Tính năng](docs/FEATURES.md) · [Hướng dẫn](docs/USER_GUIDE.vi.md) · [12 prompt](docs/PROMPT_LIBRARY.vi.md) · [Ví dụ nghiên cứu giả lập](examples/synthetic-context/README.md) · [Kiểm chứng nguồn](docs/SOURCE_VALIDATION.md)

Đây là hệ quy trình ChatGPT Skills giúp người nghiên cứu tổ chức luận án từ Context Pack, câu hỏi khoa học, Research Round, tìm và kiểm toán tài liệu, kiểm chứng kết quả, viết, dịch và tổng hợp tri thức. Mỗi claim cần bằng chứng và phiên bản nguồn. **AI không được tự cấp phê duyệt khoa học thay tác giả.**

## Các lớp chức năng

1. **Context Bootstrap:** chuẩn hóa tài liệu tác giả thành năm file nền tảng và một Gap Assessment.
2. **Thesis Lifecycle Orchestrator:** kiểm soát toàn bộ Round, nhiệm vụ, đề xuất Knowledge Delta và quyết định của tác giả.
3. **Task Execution Controller:** thực hiện đúng một nhiệm vụ khoa học có giới hạn và trả kết quả.
4. **Literature Search + Source Audit:** tìm nguồn và đánh giá provenance/khả năng hỗ trợ luận điểm.
5. **Reference Library Manager:** ID tài liệu B-ID, phiên bản và liên kết nguồn - claim.
6. **Batch Writer, Math Export:** viết theo evidence freeze, kiểm tra thuật ngữ/công thức, dịch/chuẩn bị Word theo Language Profile.
7. **Scientific Debug:** điều tra sự bất thường bằng phương pháp so sánh và bác bỏ giả thuyết trước khi sửa.
8. **Contract & Memory:** kiểm định trạng thái, xác minh authority, khôi phục phiên làm việc nhưng không dùng memory làm chân lý khoa học.

## Trạng thái thực tế

Repo hiện ở trạng thái **PUBLIC DOCS PREVIEW**: chỉ công bố tài liệu và ví dụ giả lập. RC6 đã được đối chiếu với mười Skill đang cài, nhưng **chưa phát hành bộ Skill có thể cài độc lập** vì vẫn phải kiểm toán quyền phân phối, an toàn dữ liệu và canary.

Xem [hướng dẫn tiếng Việt](docs/USER_GUIDE.vi.md) để hiểu từng bước, điểm Human Review và yêu cầu an toàn trước khi công bố.

**HungLab** · https://hunglab.xyz · founder@hunglab.xyz
