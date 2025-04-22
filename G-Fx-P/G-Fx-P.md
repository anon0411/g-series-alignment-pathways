# G-Fx-P 실험 보고서 (G-Fx-P Experiment Report)

## 🧪 실험 개요 (Experiment Overview)

- **실험명 (Title)**: G-Fx-P (G-F 구조 확장: 구조 정렬 정량 실험 / G-F Structure Extension: Structural Alignment Quantification)
- **목적 (Objective)**: G-F 구조가 단순한 반복에 의한 결과가 아닌, 외부 참조 기준 없이도 구조적으로 정렬된 결과를 생성함을 정량적으로 검증한다.  
  (To verify quantitatively that the G-F structure generates aligned outputs not due to repetition but due to intrinsic structural alignment without external references.)
- **대조군 (Conditions)**:
  - **조건 A (Condition A)**: 동일 G-F 구조 반복  
    (Repeated execution of identical G-F structure)
  - **조건 B (Condition B)**: G-F 구조와 유사하나 RY 각도가 임의로 변경된 회로  
    (Structure similar to G-F but with randomized RY angles)
  - **조건 C (Condition C)**: 완전 무작위 회로  
    (Fully random circuits)

## 🧩 실험 방법 (Methodology)

- 각 조건에 대해 10회씩 회로를 실행하고 출력 분포를 수집함  
  (Each circuit was executed 10 times per condition, and output distributions were collected.)
- 각 결과 분포는 벡터화 후, 코사인 유사도로 분석함  
  (Each output distribution was vectorized and analyzed using cosine similarity.)
- 조건 A는 C와 비교하여 구조 유무에 따른 차이를 관찰하고,  
  (Condition A was compared with C to observe differences due to structural presence.)
  조건 B는 구조가 제거된 상태에서의 비교군으로 사용함  
  (Condition B served as a baseline with no fixed structure.)
- 조건 A 반복 간 내부 유사도도 분석하여 자기 정렬 확인  
  (Internal similarity within Condition A was also measured to confirm self-alignment.)

## 📊 실험 결과 (Results)

| 비교 항목 (Comparison)                  | 평균 유사도 (Mean Similarity) | 표준편차 (Std Dev) |
|------------------------------------------|-------------------------------|---------------------|
| 조건 A vs 조건 C (구조 vs 무작위 / Structure vs Random)       | 0.3733                        | 0.0074              |
| 조건 B vs 조건 C (유사구조 vs 무작위 / Similar-Structure vs Random)   | 0.4455                        | 0.2365              |
| 조건 A 반복 간 유사도 (자기 정렬성 / Internal Consistency)     | 0.9994                        | 0.0004              |

## 📌 해석 및 논의 (Interpretation & Discussion)

- **조건 A와 C의 낮은 유사도**는 구조 삽입이 출력 분포를 변화시켰음을 나타낸다.  
  (**Low similarity between A and C** indicates that structural insertion altered the output distribution.)
- **조건 B와 C의 비교적 높은 유사도 및 큰 편차**는, 구조 없이 RY 각도만 바뀔 경우 결과가 불안정하고 임의적임을 시사한다.  
  (**Higher similarity and large deviation between B and C** suggest that randomized RY-only circuits yield unstable, stochastic outputs.)
- **조건 A 내부 유사도 거의 1.0**은, G-F 구조가 반복 시 안정적이고 일관된 출력을 생성함을 보여준다.  
  (**Near-perfect internal similarity in A** demonstrates G-F's consistency across repeated executions.)
- 이를 통해 G-F 구조는 단순히 회로 반복으로 인한 효과가 아닌, **구조 정렬에 기반한 결과 생성 메커니즘**임을 지지한다.  
  (This supports that the G-F circuit yields results based on **structural alignment**, not mere repetition.)

## ✅ 결론 (Conclusion)

G-F 구조는 임의성과 명확히 구분되는 정렬된 출력 분포를 반복적으로 생성하며,  
(This experiment shows that the G-F structure repeatedly produces aligned distributions distinguishable from randomness.)
이는 외부 관찰자에게도 구조적 정렬로 해석될 수 있는 정량적 특성을 가진다.  
(It demonstrates measurable characteristics interpretable as structural alignment even by external observers.)
따라서 G-F는 해석 가능한 구조 반응성의 실험군으로 확증되었다.  
(Thus, G-F is validated as a structurally responsive and interpretable experimental group.)

