---
lab:
    title: 'Power BI Desktop에서 데이터 모델링, 2부'
    module: '모듈 4 - Power BI에서 데이터 모델 디자인'
---


# **Power BI Desktop에서 데이터 모델링, 2부**

**랩을 완료하는 데 예상되는 시간은 45분입니다.**

이 랩에서는 **Salesperson** 테이블과 **Sales** 테이블 간에 다대다 관계를 만듭니다. 

이 랩의 학습 내용은 다음과 같습니다.

- 다 대 다 관계 구성하기

### **랩 스토리**

이 랩은 데이터를 준비하여 보고서와 대시보드로 게시하는 전체 스토리로 제작된 랩 시리즈에 포함되어 있는 여러 랩 중 하나입니다. 랩은 원하는 순서로 완료하면 됩니다. 그러나 여러 랩을 진행하려는 경우 처음 10개 랩은 다음 순서로 수행하는 것이 좋습니다.

1. Power BI Desktop에서 데이터 준비

2. Power BI Desktop에서 데이터 로드

3. Power BI Desktop에서 데이터 모델링, 1부

4. **Power BI Desktop에서 데이터 모델링, 2부**

5. Power BI Desktop에서 DAX 계산 만들기, 1부

6. Power BI Desktop에서 DAX 계산 만들기, 2부

7. Power BI Desktop에서 보고서 디자인, 1부

8. Power BI Desktop에서 보고서 디자인, 2부

9. Power BI 대시보드 만들기

10. Power BI 페이지를 매긴 보고서 만들기

11. Power BI Desktop에서 데이터 분석 수행

12. 행 수준 보안 적용

## **연습 1: 다대다 관계 만들기**

이 연습에서는 **Salespereson** 테이블과 **Sales** 테이블 간에 다대다 관계를 만듭니다.

### **작업 1: 시작**

이 작업에서는 랩용 환경을 설정합니다.

*중요: 이전 랩을 정상적으로 완료했으며 작업을 계속 이어서 하는 경우 이 작업을 완료하지 말고 다음 작업부터 계속 진행하세요.*

1. Power BI Desktop을 열려면 작업 표시줄에서 Microsoft Power BI Desktop 바로 가기를 클릭합니다.

 	![그림 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)

1. 시작 창을 닫으려면 창 왼쪽 위의 **X**를 클릭합니다.

 	![그림 7](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image2.png)

1. 시작 Power BI Desktop 파일을 열려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **보고서 열기**를 선택합니다.

 	![그림 6](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image3.png)

1. **보고서 찾아보기**를 클릭합니다.

 	![그림 5](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image4.png)

1. **열기** 창에서 **D:\DA100\Labs\04-configure-data-model-in-power-bi-desktop-advanced\Starter** 폴더로 이동합니다.

1. **판매 분석** 파일을 선택합니다.

1. **열기**를 클릭합니다.

 	![그림 4](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image5.png)

1. 정보 창이 열릴 수도 있는데 모두 닫으면 됩니다.

1. 파일 복사본을 만들려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **다른 이름으로 저장**을 선택합니다.

 	![그림 3](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image6.png)

1. 변경 내용을 적용하라는 메시지가 표시되면 **적용**을 클릭합니다.

 	![그림 15](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image7.png)

1. **다른 이름으로 저장** 창에서 **D:\DA100\MySolution** 폴더로 이동합니다.

1. **저장**을 클릭합니다.

 	![그림 2](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image8.png)

### **작업 2: 다 대 다 관계 만들기**

이 작업에서는 **Salesperson** 테이블과 **Sales** 테이블 간에 다대다 관계를 만듭니다.

1. Power BI Desktop에서 보고서 뷰의 **필드** 창에서 다음 두 필드를 선택하여 테이블 시각적 개체를 만듭니다.

	- Salesperson \| 영업 사원

	- Sales \| 영업

	*이 랩에서는 단축 표기를 사용해 필드를 참조합니다. 다음과 같이 표시됩니다. **Salesperson \| Salesperson** . 이 예제에서 **Salesperson**은 테이블 이름이고 **Salesperson**은 필드 이름입니다.*

	![그림 1](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image9.png)

	*이 테이블에는 각 영업 사원의 판매 내역이 표시됩니다. 그러나 영업 직원과 판매 간에는 또 다른 관계가 있습니다. 일부 영업 사원은 하나, 둘 또는 더 많은 판매 지역에 속합니다. 또한 판매 지역에는 여러 영업 사원이 할당될 수 있습니다.*

	*실적 관리 측면에서 영업 직원의 판매량(할당된 지역을 기준으로 함)을 분석하고 판매 목표와 비교해야 합니다. 다음 연습에서 이 분석을 지원하는 관계를 만들 것입니다.*

2. Michael Blythe의 판매 금액이 약 9백만 달러인 것을 확인합니다.

3. 모델 뷰로 전환합니다.

	![그림 10](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image10.png)

4. **SalespersonRegion** 테이블을 끌어 **Region** 및 **Salesperson** 테이블 사이에 배치합니다.

5. 끌어서 놓기 기술을 사용하여 다음의 두 모델 관계를 만듭니다.

	- **Salesperson \| EmployeeKey** 대 **SalespersonRegion \| EmployeeKey**

	- **Region \| SalesTerritoryKey**에서 **SalespersonRegion \| SalesTerritoryKey**

	***SalespersonRegion** 테이블은 브리징 테이블로 간주될 수 있습니다.*

6. 보고서 뷰로 전환하면 시각적 개체가 업데이트되지 않은 것을 볼 수 있습니다. 즉, Michael Blythe의 판매량이 변경되지 않았습니다.

7. 모델 뷰로 다시 전환한 다음 **영업 사원** 테이블에서 관계 필터 방향(화살표)을 따릅니다.

	***Salesperson** 테이블이 **Sales** 테이블을 필터링한다고 가정해 보겠습니다. Salesperson 테이블은 **SalespersonRegion** 테이블도 필터링하지만 **Region** 테이블로 필터를 전파하여 필터링을 계속 진행하지는 않습니다(화살촉이 잘못된 방향을 가리키고 있음).*

	![그림 380](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image11.png)

8. **지역**과 **SalespersonRegion** 테이블 간의 관계를 편집하려면 해당 관계를 두 번 클릭합니다.

9. **관계 편집** 창의 **교차 필터 방향** 드롭다운 목록에서 **모두**를 선택합니다.

10. **보안 필터를 양방향으로 적용** 체크박스를 선택합니다.

	![그림 381](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image12.png)

11. **확인**을 클릭합니다.

	![그림 335](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image13.png)

12. 관계에 이중 화살표가 있습니다.

	![그림 382](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image14.png)

13. 보고서 뷰로 전환한 다음 판매 값이 아직 변경되지 않은 것을 확인합니다.

	*이제 이 문제는 **영업 사원**과 **판매** 테이블 사이에 두 개의 가능한 필터 전파 경로가 있다는 사실과 관련이 있습니다. 이러한 모호성은 내부적으로 “최소 테이블 수” 평가를 기반으로 해결됩니다. 필터링을 명확하게 적용하려면 이러한 유형의 모호성이 있는 모델을 디자인해서는 안 됩니다. 이 문제는 이 랩의 뒷부분에서 일부분 해결되며, **Power BI Desktop에서 DAX 계산 만들기, 1부** 랩을 완료하면 모두 해결됩니다.*

14. 모델 뷰로 전환합니다.

15. 브리징 테이블을 통해 필터 전파를 강제로 적용하려면 **Salesperson** 및 **Sales** 테이블 간의 관계를 편집(두 번 클릭)합니다.

16. **관계 편집** 창에서 **이 관계를 활성으로 만들기** 체크박스를 선택 취소합니다.

	![그림 383](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image15.png)

17. **확인**을 클릭합니다.

	![그림 5696](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image16.png)

	*이제는 활성 경로로만 필터가 전파됩니다.*

18. 다이어그램에서 비활성 관계가 파선으로 표시됩니다.

	![그림 5697](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image17.png)

19. 보고서 뷰로 전환하면 Michael Blythe의 판매량이 거의 2,200만 달러인 것을 볼 수 있습니다.

	![그림 5698](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image18.png)

20. 또한 각 영업 사원의 판매액(추가 된 경우)이 테이블 총액을 초과합니다.

	*다대다 관계에서는 이러한 현상이 흔히 나타납니다. 지역 판매 결과가 이중, 삼중 등으로 계산되기 때문입니다. 목록에 두 번째로 나온 판매원인 Brian Welcker를 보십시오. 그의 판매 금액은 총 판매 금액과 동일합니다. 이는 그가 영업 이사이기 때문에 올바른 결과이며 그의 판매량은 모든 지역의 판매량으로 측정됩니다.*

	*다대다 관계가 작동하는 동안에는 이제 영업 사원이 달성한 판매량을 분석할 수 없습니다(관계가 비활성 상태이므로). **Power BI Desktop에서 DAX 계산 만들기, 1부** 랩에서 실적 분석용으로 영업 직원에게 할당된 영업 지역에서 발생한 판매량을 분석할 수 있게 해 주는 계산된 테이블을 추가할 때 관계를 다시 활성화할 수 있습니다.*

21. 모델링 뷰로 전환한 다음 다이어그램에서 **영업 사원** 테이블을 선택합니다.

22. **속성** 창의 **이름** 상자에서 텍스트를 **Salesperson (Performance)** 으로 바꿉니다.

	*이제 이름이 변경된 테이블은 할당된 판매 지역의 판매량을 기반으로 영업 사원의 실적을 보고하고 분석하는 데 사용됩니다.*

### **작업 3: 목표 테이블 관련**

이 작업에서는 **Targets** 테이블에 대한 관계를 만듭니다.

1. **Salesperson (Performance)** 에서 관계를 만듭니다. **\| 직원 ID** 열 및 **목표 \| EmployeeID** 열에서 관계를 만듭니다.

2. 보고서 뷰에서 **여러 목표 \| 대상** 필드를 테이블 시각적 개체에 추가합니다.

3. 모든 열이 표시되도록 테이블 시각적 개체의 크기를 조정합니다.

	![그림 5699](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image19.png)

	*이제 판매와 목표를 시각화할 수 있지만 두 가지 이유로 주의해야 합니다. 첫째, 기간을 기준으로 한 필터가 없으므로 목표(향후 목표 금액 포함)를 기준으로 한 필터도 없습니다. 둘째, 대상이 추가되지 않으므로 합계를 표시해서는 안 됩니다. 합계는 시각적 개체의 서식을 지정하여 사용하지 않도록 설정하거나 계산 논리를 사용하여 제거할 수 있습니다. **Power BI Desktop에서 DAX 계산 만들기, 2부** 랩에서 두 번째 방식에 따라 대상 측정을 만들 것입니다. 이 측정은 영업 직원을 여러 명 필터링하면 BLANK를 반환합니다.*

### **작업 4: 완료**

이 작업에서는 랩을 완료합니다.

1. Power BI Desktop 파일을 저장합니다.

2. 쿼리를 적용하라는 메시지가 표시되면 **나중에 적용**을 클릭합니다.

3. 다음 랩을 시작하려면 Power BI Desktop을 열어 둡니다.

	***Power BI Desktop에서 DAX 계산 만들기, 2부** 랩에서 DAX를 사용하는 계산으로 데이터 모델을 개선할 것입니다.*
