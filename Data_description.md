# 📊 Dataset Description: Telco Customer Churn
**프로젝트 명: 통신사 고객 이탈 데이터 분석 및 예측 모델링**

## 1. 개요 (Overview)
- **데이터 출처**: IBM Sample Data / Kaggle (Telco Customer Churn)
- [cite_start]**데이터 설명**: 캘리포니아 지역 고객 7,043명의 통신 서비스 이용 데이터를 포함하고 있습니다. [cite: 15]
- [cite_start]**주요 목표**: 고객 행동 데이터를 분석하여 이탈(Churn) 여부를 예측하고, 유지(Retention) 전략을 제안합니다. [cite: 25]

---

## 2. 데이터 구성 (Data Dictionary)

[cite_start]본 프로젝트는 MVP 모델 개발을 위해 가장 영향력이 큰 5개의 핵심 변수와 타겟 변수를 선정했습니다. [cite: 16]

| 컬럼명 (Column) | 설명 (Description) | 데이터 타입 | 비고 (Remarks) |
| :--- | :--- | :--- | :--- |
| **gender** | 고객의 성별 | Categorical | Male: 1, Female: 0 |
| **SeniorCitizen** | 고령자 여부 | Binary | 0 (No) / 1 (Yes) |
| **tenure** | 서비스 가입 기간 (월) | Numeric | 1 ~ 72개월 |
| **Contract** | 서비스 계약 형태 | Categorical | Month-to-month(0), One year(1), Two year(2) |
| **MonthlyCharges** | 매월 청구되는 요금 | Numeric | 단위: USD ($) |
| **Churn (Target)** | 고객의 이탈 여부 | Binary | Yes: 1, No: 0 |

---

## 3. 데이터 전처리 (Data Preprocessing)

[cite_start]데이터를 AI 모델에 학습시키기 위해 다음과 같은 전처리를 수행했습니다. [cite: 28, 42]

* [cite_start]**인코딩 (Encoding)**: 범주형 데이터(gender, Contract)를 수치 데이터로 변환했습니다. [cite: 28]
* [cite_start]**결측치 처리 (Missing Values)**: 데이터의 안정성을 위해 결측치는 `0`으로 처리했습니다. [cite: 19]
* [cite_start]**데이터 분할 (Split)**: 전체 데이터를 8:2 비율로 학습용(Train)과 테스트용(Test) 데이터로 나누었습니다. [cite: 16]

---

## 4. 활용 모델 (Machine Learning Models)

[cite_start]본 데이터는 다양한 알고리즘의 성능 비교를 위해 사용됩니다: [cite: 28, 29]
* [cite_start]**Logistic Regression**: 선형 분류 기반의 기초 모델 [cite: 28]
* [cite_start]**Random Forest**: 결정 트리 기반의 앙상블 모델 [cite: 30]
* [cite_start]**XGBoost**: 고성능 그래디언트 부스팅 모델 [cite: 28]
* [cite_start]**Deep Learning (ANN)**: 다층 신경망 구조의 딥러닝 모델 [cite: 29]

---

## 5. 기대 성과 (Business Impact)

* [cite_start]**이탈 방지**: 고위험 고객 선제적 관리로 매출 손실 방지 [cite: 26, 35]
* [cite_start]**비용 절감**: 불필요한 마케팅 비용 줄이고 효율적인 자원 배분 가능 [cite: 36, 37]
* [cite_start]**데이터 기반 의사결정**: 과학적 수치에 기반한 마케팅 전략 수립 [cite: 49]