---
lab:
    title: 'Power BI Desktop에서 DAX 계산 만들기, 1부'
    module: '모듈 5 - Power BI에서 DAX를 사용하여 모델 계산 만들기'
---


# **Power BI Desktop에서 DAX 계산 만들기, 1부**

**랩을 완료하는 데 예상되는 시간은 45분입니다.**

이 랩에서는 DAX(Data Analysis Expressions)를 사용하여 계산된 테이블, 계산된 열 및 단순 측정값을 만듭니다.

이 랩의 학습 내용은 다음과 같습니다.

- 계산된 테이블 만들기

- 계산된 열 만들기

- 측정값 만들기

### **랩 스토리**

이 랩은 데이터를 준비하여 보고서와 대시보드로 게시하는 전체 스토리로 제작된 랩 시리즈에 포함되어 있는 여러 랩 중 하나입니다. 랩은 원하는 순서로 완료하면 됩니다. 그러나 여러 랩을 진행하려는 경우 처음 10개 랩은 다음 순서로 수행하는 것이 좋습니다.

1. Power BI Desktop에서 데이터 준비

2. Power BI Desktop에서 데이터 로드

3. Power BI Desktop에서 데이터 모델링, 1부

4. Power BI Desktop에서 데이터 모델링, 2부

5. **Power BI Desktop에서 DAX 계산 만들기, 1부**

6. Power BI Desktop에서 DAX 계산 만들기, 2부

7. Power BI Desktop에서 보고서 디자인, 1부

8. Power BI Desktop에서 보고서 디자인, 2부

9. Power BI 대시보드 만들기

10. Power BI 페이지를 매긴 보고서 만들기

11. Power BI Desktop에서 데이터 분석 수행

12. 행 수준 보안 적용

## **연습 1: 계산된 테이블 만들기**

이 연습에서는 계산된 테이블 두 개를 만듭니다. 첫 번째는 **영업 직원** 테이블로, **영업** 테이블과의 직접 관계를 설정할 수 있습니다. 두 번째는 **날짜** 테이블입니다.

### **작업 1: 시작**

이 작업에서는 랩용 환경을 설정합니다.

*중요: 이전 랩을 정상적으로 완료했으며 작업을 계속 이어서 하는 경우 이 작업을 완료하지 말고 다음 작업부터 계속 진행하세요.*

1. Power BI Desktop을 열려면 작업 표시줄에서 Microsoft Power BI Desktop 바로 가기를 클릭합니다.

 	![그림 50](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image1.png)

1. 시작 창을 닫으려면 창 왼쪽 위의 **X**를 클릭합니다.

 	![그림 49](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image2.png)

1. 시작 Power BI Desktop 파일을 열려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **보고서 열기**를 선택합니다.

 	![그림 48](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image3.png)

1. **보고서 찾아보기**를 클릭합니다.

 	![그림 47](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image4.png)

1. **열기** 창에서 **D:\DA100\Labs\05-create-dax-calculations-in-power-bi-desktop\Starter** 폴더로 이동합니다.

1. **판매 분석** 파일을 선택합니다.

1. **열기**를 클릭합니다.

 	![그림 35](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image5.png)

1. 정보 창이 열릴 수도 있는데 모두 닫으면 됩니다.

1. 파일 복사본을 만들려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

1. **다른 이름으로 저장**을 선택합니다.

 	![그림 34](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image6.png)

1. 변경 내용을 적용하라는 메시지가 표시되면 **적용**을 클릭합니다.

 	![그림 25](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image7.png)

1. **다른 이름으로 저장** 창에서 **D:\DA100\MySolution** 폴더로 이동합니다.

1. **저장**을 클릭합니다.

	![그림 13](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image8.png)

### **작업 2: Salesperson 테이블 만들기**

이 작업에서는 **Salesperson** 테이블(**Sales**와의 직접 관계)을 만듭니다.

1. Power BI Desktop 보고서 뷰의 **모델링** 리본에 있는 **계산** 그룹 내부에서 **새 테이블**을 클릭합니다.

	![그림 1](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image9.png)

2. 수식 표시줄(계산을 만들거나 편집할 때 리본 바로 아래에 열림)에서 **Salesperson =** 을 입력하고 **Shift+Enter**를 누른 다음, **'Salesperson (Performance)'** 를 입력하고 나서 **Enter** 키를 누릅니다.

	![그림 4](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image10.png)

	*편의를 위해 이 랩의 모든 DAX 정의를 **D:\DA100\Labs\05- create-dax-calculations-in-power-bi-desktop\Assets\Snippets.txt**에 위치한 코드 조각 파일에서 복사할 수 있습니다.*

	*먼저 테이블 이름을 입력하고 나서 등호(=)를 입력한 다음 테이블을 반환하는 DAX 수식을 입력하면 계산된 테이블이 만들어집니다. 데이터 모델에 이미 있는 테이블 이름을 사용할 수는 없습니다.*

	*수식 입력줄에는 유효한 DAX 수식을 입력할 수 있습니다. 자동 완성, IntelliSense 및 색상 코딩과 같은 기능이 포함되어 있어 수식을 빠르고 정확하게 입력할 수 있습니다.*

	*이 테이블 정의는 **Salesperson (Performance)** 테이블의 복사본을 만듭니다. 데이터는 복사할 수 있지만 표시 유형, 서식 지정 등과 같은 모델 속성은 복사할 수 없습니다.*

	*팁: "공백"(예: 캐리지 리턴 및 탭)을 입력하여 직관적이고 읽기 쉬운 형식으로 수식을 배치하는 것이 좋으며, 특히 수식이 길고 복잡할 때는 더욱 유용합니다. 캐리지 리턴을 입력하려면 **Shift+Enter**를 누릅니다. "공백"은 선택 사항입니다.*

3. **필드** 창에서 테이블 아이콘은 파란색 음영(계산된 테이블을 나타냄)으로 표시됩니다.

	![그림 10](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image11.png)

	*계산된 테이블은 테이블을 반환하는 DAX 수식을 사용하여 정의됩니다. 계산된 테이블은 값을 구체화하고 저장하기 때문에 데이터 모델의 크기가 증가된다는 점을 알고 있어야 합니다. 이 데이터 모델에서는 새(향후) 날짜 값이 테이블로 로드될 때와 마찬가지로 수식 종속성이 새로 고칠 때마다 다시 계산됩니다.*

	*Power Query 원본 테이블과는 달리, 계산된 테이블을 사용하여 외부 데이터 원본의 데이터를 로드할 수 없습니다. 이미 로드된 데이터 모델을 기반으로 데이터를 변환할 수 있습니다.*

4. 모델 뷰로 전환합니다.

5. 이제 **Salesperson** 테이블을 사용할 수 있습니다(이 테이블이 보기에는 숨겨져 있을 수 있으며, 이 경우 가로로 스크롤하여 찾으세요).

6. **Salesperson \| EmployeeKey**열과 **Sales \| EmployeeKey** 열 간의 관계를 만듭니다.

7. **Salesperson (Performance)** 테이블과 **Sales** 테이블 간의 비활성 관계를 마우스 오른쪽 단추로 클릭하고 나서 **삭제**를 선택합니다.

	![그림 2](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image12.png)

8. 삭제할지 묻는 메시지가 표시되면, **삭제**를 클릭합니다.

	![그림 3](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image13.png)

9. **Salesperson** 테이블에서 다음 열을 한꺼번에 선택하여 숨깁니다 (**Is Hidden** 속성을 **예**로 설정).

	- EmployeeID

	- EmployeeKey

	- UPN

10. 모델 다이어그램에서 **Salesperson** 테이블을 선택합니다.

11. **Properties** 창에서 **설명** 상자에 다음을 입력합니다. **판매와 관련된 영업 직원**

	*사용자가 테이블이나 필드에 커서를 가져가면 해당 설명이 **필드** 창에 도구 설명으로 나타납니다.*

12. **Salesperson(Performance)** 테이블의 경우 설명을 다음으로 설정합니다. **지역과 관련된 영업 사원**

	*이제 이 데이터 모델은 영업 직원을 분석할 때 대안을 제공합니다. **Salesperson** 테이블을 사용하면 영업 사원의 매출을 분석할 수 있으며 **Salesperson (Performance)** 테이블을 통해 영업 사원에게 할당된 영업 지역에서 이루어진 매출을 분석할 수 있습니다.*

### **작업 3: 날짜 테이블 만들기**

이 작업에서는 **날짜** 테이블을 만듭니다.

1. 데이터 뷰로 전환합니다.

	![그림 29](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image14.png)

2. **홈** 리본 탭의 **계산** 그룹 내부에서 **새 테이블**을 클릭합니다.

	![그림 5](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image15.png)

3. 수식 표시줄에서 다음을 입력합니다.


	**DAX**


	```
	Date =  
	CALENDARAUTO(6)
	```


	![그림 6](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image16.png)

	
	*CALENDARAUTO() 함수는 날짜 값으로 구성된 단일 열 테이블을 반환합니다. "자동" 동작은 모든 데이터 모델 날짜 열을 검사하여 데이터 모델에 저장된 가장 이른 날짜 및 가장 최근 날짜 값을 정합니다. 그런 다음 이 범위 내의 각 날짜에 대해 하나의 행을 만들어 어느 방향으로든 범위를 확장하여 전체 기간 동안의 데이터를 저장합니다.*

	*이 함수에는 1년의 마지막 달 번호를 단일 선택적 인수로 사용할 수 있습니다. 생략하면 값이 12가 되어 12월이 연중 마지막 달이라는 것을 뜻합니다. 6을 입력하는 경우 6월은 해당 연도의 마지막 달이라는 의미입니다.*

4. 날짜 값의 열을 확인합니다.

	![그림 7](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image17.png)

	*표시된 날짜는 미국 지역별 설정(예: mm/dd/yyyyy)을 사용하여 형식이 지정됩니다.*

5. 왼쪽 아래 모서리에 있는 상태 표시줄에서 테이블 통계를 보면 데이터 행 1826개가 생성된 것을 알 수 있으며, 이는 5년 전체 데이터에 해당합니다.

	![그림 9](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image18.png)

### **작업 4:** **계산된 열 만들기**

이 작업에서는 다른 열을 추가하여 다른 기간별로 필터링 및 그룹화합니다. 또한 다른 열의 정렬 순서를 제어하기 위해 계산된 열을 만듭니다.

*편의를 위해 이 랩의 모든 DAX 정의를 **D:\DA100\Labs\05- create-dax-calculations-in-power-bi-desktop\Assets\Snippets.txt**에 위치한 코드 조각 파일에서 복사할 수 있습니다.*

1. **테이블 도구** 상황에 맞는 리본의 **계산** 그룹에서 **새 열**을 클릭합니다.

	![그림 11](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image19.png)

2. 수식 표시줄에서 다음을 입력(하거나 코드 조각 파일에서 복사)한 후 **Enter** 키를 누릅니다.


	**DAX**


	```
	Year =
	"FY" & YEAR('Date'[Date]) + IF(MONTH('Date'[Date]) > 6, 1)
	```


	*먼저 열 이름을 입력하고 나서 등호(=)를 입력한 다음 단일 값 결과를 반환하는 DAX 수식을 입력하면 계산된 열이 만들어집니다. 열 이름은 테이블에 미리 존재할 수 없습니다.*

	*이 수식은 날짜의 연도 값을 사용하지만 월이 6월 이후인 경우에는 연도 값에 1을 추가합니다. 이것은 Adventure Works의 회계 연도를 계산하는 방법입니다.*

3. 새 열이 추가되었는지 확인합니다.

	![그림 12](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image20.png)

4. 조각 파일 정의를 사용하여 **Date** 테이블에 대한 다음과 같은 계산된 열 두 개를 만듭니다.

	- Quarter

	- Month

	![그림 14](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image21.png)

5. 계산의 유효성을 검사하려면 보고서 뷰로 전환합니다.

6. 새 보고서 페이지를 만들려면 왼쪽 하단에 있는 더하기 아이콘을 클릭합니다.

	![그림 15](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image22.png)

7. 새 보고서 페이지에 행렬 시각적 개체를 추가하려면 **시각화** 창에서 행렬 시각적 유형을 선택합니다.

	*팁: 각 아이콘 위에 커서를 가져가 시각적 개체 유형을 설명하는 도구 설명을 표시할 수 있습니다.*

	![그림 51](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image23.png)

8. **필드** 창의 **Date** 테이블 내부에서 **Year** 필드를 **행** 웰/영역으로 끌어갑니다.

	![그림 17](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image24.png)

9. **Month** 필드를 **Year** 필드 바로 아래 **행** 웰/영역으로 끌어갑니다.

	![그림 18](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image25.png)

10. 행렬 시각적 개체의 오른쪽 위(또는 시각적 개체 위치에 따라 맨 아래)에서 이중으로 갈라진 화살표 아이콘(모든 연도를 한 수준 아래로 확장)을 클릭합니다.

	![그림 19](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image26.png)

11. 연도가 월로 확장되고 월이 연대순이 아닌 영문자순으로 정렬됩니다.

	![그림 20](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image27.png)

	*기본적으로 텍스트 값은 알파벳순으로 정렬되고, 숫자는 가장 작은 값에서 가장 큰 값으로 정렬되며 날짜는 가장 빠른 날짜에서 가장 늦은 날짜로 정렬됩니다.*

12. **월** 필드 정렬 순서를 사용자 지정하려면 데이터 뷰로 전환합니다.

13. **MonthKey** 열을 **Date** 테이블에 추가합니다.


	**DAX**


	```
	MonthKey =
	(YEAR('Date'[Date]) * 100) + MONTH('Date'[Date])
	```


	*이 수식은 매년/월의 조합에 대한 숫자 값을 계산합니다.*

14. 데이터 뷰에서 새 열에 숫자 값(예: 2017년 7월은 201707)이 포함되어 있는지 확인합니다.

	![그림 21](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image28.png)

15. 보고서 뷰로 다시 전환합니다.

16. **필드** 창에서 **월** 필드가 선택되었는지 확인합니다(선택하고 나면 배경이 진한 회색이 됨).

17. **열 도구** 상황에 맞는 리본에 있는 **정렬** 그룹에서 **열 기준 정렬**을 클릭한 다음 **MonthKey**를 선택합니다.

	![그림 22](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image29.png)

18. 행렬 시각적 개체에서 월이 이제 연대순으로 정렬됩니다.

	![그림 23](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image30.png)

### **작업 5:** **날짜 테이블 완료**

이 작업에서는 열을 숨기고 계층 구조를 만들어서 **Date** 테이블의 디자인을 완료합니다. 그러고 나면 **Sales** 및 **Targets** 테이블과의 관계를 만듭니다.

1. 모델 뷰로 전환합니다.

2. **Date** 테이블에서 **MonthKey** 열을 숨깁니다.

3. **필드** 우측 창에서 **날짜** 테이블을 선택하고 **연도** 열을 마우스 오른쪽 단추를 클릭한 후 **계층 구조 만들기**를 선택합니다. 

4. 마우스 오른쪽 단추를 클릭하고 **이름 변경**을 선택하여 새로 만들어진 계층 구조의 이름을 **Fiscal**로 변경합니다. 
5. 필드 창에서 나머지 2개의 필드를 선택하고 마우스 오른쪽 단추를 클릭합니다. **계층 구조에 추가** -> **Fiscal**를 선택하여 해당 필드를 Fiscal 계층 구조에 추가합니다.
	
	- Quarter

	- Month

	![그림 24](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image31.png)

6. 다음 두 모델 관계를 만듭니다.

	- **Date \| Date**와 **Sales \| OrderDate**

	- **Date \| 날짜** 와 **대상** 간 **\| TargetMonth**

7. 다음 두 개 열을 숨깁니다.

	- Sales \| OrderDate

	- Targets \| TargetMonth

### **작업 6: 날짜 테이블 표시**

이 작업에서는 **Date** 테이블을 날짜 테이블로 표시합니다.

1. 보고서 뷰로 전환합니다.

2. **필드** 창에서 **Date** 테이블(**Date** 필드 아님)을 선택합니다.

3. **테이블 도구** 상황에 맞는 리본에 있는**일정** 그룹 내부에서 **날짜 테이블로 표시**를 클릭하고 **날짜 테이블로 표시**를 선택합니다.

	![그림 8](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image32.png)

4. **날짜 테이블로 표시** 창의 **날짜 열** 드롭다운 목록에서 **날짜**를 선택합니다.

	![그림 37](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image33.png)

5. **확인**을 클릭합니다.

	![그림 26](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image34.png)

6. Power BI Desktop 파일을 저장합니다.

	*Power BI Desktop은 이제 이 테이블이 날짜(시간)를 정의한다는 것을 이해합니다. 이는 시간 인텔리전스 계산을 사용할 때 중요합니다. **Power BI Desktop에서 DAX 계산 만들기, 2부** 랩에서 시간 인텔리전스 계산을 사용할 것입니다.*

	*데이터 원본에 날짜 테이블이 없을 때는 날짜 테이블에 대한 이 디자인 접근 방식이 적합합니다. 데이터 웨어하우스가 있는 경우 데이터 모델의 날짜 논리를 "재정의"하는 대신 날짜 차원 테이블에서 날짜 데이터를 로드하는 것이 좋습니다.*

## **연습 2: 측정값 만들기**

이 연습에서는 여러 측정값을 만들고 형식을 지정합니다.

### **작업 1: 간단한 측정값 만들기**

이 작업에서는 간단한 측정값을 만듭니다. 간단한 측정값은 단일 열의 값을 집계하거나 테이블의 행 개수를 계산합니다.

1. 보고서 뷰의 **2페이지**에 있는 **필드** 창에서 **판매**를 드래그합니다 **\| Unit Price** 필드를 행렬 시각적 개체로 끌어갑니다.

	*이 랩에서는 단축 표기를 사용해 필드를 참조합니다. 다음과 같이 표시됩니다. **Sales \| Unit Price**. 이 예제에서 **Sales**는 테이블 이름이고 **Unit Price**는 필드 이름입니다.*

	![그림 27](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image35.png)

	***Power BI Desktop에서 데이터 모델링, 2부** 랩에서 확인했던 것처럼, **Average**를 기준으로 내용이 요약되도록 **Unit Price** 열을 설정합니다. 행렬 시각적 개체에 표시되는 결과는 월별 평균 단가(단가 값의 합을 단가 개수로 나눈 값)입니다.*

2. 시각적 필드 창(**시각화** 창 아래에 있음)의 **값** 필드 웰/영역에 **단가**가 나열됩니다.

	![그림 28](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image36.png)

3. **Unit Price** 드롭다운 화살표를 클릭하고 나서 사용 가능한 메뉴 옵션을 확인합니다.

	![그림 30](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image37.png)

	*시각적 숫자 열을 사용하면 보고서 작성자가 보고서 디자인 시 열 값이 요약되는(또는 요약되지 않는) 방식을 결정할 수 있습니다. 그러면 부적절한 보고가 발생할 수 있습니다. 그러나 일부 데이터 모델러는 운에 맡기는 것을 좋아하지 않아 이러한 열을 숨기고 대신 측정값에 의해 정의된 집계 논리를 노출하도록 선택합니다. 여러분이 이 랩에서 적용할 접근 방식입니다.*

4. 측정값을 만들려면 **필드** 창에서 **Sales** 테이블을 오른쪽 단추로 클릭한 다음 **새 측정값**을 선택합니다.

	![그림 31](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image38.png)

5. 수식 표시줄에서 다음 측정값 정의를 추가합니다.


	**DAX**


	```
	Avg Price =  
	‎AVERAGE(Sales[Unit Price])
	```


6. **Avg Price** 측정값을 행렬 시각적 개체에 추가합니다.

7. **Unit Price** 열과 동일한 결과(다른 서식 사용)가 생성됩니다.

8. **값** 웰에서 **Avg Price** 필드에 대한 상황에 맞는 메뉴를 열면 집계 기술을 변경할 수 없다는 것을 알게 됩니다.

	![그림 32](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image39.png)

	*측정값의 집계 동작을 수정할 수는 없습니다.*

9. 코드 조각 파일 정의를 사용하여 **판매** 테이블에 대한 다음의 다섯 가지 측정값을 만듭니다.

	- Median Price

	- Min Price

	- Max Price

	- Orders

	- Order Lines

	***Orders** 측정값에 사용된 DISTINCTCOUNT() 함수는 중복을 무시하고 주문을 한 번만 셉니다. **Order Lines** 측정값에 사용된 COUNTROWS() 함수는 테이블에 대해 작동합니다.*

	*이 경우 주문 수는 고유한 **SalesOrderNumber** 열 값을 계산하여 주문 수를 계산하며 주문 라인 수는 단순히 테이블 행 수입니다(각 행은 주문 라인임).*

10. 모델 뷰로 전환한 다음 네 가지 가격 측정값, 즉 **Avg Price**, **Max Price**, **Median Price** 및 **Min Price**를 다중 선택합니다.

11. 측정값을 다중 선택하기 위해 다음 요구 사항을 구성합니다.

	- 형식을 소수점 두 자리로 설정합니다.

	- **Pricing**이라는 표시 폴더에 할당합니다.

	![그림 33](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image40.png)

12. **단가** 열을 숨깁니다.

	*이제 **단가** 열을 보고서 작성자가 사용할 수 없습니다. 보고서 작성자는 모델에 추가된 가격 측정값을 사용해야 합니다. 이 설계 방식을 통해 보고서 작성자가 가격을 합산하여 부적절하게 집계하지 않도록 합니다.*

13. **Order Lines** 및 **Orders** 측정값을 다중 선택하고 다음 요구 사항을 구성합니다.

	- 천 단위 구분 기호를 사용하도록 형식 설정

	- **Counts**라는 이름의 표시 폴더에 할당

	![그림 36](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image41.png)

14. 보고서 뷰의 행렬 시각적 개체의 **값** 웰/영역에서 **단가** 필드에 대해 X를 클릭하여 제거합니다.

	![그림 38](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image42.png)

15. 행렬 시각적 개체의 크기를 늘려서 페이지 너비와 높이를 채웁니다.

16. 다음의 다섯 가지 측정값을 행렬 시각적 개체에 추가합니다.

	- Median Price

	- Min Price

	- Max Price

	- Orders

	- Order Lines

17. 결과가 합리적으로 보이고 서식이 올바르게 지정되었는지 확인합니다.

	![그림 39](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image43.png)

### **작업 2: 추가 측정값 만들기**

이 작업에서는 보다 복잡한 수식을 사용하는 추가 측정값을 만듭니다.

1. 보고서 뷰에서 **1페이지**를 선택합니다.

	![그림 40](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image44.png)

2. 테이블 시각적 개체를 검토하며 **Target** 열의 합계를 확인합니다.

	![그림 41](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image45.png)

	*이전 랩에서 살펴본 것처럼, 영업 직원과 지역 간에는 다대다 관계가 적용됩니다. 즉, 판매 지역 할당에 따라 각 영업 직원마다 영업 직원 대상이 설정되므로 대상 값을 하나로 합산하는 것은 의미가 없습니다. 대상 값은 단일 영업 사원을 필터링할 때만 표시되어야 합니다. 이제 이 작업을 위해 측정값을 구현할 것입니다.*

3. 테이블 시각적 개체를 선택하고 **시각화** 창에서 **Target** 필드를 제거합니다.

	![그림 42](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image46.png)

4. **Targets**의 이름을 바꿉니다. **\| Target** 열의 이름을 **Targets \| TargetAmount**로 바꿉니다.

	*팁: 보고서 뷰에서 열의 이름을 바꿀 수 있는 방법에는 몇 가지가 있습니다. **필드** 창에서 열을 마우스 오른쪽 단추로 클릭한 다음 **Rename** 또는 열을 두 번 클릭하거나 **F2** 키를 누를 수 있습니다.*

	***Target**이라는 측정값을 만들려고 합니다. 같은 테이블에 같은 이름의 열과 측정값을 사용할 수 없습니다.*

5. **Targets** 테이블에서 다음 측정값을 만듭니다.


	**DAX**


	```
	Target =

	IF(

	HASONEVALUE('Salesperson (Performance)'[Salesperson]),

	SUM(Targets[TargetAmount])

	)
	```


	*HASONEVALUE() 함수는 **Salesperson** 열의 단일 값이 필터링되는지 여부를 테스트합니다. true면 이 식은 (해당 영업 사원에 대한) 목표 금액의 합계를 반환합니다. false가 되면 빈 값이 반환됩니다.*

6. 소수점 첫째자리가 되도록 **대상** 측정값의 형식을 지정합니다.

	*팁: **측정 도구** 컨텍스트 리본 메뉴를 사용할 수 있습니다.*

7. **TargetAmount** 열을 숨깁니다.

	*팁: **필드** 창에서 열을 마우스 오른쪽 단추로 클릭한 다음 **숨기기**를 선택하면 됩니다.*

8. **Target** 측정값을 테이블 시각적 개체에 추가합니다.

9. **Target** 열 합계가 이제 BLANK입니다.

	![그림 43](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image47.png)

10. 코드 조각 파일 정의를 사용하여 **Targets** 테이블에 대한 다음 두 가지 측정값을 만듭니다.

	- 분산

	- 분산 한계

11. 소수점 0자리가 되도록 **Variance** 측정값의 형식을 지정합니다.

12. **Variance Margin** 측정값을 소수점 두 자리의 백분율로 지정합니다.

13. **Variance** 및 **Variance Margin** 측정값을 테이블 시각적 개체에 추가합니다.

14. 모든 열과 행을 확인할 수 있도록 테이블 시각적 개체의 크기를 조정합니다.

	![그림 44](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image48.png)

	*모든 영업 직원이 목표를 충족하지 못하는 것처럼 보이지만, 테이블 시각적 개체는 아직 특정 기간별로 필터링되지 않았음을 기억하세요. **Power BI Desktop에서 보고서 디자인, 1부** 랩에서 사용자가 선택한 기간을 기준으로 시각적 개체를 필터링하는 판매 실적 보고서를 생성할 것입니다.*

15. **필드** 창의 오른쪽 위 모서리에서 창을 축소했다가 확장하여 엽니다.

	![그림 45](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image49.png)

	*창을 축소했다가 다시 열면 콘텐츠가 재설정됩니다.*

16. 이제 **Targets** 테이블이 목록의 맨 위에 나타납니다.

	![그림 46](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image50.png)

	*표시되는 측정값만 포함하는 테이블은 목록 맨 위에 자동으로 나열됩니다.*

### **작업 3: 완료**

이 작업에서는 랩을 완료합니다.

1. Power BI Desktop 파일을 저장합니다.

2. 다음 랩을 시작하려면 Power BI Desktop을 열어 둡니다.

	***Power BI Desktop에서 DAX 계산 만들기, 2부** 랩에서 DAX를 사용하는 고급 계산으로 데이터 모델을 개선할 것입니다.*
