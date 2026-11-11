# HR Workforce Dashboard

> Dashboard Power BI phân tích nhân sự: quy mô lực lượng lao động, nghỉ việc (turnover), mức độ hài lòng/gắn kết, vắng mặt, chi phí lương và nguồn tuyển dụng.

---

## 1. Tổng quan dự án

**Mục tiêu:** Cung cấp cho bộ phận HR và ban lãnh đạo một góc nhìn về sức khỏe lực lượng lao động, từ đó phát hiện điểm nóng (phòng ban có tỷ lệ nghỉ việc cao, nhóm nhân sự rủi ro) và hỗ trợ ra quyết định về giữ chân, tuyển dụng và ngân sách nhân sự.

### Mô hình dữ liệu

Mô hình dạng star gồm các bảng:

- **Employee** (fact): thông tin nhân viên, giới tính, nhóm tuổi, nguồn tuyển dụng, lý do nghỉ việc, trạng thái, rủi ro giữ chân (Retention Risk), chủng tộc, v.v.
- **Department**, **Position**, **Manager**, **Performance**, **MaritalStatus**: các bảng chiều (dimension)
- **Dimensions**: bảng hỗ trợ cho slicer chọn chiều phân tích động
- **_Measures**: bảng chứa các measure DAX (Total Employees, Turnover Rate, Avg. Tenure, v.v.)

### Cấu trúc report

| Trang | Nội dung |
|---|---|
| **Executive Summary** | 7 thẻ KPI, 5 biểu đồ phân tích, 1 bảng tổng hợp theo phòng ban, slicer chọn chiều phân tích (Dimension) |
| **Workforce Database** | Bảng chi tiết theo từng nhân viên, có bộ lọc Department, Performance Score, Manager, Employee Name |

### KPI chính (Executive Summary)

 <img width="1026" height="70" alt="image" src="https://github.com/user-attachments/assets/fffc976d-ce81-4bd3-ab7c-a3bd99e5b2a9" />


### Các biểu đồ chính
- Age Distribution: Số nhân viên theo nhóm tuổi (nhóm tuổi: 25-34, 35-44, 45-54, 55-64, 65+)
<img width="538" height="368" alt="image" src="https://github.com/user-attachments/assets/fb46d6d1-4460-4a3f-9f66-5af2a34239f7" />

- Gender Distribution: Cơ cấu giới tính, tooltip hiển thị Turnover Rate
<img width="584" height="392" alt="image" src="https://github.com/user-attachments/assets/30b947d5-ebd1-4ff6-b8a7-4e8dae62e5f9" />

- Departure Reason: Số nhân viên theo lý do nghỉ việc (vd: More Money, Career Change, Unhappy, Relocation Out Of Area, Military, Return To School, Terminated for Cause, No-Call No-Show…)
<img width="794" height="410" alt="image" src="https://github.com/user-attachments/assets/bea3a140-e71a-4757-9e05-d6e693c42d22" />

- Turnover Rate by Department: Tỷ lệ nghỉ việc theo phòng ban
<img width="769" height="370" alt="image" src="https://github.com/user-attachments/assets/04934ece-cebc-48d9-b9ab-c04a13cfe0a4" />

- Top Recruitment Sources: Funnel nguồn tuyển dụng (LinkedIn, Employee Referral, Google Search, CareerBuilder, Diversity Job Fair, Website…), tooltip hiển thị Engagement và Tenure
<img width="612" height="442" alt="image" src="https://github.com/user-attachments/assets/cbe9137f-f502-47c7-bf39-2d5b6306dd7f" />

- Workforce Metrics Overview by Dimension: Bảng so sánh các chỉ số chính theo phòng ban, vị trí, giới tính, quốc tịch, tuổi, tình trạng hôn nhân, dân tộc
<img width="717" height="234" alt="image" src="https://github.com/user-attachments/assets/69e92a3d-8279-4d75-93db-e3e254ed2752" />

- Trang Workforce Database: Tổng hợp thông tin về nhân viên với các bộ lọc Tên, Phòng ban, Performance score, Quản lý
<img width="956" height="488" alt="image" src="https://github.com/user-attachments/assets/77c9e072-79ba-46e1-a10d-02969da7c3e1" />

---

## 2. Main Findings

|  | Vấn đề | Nhận định | Nguồn biểu đồ |
|---|---|---|---|
| 1 | Quy mô và chi phí | Tổng nhân sự - 298, tổng chi phí lương - 20M, tuổi trung bình - 47.8 | KPI cards |
| 2 | Turnover | Tỷ lệ nghỉ việc toàn công ty - 34.9%; phòng ban cao nhất: Production (40.89%), thấp nhất: 16.67% | Turnover Rate by Department |
| 3 | Lý do nghỉ việc | Lý do phổ biến nhất: Another position (19.23% tổng số nghỉ); nhóm lý do có thể kiểm soát (lương, không hài lòng, chính sách làm việc) chiếm 42.31% | Departure Reason |
| 4 | Cơ cấu tuổi | Nhóm tuổi đông nhất: 35-44; tỷ trọng nhóm 55+ (nguy cơ nghỉ hưu): 20.47% | Age Distribution |
| 5 | Nguồn tuyển dụng | Nguồn đưa về nhiều nhân sự nhất: Indeed; nguồn có Tenure tốt nhất: Google Search | Top Recruitment Sources |
| 6 | Đa dạng giới | Tỷ lệ Nam/Nữ 0.76:1; chênh lệch turnover giữa hai giới 1.39% | Gender Distribution |
| 7 | Hài lòng, gắn kết, vắng mặt | Phòng ban có Satisfaction thấp và Absenteeism cao: Production, IT/IS | Bảng Workforce Metrics |
| 8 | Hiệu suất | Satisfaction Score và mối liên hệ với Retention Risk | Trang Workforce Database |

---

## 3. Main Recommendations

1. **Giảm turnover ở phòng ban rủi ro cao:** thực hiện khảo sát nghỉ việc (exit interview) và stay interview tại các phòng ban có Turnover Rate cao nhất; đặt mục tiêu giảm tỷ lệ theo quý.
2. **Xử lý các lý do nghỉ việc kiểm soát được:** nếu "More Money" và "Unhappy" nổi bật, rà soát khung lương so với thị trường, lộ trình thăng tiến và chất lượng quản lý trực tiếp.
3. **Tối ưu kênh tuyển dụng:** tăng ngân sách cho nguồn mang lại nhân viên gắn bó lâu dài; xem xét cắt giảm nguồn có tenure ngắn.
4. **Chuẩn bị kế nhiệm:** với nhóm tuổi 55+, xây dựng kế hoạch chuyển giao tri thức và đào tạo nhân sự kế cận.
5. **Theo dõi nhóm Retention Risk cao:** sử dụng bộ lọc Satisfaction Score + Retention Risk ở trang Workforce Database để ưu tiên giữ chân nhân viên hiệu suất cao có rủi ro nghỉ.
6. **Cải thiện vắng mặt và hài lòng:** triển khai chương trình can thiệp tại phòng ban có Absenteeism cao, Satisfaction thấp (làm việc linh hoạt, wellbeing, đào tạo quản lý).
---

## 5. Hạn chế

- README này được tạo từ cấu trúc report, nên các số liệu và kết luận cụ thể cần được xác nhận trực tiếp từ dashboard.
- Dữ liệu mang tính phân tích mô tả; chưa có mô hình dự báo turnover.
