# 02 — Group Problem Statement

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm |
|---:|---|---|---|
| 1 | Phạm Xuân Phong | 2A202602027 | Thành viên |
| 2 | Bùi Hoàng Vương | 2A202601553 | Trưởng nhóm |
| 3 | Đặng Tiến Thành | 2A202601305 | Thành viên |
| 4 | Ngô Thành Đạt | 2A202601323 | Thành viên |
| 5 | Nguyễn Chí Quang | 2A202601932 | Thành viên |
| 6 | Nguyễn Lê Minh | 2A202601047 | Thành viên |

## Group convergence

Qua thảo luận, nhóm gom các candidate thành những nhóm có workflow và bottleneck
tương tự.

| Cluster | Candidate examples | Pattern chung |
|---|---|---|
| Đối chiếu hồ sơ | CV, hồ sơ tín dụng | Kiểm tra tài liệu theo một bộ tiêu chí |
| Tổng hợp thông tin | Báo cáo tiến độ, patient brief, bản ghi họp | Ghép thông tin dài hoặc phân tán |
| Phân loại, tổng hợp và ưu tiên | Gán nhãn ảnh, complaint khách hàng, phân tích comment bán hàng | Gắn nhãn, gom nhóm và xác định nội dung cần xử lý |
| Hỗ trợ hiểu nội dung | Lỗ hổng kiến thức, slide, phiếu xét nghiệm | Chuyển thông tin khó thành nội dung dễ hiểu |
| Phân mảnh công cụ | Email, chatbot, coding agent | Phải chuyển nhiều công cụ hoặc làm lại |

## Shortlist và score

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Phân tích comment bán hàng | 4 | 5 | 2 | 3 | 5 | 5 | 4 | 28 |
| Đối chiếu CV với JD | 5 | 5 | 3 | 4 | 3 | 4 | 3 | 27 |
| Tổng hợp báo cáo tiến độ | 4 | 4 | 2 | 3 | 5 | 5 | 3 | 26 |

Nhóm chọn: **Phân tích comment bán hàng**.

Vì sao chọn:

- Actor và workflow tương đối rõ.
- Có thể giới hạn trong một file comment của một bài đăng hoặc chiến dịch.
- Output có thể kiểm tra bằng comment gốc.
- Có thể so sánh No AI, Rule, Workflow và Agent.

Vì sao không chọn các bài khác:

- Đối chiếu CV với JD: liên quan dữ liệu cá nhân và nguy cơ thiên lệch.
- Tổng hợp báo cáo tiến độ: chưa rõ nguồn dữ liệu, tần suất và baseline.

## Quick validation

Nhóm chưa phỏng vấn trực tiếp người vận hành shop và chưa có file comment thật
được phép sử dụng. Vì vậy, pain và impact hiện vẫn là giả thuyết cần kiểm chứng.

| Nguồn | Số người / mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Quick interview | Chưa thực hiện | Chưa có | Chưa có bằng chứng trực tiếp từ actor | Chưa kết luận pain đã được xác nhận |
| Tập comment thật | Chưa có | Chưa có | Chưa đo được thời gian và chất lượng | Chưa sử dụng baseline ước đoán |

Validation cần thực hiện:

- Hỏi 2–3 người vận hành shop về lần gần nhất họ phải tổng hợp comment.
- Ghi lại workflow, bước mất công nhất và thời gian xử lý.
- Kiểm tra công cụ họ đang dùng và phần công cụ đó chưa giải quyết.
- Lấy một file comment công khai được phép sử dụng; pilot dự kiến đánh giá tối
  thiểu 50 comment.

Insight hiện tại:

```text
Việc người vận hành shop còn đau ở bước phân loại và tổng hợp comment mới là giả
thuyết của nhóm, chưa phải kết luận đã được validation xác nhận.
```

## Research giải pháp

Nhóm tìm các công cụ đang giải quyết những phần gần với workflow này.

| Nguồn / tool | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Meta Business Suite Inbox | [Tài liệu](https://www.facebook.com/help/messenger-app/294426838452244) | Gom, tìm, lọc, đánh dấu và trả lời comment Facebook/Instagram | Có sẵn trong hệ sinh thái Meta | Tài liệu chưa mô tả tự tổng hợp nhóm nội dung kèm comment dẫn chứng | Không coi thu thập comment là bottleneck chính |
| Harasocial | [Tài liệu](https://www.haravan.com/pages/phan-mem-quan-ly-chat-da-kenh-harasocial) | Gom hội thoại, gắn nhãn từ khóa, chatbot và hỗ trợ bán hàng | Workflow gần với shop tại Việt Nam | Thông tin từ nhà cung cấp; nhóm chưa dùng thử | Phải so pilot với công cụ shop đang dùng |
| Sapo Social | [Tài liệu](https://support.sapo.vn/bao-cao-sapo-social-3-0) | Báo cáo số comment, khách hàng, phản hồi và năng suất | Có thống kê vận hành comment | Tài liệu chưa mô tả phân loại ý nghĩa từng comment | Không dùng số lượng comment thay cho insight |

Research takeaway:

```text
Các công cụ hiện có đã giải quyết việc gom, tìm, trả lời hoặc thống kê comment.
Nhóm chỉ nên thử Workflow nếu validation cho thấy người vận hành shop vẫn mất
công ở bước phân loại ý nghĩa và tổng hợp chủ đề.
```

## Workflow before/after

```text
CURRENT STATE — 5 bước; T0 và thời gian từng bước chưa đo

[1 Người bán copy/export comment]
→ [2 Người bán bỏ dòng trống, trùng]
→ [3 Người bán đọc và gắn nhóm từng comment]  <-- bottleneck
→ [4 Người bán tổng hợp chủ đề và ví dụ]
→ [5 Người vận hành shop quyết định]

FUTURE STATE — 5 bước

[1 Người bán nhập file]
→ [2 Rule bỏ dòng trống, trùng và che số điện thoại/email]
→ [3 AI đề xuất nhãn và nhóm chủ đề]
→ [4 Người bán kiểm tra comment nguồn]  <-- human boundary
→ [5 Người bán quyết định]

Fallback:
Case không rõ hoặc AI lỗi → người bán xử lý thủ công.

Bottleneck mới:
Người bán review các nhãn chưa rõ và comment dẫn chứng.

Handoff:
Nền tảng → người bán tạo file → Workflow xử lý
→ người bán review → người bán quyết định.
```

Thời gian hiện tại:

| Bước | Thời gian | Tần suất |
|---|---:|---|
| Copy/export comment | Chưa đo | Chưa xác nhận |
| Bỏ dòng trống, trùng | Chưa đo | Chưa xác nhận |
| Đọc và gắn nhóm | Chưa đo | Chưa xác nhận |
| Tổng hợp chủ đề và ví dụ | Chưa đo | Chưa xác nhận |
| Review và quyết định | Chưa đo | Chưa xác nhận |

`T0` sẽ được tính từ lúc người bán bắt đầu xử lý file đến khi hoàn thành và duyệt
bản tổng hợp.

Tỷ lệ nhãn khớp được tính bằng số comment có nhãn chính trùng với nhãn do người
bán xác nhận, chia cho tổng số comment trong tập đánh giá. Pilot dự kiến dùng tối
thiểu 50 comment; số lượng chính xác sẽ được chốt sau khi nhóm có file thật.

Before/after impact:

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Tổng thời gian | `T0`, chưa đo | Không quá `50% T0` | Mục tiêu pilot; đo cùng actor, cùng file |
| Bước thủ công chính | Đọc và gắn nhãn toàn bộ | Review nhãn chưa rõ | Human boundary |
| Nhãn khớp với người bán | Chưa đo | Từ 80% | Mục tiêu pilot; so với tập do người bán gắn nhãn |
| Insight có comment nguồn | Chưa theo dõi | 100% | Mỗi insight có dẫn chứng |
| Risk mới | Bỏ sót khi đọc | AI gắn sai hoặc suy diễn | Người bán review |

## Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Người trực tiếp vận hành shop nhỏ và tự xử lý comment công khai. |
| **Workflow** | Thu thập → làm sạch → đọc → gắn nhóm → tổng hợp → quyết định. |
| **Bottleneck** | Đọc, gắn nhóm và tổng hợp từng comment. |
| **Impact** | Giả thuyết: thao tác tăng theo số comment và có thể bỏ sót nội dung cần xử lý. Nhóm chưa có evidence trực tiếp và baseline. |
| **Success Metric** | Mục tiêu pilot, chưa đo: giảm ít nhất 50% thời gian; từ 80% nhãn khớp; 100% insight có comment nguồn. |
| **Boundary** | Một file comment công khai của một bài đăng hoặc chiến dịch trên một nền tảng số; che số điện thoại/email trước khi gửi vào AI. |

## Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** | Spreadsheet, bộ nhãn và checklist | Comment ít, người bán có thể đọc hết | Vẫn phải đọc toàn bộ | Dùng làm baseline |
| **Rule** | Bỏ dòng trống/trùng và bắt từ khóa rõ | Nhãn có từ khóa ổn định | Khó hiểu tiếng lóng, phủ định và comment nhiều ý | Dùng ở bước làm sạch |
| **Workflow** | Rule làm sạch → AI đề xuất → người bán review | Các bước cố định nhưng cần hiểu ngôn ngữ | AI có thể gắn sai nhãn | **Chọn để thử** |
| **Agent** | Tự lấy dữ liệu, phân tích và hành động | Workflow nhiều nguồn và nhiều nhánh | Quyền rộng, khó kiểm soát | Không chọn |

Mức chọn:

```text
Workflow.
```

Vì sao:

- Rule phù hợp với bước làm sạch dữ liệu.
- AI hỗ trợ bước cần hiểu ngôn ngữ và tổng hợp.
- Người bán vẫn kiểm tra comment nguồn và quyết định.
- Chưa cần Agent vì workflow tuyến tính, không cần AI tự lập kế hoạch.

## Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Người trực tiếp vận hành shop nhỏ và tự xử lý comment công khai sau một bài đăng hoặc chiến dịch trên nền tảng số. |
| **Workflow** | Nhập file → Rule làm sạch → AI đề xuất nhãn/tổng hợp → người bán kiểm tra → quyết định. |
| **Bottleneck** | Đọc và gắn nhóm thủ công để tìm câu hỏi, phàn nàn, phản đối và yêu cầu tư vấn lặp lại. |
| **Impact** | Giả thuyết: thao tác tăng theo số comment và có thể bỏ sót nội dung cần xử lý. Nhóm chưa có evidence trực tiếp và baseline. |
| **Success Metric** | Mục tiêu pilot, chưa đo: thời gian không quá `50% T0`; từ 80% nhãn khớp; 100% insight có comment nguồn. |
| **Boundary** | Một file, một nền tảng số, một bài đăng/chiến dịch; che số điện thoại/email; không đọc tin nhắn riêng, không tự trả lời/xóa comment hoặc ra quyết định kinh doanh. |
| **AI intervention point** | Sau Rule làm sạch, trước bước người bán review. |
| **Mức chọn** | Workflow. |
| **Rủi ro & người thật kiểm tra** | AI có thể hiểu sai ngữ cảnh hoặc suy diễn; người bán phải duyệt trước khi sử dụng. |

## Final decision

Decision:

```text
Not Yet.
```

Cần validate trước:

- Phỏng vấn 2–3 người trực tiếp vận hành shop.
- Dùng một file comment công khai được phép sử dụng, dự kiến tối thiểu 50 comment.
- Đo thời gian xử lý thủ công `T0`.
- So sánh spreadsheet, Rule và Workflow trên cùng dữ liệu.

Pilot nhỏ nhất sau khi validation xác nhận pain:

- Một người vận hành shop.
- Một file comment của một bài đăng hoặc chiến dịch.
- Một tập mẫu do người bán gắn nhãn để đối chiếu.
- Đo thời gian, tỷ lệ nhãn khớp và số lỗi phải sửa.

Exit / rollback:

- Nếu công cụ hiện tại đã đủ hoặc Rule đạt mục tiêu, không thêm AI.
- Nếu AI không đạt mức nhãn người bán chấp nhận, quay về Rule và xử lý thủ công.
- Không cho hệ thống tự trả lời khách hoặc tự ra quyết định kinh doanh.

Decision rationale:

- Actor, workflow, bottleneck và boundary đã rõ.
- Có phương án No AI và Rule để so sánh.
- Chưa có validation trực tiếp, tập comment thật và baseline thời gian.
- Vì vậy, nhóm chốt candidate để kiểm chứng tiếp nhưng chưa quyết định xây.
