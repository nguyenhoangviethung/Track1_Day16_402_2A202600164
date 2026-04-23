
---

# Day 16 Submission - Name [Nguyễn Hoàng Việt Hùng-2A202600164]

---

## 1. Idea reframed

Original idea:
> Xây dựng một hệ thống đặt phòng thông minh tích hợp AI chatbot, giúp người dùng tìm kiếm, gợi ý và tự động đặt phòng/sân thể thao theo thời gian thực thay vì dùng email hay form thủ công.

Reframed as a product opportunity:
> **(Observed gap):** Hiện tại việc phân bổ tài nguyên không gian ở trường học (300+ phòng) đang bị tắc nghẽn do quy trình thủ công (email/form mất 2-3 ngày), dẫn đến tỷ lệ trùng lịch cao (15%) và gây ra sự tranh giành gay gắt giữa các câu lạc bộ, giảng viên và phòng ban.
> **(Founding belief):** Chúng tôi tin rằng nếu cung cấp một nền tảng real-time booking kết hợp Chatbot hiểu ngôn ngữ tự nhiên để tự động hóa khâu check lịch, gợi ý phòng trống thay thế và tự động duyệt các yêu cầu ngắn (dưới 2h), nhà trường sẽ giải quyết triệt để bài toán xung đột tài nguyên và tiết kiệm hàng ngàn giờ chờ đợi cho người dùng.

---

## 2. Customer / Segment Card

- **Segment name:** Ban quản lý cơ sở vật chất (Admin) & Thủ lĩnh các Tổ chức/Câu lạc bộ tại các trường Đại học/Học viện quy mô lớn.
- **Operational context:** Hệ thống phòng học/lab/sân bãi phân tán nhiều tòa nhà; Quy trình hiện tại phụ thuộc vào Email/Google Form và phê duyệt thủ công (Human-in-the-loop); Tài nguyên luôn trong tình trạng quá tải cục bộ vào giờ cao điểm.
- **Recurring workflow:** 1. Check lịch trống trên bảng tính/form. 2. Gửi yêu cầu đặt phòng (kèm mục đích). 3. Chờ Admin duyệt (2-3 ngày). 4. Gửi email xác nhận/thương lượng đổi phòng nếu có xung đột.
- **Pain moment:** Khoảnh khắc nhận được thông báo "Phòng đã có người đặt" ngay trước giờ sự kiện diễn ra, hoặc chuỗi email qua lại 5-7 lần chỉ để chốt đổi một phòng họp gấp dưới 2 giờ.
- **Why now:** Nhu cầu tổ chức hoạt động ngoại khóa/seminar của sinh viên Gen Z tăng vọt; Ban giám hiệu đang chịu áp lực chuyển đổi số (Smart Campus) và cần tối ưu hóa chi phí vận hành (điện năng, nhân sự quản trị).
- **Access path:** Tiếp cận Top-down qua Ban Giám Hiệu/Giám đốc CNTT (CIO); hoặc Bottom-up qua việc cung cấp tool miễn phí cho Phòng Công tác Sinh viên; Demo tại các hội thảo EdTech/Smart Education.

One-sentence description:
> Nhóm sinh viên, giảng viên và cán bộ quản lý tại các đại học lớn đang mệt mỏi với quy trình mượn phòng thủ công mất 2-3 ngày, thường xuyên gặp cảnh trùng lịch và lãng phí tài nguyên do thiếu sự điều phối thông minh theo thời gian thực.

---

## 3. Need Map (2-3 needs)

### Need #1 (priority)
- **Statement (JTBD):** When **cần tổ chức buổi họp/học gấp**, I want **biết ngay phòng nào đang trống và đặt được luôn**, so I can **duy trì tiến độ công việc mà không phải chờ đợi phê duyệt thủ công.**
- **Current workaround:** Chạy đi tìm phòng trống trực tiếp, "chiếm dụng" tạm thời, hoặc nhắn tin cầu cứu trên các nhóm chat Zalo/Teams nội bộ.
- **Pain signal:** Mất 2-3 ngày chờ đợi email xác nhận chỉ cho một buổi họp kéo dài 1 tiếng.
- **Evidence / proxy evidence:** Tỷ lệ conflict 15% và các chuỗi email/ticket support kéo dài hàng chục tin nhắn chỉ để chốt 1 phòng.
- **Why underserved:** Quy trình hiện tại là "con người xử lý" (human-in-the-loop), không thể đáp ứng tốc độ thời gian thực (real-time execution).

### Need #2
- **Statement (JTBD):** When **phòng mong muốn đã bị chiếm chỗ**, I want **được gợi ý ngay các lựa chọn thay thế tương đồng về thiết bị và vị trí**, so I can **không phải tốn công tra cứu lại từ đầu.**
- **Current workaround:** Tự tra cứu lại danh sách hàng trăm phòng bằng mắt thường hoặc đành chấp nhận hủy/dời lịch sự kiện.
- **Pain signal:** Câu trả lời "Hết phòng" cộc lốc từ admin mà không kèm theo bất kỳ giải pháp tư vấn (consulting) nào khác.
- **Evidence / proxy evidence:** Người dùng thường xuyên tranh giành một vài phòng "hot" vì không biết các phòng ở tòa nhà khác có tính năng tương đương vẫn đang trống.
- **Why underserved:** Các bộ lọc (SQL rule-based filter) hiện tại quá cứng nhắc, không có khả năng hiểu ngữ nghĩa (Semantic) của nhu cầu (ví dụ: cần "chỗ yên tĩnh" thì phòng nào đáp ứng được).

### Need #3 (optional)
- **Statement (JTBD):** When **quản lý và điều phối danh sách phòng**, I want **hệ thống tự động thực thi các chính sách (Policy-as-Code)**, so I can **giảm tải việc phải giải thích nội quy và xử lý các ca tranh chấp thủ công.**
- **Current workaround:** Admin phải học thuộc luật, nhớ lịch các dịp lễ và trực tiếp từ chối/khóa phòng bằng thao tác tay.
- **Pain signal:** Admin bị quá tải (burnout) vì phải đóng vai trò "cảnh sát" đi xử lý các ca "đá phòng" hoặc giải thích lặp đi lặp lại tại sao sinh viên không được mượn phòng Lab.
- **Evidence / proxy evidence:** Sự tồn tại của các tập file PDF quy định dài dằng dặc trên website trường nhưng không ai đọc, dẫn đến tỷ lệ yêu cầu sai rule rất cao.
- **Why underserved:** Chính sách mượn phòng (Policy) đang nằm trên văn bản tĩnh, chưa được số hóa thành dạng Vector (RAG) để nhúng thẳng vào luồng duyệt tự động của AI.

---

## 4. Strategy Statement

For **các trường Đại học quy mô lớn và tập đoàn giáo dục** who struggle with **sự lãng phí tài nguyên không gian và quy trình quản lý thủ công chậm chạp**,  
our product helps them **tự động hóa hoàn toàn việc điều phối, giải quyết xung đột và đặt phòng theo thời gian thực** through **một AI Agent có khả năng hiểu ngôn ngữ tự nhiên, gợi ý ngữ nghĩa (Semantic Search) và thực thi chính sách tự động (Policy RAG)**,  
unlike **các hệ thống điền form tĩnh (Google Forms) hay phần mềm quản lý lịch truyền thống (Rule-based Booking Systems)**,  
because we can leverage **kiến trúc Vector Database kết hợp LLM để biến việc "đặt phòng" thành một trải nghiệm "tư vấn không gian" cá nhân hóa.**

---

## 5. Moat Hypothesis

**Moat mechanism:** Contextual Data & Policy-Learning Flywheel (Bánh đà dữ liệu ngữ cảnh & Chính sách)

If we deploy **10-15+ campus networks** in **khối giáo dục Đại học**, the following improve:
1. **Semantic Match Rate:** Hệ thống Vector DB ngày càng thu thập nhiều biến thể về cách sinh viên/giảng viên diễn đạt nhu cầu "mơ hồ" (vd: "cần chỗ quay Tiktok", "chỗ tập kịch"), giúp khả năng match phòng đúng nhu cầu tiệm cận 100%.
2. **Predictive Analytics:** Hệ thống học được "tính thời vụ" (Exam weeks, Club weeks) của từng trường, từ đó chủ động đề xuất cấu hình lại không gian (vd: biến phòng họp thành phòng tự học) trước khi nghẽn mạng xảy ra.
3. **Autonomous Approval:** Kho dữ liệu RAG về các "ngoại lệ" (edge cases) được admin giải quyết trong quá khứ ngày càng dày lên, giúp Agent tự trị cao hơn trong việc ra quyết định duyệt/từ chối mà không cần gọi Admin.

Why competitors cannot easily replicate this:
> Các phần mềm SaaS ERP/Booking truyền thống được xây dựng trên kiến trúc Database quan hệ (Relational DB) với các Schema cứng ngắc. Để sao chép, họ phải đập bỏ và viết lại toàn bộ core engine sang Vector DB. Hơn nữa, họ thiếu nguồn dữ liệu "Hội thoại tự nhiên" (Conversational Data) đặc thù của môi trường học đường để huấn luyện RAG hiệu quả.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | $50M - $80M/year | Toàn bộ khối ĐH, Cao đẳng, Trường Quốc tế, Học viện và Tòa nhà văn phòng chia sẻ tại Đông Nam Á có nhu cầu giải pháp Smart Campus/Smart Office. | Medium |
| SAM | $5M - $10M/year | Khối trường Đại học tư thục, Trường quốc tế và các trường Đại học công lập tự chủ tài chính cấp cao tại Việt Nam (VD: VinUni, RMIT, FPT, NEU...). | High |
| SOM | $100K - $200K ARR | 3-5 trường Đại học lớn tại Hà Nội/TP.HCM làm pilot (Pilot fee + SaaS Subscription ban đầu) trong 12-18 tháng tới. | High |

**Top 3 unknowns requiring further research:**
1. **Sales Cycle & Economic Buyer:** Chu kỳ chốt sale B2B cho trường Đại học là bao lâu? Ai là người thực sự cầm ngân sách (Trưởng phòng CSVC, Giám đốc IT, hay Ban Giám Hiệu)?
2. **Integration Friction:** Mức độ khó khăn khi phải tích hợp (API hooks) AI Agent này với các hệ thống core cũ (Student Information System, Active Directory) của nhà trường.
3. **Pricing Model:** Nên thu phí SaaS theo số lượng tài nguyên phòng (Per Room), theo Active Users (Per Student), hay theo Tier mức độ sử dụng AI (Token usage)?

**Judgment:**
- [x] Worth pursuing but not now (need to validate **chu kỳ bán hàng B2B (Sales Cycle) và khả năng tích hợp hệ thống cũ của trường** first)
*(Ghi chú: Lựa chọn này thể hiện sự trưởng thành, nhìn nhận rõ rào cản B2B dù giải pháp công nghệ rất tốt).*

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Chúng tôi là một "Trợ lý Điều phối Không gian Thông minh" (Smart Space Orchestrator), giúp chuyển đổi trải nghiệm tranh giành phòng ốc mệt mỏi thành một luồng giao tiếp mượt mà, nơi người dùng chỉ cần "nói" nhu cầu và AI sẽ lo phần còn lại.

**What we are not / not yet:**
> Chúng tôi không phải là một hệ thống Quản lý Tài sản Doanh nghiệp (Enterprise Asset Management - EAM) toàn diện, và không nhằm mục đích thay thế các phần mềm kiểm kê tài sản phần cứng chuyên sâu của phòng ban IT.

---

## 8. Self-assessment before Day 17

Trong 6 mat xich (Idea -> Customer -> Need -> Strategy -> Moat -> Market Size), mat xich nao yeu nhat hien tai?

> **Market Size & Go-to-Market (GTM) Strategy đang là mắt xích yếu nhất.** Dù bài toán (Need) rất rõ và giải pháp (Idea/Strategy) vượt trội nhờ AI, nhưng thị trường Giáo dục (EdTech B2B) nổi tiếng với quy trình ra quyết định rườm rà, giải ngân chậm. Rủi ro "chết lâm sàng" trong lúc chờ trường học ký hợp đồng là rất cao.

Open questions chung toi muon kham pha them o Day 17:
1. Làm thế nào để định lượng hóa (Quantify) nỗi đau "chờ duyệt 2-3 ngày" thành ROI bằng tiền (VND) để thuyết phục Ban Giám Hiệu chịu mở hầu bao?
2. Có nên Pivot (xoay trục) hoặc mở rộng (Spin-off) giải pháp này sang thị trường Coworking Space / SME Offices để có dòng tiền sống sót nhanh hơn trước khi đánh chiếm các trường Đại học không?
3. Thiết kế chiến lược "Trojan Horse" như thế nào? (Tặng miễn phí cho các Câu lạc bộ sinh viên dùng trước để tạo áp lực bottom-up lên phòng Admin phải mua bản quyền).