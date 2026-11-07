# Báo cáo cá nhân — Day 01: Lọc tin nhắn rác bằng ML, DL, Embedding và LLM

- **MSSV:** 2A202603947
- **Họ và tên:** Lã Quốc Nghị
- **SEED** (in ở ô đầu notebook): 6571

## 1. Bằng chứng

| Tệp | Có? |
| --- | --- |
| [`day01_lab.ipynb`](day01_lab.ipynb) — notebook đã chạy, còn output | ☑ |
| [`lab1_report.json`](lab1_report.json) — do ô "Báo cáo cuối" sinh ra | ☑ |
| [`hand_calc.jpg`](hand_calc.jpg) — ảnh tính tay có các bước | ☑ |

## 2. Kết quả chính
| Cách | F1 (test) | F1 (SUB 40) | p95 ms/tin | USD / 1k tin |
| --- | ---: | ---: | ---: | ---: |
| 1. BoW + LogReg | 0.888 | 0.857 | 0.112 | 0.0 |
| 2. BoW + MLP | 0.902 | 0.857 | 2.448 | 0.0 |
| 3a. Encoder + kNN | 0.893 | 0.974 | 60.925 | 0.0 |
| 3b. Encoder + LogReg | 0.950 | 0.947 | 63.579 | 0.0 |
| 3c. Encoder + MLP head | 0.956 | 0.947 | 104.816 | 0.0 |
## 3. Dự đoán và thực tế

*Chọn 3 dự đoán `predict(...)` lệch nhiều nhất so với kết quả. Mỗi cái: bạn đoán gì, ra gì, vì sao lệch.*

## 4. Phân tích 50 case khó

*Model nào tụt nhiều nhất, ở nhóm case nào? Nêu 2 case cụ thể và cơ chế khiến model sai.*

## 5. Thử thách cá nhân

*Đề theo SEED của bạn, cách làm, kết quả, giải thích.*

## 6. Phương án cho sản phẩm thật
*Với yêu cầu p95 < 50 ms/tin cho 10 triệu SMS/ngày: chọn phương án nào, dẫn số liệu nào, chấp nhận đánh đổi gì.*
> Chọn: BoW + LogReg, Dẫn số liệu: F1 test 0.888, F1 SUB 0.857, p95 0.112 ms (<< 50 ms), 0 USD/1k tin. Chấp nhận đánh đổi Recall BoW ~0.80, có thể sẽ có spam lọt qua

## 7. AI log và điều đã học

*Mỗi lần dùng AI: hỏi gì, nhận gì, bạn sửa gì. Sau đó 2–3 câu: điều bạn hiểu ra hôm nay mà trước đó chưa hiểu.*
> Nhờ AI implement call_openai / parse_label / llm_classify_batch phần 4, nhận lại code, sửa lại code và chạy test. Học được cách implement AI api bằng code python
