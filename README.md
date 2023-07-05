### 팀 정보
- 팀 이름: Data Achiever
- 참여자 이름 :  임나래, 유하민, 이현준, 이재은
- 프로젝트 명 : 이커머스 플랫폼 문제 진단

2) **단계별로 주어진 질문들을 읽고, 팀원들과 논의하여 도출한 내용을 작성하세요. 분량은 자유 입니다.** 

### Step 1-3 : 비즈니스 의미 부여

| 1. 프로젝트를 통해 해결하려고 했던 문제는 무엇이었나요? 왜 이런 프로젝트를 기획하고 실행했나요?  |
| --- |
| 본 프로젝트는 인도네시아 패션 이커머스 기업 ‘패션캠퍼스’ 에서의
최근 2개월 동안의 매출 하락 문제를 해결하고자 기획했습니다.
데이터 분석을 통해 기업의 충성도 높은 고객 그룹의 이탈이 발생하고 있는 것을 확인했고,
이를 막고 과거의 충성도 높은 고객을 다시 활성화시켜 매출 회복 및 회사의 성장을 도모하고자 했습니다. |

| 2. 이 문제는 왜 중요한가요? 이 문제를 해결하면 어떤 가치(benefit)이 있을까요? 왜 그렇게 생각하시나요?  |
| --- |
| 신규 고객의 유입이 지속적으로 이루어지고 있음에도 불구하고, 매출이 급격히 감소하는 문제가 발생하였습니다. 
이 문제의 원인을 충성도 높은 고객군의 이탈 및 타겟화되지 않은 프로모션으로 파악하였으며, 
이에 따라 기존 고객의 재구매를 유도함으로써 매출 회복이 가능하다고 판단하였습니다.
 이렇게 고객 이탈을 방지하고, 고객 충성도를 확보하는 것은 매출 회복에 큰 도움이 될 것으로 예상했습니다. |

| 3. 이 문제를 똑같이 느낄 만한, 혹은 관심있어 할 만한 사람들(회사, 분야 등)은 누구일까요?  |
| --- |
| 본 프로젝트에 관심을 가질 수 있는 관계자는 (패션)이커머스 기업의 기획자, 마케팅 담당자, 그리고 UX/UI 담당자 등 입니다. |

### Step 4-7 : 프로젝트 과정 정리

| 4. 어떤 과정을 거쳐 프로젝트를 진행했나요? 팀원들의 역할 분담도 기재해 주세요.   |
| --- |
| 1. 사전 기획 : 데이터 파악, 외부 데이터 수집, 상품/비지니스/유저 측면의 데이터 EDA |
| 2. 데이터 탐색 : 정의 된 문제와 목표에 따른 데이터 정제 및 정규화 |
| 3. 데이터 분석 : 고객 세분화, 세그먼트 별 데이터 분석, 퍼널분석, 이탈함수 제작  |
| 4. 이탈모형 제작 : 이탈 판별 지표 선정 , 이탈 모형 제작, 모형 성능 최적화 및 시각화 |
1. 팀원들의 역할 분담

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fe2b23d3-33ba-4703-b483-567c5595ab0e/Untitled.png)

| 5. 어떤 데이터를 활용했으며, 출처는 어디인가요? 데이터의 특성(크기, 종류 등등)은 어떠한가요?    |
| --- |
|  |

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e8ed91ec-fac3-4d98-b4ad-14a13b49e370/Untitled.png)

| 6. 각 팀원들은 어떤 업무를 수행하셨나요? 그 업무를 수행하기 위해 어떤 일을 하셨나요? 어떤 알고리즘, 모델, 기법 등을 사용했나요? 각 팀원별로 구분하여 작성해 주세요.   |
| --- |
| 임나래

▶ 개발 환경: Colab, VSCode, Github 
▶ 사용 언어: Python 
▶ 라이브러리: pandas, numpy, datetime, sklearn, imblearn.over_sampling, matplotlib.pyplot 
▶ 주 사용 코드 :  merge, groupby, cut

-Product 관점에서의 Data EDA
Product 관점에서의 카테고리별 매출(연/월)
카테고리별 구매 고객의 인구통계학적 분석, 구매패턴 분석

- Age Segmentation 
연령 세분화 및 타겟 연령 선정 
연령에 따른 제품 구매 추이 파악
방문빈도, 구매전환율 , 객단가, Average Order Value(AOV) 

- RFM Score Segmentation
R(3),F(2),M(2) 등급 부여하여 고객 세분화 및 세그먼트 별 RFM 지표 분석 
기간별(연/월) 세그먼트 매출 추이 분석 
Average Transaction Value(ATV), 객단가

- 미구매 고객의 퍼널분석 
미구매 고객의 성별, 연령에 따른 Segmentation
session_id별 이벤트 및 경로 분석

- 이탈 모형 제작 : LightGBM 
학습 모델의 타겟 불균형 해소 : upsampling(SMOTE, Random Over Sampler), 
gridsearchCV를 통한 최적의 파라미터 도출 후 모델 성능 비교
성능 지표 :  confusio matrix, classification matrix, roc auc curve  |
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
| 이현준

▶ 개발 환경: Colab, VSCode, Github 
▶ 사용 언어: python
▶ 라이브러리: pandas, numpy, matplotlib, seaborn, pyplot, sklearn, imblearn, hyperopt

- 인도네시아 시장 조사
문제 상황에 영향을 미치는 외부 요인이 있는지 분석하기 위해 
인도네시아 현지 상황, 의류산업 등을 조사하여 팀원들과 공유
인도네시아 패션시장 현황에 대한 자료를 조사하여 선호 브랜드, 중고 의류 시장 성장에 대해 조사

- 중고 관련 EDA
매년 중고 관련 검색횟수와 회원 중 중고를 검색하는 비율이 증가하는 것을 확인

- 구매, 방문 분석
문제기간 동안 구매 및 방문횟수가 감소한다는 사실 파악
원인 파악을 위해 주기, CVR, 나이, 성비 등의 관점에서 분석하였으나 인사이트 도출 실패

- XGBClassifier 모델 제작
타겟 불균형 해소를 위해 SMOTE를 이용한 upsampling 사용
RandomSearchCV, BayesianSearch를 통해 하이퍼 파라미터 튜닝 후 성능 비교  |
| 이재은

▶ 개발 환경 : Colab, VS code
▶ 사용 언어 : python
▶ 라이브러리 : pandas, numpy, matplotlib, plotly, sklearn

promotion
- (by age, gender, date etc.)을 팀원들에게 공유하면서 promotion에 문제가 있음을 파악

transaction
- 월별 sales 분석을 통한 문제 발견

customer
- first_join_date 기준으로 신규고객 증가 파악

random forest 이탈모델 제작
- upsampling - class weight, 최적화 - gridsearchcv)

해외 자료 수집
- 인도네시아 내 동종 업계에 있는 패션이커머스에서 중고로 성공한 케이스, 
인도네시아에서의 10-20대의 중고 선호) |
|  |

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

## 📸 회의 진행 캡쳐 화면

- 날짜와 시간, 팀원의 얼굴이 모두 나오도록 캡쳐해주세요.
- 오전, 오후 모두 팀 회의를 진행했다면 각각 오전 중 1번, 오후 중 1번 총 2장의 사진을 넣어주세요 🙂
    - 한 번만 진행했다면 한 장의 사진만 넣어주시면 됩니다.

[]()

<aside>
📝 **프로젝트 소화하기 결과물 자동제출 (오후 6시 15분)**

</aside>

📢 프로젝트 소화하기 결과는 **오후 6시 15분 이후 코드스테이츠 크루가 직접 해당 페이지의 [내보내기] 기능을 활용해 결과물을 확보**할 예정입니다. 

📢 위 내용은 **오후 4시까지 1차 작성 완료하시고, 4시 이후 추가 사항을 기입하는 경우에는 오후 6시 15분 내로 꼭 종료**되어야 합니다.
