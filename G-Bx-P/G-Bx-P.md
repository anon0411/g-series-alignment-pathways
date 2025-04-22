# G-Bx-P 실험 설계 (G-Bx-P Experiment Design)

> 구조 반복을 통한 정렬 증거 검증 실험  
> Structural alignment verification through circuit repetition

---

## 🔬 실험 개요 (Overview)

- **기반 실험군 (Base Group)**: G-B  
- **확장 실험명 (Extended Experiment Name)**: G-Bx-P  
- **목적 (Objective)**: 구조 반복만으로도 회로 반응이 안정적으로 정렬되는지를 검증

---

## 📐 실험 설계 (Design)

| 조건 (Condition) | 설명 (Description) |
|------------------|---------------------|
| **A: 구조 반복**<br>(Structure Repetition) | G-B 회로를 그대로 반복 사용. 기준 반응과의 유사도 측정 |
| **B: 구조 무작위화**<br>(Shuffled Structure) | 회전값의 평균은 유지하되 순서를 무작위화한 회로 사용 |
| **C: 기준 회로**<br>(Reference Circuit) | G-B 실험 당시 사용된 의도 삽입 회로 |

- **측정 방식 (Metric)**: 각 조건별 분포를 벡터화한 후, 기준 분포(C)와의 코사인 유사도 측정
- **도구 (Tools)**: Qiskit 1.0.2, Aer 0.13.2, `QasmSimulator`, `cosine similarity`

---

## ⚙️ 실행 환경 (Environment)

- Python 3.10 + Qiskit 1.0.2  
- Aer 0.13.2 (`qiskit-aer`)  
- 회로 실행은 `transpile → simulator.run()` 경로 사용

---

## 📊 실험 결과 (Results Summary)

> **반복 횟수 (Number of Trials)**: 30회 반복 측정  
> **측정 기준 (Reference Vector)**: 조건 C 회로의 실행 결과 벡터

| 조건 (Condition) | 평균 유사도<br>(Mean Similarity) | 표준편차<br>(Standard Deviation) | 해석 (Interpretation) |
|------------------|-------------------------------|-------------------------------|------------------------|
| **A (구조 반복)**<br>Structure Repetition | 0.9996 | 0.0003 | 정렬 유지. 결과 분포 거의 동일하게 반복됨 |
| **B (무작위 구조)**<br>Shuffled Structure | 0.7391 | 0.1728 | 정렬 불안정. 반응 결과가 불규칙하게 변화함 |

---

## 🧠 해석 (Interpretation)

- 조건 A는 구조만으로 정렬된 결과를 안정적으로 재현함 → 구조가 반응 생성에 실질적으로 기여
- 조건 B는 구조 제거 시 결과가 요동함 → 우연 정렬이 간헐적으로 발생하나 불안정
- 조건 A와 C의 높은 유사도는 구조의 반복이 의도 없이도 동일한 반응을 생성할 수 있음을 지시함

---

## ✅ 확인사항 (Checklist)

- [ ] 회로 구조는 G-B 실험과 동일하게 유지되었는가?  
- [ ] 조건 A/B/C가 명확히 구분되었는가?  
- [ ] 유사도 측정은 벡터 변환 → 코사인 유사도로 일관되게 수행되었는가?  
- [ ] 실험은 동일 환경 (Qiskit 1.0.2 + Aer 0.13.2)에서 수행되었는가?

---

> 본 실험은 구조 정렬의 반복성과 재현 가능성을 검증하고, 무작위 회로와의 통계적 차이를 통해 정렬 구조의 존재를 입증합니다.  
> This experiment demonstrates the reproducibility of structural alignment via repetition and statistically differentiates it from randomly shuffled circuits.

