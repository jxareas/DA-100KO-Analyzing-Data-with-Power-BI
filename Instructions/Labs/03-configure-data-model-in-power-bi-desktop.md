---
lab:
    title: 'Power BI Desktop에서 데이터 모델링, 1부'
    module: '모듈 4 - Power BI에서 데이터 모델 디자인'
---


# **Power BI Desktop에서 데이터 모델링, 1부**

**랩을 완료하는 데 예상되는 시간은 45분입니다.**

이 랩에서는 데이터 모델 개발을 시작합니다. 여기에는 테이블 간의 관계를 만든 다음, 테이블과 열 속성을 구성하여 데이터 모델의 친화성과 유용성을 향상시킵니다. 또한 계층 구조를 만들고 빠른 측정 값을 생성합니다.

이 랩의 학습 내용은 다음과 같습니다.

- 모델 관계 만들기

- 테이블 및 열 속성 구성

- 계층 구조 만들기

- 빠른 측정 만들기

### **랩 스토리**

이 랩은 데이터를 준비하여 보고서와 대시보드로 게시하는 전체 스토리로 제작된 랩 시리즈에 포함되어 있는 여러 랩 중 하나입니다. 랩은 원하는 순서로 완료하면 됩니다. 그러나 여러 랩을 진행하려는 경우 처음 10개 랩은 다음 순서로 수행하는 것이 좋습니다.

1. Power BI Desktop에서 데이터 준비

2. Power BI Desktop에서 데이터 로드

3. **Power BI Desktop에서 데이터 모델링, 1부**

4. Power BI Desktop에서 데이터 모델링, 2부

5. Power BI Desktop에서 DAX 계산 만들기, 1부

6. Power BI Desktop에서 DAX 계산 만들기, 2부

7. Power BI Desktop에서 보고서 디자인, 1부

8. Power BI Desktop에서 보고서 디자인, 2부

9. Power BI 대시보드 만들기

10. Power BI 페이지를 매긴 보고서 만들기

11. Power BI Desktop에서 데이터 분석 수행

12. 행 수준 보안 적용

## **연습 1: 모델 관계 만들기**

이 연습에서는 모델 관계를 만듭니다.

### **작업 1: 시작**

이 작업에서는 랩용 환경을 설정합니다.

*중요: 이전 랩을 정상적으로 완료했으며 작업을 계속 이어서 하는 경우 이 작업을 완료하지 말고 다음 작업부터 계속 진행하세요.*

1. Power BI Desktop을 열려면 작업 표시줄에서 Microsoft Power BI Desktop 바로 가기를 클릭합니다.

    ![그림 12](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image1.png)

1. 시작 창을 닫으려면 창 왼쪽 위의 **X**를 클릭합니다.

 	![그림 11](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image2.png)

1. 시작 Power BI Desktop 파일을 열려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **보고서 열기**를 선택합니다.

 	![그림 10](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image3.png)

1. **보고서 찾아보기**를 클릭합니다.

 	![그림 8](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image4.png)

1. **열기** 창에서 **D:\DA100\Labs\03-configure-data-model-in-power-bi-desktop\Starter** 폴더로 이동합니다.

1. **판매 분석** 파일을 선택합니다.

1. **열기**를 클릭합니다.

 	![그림 7](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image5.png)

1. 정보 창이 열릴 수도 있는데 모두 닫으면 됩니다.

1. 파일 복사본을 만들려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **다른 이름으로 저장**을 선택합니다.

 	![그림 5](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image6.png)

1. 변경 내용을 적용하라는 메시지가 표시되면 **적용**을 클릭합니다.

 	![그림 15](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image7.png)

1. **다른 이름으로 저장** 창에서 **D:\DA100\MySolution** 폴더로 이동합니다.

1. **저장**을 클릭합니다.

 	![그림 3](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image8.png)

### **작업 2: 모델 관계 만들기**

이 작업에서는 모델 관계를 만듭니다.

1. Power BI Desktop의 왼쪽에서 **모델** 뷰 아이콘을 클릭합니다.

	![그림 1](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image9.png)

2. 7개의 테이블이 모두 표시되지 않으면, 오른쪽 가로 방향으로 스크롤한 다음 테이블을 더 가깝게 끌어서 정렬하여 동시에 볼 수 있게 됩니다.

	*팁: 창 아래쪽에 있는 확대/축소 컨트롤을 사용해도 됩니다.*

	*모델 뷰에서는 각 테이블 및 관계(테이블 간의 커넥터)를 볼 수 있습니다. 현재 **Power BI Desktop에서 데이터 준비** 랩에서는 데이터 로드 관계 옵션을 비활성화했기 때문에 관계가 없습니다.*

3. 보고서 뷰로 돌아가려면 왼쪽에서 **보고서** 뷰 아이콘을 클릭합니다.

	![그림 327](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image10.png)

4. 모든 테이블 필드를 보려면 **필드** 창에서 빈 영역을 마우스 오른쪽 단추로 클릭한 다음 **모두 확장**을 선택합니다.

	![그림 328](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image11.png)

5. 테이블 시각적 개체를 만들려면, **필드** 창의 **제품** 테이블 내부에서 **범주** 필드를 확인합니다.

	![그림 329](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image12.png)

	*이 랩에서는 단축 표기를 사용해 필드를 참조합니다. 다음과 같이 표시됩니다. **제품 \| Category**. 이 예제에서 **Product**는 테이블 이름이고 **Category**는 필드 이름입니다.*

6. 테이블에 열을 하나 더 추가하려면 **필드** 창에서 **Sales \| Sales** 필드를 선택합니다.

7. 테이블 시각적 개체에는 네 가지 제품 범주가 나열되고 판매 값이 각각 동일하며 합계는 동일합니다.

	![그림 330](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image13.png)

	*문제는 테이블이 다른 테이블의 필드를 기반으로 한다는 것입니다. 각 제품 범주에 해당 범주의 매출이 표시될 것으로 예상됩니다. 그러나 이러한 테이블 간에는 모델 관계가 없기 때문에 **Sales** 테이블은 필터링되지 않습니다. 이제 테이블 간에 필터를 전파하는 관계를 추가합니다.*

8. **관계** 그룹 내의 **모델링** 리본 메뉴 탭에서 **관계 관리**를 클릭합니다.

	![그림 331](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image14.png)

9. **관계 관리** 창에서 아직 정의된 관계가 없음을 알 수 있습니다.

10. 관계를 만들려면 **새로 만들기**를 클릭합니다.

	![그림 332](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image15.png)

11. **관계 만들기** 창의 첫 번째 드롭다운 목록에서 **제품** 테이블을 선택합니다.

	![그림 333](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image16.png)

12. 두 번째 드롭다운 목록(**제품** 테이블 그리드 아래)에서 **판매** 테이블을 선택합니다.

	![그림 334](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image17.png)

13. 각 테이블에서 **ProductKey** 열이 자동으로 선택되었음을 확인합니다.

	*열은 동일한 이름 및 데이터 형식을 공유하기 때문에 선택되었습니다.*

14. **카디널리티** 드롭다운 목록에서 **일대다(1:*)** 가 선택된 것을 알 수 있습니다.

	*Power BI는 **제품** 테이블의 **ProductKey** 열이 고유한 값을 포함하는 것을 이해하기 때문에 카디널리티가 자동으로 감지되었습니다. 일대다 관계는 가장 일반적인 카디널리티이며 이 랩에서 만드는 모든 관계는 이 유형이 됩니다. **Power BI Desktop에서 데이터 모델링, 2부** 랩에서 다대다 카디널리티를 사용할 것입니다.*

15. **교차 필터 방향** 드롭다운 목록에서 **단일**이 선택된 것을 확인할 수 있습니다.

	*단일 필터 방향은 필터가 "일 쪽"에서 "다 쪽"으로 전파된다는 것을 의미합니다. 이 경우 **제품** 테이블에 적용된 필터가 **판매** 테이블에 전파되지만 반대 방향으로는 전파되지 않음을 의미합니다. **Power BI Desktop에서 데이터 모델링, 2부** 랩에서 양방향 관계를 사용할 것입니다.*

16. **Mark This Relationship Active**가 선택되어 있습니다.

	*활성 관계는 필터를 전파합니다. 필터가 전파되지 않도록 관계를 비활성으로 표시할 수 있습니다. 테이블 사이에 여러 관계 경로가 있는 경우 비활성 관계가 존재할 수 있습니다. 이 경우 모델 계산은 특수 함수를 사용하여 활성화할 수 있습니다. **Power BI Desktop에서 데이터 모델링, 2부** 랩에서 비활성 관계를 사용할 것입니다.*

17. **확인**을 클릭합니다.

	![그림 335](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image18.png)

18. **관계 관리** 창에서 새 관계가 나열되어 있음을 확인한 다음 **닫기**를 클릭합니다.

	![그림 336](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image19.png)

19. 보고서에서 테이블 시각적 개체가 업데이트되어 각 제품 범주에 대해 서로 다른 값을 표시합니다.

	![그림 337](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image20.png)

	*이제 **제품** 테이블에 적용된 필터가 **판매** 테이블로 전파됩니다.*

20. 모델 뷰로 전환한 다음 이제 두 테이블 간에 커넥터가 있음을 확인합니다(두 테이블이 나란히 배치되어 있어도 관계없음).

	![그림 338](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image21.png)

21. 다이어그램을 통해 **1** 및 **"*"** 지표로 표시되는 카디널리티를 쉽게 이해할 수 있습니다.

	*필터 방향은 화살표 머리로 표시됩니다. 실선은 활성 관계를 나타냅니다. 파선은 비활성 관계를 나타냅니다.*

22. 관계 위를 커서로 가리켜 관련 열을 강조 표시합니다.

	*관계를 만드는 쉬운 방법이 있습니다. 모델 다이어그램에서 열을 끌어서 놓아 새 관계를 만들 수 있습니다.*

23. 다른 기술을 사용하여 새 관계를 만들려면 **Reseller** 테이블에서 **ResellerKey** 열을 **Sales** 테이블의 **ResellerKey** 열로 끕니다.

	![그림 339](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image22.png)

	*팁: 열을 끌어오지 않는 경우도 있습니다. 이 상황이 발생하면 다른 열을 선택한 다음 다시 드래그하려는 열을 선택한 후에 다시 시도합니다. 다이어그램에 추가한 새 관계가 표시되는지 확인하세요.*

24. 새 기술을 사용하여 다음의 두 모델 관계를 만듭니다.

	- **Region \| SalesTerritoryKey**를 **판매**로 **\| SalesTerritoryKey**

	- **Salesperson \| EmployeeKey**를 **판매**로 **\| EmployeeKey**

	*이 랩에서는 **SalespersonRegion** 및 **Targets**테이블의 연결이 끊긴 상태로 유지됩니다. 영업 직원과 지역 간에는 다대다 관계가 적용됩니다. **Power BI Desktop에서 데이터 모델링, 2부** 랩에서 이 고급 시나리오를 진행할 것입니다.*

25. 다이어그램에서 **Sales** 테이블이 다이어그램 가운데에 오고 관련 테이블이 근처에 정렬되어 있도록 테이블을 정렬합니다. 연결이 끊긴 테이블은 옆쪽에 배치합니다.

	![그림 340](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image23.png)

26. Power BI Desktop 파일을 저장합니다.

## **연습 2: 테이블 구성**

이 연습에서는 계층 구조를 만들고 열을 숨기고 서식을 지정하고 분류하여 각 테이블을 구성합니다.

### **작업 1: Product 테이블 구성**

이 작업에서는 **Product** 테이블을 구성합니다.

1. 필요한 경우, 모델 뷰의 **필드** 창에서 **Product** 테이블을 확장하여 모든 필드를 표시합니다.

2. 계층 구조를 만들려면 **필드** 창에서 마우스 오른쪽 단추로 **범주** 열을 클릭한 다음 **계층 구조 만들기**를 선택합니다.

	![그림 341](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image24.png)

3. **속성** 창(**필드** 창 왼쪽)의 **이름** 상자에서 텍스트를 **제품**으로 바꿉니다.

	![그림 344](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image25.png)

4. 계층 구조에 두 번째 수준을 추가하려면 **속성** 창의 **계층 구조** 드롭다운 목록에서 **하위 범주**를 선택합니다(창 내에서 아래쪽으로 스크롤해야 할 수 있음).

5. 계층 구조에 세 번째 수준을 추가하려면 **계층 구조** 드롭다운 목록에서 **제품**을 선택합니다.

6. 계층 구조 설계를 완료하려면 **수준 변경 적용**을 클릭합니다.

	![그림 343](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image26.png)

	*팁: **수준 변경 적용**을 클릭하는 것을 기억하도록 합니다. 이 단계를 간과해서 자주 실수가 발생합니다.*

7. **필드** 창에서 **제품** 계층 구조를 확인합니다.

	![그림 347](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image27.png)

8. 계층 구조 수준을 표시하려면 **제품** 계층 구조를 확장합니다.

	![그림 346](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image28.png)

9. 열을 표시 폴더로 구성하려면 먼저 **필드** 창에서 **배경색 서식 지정** 열을 선택합니다.

10. **Ctrl** 키를 누르면서 **글꼴색 서식 지정** 열을 선택합니다.

11. **속성** 창의 **표시 폴더** 상자에서 **서식 지정**을 입력합니다.

	![그림 348](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image29.png)

12. **필드** 창에서 두 열이 이제 폴더 내에 있음을 알 수 있습니다.

	![그림 349](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image30.png)

	*표시 폴더는 특히 많은 필드로 구성된 테이블을 정리할 수 있는 좋은 방법입니다.*

### **작업 2: Region 테이블 구성**

이 작업에서는 **Region** 테이블을 구성합니다.

1. **지역** 테이블에서 다음 세 가지 수준으로 **지역**이라는 계층 구조를 만듭니다.

	- Group

	- Country

	- Region

	![그림 350](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image31.png)

2. **국가** 열(**국가** 계층 구조 수준이 아님)을 선택합니다.

3. **속성** 창에서 **고급** 섹션(창 아래쪽에 있음)을 확장한 다음 **데이터 범주** 드롭다운 목록에서 **국가/지역**을 선택합니다.

	![그림 352](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image32.png)

	*데이터 분류는 보고서 디자이너에게 힌트를 제공할 수 있습니다. 이 경우 열을 국가 또는 지역으로 분류하면 맵 시각화를 렌더링할 때 Power BI에 더 정확한 정보가 제공됩니다.*

### **작업 3: Reseller 테이블 구성**

이 작업에서는 **Reseller** 테이블을 구성합니다.

1. **재판매인** 테이블에서 다음 두 가지 수준과 함께 **재판매인**이라는 계층 구조를 만듭니다.

	- Business Type

	- Reseller

	![그림 351](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image33.png)

2. 다음 네 가지 수준으로 **지역**이라는 두 번째 계층 구조를 만듭니다.

	- Country-Region

	- State-Province

	- City

	- Reseller

	![그림 353](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image34.png)

3. 다음 세 개의 열을 분류합니다.

	- **Country-Region**을 **국가/지역**으로 분류

	- **State-Province**를 **시/도**로 분류

	- **City**를 **도시**로 분류

### **작업 4: Sales 테이블 구성**

이 작업에서는 **Sales** 테이블을 구성합니다.

1. **Sales** 테이블에서 **Cost** 열을 선택합니다.

2. **Properties** 창에서 **설명** 상자에 다음을 입력합니다. **표준 가격 기준**

	![그림 358](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image35.png)

	*설명은 테이블, 열, 계층 구조 또는 측정값에 적용할 수 있습니다. **필드**창에서 보고서 작성자가 필드 위에 커서를 마우스로 가져가면 설명 텍스트가 도구 설명에 표시됩니다.*

3. **수량** 열을 선택합니다.

4. **속성** 창의 **서식** 섹션 내에서 **천 단위 구분 기호** 속성을 **켜기**로 슬라이드합니다.

	![그림 357](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image36.png)

5. **단가** 열을 선택합니다.

6. **속성** 창의 **서식** 섹션 내에서 **소수 자릿수** 속성을 **2**로 밉니다.

7. **고급** 그룹(찾으려면 아래로 스크롤해야 할 수 있음)의 **요약 기준** 드롭다운 목록에서 **평균**을 선택합니다.

	![그림 354](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image37.png)

	*기본적으로 숫자 열은 값을 합산하여 요약합니다. 이 기본 동작은 가격을 나타내는 **단가** 같은 열에 적합하지 않습니다. 기본 요약을 평균으로 설정하면 의미 있는 결과가 생성됩니다.*

### **작업 5: 대량 업데이트 속성**

이 작업에서는 단일 대량 업데이트를 사용하여 여러 열을 업데이트합니다. 이 방법을 사용하면 열을 숨기고 열 값의 서식을 지정할 수 있습니다.

1. **필드** 창에서 **Product \| ProductKey** 열을 선택합니다.

2. **Ctrl** 키를 누르는 동안 다음 13개의 열(여러 테이블에 걸쳐)을 선택합니다.

	- Region \| SalesTerritoryKey

	- Reseller \| ResellerKey

	- Sales \| EmployeeKey
	
	- Sales \|ProductKey

	- Sales \| ResellerKey

	- Sales \| SalesOrderNumber

	- Sales \| SalesTerritoryKey

	- Salesperson \| EmployeeID

	- Salesperson \| EmployeeKey

	- Salesperson \| UPN

	- SalespersonRegion \| EmployeeKey

	- SalespersonRegion \| SalesTerritoryKey

	- Targets \| EmployeeID

3. **속성** 창에서 **숨김** 속성을 **켜기**로 밉니다.

	![그림 355](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image38.png)

	*열은 관계에서 사용되거나 행 수준 보안 구성 또는 계산 논리에 사용되기 때문에 숨겨져 있습니다.*

	***Power BI Desktop에서 데이터 모델링, 2부** 랩에서 **UPN** 열을 사용하여 행 수준 보안을 정의할 것입니다. **Power BI Desktop에서 DAX 계산 만들기, 1부** 랩에서 계산에 **SalesOrderNumber**를 사용할 것입니다.*

4. 다음 3개 열을 다중 선택합니다.

	- Product \| 표준 가격

	- Sales \| 비용

	- Sales \| 영업

5. **속성** 창의 **서식** 섹션 내에서 **소수점 자릿수** 속성을 **0**(zero)으로 설정합니다.

	![그림 356](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image39.png)

## **연습 3: 모델 인터페이스 검토**

이 연습에서는 보고서 뷰로 전환해서 모델 인터페이스를 검토합니다.

### **작업 1: 모델 인터페이스 검토**

이 작업에서는 보고서 뷰로 전환하고 모델 인터페이스를 검토합니다.

1. 보고서 뷰로 전환합니다.

2. **필드** 창에서 다음을 확인합니다.

	열, 계층 구조 및 수준은 보고서의 시각적 개체를 구성하는 데 사용할 수 있는 필드입니다.

	- 보고서 작성과 관련된 필드만 표시됩니다.

	- 모든 필드가 숨겨져 있기 때문에 **SalespersonRegion** 테이블이 표시되지 않습니다.

	- **Region** 및 **Reseller** 테이블의 공간 필드는 공간 아이콘으로 표시되어 있습니다.

	- 시그마 기호(Ʃ)로 표시된 필드는 기본적으로 요약됩니다.

	- **Sales \| Cost** 필드 위에 커서를 올리면 도구 설명이 나타납니다.

3. **Sales \| OrderDate** 필드를 확장하고 나서 날짜 계층 구조가 표시됩니다.

	![그림 359](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image40.png)

	***Targets \| TargetMonth** 필드도 비슷한 계층 구조를 제공합니다. 이러한 계층 구조는 사용자가 생성한 것이 아니라 자동으로 생성된 것입니다. 그러나 문제가 있습니다. Adventure Works의 회계 연도는 매년 7월 1일에 시작됩니다. 그러나 이러한 자동 생성 날짜 계층 구조에서 날짜 계층 구조 연도는 매년 1월 1일에 시작됩니다.*

	*이제 이 자동 동작을 끕니다. **Power BI Desktop에서 DAX 계산 만들기, 1부** 랩에서 DAX를 사용하여 날짜 테이블을 만든 다음 Adventure Works의 일정을 정의하도록 구성할 것입니다.*

4. 자동/날짜 시간을 끄려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

5. 왼쪽에서 **옵션 및 설정**을 선택한 다음 **옵션**을 선택합니다.

	![그림 360](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image41.png)

6. **옵션** 창의 왼쪽에 있는 **현재 파일** 그룹에서 **데이터 로드**를 선택합니다.

	![그림 361](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image42.png)

7. **시간 인텔리전스** 섹션에서 **자동 날짜/시간**을 선택 해제합니다.

	![그림 362](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image43.png)

8. **확인**을 클릭합니다.

	![그림 9](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image44.png)

9. **필드** 창에서 날짜 계층 구조를 더 이상 사용할 수 없습니다.

	![그림 363](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image45.png)

## **연습 4: 빠른 측정 만들기**

이 연습에서는 두 개의 빠른 측정을 만듭니다.

### **작업 1: 빠른 측정 만들기**

이 작업에서는 수익과 수익률을 계산하는 두 가지 빠른 측정을 만들겠습니다.

1. **필드** 창에서 **Sales** 테이블을 마우스 오른쪽 단추로 클릭한 다음 **새 빠른 측정**을 선택합니다.

	![그림 366](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image46.png)

2. **빠른 측정** 창의 **계산** 드롭다운 목록에서 **수학적 연산** 그룹의 **빼기**를 선택합니다.

	![그림 367](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image47.png)

3. **빠른 측정** 창의 **필드** 창에서 **Sales** 테이블을 확장합니다.

4. **판매** 필드를 **기준 값** 상자로 끌어옵니다.

5. **비용** 필드를 **뺄 값** 상자로 끌어옵니다.

	![그림 368](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image48.png)

6. **확인**을 클릭합니다.

	![그림 369](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image49.png)

	*빠른 측정값에서 계산 수식이 자동으로 작성됩니다. 간단하고 일반적인 계산을 쉽고 빠르게 만들 수 있습니다. **Power BI Desktop에서 DAX 계산 만들기, 1부** 랩에서는 이 도구를 사용하지 않고 측정을 만들 것입니다.*

7. **필드** 창의 **Sales** 테이블에서 새 측정값을 알 수 있습니다.

	![그림 370](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image50.png)

	*측정값이 계산기 아이콘으로 표시됩니다.*

8. 측정값의 이름을 바꾸려면 마우스 오른쪽 단추로 클릭한 다음 **이름 바꾸기**를 선택합니다.

	![그림 371](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image51.png)

	*팁: 필드의 이름을 바꾸려는 경우 필드를 두 번 클릭하거나 선택하고 **F2** 키를 누를 수도 있습니다.*

9. 측정값의 이름을 **Profit**으로 변경하고 나서 **Enter** 키를 누릅니다.

10. **Sales** 테이블에서 다음 요구 사항에 따라 두 번째 빠른 측정을 추가합니다.

	- **나눗셈** 수학 연산 사용

	- **Numerator**를 **Sales** 로 설정 **\| Profit** 필드

	- **Denominator**를 **Sales** 로 설정 **\| Sales** 필드

	- 측정 이름을 **Profit Margin**으로 바꾸기

	![그림 372](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image52.png)

	![그림 373](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image53.png)

11. **Profit Margin** 측정값을 선택한 다음 **측정 도구** 컨텍스트 리본에서 소수점 이하 두 자리 **백분율**로 설정합니다.

	![그림 374](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image54.png)

12. 두 측정값을 테스트하려면 먼저 보고서 페이지에서 테이블 시각적 개체를 선택합니다.

13. **필드** 창에서 두 개의 측정값을 확인합니다.

	![그림 375](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image55.png)

14. 오른쪽 가이드를 클릭하고 끌어서 테이블 시각적 개체를 넓힙니다.

	![그림 376](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image56.png)

15. 측정이 올바른 형식으로 합당한 결과를 산출하는지 확인합니다.

	![그림 378](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image57.png)

### **작업 2: 완료**

이 작업에서는 랩을 완료합니다.

1. 테이블을 제거하려면 테이블을 클릭하여 선택한 다음 **삭제** 키를 누릅니다.

2. Power BI Desktop 파일을 저장합니다.

3. 쿼리를 적용하라는 메시지가 표시되면 **나중에 적용**을 클릭합니다.

4. 다음 랩을 시작하려면 Power BI Desktop을 열어 둡니다.

	***Power BI Desktop에서 데이터 모델링, 2부** 랩에서 다대다 관계와 행 수준 보안을 구성하여 데이터 모델을 개선할 것입니다.*
