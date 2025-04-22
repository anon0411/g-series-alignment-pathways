# 🧪 G-Ex-P 구조 반응성 임계 실험 (Threshold Analysis of Structural Generalization)

## 📘 실험 개요 (Experiment Overview)

본 실험은 G-Ex-P 실험의 후속으로, 구조가 외부 입력 변화에 얼마나 견고하게 반응을 유지하는지를 정량적으로 측정합니다.
즉, 구조 반응성이 유지되는 "노이즈 허용 한계"를 탐색하여 구조 기반 반응의 일반화 가능성의 경계를 파악하고자 합니다.

This experiment is a follow-up to G-Ex-P, aiming to quantitatively determine how robustly a fixed structure can generalize across increasing external input noise. It identifies the boundary at which structural generalization begins to break down.

---

## 🎯 실험 목적 (Objective)

- 구조적 반응의 일반화 임계값 확인
- 입력 변화(B)의 노이즈 크기 증가에 따른 구조 반응성(A-B 유사도)의 유지 여부 확인
- 구조가 없는 조건(C)과의 비교를 통해 구조의 효과(G_ex > 1 여부) 정량화

---

## ⚙️ 실험 조건 (Experimental Conditions)

- 회로 구조: G-A 구조 기반 RY 회전
- 입력 노이즈: 0.00 ~ 0.60 (0.05 간격)
- 반복 횟수: 각 조건당 10회 반복
- 측정 항목: A-B 유사도, B-C 유사도, G_ex = A-B / B-C

---

## 📊 요약 결과 (Summary Results)

| 노이즈 (Noise) | G_ex 평균 | G_ex 표준편차 | A-B 유사도 평균 | B-C 유사도 평균 |
|----------------|------------|----------------|-------------------|-------------------|
| 0.00           | 4.75       | ±3.17          | 0.997             | 0.349             |
| 0.05           | 6.19       | ±7.62          | 0.996             | 0.333             |
| 0.10           | 2.64       | ±1.95          | 0.987             | 0.555             |
| 0.35           | 5.43       | ±1.61          | 0.924             | 0.183             |
| 0.40           | 4.81       | ±5.55          | 0.892             | 0.406             |
| 0.45           | 27.00      | ±67.96         | 0.831             | 0.321             |
| 0.50           | 2.09       | ±2.36          | 0.863             | 0.638             |
| 0.55           | 86.85      | ±223.92        | 0.845             | 0.233             |
| 0.60           | 15.66      | ±29.72         | 0.823             | 0.289             |

---

## 🔍 해석 (Interpretation)

- **G_ex > 1이 유지되는 영역**은 구조가 입력 변화에도 효과적으로 반응을 유지하는 구간입니다.
- **0.45 이후부터 A-B 유사도가 급격히 하락하고, G_ex의 분산이 급등**하며 구조 반응성이 불안정해집니다.
- 이에 따라 구조 반응성의 보수적 임계점은 **0.40**, 관측적 경계는 **0.45**로 제안됩니다.

The zone where **G_ex > 1** indicates sustained structural generalization. After **noise ≥ 0.45**, both the stability of A-B similarity and the consistency of G_ex collapse, suggesting a breakdown in structural response. The conservative threshold is **0.40**, with observed collapse beginning around **0.45**.

---

## ✅ 결론 (Conclusion)

본 실험은 구조 반응의 일반화 범위를 계량화하였으며, 구조의 유의미한 영향력이 어느 수준의 입력 변화까지 유지되는지를 확인하였습니다.

This experiment quantifies the boundary of structural generalization and identifies how far structural influence persists under increasing perturbations in input.

---

