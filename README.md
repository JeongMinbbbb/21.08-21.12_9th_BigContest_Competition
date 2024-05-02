# 제9회 빅콘테스트 데이터 분석 공모전 (2021.08-2021.12)

## 주제: KBO 배럴 정의 및 타자 성적 예측
> 이 프로젝트는 제9회 빅콘테스트 데이터분석 분야 챔피언리그 스포츠테크에서 진행되었으며, 전체 대회에는 1307개 팀이 참가한 국내 최대 규모의 데이터 분석 경진대회입니다.

### 분석 목적
- 미국 리그에서 유래된 배럴 지표(좋은 타구의 생산 빈도)를 국내 리그에 도입하는 것의 적합성을 평가합니다.
- 한국형 배럴 지표를 정의하고, 이를 활용하여 타자의 시즌 잔여 경기 성적을 예측합니다.
- 예측 모델을 기반으로 유용한 인사이트를 도출합니다.

### 분석 과정
1. **한국형 배럴 지표 정의**
   - 기존 배럴 지표의 국내 도입 적합성을 검토합니다.
     ![image](https://github.com/JeongMinbbbb/21.08-21.12_BigContest_9th/assets/130365764/8c79e809-d4be-472e-9c27-dd87a090d9e3)

   - 8년치 데이터를 기반으로 두 리그 간의 타율 및 장타율 차이를 분석하여 한국형 배럴 지표에 반영합니다. 추정된 신뢰구간들이 공통적으로 포함하는 범위를 계산하고 그 범위의 중앙값 0.026을 타율 차이의 대표값으로 채택합니다.
   - 타율 0.526, 장타율 1.5를 한국형 배럴의 선별 기준으로 설정합니다.
   - 야구장의 비거리와 담장 높이를 계산하여 물리적인 가능성을 추가로 고려합니다.
     ![image](https://github.com/JeongMinbbbb/21.08-21.12_BigContest_9th/assets/130365764/fd70494b-d543-4952-ac4a-6acbe678a3d7)


2. **성적 예측 모델링**
   - 지수평활법을 활용하여 미래 시점의 잔여 경기를 대표하는 데이터셋을 생성합니다.
   - 최적의 변수를 선정하고, XGBoost와 Random Forest를 사용하여 기존 데이터를 학습합니다.
   - 생성된 잔여 경기 데이터셋을 모델에 입력하여 최종 성적 예측치를 도출합니다.

3. **활용 방안**
   - 선수 예시를 들어 전략적 활용 방법(저평가 선수 발굴, 연봉 반영, 타순 반영 등)을 제안합니다.
   - 예시: 저평가된 선수 발굴 (노시환과 페르난데스 비교)
      <p align="left">
        <img src="https://github.com/JeongMinbbbb/21.08-21.12_BigContest_9th/assets/130365764/07953fb7-5f02-4326-aa27-1f061c8c70a2" alt="image">
      </p>

### 분석 결과 및 성과
- 타자 성적 예측 모델의 성능:
   - 출루율 예측 R-squared: 0.896, MAE: 0.0141
   - OPS 예측 R-square: 0.971, MAE: 0.0211
- 성과: 252개 팀 중 상위 6% 달성, 모델의 설명력 30%p 향상

### 프로젝트 의의 및 성장한 점
1. 통계학 이론을 응용하여 창의적인 방법으로 문제를 해결
2. 미래를 통찰하는 분석 능력을 입증
3. 분석의 필요성을 지속적으로 고민하는 습관을 양성
4. 도메인 사전 지식을 활용하여 프로젝트 품질 향상

### Team Project
#### 팀 구성: 배정민 (팀장), 이한재, 조용민, 김해인
#### 소속: 동국대학교 통계학과
