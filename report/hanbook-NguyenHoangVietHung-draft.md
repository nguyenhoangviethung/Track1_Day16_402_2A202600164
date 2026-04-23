# Day 16 Submission - Name [Nguyễn Hoàng Việt Hùng-2A202600164]

---

## 1. Idea reframed

Original idea:
> Làm hệ thống đặt phòng có AI chatbot để người dùng tìm phòng và đặt phòng nhanh hơn cách gửi form.

Reframed as a product opportunity:
> Hiện tại việc đặt phòng ở trường học còn chậm, phải chờ duyệt thủ công nên nhiều lúc bị trùng lịch. Nếu có một hệ thống đặt phòng thông minh hơn thì người dùng sẽ đặt phòng nhanh hơn và nhà trường quản lý dễ hơn.

---

## 2. Customer / Segment Card

- **Segment name:** Trường đại học và các đơn vị cần đặt phòng.
- **Operational context:** Nhiều phòng học, phòng họp, sân bãi; đặt phòng qua form/email là chính.
- **Recurring workflow:** Gửi yêu cầu -> chờ duyệt -> nhận phản hồi.
- **Pain moment:** Bị trùng lịch hoặc chờ lâu mới được xác nhận.
- **Why now:** Nhu cầu sử dụng phòng tăng lên và mọi người muốn nhanh hơn.
- **Access path:** Liên hệ phòng đào tạo, phòng cơ sở vật chất, và demo cho trường.

One-sentence description:
> Người dùng trong trường cần một cách đặt phòng đơn giản hơn vì quy trình hiện tại khá mất thời gian.

---

## 3. Need Map (2-3 needs)

### Need #1 (priority)
- **Statement (JTBD):** When cần đặt phòng gấp, I want có phòng trống ngay, so I can tổ chức công việc đúng giờ.
- **Current workaround:** Nhắn tin hỏi nhau hoặc tìm phòng trống thủ công.
- **Pain signal:** Đợi xác nhận hơi lâu.
- **Evidence / proxy evidence:** Có nhiều phản nàn về trùng lịch.
- **Why underserved:** Hệ thống hiện tại chưa tự động hóa tốt.

### Need #2
- **Statement (JTBD):** When phòng muốn đặt đã bị chiếm, I want có gợi ý phòng khác, so I can không phải tìm lại từ đầu.
- **Current workaround:** Tự tìm phòng khác.
- **Pain signal:** Mất nhiều thời gian đổi phòng.
- **Evidence / proxy evidence:** Người dùng hay than phiền trên nhóm chat.
- **Why underserved:** Công cụ tìm kiếm chưa thông minh.

### Need #3 (optional)
- **Statement (JTBD):** When admin xử lý nhiều yêu cầu đặt phòng, I want hệ thống tự hỗ trợ lọc rule, so I can giảm tải công việc thủ công.
- **Current workaround:** Admin xử lý từng case.
- **Pain signal:** Dễ quá tải vào giờ cao điểm.
- **Evidence / proxy evidence:** Có nhiều ticket và email qua lại.
- **Why underserved:** Rule vẫn nằm trên văn bản, chưa được số hóa tốt.

---

## 4. Strategy Statement

For trường học có nhu cầu đặt phòng nhiều  
who struggle with quy trình đặt phòng chậm và dễ trùng lịch,  
our product helps them đặt phòng nhanh hơn  
through AI chatbot và gợi ý phòng trống,  
unlike form/email thông thường,  
because we can leverage công nghệ AI và dữ liệu lịch đặt phòng.

---

## 5. Moat Hypothesis

**Moat mechanism:** Dữ liệu đặt phòng tích lũy theo thời gian

If we deploy ở nhiều trường, the following improve:
1. Gợi ý phòng phù hợp hơn.
2. Dự đoán giờ cao điểm tốt hơn.
3. Giảm bớt việc admin phải thao tác tay.

Why competitors cannot easily replicate this:
> Vì cần thời gian thu dữ liệu và hiểu quy trình của từng trường.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $20M-$100M/year | Nhiều trường học và tổ chức cần đặt phòng thông minh | Low |
| SAM | $2M-$10M/year | Tập trung trường lớn tại Việt Nam | Medium |
| SOM | $50K-$150K ARR | Có thể có 2-4 trường dùng thử trong 12-18 tháng | Medium |

**Top 3 unknowns requiring further research:**
1. Trường sẽ mua theo gói nào và ngân sách bao nhiêu.
2. Tích hợp với hệ thống cũ có khó không.
3. Chu kỳ bán hàng B2B giáo dục mất bao lâu.

**Judgment:**
- [x] Worth pursuing but not now (cần xác thực thêm về sales cycle và tích hợp)

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Nền tảng hỗ trợ đặt phòng thông minh cho trường học.

**What we are not / not yet:**
> Chưa phải hệ thống quản trị tài sản toàn diện cho mọi nghiệp vụ trong trường.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích (Idea -> Customer -> Need -> Strategy -> Moat -> Market Size), mắt xích nào yếu nhất hiện tại?

> Market Size và GTM vẫn chưa rõ. Team chưa có đủ dữ liệu thật để chắc chắn về tốc độ bán hàng và khả năng scale nhanh trong giáo dục.

Open questions chúng tôi muốn khám phá thêm ở Day 17:
1. Làm sao tính ROI rõ ràng hơn cho nhà trường?
2. Nên bán vào segment nào trước để dễ chốt deal hơn?
3. Có nên mở rộng qua coworking/SME để test nhanh trước không?
