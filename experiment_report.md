# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600236
**Name:** Nguyễn Văn Quang
**Date:** 14/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200. | 10 | Trả lời đúng kết quả với category Electronics và có giá cao nhất |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | 2 | Trả lời đúng kết quả với category Electronics và có giá cao nhất, tuy nhiên đây không nên là sản phẩm được đề xuất cho người dùng phổ thông. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

> Nếu kết hợp logic validate data ở solution.py (price > 0 và category không rỗng) và logic của agent_simulation (Look for the product with highest price or matching category), thì kết quả trả về là hợp lệ. Tuy nhiên, để trả lời câu hỏi "What is the best electronic product?", câu trả lời nên là 1 sản phẩm phổ thông, là Laptop $1200. Đây là vấn đề liên quan đến outlier, khiến câu trả lời trả về kết quả từ dữ liệu ngoại lai đó. 
---

## 3. Ket luan

**Quality Data > Quality Prompt?** 

> Tôi đồng ý về việc chất lượng data quan trọng hơn chất lượng prompt, vì dữ liệu là nền tảng của câu trả lời của LLM, việc tạo ra 1 prompt chất lượng nhưng kết quả retrieve về bị sai, LLM cũng sẽ trả lời sai.