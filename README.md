# Shopee Business Process Management (BPM) Project 🚀

Chào mừng bạn đến với kho lưu trữ (repository) chính thức của **Nhóm 10 - Lớp IE203.F32.LT.CNTT** dành cho đồ án môn học **Hệ thống Quản trị Quy trình Nghiệp vụ (BPM)** dưới sự hướng dẫn của **ThS. Hà Lê Hoài Trung**.

Đồ án này tập trung nghiên cứu, mô tả, mô hình hóa và cải tiến kiến trúc quy trình nghiệp vụ của sàn thương mại điện tử **Shopee**. Đồng thời, nhóm phát triển ứng dụng điều hành quy trình thực tế (BPMS) dựa trên các quy trình đã tối ưu hóa ở các chương cuối.

---

## 📁 CẤU TRÚC THƯ MỤC REPOSITORY (ÁP DỤNG CHUẨN RUBRIC UIT)

Cấu trúc này tổ chức tương ứng trực tiếp với các chương báo cáo và tiêu chí đánh giá trong Rubric của Thầy:

```text
shopee-bpm-project/
├── .gitignore                  # Bỏ qua các file rác (node_modules, file tạm, .DS_Store, v.v.)
├── README.md                   # Trang chủ giới thiệu nhóm, đề tài Shopee, phân công & tiến độ
│
├── docs/                       # CHƯƠNG 1 & 2: KHẢO SÁT THỰC TẾ & PHƯƠNG PHÁP
│   ├── organization-chart/     # Sơ đồ tổ chức Shopee, mô hình kinh doanh & sổ tay thuật ngữ
│   ├── evidence/                # Minh chứng quan sát thực tế (ảnh chụp các bước mua hàng/hoàn tiền)
│   └── interview/                # Kịch bản khảo sát:
│       ├── qualitative.md      # 10 câu hỏi định tính (5 cấu trúc, 5 không cấu trúc)
│       └── quantitative.md     # 10 câu hỏi định lượng (5 cấu trúc, 5 không cấu trúc)
│
├── models/                     # CHƯƠNG 3 & 6: MÔ HÌNH HÓA QUY TRÌNH (BPMN)
│   ├── process-architecture/   # Sơ đồ kiến trúc quy trình tổng (liên kết tối thiểu 10 quy trình)
│   ├── as-is/                  # Quy trình hiện tại (file gốc .bpmn & ảnh .png):
│   │   ├── management/         # 2 quy trình quản lý (độ phức tạp cổng điều kiện > 7)
│   │   ├── core/                 # 2 quy trình cốt lõi
│   │   └── support/              # 2 quy trình hỗ trợ
│   └── to-be/                  # Quy trình cải tiến (To-be) sau khi tối ưu hóa
│
├── analysis/                   # CHƯƠNG 4 & 5: PHÂN TÍCH ĐỊNH TÍNH & ĐỊNH LƯỢNG
│   ├── qualitative/             # Phân tích định tính:
│   │   ├── va-analysis/        # Bảng phân tích giá trị gia tăng (VA/NVA/BVA - 3 cột: Liệt kê, Mô tả, Khắc phục)
│   │   ├── waste-analysis/     # Bảng phân tích lãng phí (Move, Hold, Overdo - 3 cột: Liệt kê, Mô tả, Khắc phục)
│   │   └── root-cause/          # Sơ đồ xương cá (Fishbone) hoặc Pareto phân tích nguyên nhân gốc rễ
│   └── quantitative/            # Phân tích định lượng:
│       └── calculations.xlsx   # Bảng tính Thời gian chu kỳ (Cycle time) và Chi phí (Cost)
│
├── src/                        # CHƯƠNG 7: ỨNG DỤNG ĐIỀU HÀNH QUY TRÌNH
│   ├── backend/                 # Mã nguồn phía máy chủ
│   └── frontend/                 # Giao diện tương tác hệ thống BPMS
│
└── deliverables/               # SẢN PHẨM BÀN GIAO CHÍNH THỨC NỘP THẦY
    ├── Final_Report_Nhom10.docx # Báo cáo Word chuẩn mẫu khóa luận UIT (nhãn hình dưới ảnh, nhãn bảng trên bảng)
    └── Final_Slide_Nhom10.pptx  # Slide thuyết trình chính thức (mỗi slide tối đa 1 sơ đồ quy trình)
```

---

## 🧭 HƯỚNG DẪN CHI TIẾT TỪNG PHẦN TRONG REPO

### 1. Thư mục `docs/` (Khảo sát thực tế & Kịch bản khảo sát)
- **organization-chart/**: Sơ đồ tổ chức phòng ban và mô hình kinh doanh của Shopee để làm rõ ngữ cảnh. Có file `glossary.md` là sổ tay thuật ngữ chuyên ngành (BPM, Thương mại điện tử, Logistics).
- **evidence/**: Ảnh chụp màn hình thực tế các luồng công việc trên Shopee (đặt hàng, trả hàng/hoàn tiền) làm bằng chứng quan sát.
- **interview/**: Kịch bản phỏng vấn gồm 20 câu hỏi (10 định tính, 10 định lượng), chia đều 5 cấu trúc - 5 không cấu trúc cho mỗi loại.

### 2. Thư mục `models/` (Mô hình hóa BPMN)
- **process-architecture/**: Sơ đồ kiến trúc quy trình 3 lớp của Shopee với tối thiểu 10 quy trình.
- **as-is/**: Sơ đồ quy trình hiện trạng. Mỗi lớp (Quản lý, Cốt lõi, Hỗ trợ) lưu cả file gốc thiết kế (ví dụ `.bpmn` từ Camunda/Bizagi) và file ảnh `.png` tương ứng.
  - ⚠️ Quy trình Quản lý được chọn phải có độ phức tạp cổng điều kiện (split/join) **lớn hơn 7**.
- **to-be/**: Sơ đồ quy trình cải tiến, đã loại bỏ lãng phí và tối ưu thời gian/chi phí.

### 3. Thư mục `analysis/` (Phân tích quy trình)
- **qualitative/**: Bảng phân tích giá trị gia tăng (VA/NVA/BVA) và bảng phân tích lãng phí (tập trung Move, Hold, Overdo trong 8 loại lãng phí). Cả hai bảng bắt buộc có đúng 3 cột: Liệt kê, Mô tả, Khắc phục. Kèm sơ đồ Root-cause (Fishbone hoặc Pareto).
- **quantitative/**: File Excel phân tích thời gian chu kỳ (Cycle time) và chi phí (Cost) trước/sau cải tiến.

### 4. Thư mục `src/` (Phần mềm BPMS)
Mã nguồn hoàn chỉnh của ứng dụng quản trị điều hành quy trình (BPMS), liên kết cơ sở dữ liệu và giao diện người dùng.

### 5. Thư mục `deliverables/` (Sản phẩm bàn giao nộp thầy)
Lưu các phiên bản báo cáo Word và Slide thuyết trình chính thức.
- ⚠️ Nhãn hình ảnh đặt dưới hình, nhãn bảng biểu đặt trên bảng — sai 1 lần bị trừ điểm nặng.
- ⚠️ Mỗi slide thuyết trình chỉ trình bày tối đa **1 quy trình/sơ đồ**.

---
*Chúc nhóm chúng ta có một kỳ làm đồ án đại thành công, đạt điểm số tối đa từ thầy Trung! Hãy luôn nhớ kiểm soát chéo và "đừng để rơi điểm"!*
