# Shopee Business Process Management (BPM) Project 🚀

Chào mừng bạn đến với kho lưu trữ (repository) chính thức của **Nhóm 10 - Lớp IE203.F32.LT.CNTT** dành cho đồ án môn học **Hệ thống Quản trị Quy trình Nghiệp vụ (BPM)** dưới sự hướng dẫn của **ThS. Hà Lê Hoài Trung** [200]. 

Đồ án này tập trung nghiên cứu, mô tả, mô hình hóa và cải tiến kiến trúc quy trình nghiệp vụ của sàn thương mại điện tử **Shopee** [5]. Đồng thời, nhóm phát triển ứng dụng điều hành quy trình thực tế (BPMS) dựa trên các quy trình đã tối ưu hóa ở các chương cuối [32].

---

## 👥 THÀNH VIÊN NHÓM & PHÂN CÔNG VAI TRÒ [180]

Nhóm gồm **6 thành viên**, được phân chia công việc rõ ràng nhằm đảm bảo tính nhất quán (Consistent) và kiểm soát chéo tốt [21, 23]:

| STT | Họ & Tên | MSSV | Vai trò chính | Nhiệm vụ chính trong dự án |
| :---: | :--- | :---: | :---: | :--- |
| 1 | **[Tên Nhóm Trưởng]** | [MSSV1] | **Nhóm trưởng (Leader)** | Điều phối tiến độ tổng thể, quản lý kho GitHub [24]. Phụ trách chính phần kỹ thuật & code Backend hệ thống BPMS [32, 138]. |
| 2 | **[Tên của Bạn]** | [MSSV2] | **Nhóm phó (Vice-Leader)** | Phụ trách chính **Biên tập Báo cáo (Docs)** [180], **Thiết kế Slide thuyết trình** [9]. Soát lỗi chính tả [19], kiểm soát định dạng chuẩn [19] & kiểm soát tính nhất quán của toàn bộ tài liệu [21]. Hỗ trợ phân tích quy trình quản lý. |
| 3 | **[Thành viên 3]** | [MSSV3] | **BPM Analyst (Core)** | Khảo sát, thu thập bằng chứng thực tế [11] và phân tích lớp **Quy trình Cốt lõi (Core)** của Shopee [54, 117]. |
| 4 | **[Thành viên 4]** | [MSSV4] | **BPM Analyst (Support)** | Khảo sát và phân tích lớp **Quy trình Hỗ trợ (Support)** của Shopee [54, 117]. |
| 5 | **[Thành viên 5]** | [MSSV5] | **BPM Analyst (Management)** | Khảo sát và phân tích lớp **Quy trình Quản lý (Management)** của Shopee [54, 117]. |
| 6 | **[Thành viên 6]** | [MSSV6] | **Developer** | Thiết kế cơ sở dữ liệu [56, 140], xây dựng giao diện tương tác Frontend cho ứng dụng BPMS [32, 138]. |

---

## 📁 CẤU TRÚC THƯ MỤC REPOSITORY (ÁP DỤNG CHUẨN RUBRIC UIT) [4, 156]

Cấu trúc này được tổ chức khoa học, tương ứng trực tiếp với các chương báo cáo và tiêu chí đánh giá trong Rubric của Thầy [4, 156]:

```text
shopee-bpm-project/
├── .gitignore                  # Bỏ qua các file rác (node_modules, file tạm, .DS_Store, v.v.)
├── README.md                   # Trang chủ giới thiệu nhóm, đề tài Shopee, phân công & bảng theo dõi tiến độ tuần
│
├── docs/                       # CHƯƠNG 1 & 2: KHẢO SÁT THỰC TẾ & PHƯƠNG PHÁP (Rubric 1 & 3)
│   ├── organization-chart/     # Sơ đồ tổ chức Shopee, tài liệu mô hình kinh doanh & Sổ tay thuật ngữ [11, 21]
│   ├── evidence/               # Minh chứng quan sát thực tế (ảnh chụp các bước mua hàng/hoàn tiền trên Shopee) [11, 34]
│   └── interview/              # Kịch bản họp nhóm (workshop) & Bộ câu hỏi khảo sát [11, 13]:
│       ├── qualitative.md      # 10 câu hỏi định tính (5 câu hỏi cấu trúc, 5 câu hỏi không cấu trúc) [14, 157]
│       └── quantitative.md     # 10 câu hỏi định lượng (5 câu hỏi cấu trúc, 5 câu hỏi không cấu trúc) [14, 157]
│
├── models/                     # CHƯƠNG 3 & 6: MÔ HÌNH HÓA QUY TRÌNH (BPMN) (Rubric 1 & 2)
│   ├── process-architecture/   # Sơ đồ Kiến trúc quy trình tổng (thể hiện mối liên kết của ít nhất 10 quy trình) [5, 6]
│   ├── as-is/                  # Thư mục chứa quy trình hiện tại (Lưu file gốc .bpmn & ảnh .png) [15, 135]:
│   │   ├── management/         # 2 quy trình quản lý (đảm bảo độ phức tạp cổng điều kiện > 7) [9, 17]
│   │   ├── core/               # 2 quy trình cốt lõi [9]
│   │   └── support/            # 2 quy trình hỗ trợ [9]
│   └── to-be/                  # Thư mục chứa quy trình cải tiến (To-be) sau khi đã tối ưu hóa [136]
│
├── analysis/                   # CHƯƠNG 4 & 5: PHÂN TÍCH QUY TRÌNH ĐỊNH TÍNH & ĐỊNH LƯỢNG (Rubric 4)
│   ├── qualitative/            # Phân tích định tính [14, 157]:
│   │   ├── va-analysis/        # Bảng phân tích giá trị gia tăng (VA/NVA/BVA gồm 3 cột: Liệt kê, Mô tả, Khắc phục) [15, 158]
│   │   ├── waste-analysis/     # Bảng phân tích lãng phí (Move, Hold, Overdo gồm 3 cột: Liệt kê, Mô tả, Khắc phục) [15, 158]
│   │   └── root-cause/         # Sơ đồ xương cá (Fishbone) hoặc Pareto phân tích nguyên nhân gốc rễ [16, 158]
│   └── quantitative/           # Phân tích định lượng [16, 158]:
│       └── calculations.xlsx   # Bảng tính chi tiết Thời gian chu kỳ (Cycle time) và Chi phí (Cost) [16, 158]
│
├── src/                        # CHƯƠNG 7: ỨNG DỤNG ĐIỀU HÀNH QUY TRÌNH (Thực thi công nghệ ở 2 chương cuối) [32]
│   ├── backend/                # Mã nguồn phía máy chủ ứng dụng thực thi quy trình [32, 138]
│   └── frontend/               # Giao diện tương tác hệ thống BPMS [32, 138]
│
└── deliverables/               # SẢN PHẨM BÀN GIAO CHÍNH THỨC NỘP THẦY (Rubric 5) [159]
    ├── Final_Report_Nhom10.docx # File báo cáo Word chuẩn mẫu khóa luận UIT (Nhãn hình dưới ảnh, nhãn bảng trên bảng) [19, 159]
    └── Final_Slide_Nhom10.pptx # Slide thuyết trình chính thức (Mỗi slide chỉ chứa tối đa 1 sơ đồ quy trình trực quan) [9, 159]
```

---

## 🧭 HƯỚNG DẪN CHI TIẾT TỪNG PHẦN TRONG REPO

### 1. Thư mục `docs/` (Khảo sát thực tế & Kịch bản khảo sát)
*   **organization-chart/**: Chứa sơ đồ tổ chức phòng ban và mô hình kinh doanh của Shopee để làm rõ ngữ cảnh [21]. Chứa file `glossary.md` đóng vai trò Sổ tay thuật ngữ chuyên ngành (BPM, Thương mại điện tử, Logistics) [11].
*   **evidence/**: Chứa hình ảnh chụp màn hình thực tế (trải nghiệm cá nhân của các thành viên) các luồng công việc trên Shopee (như luồng đặt hàng, luồng trả hàng/hoàn tiền) làm bằng chứng quan sát thực tế [11, 25, 34].
*   **interview/**: Chứa file kịch bản phỏng vấn gồm đúng 20 câu hỏi (10 câu định tính, 10 câu định lượng) chia đều 5 cấu trúc - 5 không cấu trúc cho từng loại theo yêu cầu nghiêm ngặt của Rubric 3 [14, 157].

### 2. Thư mục `models/` (Mô hình hóa BPMN)
*   **process-architecture/**: Chứa sơ đồ kiến trúc quy trình 3 lớp của Shopee với tối thiểu **10 quy trình** [5, 6].
*   **as-is/**: Chứa sơ đồ quy trình hiện trạng (As-is). Mỗi lớp (Quản lý, Cốt lõi, Hỗ trợ) phải lưu trữ cả **file gốc thiết kế quy trình** (ví dụ file `.bpmn` từ Camunda/Bizagi) và **file hình ảnh** `.png` xuất ra tương ứng [15, 135].
    *   ⚠️ *Lưu ý về độ phức tạp:* Quy trình Quản lý được chọn mô hình hóa phải có độ phức tạp cổng điều kiện (split/join) **lớn hơn 7** để đạt trọn vẹn điểm [17, 156].
*   **to-be/**: Chứa sơ đồ quy trình cải tiến (To-be) đã loại bỏ lãng phí và tối ưu hóa thời gian/chi phí [136].

### 3. Thư mục `analysis/` (Phân tích quy trình)
*   **qualitative/**: Chứa các bảng phân tích giá trị gia tăng (VA/NVA/BVA) và bảng phân tích lãng phí (8 loại lãng phí trong đó tập trung vào Move, Hold, Overdo) [15, 158]. Cả hai bảng này bắt buộc phải thiết kế đúng **3 cột: Liệt kê, Mô tả, Khắc phục** [15, 158]. Đồng thời, lưu trữ sơ đồ Root-cause (như sơ đồ xương cá - Fishbone hoặc biểu đồ Pareto) để tìm nguyên nhân gốc rễ vấn đề [16, 158].
*   **quantitative/**: File bảng tính Excel phân tích thời gian chu kỳ (Cycle time) và chi phí (Cost) của quy trình trước và sau cải tiến [16, 158].

### 4. Thư mục `src/` (Phần mềm BPMS)
*   Mã nguồn hoàn chỉnh của ứng dụng quản trị điều hành quy trình thực tế (BPMS) liên kết cơ sở dữ liệu và giao diện người dùng [32, 59, 138].

### 5. Thư mục `deliverables/` (Sản phẩm bàn giao nộp thầy)
*   Lưu trữ các phiên bản báo cáo Word và Slide thuyết trình chính thức của nhóm. 
    *   ⚠️ *Quy tắc định dạng bắt buộc:* Nhãn hình ảnh phải đặt dưới hình, nhãn bảng biểu phải đặt trên bảng [19, 159]. Sai lỗi này 1 lần trong file Word sẽ bị trừ điểm cực kỳ nặng [21].
    *   ⚠️ *Quy tắc Slide:* Mỗi slide thuyết trình chỉ được trình bày tối đa **1 quy trình/sơ đồ** để đảm bảo trực quan [9, 18, 159].

---

## ⏰ CÁC QUY ĐỊNH & DEADLINES CỰC KỲ QUAN TRỌNG TỪ THẦY TRUNG

Nhóm chúng ta cần bám sát các lưu ý vàng sau đây từ Thầy Trung trong suốt thời gian thực hiện đồ án để **tránh bị trừ điểm đáng tiếc** hoặc bị **0 điểm** [10, 18, 21]:

1.  **Quy định về GitHub (Cảnh báo 0 điểm đồ án):**
    *   Tài khoản GitHub của thầy (**`trunghlh@uit.edu.vn`**) phải được add làm collaborator của repo này ngay trong tuần 1 [200].
    *   ⏰ **Hạn chót commit hàng tuần:** Trước **23 giờ 30 phút ngày Chủ Nhật hàng tuần** [30].
    *   🔥 **Hình phạt cực nặng:** Nếu **3 tuần liên tiếp** kho lưu trữ GitHub của nhóm không có bất kỳ biến động, cập nhật hay lịch sử commit nào từ các thành viên, nhóm sẽ bị đánh giá **0 điểm** cho toàn bộ đồ án [24, 159]!
    *   👤 **Ghi nhận công sức cá nhân:** Điểm số cuối cùng sẽ được thầy phân bổ dựa trên lịch sử commit (vết email/tên tài khoản) của từng thành viên để đảm bảo công bằng [24, 26]. **Tuyệt đối không nhờ nhóm trưởng commit hộ** [26].

2.  **Quy định về Thuyết trình (Báo cáo cuối kỳ):**
    *   Thời gian báo cáo cụ thể của từng nhóm sẽ được thầy sắp xếp sau khi kết thúc hạn nộp bài [18, 154].
    *   ⏰ **Khống chế thời gian:** Vượt quá thời gian thuyết trình quy định thì **cứ 5 phút nhóm sẽ bị trừ 1 điểm** [18, 159]. Do đó, nhóm phó sẽ chủ trì các buổi thuyết trình thử (mock presentation) để căn chỉnh thời gian thật kỹ [18].
    *   📷 **Mở Webcam:** Khi thuyết trình báo cáo, tất cả thành viên trong nhóm bắt buộc phải **bật camera** [18, 159]. Thành viên vắng mặt hoặc không bật camera (nếu không có lý do được đồng ý trước) sẽ bị trừ từ 1 đến 2 điểm cá nhân [18].

3.  **Quy định về lỗi chính tả và định dạng:**
    *   File Word báo cáo chính thức: **Cứ sai 1 lỗi chính tả sẽ bị trừ thẳng 1 điểm** [19, 159]! Nhóm phó (biên tập chính) cần rà soát thật kỹ trước khi nộp [180].

---

## 📅 TIMELINE TIẾN ĐỘ THỰC HIỆN ĐỒ ÁN (5 TUẦN)

*   **Tuần 1 (Hiện tại – 26/07/2026):** Khảo sát thực tế, thu thập minh chứng Shopee [11, 25], **đăng ký đề tài** với thầy trước Chủ Nhật tuần sau [36] $\rightarrow$ **Hoàn thành Rubric 1 (Chương 1 & 2)** [4, 156].
*   **Tuần 2 (27/07 – 02/08/2026):** Vẽ sơ đồ quy trình hiện tại **BPMN As-Is** (đảm bảo độ phức tạp cổng điều kiện > 7) [17, 156] $\rightarrow$ **Hoàn thành Rubric 2 (Chương 3)** [156].
*   **Tuần 3 (03/08 – 09/08/2026):** Phân tích quy trình định tính (Lập các bảng VA/NVA/BVA, bảng lãng phí, vẽ sơ đồ xương cá/Pareto) [15, 16, 158] $\rightarrow$ **Hoàn thành Rubric 3 (Chương 4)** [157].
*   **Tuần 4 (10/08 – 16/08/2026):** Phân tích quy trình định lượng (Tính toán Thời gian chu kỳ và Chi phí, gắn số liệu lên sơ đồ) [16, 158] $\rightarrow$ **Hoàn thành Rubric 4 (Chương 5)** [158].
*   **Tuần 5 (17/08 – 23/08/2026):** Vẽ sơ đồ cải tiến **BPMN To-Be** [136], hoàn thiện **mã nguồn ứng dụng BPMS** [32, 138], tổng rà soát định dạng/chính tả [19] và thuyết trình thử $\rightarrow$ **Hoàn thành Rubric 5 (Chương 6, 7 & Báo cáo)** [159].

---

## 📌 PHÂN CÔNG CHI TIẾT CÔNG VIỆC TRONG TUẦN 1 (Hạn chót: 26/07/2026)

Mục tiêu Tuần 1 là hoàn thiện **Chương 1 (Giới thiệu chung về Shopee)** và **Chương 2 (Kiến trúc quy trình tổng gồm 10 quy trình của Shopee)** để nộp bài tập tiến độ [118, 119]:

| Thành viên | Nhiệm vụ chi tiết trong Tuần 1 | Sản phẩm bàn giao (Deliverables) |
| :---: | :--- | :--- |
| **Nhóm trưởng** | - Đăng ký chính thức đề tài Shopee trên hệ thống của thầy [36].<br>- Khởi tạo repository Git, phân quyền cho thành viên và add thầy Trung [200].<br>- Chủ trì họp nhóm vẽ sơ đồ **Kiến trúc quy trình tổng gồm 10 quy trình** [6]. | - Link repository hoạt động.<br>- Sơ đồ kiến trúc quy trình tổng dạng ảnh `.png` [6, 156]. |
| **Nhóm phó** | - Tải mẫu báo cáo khóa luận UIT, tạo khung file Word chuẩn (Trang bìa, Mục lục tự động, Danh mục hình/bảng) [19, 159].<br>- Nhận nội dung từ các thành viên, sửa lỗi chính tả [19], rà soát định dạng nhãn bảng/hình [19] và tổng hợp thành file báo cáo Word hoàn chỉnh [180].<br>- Thiết kế Slide giới thiệu nhóm và sơ đồ kiến trúc quy trình [9, 159]. | - File Word báo cáo tiến độ tuần 1.<br>- Slide giới thiệu đề tài tuần 1 [9]. |
| **Thành viên 3** | - Thực hiện đặt 1 đơn hàng thực tế trên Shopee và thực hiện 1 yêu cầu trả hàng/hoàn tiền để chụp ảnh màn hình làm bằng chứng thực tế [11, 25, 34].<br>- Viết mô tả chi tiết bằng lời cho **4 quy trình Cốt lõi (Core)** của Shopee [54, 117]. Xác định rõ tác nhân (Actor), khách hàng (Customer), hoạt động (động từ) và kết quả (Positive/Negative) cho từng quy trình [4, 156]. | - Tài liệu Word mô tả 4 quy trình cốt lõi.<br>- Thư mục ảnh minh chứng đặt hàng/hoàn hàng [11]. |
| **Thành viên 4** | - Khảo sát và viết mô tả chi tiết bằng lời cho **3 quy trình Hỗ trợ (Support)** của Shopee (ví dụ: Onboarding người bán mới, Giải quyết khiếu nại, Đối soát tài chính) [54, 117]. Xác định rõ Actor, Customer, hoạt động và kết quả đầu ra [4, 156]. | - Tài liệu Word mô tả 3 quy trình hỗ trợ. |
| **Thành viên 5** | - Khảo sát và viết mô tả chi tiết bằng lời cho **3 quy trình Quản lý (Management)** của Shopee (ví dụ: Quản lý chiến dịch sale, Tuân thủ người bán, Quản lý đối tác giao hàng) [54, 117]. Xác định rõ Actor, Customer, hoạt động và kết quả đầu ra [4, 156]. | - Tài liệu Word mô tả 3 quy trình quản lý. |
| **Thành viên 6** | - Soạn thảo nội dung Chương 1: Giới thiệu Shopee, mô hình kinh doanh, sơ đồ tổ chức công ty [11, 21].<br>- Lập Sổ tay định nghĩa các thuật ngữ viết tắt/chuyên môn trong dự án [11].<br>- Hỗ trợ nhóm trưởng thiết lập hạ tầng kỹ thuật ban đầu cho nhóm [12]. | - Tài liệu Word nội dung Chương 1.<br>- File `glossary.md` chứa sổ tay thuật ngữ [11]. |

---
*Chúc nhóm chúng ta có một kỳ làm đồ án đại thành công, đạt điểm số tối đa từ thầy Trung! Hãy luôn nhớ kiểm soát chéo và "đừng để rơi điểm"!* [21, 35]