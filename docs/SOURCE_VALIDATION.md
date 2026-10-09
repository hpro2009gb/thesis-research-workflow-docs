# Nguồn tham chiếu và mức kiểm chứng — Thesis Suite

[README](../README.md) · [Danh mục thành phần](MEMBER_INVENTORY.md) · [Trạng thái phát hành](RELEASE_STATUS.md)

## Baseline được đối chiếu

- **Suite tham chiếu:** `thesis-research-writing-suite-v1.0.0-rc.6.zip`.
- **Định danh phiên bản:** `thesis-research-writing-suite / 1.0.0-rc.6`.
- **SHA-256 archive:** `6063d0f3d242a26dff1a55bbac57d490405de95b3e9e245d3c926f40c4cb2774`.
- **Dung lượng archive:** 1.201.405 byte.
- **Thành phần:** 10 gói Skill, bố trí theo `01-upgraded-skills` và `02-other-skills`.
- **Rollback nội bộ:** chứa bản tham chiếu RC4. RC5 từng không được chọn vì đóng gói đè shared-memory Skills.

## Kết quả kiểm tra nguồn, ngày 09/10/2026

| Phép kiểm tra | Kết quả | Ý nghĩa giới hạn |
|---|---|---|
| Đọc archive RC6 | PASS; ZIP không báo thành phần hỏng | Chỉ kiểm tra tính toàn vẹn archive |
| Cấu trúc 10 Skill thành viên | PASS; từng ZIP đọc được `SKILL.md` và `agents/openai.yaml` | Chưa chứng minh hành vi đúng |
| So sánh với bản đang cài | 10/10 thành viên khớp toàn bộ file | Có thể dùng RC6 làm baseline chính xác |
| Hai shared dependency `repo-local-memory-gate`, `repo-session-memory` | Bản đã cài khớp file với tham chiếu pin từ rc16 | Không khẳng định mọi môi trường đều tương thích |
| Canary ngữ nghĩa trên tài khoản mới | NOT RUN theo báo cáo RC6 | Không có bằng chứng độc lập về workflow hoạt động E2E |
| Quét bảo mật/phân phối của bản Skill công khai | CHƯA PASS | Một số reference/fixture mang ngữ cảnh nghiên cứu cụ thể |
| Licence cho từng gói | CHƯA XÁC MINH | Không được suy ra quyền phân phối chỉ từ sự tồn tại của ZIP |

## Tại sao không đăng trực tiếp RC6?

RC6 là baseline có giá trị kỹ thuật, nhưng không phải bản phân phối công khai đã được làm sạch. Trong một số phần còn có profile ngôn ngữ/chuyên ngành riêng, ví dụ kiểm thử và reference gắn với trường hợp nghiên cứu. Gói không kèm quyết định giấy phép đầy đủ. Việc giữ bản gốc ở môi trường riêng bảo toàn dữ liệu và không tạo tuyên bố sai về khả năng tự cài đặt.

**Repository này chỉ công khai tài liệu mô tả workflow và bộ ví dụ hoàn toàn tổng hợp.** Không kèm archive RC6, tài khoản học thuật, luận án hay kết quả khoa học của người nghiên cứu.

## Bước còn thiếu trước bản Skill Suite public

Phân loại source/fixture có tính riêng tư → xác định quyền phân phối → làm sạch từng Skill trên bản sao → đảm bảo đúng dependency closure → đóng gói với hash → kiểm thử cấu trúc và hành vi phủ Gate/authority → canary trên phiên ChatGPT mới với Context Pack tổng hợp → duyệt chính xác artifact phát hành.

**Release posture:** `PUBLIC_DOCS_PREVIEW` cho tài liệu, `BLOCKED` cho việc tuyên bố bộ Skill Suite đã sẵn sàng phát hành.

## Isolated local test evidence (2026-10-09)

- Python UTF-8 Skill validator: PASS for all 10/10 RC6 member source copies.
- Thesis contract regression: 10 unit tests PASS.
- VNext contract test script: PASS, including negative authority, evidence and read-only Scientific Debug conditions.
- Reference Library test script: PASS, including version mismatch and stale-change cases.
- Test target: isolated local RC6 source copies, not a new sanitized or published Skill ZIP.
- These tests do not replace a recipient-account end-to-end canary or rights/privacy verification.

## Sanitized Skill candidate verification — 9 October 2026

The ten-Skill **public-portfolio candidate** was assembled **privately** from the immutable RC6 source. This is engineering evidence, **not** a public Skill release or evidence of fresh-account runtime success.

- Ten individual Skill ZIPs passed structural packaging, archive integrity and source-to-ZIP byte comparison.
- Exactly 205 candidate files are accounted for in those ZIPs. All 103 detected Skill entrypoint links to local references/scripts exist.
- Generic source review replaced research-instance identifiers, a private notation profile and dissertation-specific example fixtures with fictional or context-profile-driven material.
- The configured pattern scan reported no remaining matches for the specified identity, private-path or project-domain signatures. Pattern scans are not a guarantee of zero sensitive or copyrighted content.
- Contract test suite: 10/10 PASS; VNext contract negatives and Reference Library tests also PASS.
- Two shared-memory dependencies are external to these ten ZIPs: repo-local-memory-gate and repo-session-memory. Their recipient-account availability and licensing are not established.
- Redistribution licence, ownership and third-party content rights remain unapproved. Independent fresh-account canary and full multi-Skill authority verification have not run.

**Status remains PUBLIC_DOCS_PREVIEW for this repository and SKILL_SUITE_BLOCKED for distributing installable files.** No ZIP from the sanitized candidate or original RC6 is published here.
