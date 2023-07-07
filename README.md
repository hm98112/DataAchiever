# 이커머스 플랫폼 문제 진단 프로젝트
### 팀 정보
- **팀명:** Data Achiever
- **팀원:**  임나래(팀장), 유하민, 이현준, 이재은
- **프로젝트 명:** 이커머스 플랫폼 문제 진단


### 1. 문제정의 및 프로젝트 목표

<p align="center">
    <img src="https://github.com/hm98112/DataAchiever/assets/120023920/1e628dfa-5c0e-4e26-86e9-51f0084a12b5" alt="signup-graph"/><br/>
    [ 매년 회원가입 고객 수 (22년 07월 집계) ]
</p>
<p align="center">
  <img src="https://github.com/hm98112/DataAchiever/assets/120023920/aa5a3473-2c89-41a7-b06d-d59434ff43f9" alt="sales-graph"/><br/>
    [ 연간 매출 추이 ]
</p> 
&nbsp;본 프로젝트는 인도네시아 패션 이커머스 기업 ‘패션캠퍼스’의 데이터를 통해 매출 하락의 원인을 분석하고 이를 개선하는 것을 목표로 한다.<br/>
위 두 그래프에서 보이듯 매년 회원가입 수와 매출이 증가했지만 최근 2개월의 매출 하락이 눈에 띄는 것을 확인할 수 있다.<br/>
&nbsp;간단한 EDA 과정에서 통계적 기법인 RFM 구분을 통해 기업의 충성도 높은 고객 그룹의 이탈이 매출 하락의 주요한 원인으로 진단했다. 이커머스에서 사용하는 지표 분석을 통해 충성도 높은 고객과 그렇지 않은 고객의 유의미한 차이가 발생하는 요인을 파악하고 개선하는 액션을 도출한다.
이를 통해 기존 고객의 이탈을 예방하고 과거의 충성도 높았던 고객의 재구매를 유도해 매출 회복 및 회사의 성장에 기여한다.

### 2. 프로젝트 기대효과 및 타당성
고객 이탈을 방지하고, 고객 충성도를 확보하는 것을 통해 매출의 회복이 기대된다.<br/>
타겟 그룹을 명확하게 선정하고 분석함으로 경제성이 높은 액션으로 이어진다.<br/>

### 3. 프로젝트 진행 과정 및 역할 분담
1) 사전 기획 : 데이터 파악, 외부 데이터 수집, 상품/비지니스/유저 측면의 데이터 EDA<br/>
2) 데이터 탐색 : 정의 된 문제와 목표에 따른 데이터 정제 및 정규화<br/>
3) 데이터 분석 : 고객 세분화, 세그먼트 별 데이터 분석, 퍼널분석, 이탈함수 제작<br/>
4) 이탈모형 제작 : 이탈 판별 지표 선정 , 이탈 모형 제작, 모형 성능 최적화 및 시각화<br/>

5) 팀원들의 역할 분담<br/>

![image](https://github.com/hm98112/DataAchiever/assets/120023920/90bba0f4-8c60-4c21-9f23-792b4e661594)


### 4. 데이터 출처 및 정보
데이터출처: [kaggle fashion campus](https://www.kaggle.com/datasets/latifahhukma/fashion-campus)
![image](https://github.com/hm98112/DataAchiever/assets/120023920/308a3c12-37c9-421e-aa5f-55e074ff5eaa)




| 6. 각 팀원들은 어떤 업무를 수행하셨나요? 그 업무를 수행하기 위해 어떤 일을 하셨나요? 어떤 알고리즘, 모델, 기법 등을 사용했나요? 각 팀원별로 구분하여 작성해 주세요.   |
| --- |
|
| 유하민

▶ 개발 환경: vscode(jupyter notebook), github
▶ 사용 언어: python
▶ 라이브러리: pandas, numpy, datetime, sklearn, imblearn.over_sampling, matplotlib.pyplot

-세션 분할 진행
Groupby, diff 를 통해 하나의 세션 아이디에서 각 이벤트의 시간 차이를 계산
이벤트 시간 갱신이 30분이 넘어가는 데이터에 대해 새로운 세션 아이디를 부여하여 
새로운 새션으로 재정의하여 분석에 사용

-세션 관련 행동 분석
새로 재정의 된 세션을 사용하여 각 고객의 특성 분석
평균 세션 수(방문), 세션 지속시간, 세션의 마지막 이벤트 비율 분석 등

-이탈 판별 함수 작성
마지막 구매를 기준으로 25일 동안 재구매가 이루어지지 않는 고객에 대해 
월별 이탈여부를 판별하는 함수 작성

-모델 학습 데이터 생성
분석한 내용을 총합하여 주요 특성을 선정하여 타겟과 결합한 학습 데이터프레임 생성

-로지스틱 분류 모델 학습
타겟 불균형 해소를 위해 smote,svmsmote 를 통한 오버샘플링 진행하여 실험
타겟 불균형 해소를 위해 Pandas 조건식을 이용한 다운샘플링 진행하여 실험
gridsearch를 통한 하이퍼 파라미터 조정 |


| 7. 프로젝트 결과는 어떤가요?   |
| --- |
| 분석을 통해 지금까지 진행해 온 프로모션의 문제점이 고객 이탈 및 매출 하락에 영향을 미쳤다고 판단하였고, 
고객을 세분화하여 타겟화 된 프로모션을 통해 매출 회복 및 향상을 기대합니다. |

### Step 8-10 : 회고 및 발전 가능성

| 8. 잘 한 점, 만족한 점은 무엇인가요?  |
| --- |
| 프로젝트의 성공적 진행을 위해 팀 내에서 자주 회의를 진행하고, 
깃헙을 통해 코드 공유 및 리뷰를 하며 상호 피드백을 적극적으로 주고받았습니다. 
이는 프로젝트의 방향성을 잡는 데 큰 도움이 되었습니다. 
또한, 고객을 세분화 하여 타겟화 된 액션아이템을 수립하는 방향으로 프로젝트를 진행하여, 
단순히 ‘매출을 올리겠다’ 는 목표보다 더욱 현실적이고 명확한 목표 수립을 할 수 있었습니다. 
더불어, 분석 및 모델링을 위해 끝까지 노력한 점도 프로젝트의 성공 요인으로 작용하였습니다. |

| 9. 아쉬운 점, 한계점은 무엇인가요?  |
| --- |
| 프로젝트 진행 중 UX/UI , 검색 키워드, 프로모션 관련 정보의 부재 등 데이터상의 한계점이 있었습니다. 
또한, 각자 나눠 분석한 파일을 합치는 데 시간이 오래 소요됨으로써, 목표 수립이 지연되며 
시간 분배에 어려움이 있었습니다. 이로 인해 모델 업그레이드나 모델 실험에 충분한 시간을 투자하지 못한 점이 아쉬웠습니다. |

| 10. 다시 한다면 어떤 점을 개선하고 싶은가요?  |
| --- |
| 시간 분배에 주의를 기울여 효율적인 진행을 도모하고, 이탈 모델의 업그레이드를 진행하고 싶습니다. 
추가로, 도메인 지식과 지표에 대한 공부를 통해 더 효율적으로 분석을 진행하고, 
액션아이템 실행 시 추후 기대 효과에 대한 수치를 제시하여 본 분석에 대한 신뢰도를 높이고 싶습니다. |


