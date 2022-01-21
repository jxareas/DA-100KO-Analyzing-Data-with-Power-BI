---
lab:
    title: 'Power BI Desktop에서 데이터 분석 수행'
    module: '모듈 10 - 고급 분석 수행'
---


# **Power BI Desktop에서 데이터 분석 수행**

**랩을 완료하는 데 예상되는 시간은 45분입니다.**

이 랩에서는 **판매 탐색** 보고서를 만듭니다.

이 랩의 학습 내용은 다음과 같습니다.

- 애니메이션 분산 차트 만들기

- 시각적 개체를 사용하여 값 예측

- 분해 트리 시각적 개체를 사용하여 작업하기

- 주요 영향 요인 시각적 개체를 사용하여 작업하기

### **랩 스토리**

이 랩은 데이터를 준비하여 보고서와 대시보드로 게시하는 전체 스토리로 제작된 랩 시리즈에 포함되어 있는 여러 랩 중 하나입니다. 랩은 원하는 순서로 완료하면 됩니다. 그러나 여러 랩을 진행하려는 경우 처음 10개 랩은 다음 순서로 수행하는 것이 좋습니다.

1. Power BI Desktop에서 데이터 준비

2. Power BI Desktop에서 데이터 로드

3. Power BI Desktop에서 데이터 모델링, 1부

4. Power BI Desktop에서 데이터 모델링, 2부

5. Power BI Desktop에서 DAX 계산 만들기, 1부

6. Power BI Desktop에서 DAX 계산 만들기, 2부

7. Power BI Desktop에서 보고서 디자인, 1부

8. Power BI Desktop에서 보고서 디자인, 2부

9. Power BI 대시보드 만들기

10. Power BI 페이지를 매긴 보고서 만들기

11. **Power BI Desktop에서 데이터 분석 수행**

12. 행 수준 보안 적용

## **연습 1: 보고서 만들기**

이 연습에서는 **판매 탐색** 보고서를 만듭니다.

### **작업 1: 시작 - 로그인**

이 작업에서는 Power BI에 로그인하여 랩용 환경을 설정합니다.

*중요: 이전 랩에서 Power BI에 이미 로그인했다면 다음 작업부터 진행하세요.*

1. 작업 표시줄에서 Microsoft Edge를 열려면 Microsoft Edge 프로그램 바로 가기를 클릭합니다.

 	![그림 7](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image1.png)

1. Microsoft Edge 브라우저 창에서 **https://powerbi.com** 으로 이동합니다.

 	*팁: Microsoft Edge 즐겨찾기 모음에서 Power BI 서비스 즐겨찾기를 사용할 수도 있습니다.*

1. **로그인** 오른쪽 상단 모서리에 위치)을 클릭합니다.

 	![그림 5](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image2.png)

1. 제공된 계정 세부 정보를 입력합니다.

1. 암호를 업데이트하라는 메시지가 표시되면 제공된 암호를 다시 입력한 다음 새 암호를 입력하고 확인합니다.

 	*중요: 새 암호를 기록해 두어야 합니다.*

1. 로그인 프로세스를 완료합니다.

1. Microsoft Edge에서 로그인 상태를 유지하라는 메시지가 표시되면 **예**를 클릭합니다.

1. Microsoft Edge 브라우저 창의 Power BI 서비스 내 **탐색** 창에서 **내 작업 영역**을 확장합니다.

 	![그림 4](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image3.png)

1. Microsoft Edge 브라우저 창을 열어 둡니다.

### **작업 2: 시작 - 데이터 세트 만들기**

이 작업에서는 데이터 세트를 만들어 랩용 환경을 설정합니다.

*중요: **Power BI 대시보드 만들기** 랩에서 데이터 세트를 이미 게시했다면 다음 작업부터 진행하세요.*

1. Microsoft Edge 브라우저 창의 Power BI 서비스 내 **탐색** 창 아래쪽에서 **데이터 가져오기**를 클릭합니다.

	![그림 8](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image4.png)

2. **파일** 타일에서 **가져오기**를 클릭합니다.

	![그림 10](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image5.png)

3. **파일 찾기** 타일을 클릭합니다.

	![그림 11](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image6.png)

4. **열기** 창에서 **D:\DA100\Labs\09- create-power-bi-dashboard\Solution** 폴더로 이동합니다.

5. **Sales Analysis.pbix** 파일을 선택한 다음 **열기**를 클릭합니다.

6. 데이터 세트를 바꾸라는 메시지가 표시되면 **바꾸기**를 클릭합니다.

### **작업 3: 보고서 만들기**

이 작업에서는 **판매 탐색** 보고서를 만듭니다.

1. Power BI Desktop을 열려면 작업 표시줄에서 Microsoft Power BI Desktop 바로 가기를 클릭합니다.

	*중요: Power BI Desktop을(이전 랩에서) 이미 열었다면 해당 인스턴스를 닫습니다.*

	![그림 14](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image7.png)

2. 시작 창을 닫으려면 창 왼쪽 위의 **X**를 클릭합니다.

	![그림 13](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image8.png)

3. Power BI Desktop이 Power BI 서비스에 로그인되어 있지 않으면 오른쪽 위에 있는 **로그인**을 클릭합니다.

	![그림 16](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image9.png)

4. Power BI 서비스에 로그인하는 데 사용한 것과 같은 계정을 사용하여 로그인 프로세스를 완료합니다.

5. 파일을 저장하려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

6. **저장**을 선택합니다.

	![그림 12](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image10.png)

7. **다른 이름으로 저장** 창에서 **D:\DA100\MySolution** 폴더로 이동합니다.

8. **파일 이름** 상자에 **Sales Exploration**을 입력합니다.

	![그림 1](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image11.png)

9. **판매 분석** 데이터 세트에 대한 라이브 연결을 만들려면 **홈** 리본 탭의 **데이터** 그룹 내부에서 **Power BI 데이터 세트**를 클릭합니다.

	![그림 15](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image12.png)

10. **데이터 세트를 선택하여 보고서 만들기** 창에서 **판매 분석** 데이터 세트를 선택합니다.

11. **만들기**를 클릭합니다.

	![그림 17](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image13.png)

12. Power BI Desktop 파일을 저장합니다.

	*이제 4개의 보고서 페이지를 만들고 각 페이지에서 서로 다른 시각적 개체로 작업하여 데이터를 분석하고 탐색합니다.*

## **연습 2: 분산 차트 만들기**

이 연습에서는 애니메이션화할 수 있는 분산 차트를 만듭니다.

### **작업 1: 애니메이션 분산 차트 만들기**

이 작업에서는 애니메이션화할 수 있는 분산 차트를 만듭니다.

1. **페이지 1**의 이름을 **분산형 차트**로 바꿉니다.

	![그림 67](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image14.png)

2. 보고서 페이지에 **분산형 차트** 시각적 개체를 추가한 다음 전체 페이지를 채우도록 크기를 조정하여 배치합니다.

	![그림 18](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image15.png)

	![그림 75](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image16.png)

3. 다음 필드를 시각적 개체 웰/영역에 추가합니다.

	이 랩에서는 단축 표기를 사용해 필드를 참조합니다. 다음과 같이 표시됩니다. **Reseller | Business Type**. 이 예제에서 **Reseller**는 테이블 이름이고 **Business Type**은 필드 이름입니다.

	- 범례: **재판매인 | 비즈니스 유형**

	- X축: **영업 | 영업** 

	- Y축: **영업 | 이익률**

	- 크기: **영업 | 수량**

	- 재생 축: **Date | Quarter**

	![그림 39](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image17.png)

	*필드가 **재생 축** 웰/영역에 추가되면 차트를 애니메이션화할 수 있습니다/.*

4. **필터** 창에서 **제품 | 범주** 필드를 **이 페이지의 필터** 웰/영역으로 끌어옵니다.

5. 필터 카드에서 **자전거**로 필터링합니다.

	![그림 40](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image18.png)

6. 차트를 애니메이션화하려면 왼쪽 하단 모서리에서 **재생**을 클릭합니다.

	![그림 41](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image19.png)

7. **FY2018 Q1**부터 **FY2020 Q4**까지의 전체 애니메이션 주기를 시청합니다.

	*분산형 차트를 사용하면 측정값, 이 경우 주문 수량, 판매 수익 및 이익률을 동시에 이해할 수 있습니다.*

	*각 거품형은 재판매인 비즈니스 유형을 나타냅니다. 거품 크기의 변화는 주문 수량이 증가하거나 감소하는 것을 반영합니다. 수평 이동은 매출의 증가/감소를 나타내며 수직 이동은 수익성의 증가/감소를 나타냅니다.*

8. 애니메이션이 중지되면 거품 중 하나를 클릭하여 시간 경과에 따른 추적을 표시합니다.

9. 거품 위를 마우스로 가리켜서 해당 시점에 재판매인 유형에 대한 측정값을 설명하는 도구 설명을 표시합니다.

10. **필터** 창에서 **의류**로만 필터링하면 매우 다른 결과가 생성됩니다.

11. Power BI Desktop 파일을 저장합니다.

## **연습 3: 예측 만들기**

이 연습에서는 향후 판매 수익을 결정할 예측을 만듭니다.

### **작업 1: 예측 만들기**

이 작업에서는 향후 판매 수익을 결정할 예측을 만듭니다.

1. 새 페이지를 추가한 다음 페이지의 이름을 **예측**으로 바꿉니다.

	![그림 66](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image20.png)

2. 보고서 페이지에 **꺾은선형 차트** 시각적 개체를 추가한 다음 전체 페이지를 채우도록 크기를 조정하여 배치합니다.

	![그림 19](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image21.png)

	![그림 74](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image22.png)

  

3. 다음 필드를 시각적 개체 웰/영역에 추가합니다.

	- 축: **Date | Date**

	- 값: **영업 | 영업** 

	![그림 46](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image23.png)

4. **필터** 창에서 **날짜 | 연도** 필드를 **이 페이지의 필터** 웰/영역에 추가합니다.

5. 필터 카드에서 2년으로 필터링합니다. **FY2019** 및 **FY2020**.

	![그림 47](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image24.png)

	*시간 표시 막대를 통해 예측할 때 정확하고 안정적인 예측을 생성하려면 최소 2주기(연도)의 데이터가 필요합니다.*

  

6. **제품** 추가 **| 범주** 필드도 **이 페이지의 필터** 웰/영역에 추가하고, **자전거**로 필터링합니다.

	![그림 48](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image25.png)

7. 예측을 추가하려면 **시각화** 창 아래 **분석** 창을 선택합니다.

	![그림 20](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image26.png)

8. **예측** 섹션을 확장합니다.

	![그림 50](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image27.png)

	***예측** 섹션을 사용할 수 없는 경우 시각적 개체가 올바르게 구성되지 않았기 때문일 수 있습니다. 예측은 축에는 단일 필드의 형식 날짜가 있고 값 필드가 하나밖에 없는 두 조건이 충족될 때만 사용할 수 있습니다.*

9. **추가**를 클릭합니다.

	![그림 51](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image28.png)

10. 다음 예측 속성을 구성합니다.

	- 예측 범위: 1개월

	- 신뢰 구간: 80%

	- 계절성: 365

11. **적용**을 클릭합니다.

	![그림 52](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image29.png)

12. 선 시각적 개체에서 예측이 기록 데이터를 한 달 이상 연장한 것을 알 수 있습니다.

	*회색 영역은 신뢰도를 나타냅니다. 신뢰도가 클수록 안정감과 정확도가 떨어지므로 예측은 다음과 같을 수 있습니다.*

	*주기의 길이를 알고 있는 경우(이 경우 연간), 계절성 포인트를 입력해야 합니다. 때로는 주간(7일) 또는 월간(30일)일 수 있습니다.*

13. **필터** 창에서 **의류**로만 필터링하면 다른 결과가 생성됩니다.

14. Power BI Desktop 파일을 저장합니다.

## **연습 4: 분해 트리로 작업**

이 연습에서는 분해 트리를 만들어 재판매인의 지리 및 이윤 간의 관계를 탐색합니다.

### **작업 1: 분해 트리로 작업**

이 작업에서는 분해 트리를 만들어 재판매인의 지리 및 이익률 간의 관계를 탐색합니다.

1. 새 페이지를 추가한 다음 페이지 이름을 **분해 트리**로 바꿉니다.

	![그림 65](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image30.png)

2. **삽입** 리본의 **AI 시각적 개체** 그룹 내부에서 **분해 트리**를 클릭합니다.

	*팁: AI 시각적 개체는 **시각화** 창에서도 사용할 수 있습니다.*

	![그림 54](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image31.png)

3. 시각적 개체가 전체 페이지를 채우도록 크기를 조정하여 배치합니다.

	![그림 73](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image32.png)

4. 다음 필드를 시각적 개체 웰/영역에 추가합니다.

	- 분석: **영업 | 이익률**

	- 설명: **재판매인 | 지리** (전체 계층 구조)

	![그림 57](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image33.png)

5. **필터** 창에서 **날짜 | 연도** 필드를 **이 페이지의 필터**에 추가하고 필터를 **FY2020**으로 설정합니다.

	![그림 59](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image34.png)

6. 분해 트리 시각적 개체에서 트리의 루트를 확인합니다. **이익률** -0.94%

	![그림 21](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image35.png)

7. 플러스 아이콘을 클릭하고 컨텍스트 메뉴에서 **높은 값**을 선택합니다.

	![그림 61](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image36.png)

8. 분해 트리는 가장 높은 이윤으로 주문한 재판매인을 제시합니다.

9. 해당 수준을 제거하려면 시각적 개체 상단에서 **재판매인** 레이블 옆에 있는 **X**를 클릭합니다.

	![그림 62](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image37.png)

10. 플러스 아이콘을 다시 클릭한 다음 **국가-지역** 수준으로 확장합니다.

11. **미국**에서 **시-도** 수준으로 확장합니다.

12. **주-도**의 시각적 개체 하단에 있는 아래쪽 화살표를 사용한 다음 수익성이 낮은 상태로 스크롤합니다.

13. **뉴욕** 주는 수익성이 부정적임을 알 수 있습니다.

14. **뉴욕**에서 **재판매인** 수준으로 확장합니다.

15. 근본 원인을 쉽게 분리할 수 있습니다.

	![그림 22](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image38.png)

	***미국**은 **FY2020**에 수익을 내지 못하고 있습니다. **뉴욕** 주는 양의 수익성을 달성하지 못하고 있는 주 중 하나입니다. 이는 상품에 대해 표준 가격보다 낮은 가격을 지급한 네 재판매인 때문입니다.*

16. Power BI Desktop 파일을 저장합니다.

## **연습 5: 주요 영향 요인으로 작업**

이 연습에서는 주요 영향 요인인 AI 시각적 개체를 사용하여 재판매인의 비즈니스 유형 및 지리 내에서 수익성에 어떤 영향을 미치는지 확인합니다.

### **작업 1: 주요 영향 요인으로 작업**

이 작업에서는 주요 영향 요인인 AI 시각적 개체를 사용하여 재판매인의 비즈니스 유형 및 지리 내에서 수익성에 어떤 영향을 미치는지 확인합니다.

1. 새 페이지를 추가한 다음 페이지의 이름을 **주요 영향 요인**으로 바꿉니다.

	![그림 64](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image39.png)

2. **삽입** 리본의 **AI 시각적 개체** 그룹 내부에서 **주요 영향 요인**을 클릭합니다.

	*팁: AI 시각적 개체는 **시각화** 창에서도 사용할 수 있습니다.*

	![그림 71](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image40.png)

3. 시각적 개체가 전체 페이지를 채우도록 크기를 조정하여 배치합니다.

	![그림 72](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image41.png)

4. 시각적 개체 웰에 다음 필드를 추가합니다.

	- 분석: **영업 | 이익률**

	- 설명: **재판매인 | 비즈니스 유형** 및 **재판매인 | 지리** (전체 계층 구조)

	- 확장 기준: **영업 | 수량**

	![그림 3](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image42.png)

5. 시각적 개체의 왼쪽 상단에는 **키 영향 요소**에 초점을 맞추고 있으며 특정 영향 요소는 증가할 이익의 마진에 영향을 미치는 것을 파악하도록 설정되어 있습니다.

	![그림 76](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image43.png)

6. 결과를 검토하면 **Bothell** 도시가 증가할 가능성이 더 높습니다.

7. 대상을 수정하여 이윤이 감소하는 데 영향을 미치는 것이 무잇인지 확인합니다.

	![그림 77](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image44.png)

8. 결과 검토.

9. 세그먼트를 감지하려면 왼쪽 상단에서 **상위 세그먼트**를 선택합니다.

	![그림 78](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image45.png)

10. 이제 이윤이 높을 가능성이 있는 세그먼트를 결정하는 것이 목표입니다.

11. 시각적 개체가 세그먼트(원)를 표시하면 세그먼트 중 하나를 클릭하여 세그먼트에 대한 정보를 표시합니다.

12. 세그먼트 결과 검토.

### **작업 2: 완료**

이 작업에서는 랩을 완료합니다.

1. **분산 차트** 페이지를 선택합니다.

2. Power BI Desktop 파일을 저장합니다.

3. 작업 영역에 파일을 게시하려면 **홈** 리본 탭의 **공유** 그룹 내부에서 **게시**를 클릭합니다.

	![그림 23](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image46.png)

4.  Power BI Desktop을 닫습니다.
