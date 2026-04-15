[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23573968&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** 26ai.quangnv@vinuni.edu.vn

**Name:** Nguyễn Văn Quang

---

## Mo ta

Bài lab giới thiệu concept cơ bản của Data Engineering - ETL (Extract - Transform - Load)

---

## Cach chay (How to Run)

### Prerequisites
```bash
python -m venv venv
# linux: source .venv/bin/activate 
# windows: .\venv\Scripts\activate
pip install pandas pytest
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Tổng có 5 record, 3 record hợp lệ, 2 record bị loại.