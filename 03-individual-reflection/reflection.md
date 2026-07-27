# 03 — Individual Reflection

## Vai trò và đóng góp của tôi

Tôi là thành viên đề xuất, tập trung vào phần scan cá nhân và hỗ trợ nhóm ở các
phần research, workflow và viết report.

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Đưa ra 9 problems, bổ sung actor và dấu hiệu quan sát được | Có danh sách đủ rộng để chọn top 3 |
| Pitch Problem Card | Chọn bài sàng lọc CV và chuẩn bị actor, workflow, bottleneck để pitch | Bài có phạm vi rõ và có phương án non-AI để so sánh |
| Challenge | Đặt câu hỏi liệu checklist hoặc ATS hiện có đã đủ và AI có thể loại nhầm ứng viên không | Làm rõ rủi ro và phần cần con người kiểm tra |
| Group convergence | Đóng góp các candidate cá nhân và hỗ trợ nhóm gom các bài có pattern gần nhau | Nhóm thu hẹp về bài phân tích comment |
| Research | Hỗ trợ đối chiếu các công cụ quản lý và phân tích comment hiện có | Nhóm không còn xem “thiếu công cụ AI” là vấn đề chính |
| Workflow nhóm | Góp ý current/future workflow, bottleneck và bước người bán review | AI được đặt trong một bước cụ thể, không tự quyết định thay người bán |
| Viết report nhóm | Hỗ trợ sắp xếp nội dung theo mẫu và rà soát actor, metric, boundary | Report rõ phạm vi, cách đo và những evidence còn thiếu |
| Decision | Cùng nhóm xem lại dữ liệu hiện có trước khi chốt | Nhóm chọn `Not Yet` thay vì kết luận `Go` quá sớm |

## Tôi đã dùng AI như thế nào?

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Kiểm tra actor và dấu hiệu của các problem | Chỉ ra các ý còn rộng hoặc chưa rõ ai chịu ảnh hưởng | Một số gợi ý chung chung, không có dấu hiệu thật | Giữ các vấn đề có bối cảnh cụ thể và ghi rõ phần chưa đo |
| Problem Card | Phản biện workflow, bottleneck và phương án non-AI | Giúp các card đủ field và dễ so sánh | Có lúc sửa quá nhiều, làm câu chữ thiếu tự nhiên | Giữ ý ban đầu và chỉ sửa chỗ mơ hồ |
| Workflow | Sắp xếp current/future workflow và gợi ý cách đo | Làm rõ bước AI hỗ trợ và bước con người review | Có lúc đưa ra thời gian ước lượng như số liệu thật | Ghi `chưa đo` và nêu cách đo thay vì tự đặt số |
| Research | Tìm công cụ và nguồn tham khảo | Giúp tìm nhanh các giải pháp đã tồn tại | Nguồn đầu tiên đúng kỹ thuật nhưng xa thực tế shop nhỏ | Ưu tiên công cụ gần bối cảnh như Meta Business Suite, Harasocial và Sapo Social |
| Problem Statement | Kiểm tra actor, bottleneck, metric và boundary | Giúp phát hiện những thành phần còn thiếu | Dễ diễn đạt thành “thiếu công cụ AI” | Chuyển trọng tâm về việc đọc, phân loại và tổng hợp comment thủ công |
| Rule / Workflow / Agent | So sánh mức tự động hóa phù hợp | Làm rõ khác biệt giữa Rule, Workflow và Agent | Có xu hướng đề xuất Agent khi evidence chưa đủ | Chọn Workflow có người bán review; Rule dùng cho bước đơn giản |
| Decision | Phản biện điều kiện `Go` và evidence còn thiếu | Giúp liệt kê dữ liệu cần kiểm chứng | AI không thể xác nhận pain hoặc baseline khi chưa có dữ liệu thật | Chọn `Not Yet` và ghi rõ điều kiện cần kiểm chứng tiếp |

## Điều tôi học được

- Khi nghe các candidate của thành viên khác, tôi nhận ra nhiều bài khác lĩnh vực
  nhưng cùng nghẽn ở việc đọc, phân loại hoặc tổng hợp thông tin.
- Nhóm có lúc đi theo hướng solution-first khi tập trung vào việc “thiếu công cụ
  AI”. Sau khi xem lại workflow và các công cụ hiện có, nhóm chuyển trọng tâm về
  pain trong bước xử lý comment thủ công.
- Tôi thay đổi từ việc nghĩ đến một Agent phân tích comment sang một Workflow có
  người bán review, vì dữ liệu và mức độ chính xác chưa được kiểm chứng.
- Một problem cần đi từ actor, workflow và bottleneck đến metric, boundary rồi mới
  đánh giá AI có phù hợp hay không.
- Research giúp biết giải pháp nào đã tồn tại nhưng không thay thế validation với
  người dùng thật.

Điều khó nhất với tôi là viết metric khi chưa có số liệu thực tế. Tôi hiểu rằng
ghi `T0 chưa đo` và nêu cách đo trung thực hơn việc đưa ra một con số không có
nguồn.

## Mạch tôi hiểu về bài toán

```text
Problem: người vận hành shop phải đọc và tổng hợp comment thủ công
→ Workflow: xác định các bước hiện tại và bước nghẽn
→ Metric: đo T0, độ khớp nhãn và tỷ lệ comment bị bỏ sót
→ Boundary: một file comment từ một nền tảng, không tự trả lời khách
→ AI: dùng Workflow để hỗ trợ phân loại và tổng hợp, người bán kiểm tra
→ Decision: Not Yet vì chưa có dữ liệu thật và baseline
```

## Nếu làm lại

Tôi sẽ cùng nhóm phỏng vấn người vận hành shop và đo thời gian xử lý một tập
comment trước khi chốt metric. Tôi cũng sẽ challenge rõ hơn về evidence của pain,
khả năng dùng Rule hoặc công cụ hiện có, đồng thời ghi lại đóng góp của từng người
ngay trong buổi thảo luận.
