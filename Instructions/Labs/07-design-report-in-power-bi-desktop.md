---
lab:
    title: 'Power BI Desktop에서 보고서 디자인, 1부'
    module: '모듈 7 - 보고서 만들기'
---


# **Power BI Desktop에서 보고서 디자인, 1부**

**이 랩을 완료하는 데 걸리는 예상 완료 시간은 45분입니다.**

이 랩에서는 세 페이지로 구성된 보고서를 만듭니다. 그런 다음 보고서를 Power BI에 게시합니다. 이렇게 하면 보고서를 열고 상호 작용할 수 있습니다.

이 랩의 학습 내용은 다음과 같습니다.

- 보고서 디자인

- 시각적 개체 필드 및 서식 속성 구성

### **랩 스토리**

이 랩은 데이터를 준비하여 보고서와 대시보드로 게시하는 전체 스토리로 제작된 랩 시리즈에 포함되어 있는 여러 랩 중 하나입니다. 랩은 원하는 순서로 완료하면 됩니다. 그러나 여러 랩을 진행하려는 경우 처음 10개 랩은 다음 순서로 수행하는 것이 좋습니다.

1. Power BI Desktop에서 데이터 준비

2. Power BI Desktop에서 데이터 로드

3. Power BI Desktop에서 데이터 모델링, 1부

4. Power BI Desktop에서 데이터 모델링, 2부

5. Power BI Desktop에서 DAX 계산 만들기, 1부

6. Power BI Desktop에서 DAX 계산 만들기, 2부

7. **Power BI Desktop에서 보고서 디자인, 1부**

8. Power BI Desktop에서 보고서 디자인, 2부

9. Power BI 대시보드 만들기

10. Power BI 페이지를 매긴 보고서 만들기

11. Power BI Desktop에서 데이터 분석 수행

12. 행 수준 보안 적용

## **연습 1: 보고서 만들기**

이 연습에서는 **판매 보고서**라는 세 페이지로 구성된 보고서를 만듭니다.

### **작업 1: 시작 - 로그인**

이 작업에서는 Power BI에 로그인하여 랩용 환경을 설정합니다.

*중요: Power BI에 이미 로그인했다면 다음 작업부터 진행하세요.*

1. 작업 표시줄에서 Microsoft Edge를 열려면 Microsoft Edge 프로그램 바로 가기를 클릭합니다.

 	![그림 65](Linked_image_Files/07-design-report-in-power-bi-desktop_image1.png)

1. Microsoft Edge 브라우저 창에서 **https://powerbi.com**으로 이동합니다.

 	*팁: Microsoft Edge 즐겨찾기 모음에서 Power BI 서비스 즐겨찾기를 사용할 수도 있습니다.*

1. **로그인** 오른쪽 상단 모서리에 위치)을 클릭합니다.

 	![그림 63](Linked_image_Files/07-design-report-in-power-bi-desktop_image2.png)

1. 제공된 계정 세부 정보를 입력합니다(**리소스** 확인).

1. 암호를 업데이트하라는 메시지가 표시되면 제공된 암호를 다시 입력한 다음 새 암호를 입력하고 확인합니다.

 	*중요: 새 암호를 기록해 두어야 합니다.*

1. 로그인 프로세스를 완료합니다.

1. Microsoft Edge에서 로그인 상태를 유지하라는 메시지가 표시되면 **예**를 클릭합니다.

1. Microsoft Edge 브라우저 창을 열어 둡니다.

### **작업 2: 시작하기 – 맵 및 채워진 맵 시각적 개체 활성화**

이 작업에서는 Power BI 관리 포털에서 통합 설정을 업데이트하여 랩 환경에서 맵 및 채워진 맵 시각적 개체를 활성화합니다. 


1. Power BI 관리 포털을 열려면 브라우저 오른쪽 위에 있는 **설정** 아이콘을 클릭합니다.

 	![그림 101](Linked_image_Files/07-design-report-in-power-bi-desktop_image101.png)

1. **관리 포털**을 선택합니다.

 	![그림 102](Linked_image_Files/07-design-report-in-power-bi-desktop_image102.png)

1. 페이지 아래로 스크롤하여 통합 설정으로 이동합니다. 화살표를 클릭하여 지도 및 등치 지역도 시각적 개체 옵션을 확장합니다.

 	![그림 103](Linked_image_Files/07-design-report-in-power-bi-desktop_image103.png)

1. 지도 및 등치 지역도 시각적 개체 옵션을 **사용**으로 설정합니다.

1. **적용**을 클릭하여 변경 내용을 적용합니다. 

	![그림 104](Linked_image_Files/07-design-report-in-power-bi-desktop_image104.png)

1. 테넌트 설정 변경을 적용하는 데 15분 정도 걸린다는 메시지가 브라우저의 오른쪽 위에 나타납니다. 


	![그림 105](Linked_image_Files/07-design-report-in-power-bi-desktop_image105.png)



1. Microsoft Edge 브라우저 창을 열어 둡니다.

### **작업 3: 시작 - 보고서 열기**

이 작업에서는 시작 보고서를 열어 랩용 환경을 설정합니다.

*중요: 이전 랩을 정상적으로 완료했으며 작업을 계속 이어서 하는 경우 이 작업을 완료하지 말고 다음 작업부터 계속 진행하세요.*

1. Power BI Desktop을 열려면 작업 표시줄에서 Microsoft Power BI Desktop 바로 가기를 클릭합니다.

	![그림 48](Linked_image_Files/07-design-report-in-power-bi-desktop_image3.png)

2. 시작 창을 닫으려면 창 왼쪽 위의 **X**를 클릭합니다.

	![그림 47](Linked_image_Files/07-design-report-in-power-bi-desktop_image4.png)

3. Power BI 서비스에 로그인하려면 오른쪽 위에 있는 **로그인**을 클릭합니다.

	![그림 66](Linked_image_Files/07-design-report-in-power-bi-desktop_image5.png)

4. Power BI 서비스에 로그인하는 데 사용한 것과 같은 계정을 사용하여 로그인 프로세스를 완료합니다.

5. 시작 Power BI Desktop 파일을 열려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

6. **보고서 열기**를 선택합니다.

	![그림 31](Linked_image_Files/07-design-report-in-power-bi-desktop_image6.png)

7. **보고서 찾아보기**를 클릭합니다.

	![그림 30](Linked_image_Files/07-design-report-in-power-bi-desktop_image7.png)

8. **열기** 창에서 **D:\DA100\Labs\07- design-report-in-power-bi-desktop\Starter** 폴더로 이동합니다.

9. **판매 분석** 파일을 선택합니다.

10. **열기**를 클릭합니다.

	![그림 16](Linked_image_Files/07-design-report-in-power-bi-desktop_image8.png)

11. 정보 창이 열릴 수도 있는데 모두 닫으면 됩니다.

12. 파일 복사본을 만들려면 **파일** 리본 탭을 클릭하여 Backstage 뷰를 엽니다.

13. **다른 이름으로 저장**을 선택합니다.

	![그림 8](Linked_image_Files/07-design-report-in-power-bi-desktop_image9.png)

14. 변경 내용을 적용하라는 메시지가 표시되면 **적용**을 클릭합니다.

	![그림 5](Linked_image_Files/07-design-report-in-power-bi-desktop_image10.png)

15. **다른 이름으로 저장** 창에서 **D:\DA100\MySolution** 폴더로 이동합니다.

16. **저장**을 클릭합니다.

	![그림 4](Linked_image_Files/07-design-report-in-power-bi-desktop_image11.png)

### **작업 4: 1페이지 디자인**

이 작업에서는 첫 번째 보고서 페이지를 디자인합니다. 디자인을 완료하면 페이지는 다음과 같은 모습이 됩니다.

![로고, 슬라이서 2개, 시각적 개체 3개로 구성된 1페이지의 이미지](Linked_image_Files/07-design-report-in-power-bi-desktop_image12.png)

1. Power BI Desktop에서 페이지의 이름을 바꾸려면 왼쪽 하단에서 **1페이지**를 마우스 오른쪽 단추로 클릭한 다음 **이름 바꾸기**를 선택합니다.

	![그림 36](Linked_image_Files/07-design-report-in-power-bi-desktop_image13.png)

	*팁: 페이지 이름을 두 번 클릭하여 이름을 바꿀 수도 있습니다.*

2. 페이지의 이름을 **개요**로 바꾼 다음 **Enter** 키를 누릅니다.

	![그림 37](Linked_image_Files/07-design-report-in-power-bi-desktop_image14.png)

3. 이미지를 추가하려면 **삽입** 리본 탭의 **요소** 그룹에서 **이미지**를 클릭합니다.

	![그림 1](Linked_image_Files/07-design-report-in-power-bi-desktop_image15.png)

4. **열기** 창에서 **D:\DA100\Resources** 폴더로 이동합니다.

5. **AdventureWorksLogo.jpg** 파일을 선택한 다음, **열기**를 클릭합니다.

	![그림 11](Linked_image_Files/07-design-report-in-power-bi-desktop_image16.png)

6. 이미지를 끌어 왼쪽 위에 놓고 안내선 표식도 끌어 크기를 조정합니다.

	![그림 12](Linked_image_Files/07-design-report-in-power-bi-desktop_image17.png)

7. 슬라이서를 추가하려면 먼저 보고서 페이지의 빈 영역을 클릭하여 이미지를 선택 취소합니다.

8. **필드** 창에서 **날짜 | 연도** 필드(계층 구조의 **연도** 수준이 아님)를 선택합니다.

	*이 랩에서는 단축 표기를 사용해 필드를 참조합니다. 다음과 같이 표시됩니다. **Date | Year**. 이 예제에서 **Date**는 테이블 이름이고 **Year**는 필드 이름입니다.*

9. 연도 값 테이블이 보고서 페이지에 추가된 것을 볼 수 있습니다.

10. 시각적 개체를 테이블에서 슬라이서로 변환하려면 **시각화** 창에서 **슬라이서**를 선택합니다.

	![그림 49](Linked_image_Files/07-design-report-in-power-bi-desktop_image18.png)

11. 슬라이서를 목록에서 드롭다운으로 변환하려면 슬라이서 오른쪽 위에 있는 아래쪽 화살표를 클릭한 다음 **드롭다운**을 선택합니다.

	![그림 18](Linked_image_Files/07-design-report-in-power-bi-desktop_image19.png)

12. 너비가 이미지 너비와 같아지도록 슬라이서 크기를 조정하여 이미지 아래에 오도록 배치합니다.

	![그림 19](Linked_image_Files/07-design-report-in-power-bi-desktop_image20.png)

13. **년** 슬라이서에서 드롭다운 목록을 열고 **FY2020**을 선택한 다음 드롭다운 목록을 축소합니다.

	![그림 20](Linked_image_Files/07-design-report-in-power-bi-desktop_image21.png)

	*이제 보고서 페이지는 **FY2020**을 기준으로 필터링됩니다.*

14. 보고서 페이지의 빈 영역을 클릭하여 슬라이서를 선택 취소합니다.

15. **지역 | 지역** 필드(계층 구조의 **지역** 수준이 아님)을 기반으로 두 번째 슬라이서를 만듭니다.

16. 슬라이서를 목록으로 유지하고 크기를 조정한 다음 **년** 슬라이서 아래에 배치합니다.

	![그림 21](Linked_image_Files/07-design-report-in-power-bi-desktop_image22.png)

17. 슬라이서의 서식을 지정하려면 **시각화** 창 아래에서 **형식** 창을 엽니다.

	![그림 50](Linked_image_Files/07-design-report-in-power-bi-desktop_image23.png)

18. **선택 컨트롤** 그룹을 확장합니다.

	![그림 23](Linked_image_Files/07-design-report-in-power-bi-desktop_image24.png)

19. **"모두 선택" 옵션 표시**를 **켜짐**으로 설정합니다.

	![그림 24](Linked_image_Files/07-design-report-in-power-bi-desktop_image25.png)

20. **지역** 슬라이서에서 이제 첫 번째 항목이 **모두 선택**인지 확인합니다.

	*이 항목을 선택하면 모든 항목이 선택되거나 선택 취소됩니다. 이를 통해 보고서 사용자가 필요한 슬라이서 항목을 쉽게 설정할 수 있습니다.*

21. 보고서 페이지의 빈 영역을 클릭하여 슬라이서를 선택 취소합니다.

22. 페이지에 차트를 추가하려면 **시각화** 창에서 **선 및 누적된 열 차트** 시각적 개체 유형을 클릭합니다.

	![그림 51](Linked_image_Files/07-design-report-in-power-bi-desktop_image26.png)

23. 보고서 페이지의 전체 너비를 채우도록 시각적 개체의 크기를 조정한 다음 로고 오른쪽에 배치합니다.

	![그림 26](Linked_image_Files/07-design-report-in-power-bi-desktop_image27.png)

24. 다음 필드를 시각적 개체에 끌어서 놓습니다.

	- Date | Month

	- Sales | 영업

25. 시각적 개체 필드 창(**필드** 창이 아니며 **시각화** 창 아래에 시각적 필드 창 위치)에서 필드가 **공유 축** 및 **열 값** 웰/영역에 할당되었는지 확인합니다.

	![그림 27](Linked_image_Files/07-design-report-in-power-bi-desktop_image28.png)

	*필드를 시각적 개체로 드래그하면 기본 웰/영역에 추가됩니다. 정밀도를 위해 필드를 웰/영역으로 직접 끌어올 수 있습니다. 다음 작업에서 이와 같이 필드를 끌어올 것입니다.*

26. **필드** 창에서 **Sales | 이윤** 필드를 **줄 값** 웰/구역으로 끌어옵니다.

	![그림 28](Linked_image_Files/07-design-report-in-power-bi-desktop_image29.png)

27. 시각적 개체에는 11개월만 있습니다.

	*2020년 6월의 마지막 달에는 아직 판매량이 없습니다. 기본적으로 시각적 개체는 판매량이 비어 있는 월을 제거했습니다. 이제 모든 월을 표시하도록 시각적 개체를 구성합니다.*

28. 시각적 필드 창의 **공유 축** 웰/영역에서 **월** 필드에 대해 아래쪽 화살표를 클릭한 후 **데이터 없이 항목 표시**를 선택합니다.

	![그림 52](Linked_image_Files/07-design-report-in-power-bi-desktop_image30.png)

29. 이제 **2020년 6월** 달이 나타납니다.

30. 보고서 페이지의 빈 영역을 클릭하여 차트를 선택 취소합니다.

31. 페이지에 차트를 추가하려면 **시각화** 창에서 **지도** 시각적 개체 유형을 클릭합니다.

	![그림 53](Linked_image_Files/07-design-report-in-power-bi-desktop_image31.png)

32. 위에 있는 차트의 너비 절반을 채우도록 시각적 개체의 크기를 조정한 다음 세로 막대형 차트/꺾은선형 차트 아래에 배치합니다.

	![그림 33](Linked_image_Files/07-design-report-in-power-bi-desktop_image32.png)

33. 다음 필드를 시각적 개체 웰/영역에 추가합니다.

	- 위치: **지역 | 국가**

	- 범례: **제품 | 범주**

	- 크기: **영업 | 영업**

34. 보고서 페이지의 빈 영역을 클릭하여 차트를 선택 취소합니다.

35. 페이지에 차트를 추가하려면 **시각화** 창에서 **누적된 막대형 차트** 시각적 개체 유형을 클릭합니다.

	![그림 54](Linked_image_Files/07-design-report-in-power-bi-desktop_image33.png)

36. 나머지 보고서 페이지 공간을 채우도록 시각적 개체의 크기를 조정하여 배치합니다.

	![그림 35](Linked_image_Files/07-design-report-in-power-bi-desktop_image34.png)

37. 다음 필드를 시각적 개체 웰/영역에 추가합니다.

	- 축: **제품 | 범주**

	- 값: **영업 | 수량**

38. 시각적 개체의 서식을 지정하려면 **형식** 창을 엽니다.

	![그림 3](Linked_image_Files/07-design-report-in-power-bi-desktop_image35.png)

39. **데이터 색** 그룹을 확장한 다음 **기본 색** 속성을 적절한 색(세로 막대형 차트/꺾은선형 차트를 보완하는 색)으로 설정합니다.

40. **데이터 레이블** 속성을 **On**으로 설정합니다.

	![그림 2](Linked_image_Files/07-design-report-in-power-bi-desktop_image36.png)

41. Power BI Desktop 파일을 저장합니다.

	*이제 첫 번째 페이지의 디자인이 완료되었습니다.*

### **작업 5: 2페이지 디자인**

이 작업에서는 두 번째 보고서 페이지를 디자인합니다. 디자인을 완료하면 페이지는 다음과 같은 모습이 됩니다.

![슬라이서 1개와 행렬로 구성된 2페이지의 이미지](Linked_image_Files/07-design-report-in-power-bi-desktop_image37.png)

*중요: 랩에 자세한 지침이 이미 제공된 경우 랩 단계에서는 더 간결한 지침이 제공됩니다. 자세한 지침이 필요한 경우 이 랩의 다른 작업을 참조하세요.*

1. 새 페이지를 만들려면 왼쪽 아래에서 더하기 아이콘을 클릭합니다.

	![그림 42](Linked_image_Files/07-design-report-in-power-bi-desktop_image38.png)

2. **이익**으로 페이지 이름을 바꿉니다.

	![그림 43](Linked_image_Files/07-design-report-in-power-bi-desktop_image39.png)

  
​ 

3. **지역 | 지역** 필드를 기반으로 슬라이서를 추가합니다.

4. **형식** 창을 사용하여 **선택 컨트롤** 그룹에서 "모두 선택" 옵션을 사용하도록 설정합니다.

5. 높이가 보고서 높이의 절반 정도가 되도록 시각적 개체의 크기를 조정한 다음 보고서 페이지 왼쪽에 배치합니다.

	![그림 44](Linked_image_Files/07-design-report-in-power-bi-desktop_image40.png)

6. 행렬 시각적 개체를 추가한 다음 보고서 페이지의 나머지 공간을 채우도록 크기를 조정하여 배치합니다.

	![그림 45](Linked_image_Files/07-design-report-in-power-bi-desktop_image41.png)

7. **날짜 | 회계 연도** 계층을 행렬 **행** 웰/영역에 추가합니다.

	![그림 46](Linked_image_Files/07-design-report-in-power-bi-desktop_image42.png)

8. 다음 5개의 매출 테이블 필드를 **값** 웰/영역에 추가합니다.

	- Orders(**개수** 폴더에서)

	- Sales

	- Cost

	- Profit

	- Profit Margin

	![그림 55](Linked_image_Files/07-design-report-in-power-bi-desktop_image43.png)

9. **필터** 창(**시각화** 창 왼쪽에 위치)에서 **이 페이지의 필터** 웰/영역을 잘 확인하세요(아래로 스크롤해야 할 수 있음).

	![그림 57](Linked_image_Files/07-design-report-in-power-bi-desktop_image44.png)

10. **필드** 창에서 **Product | 범주** 필드를 **이 페이지의 필터** 웰/영역으로 끌어옵니다.

11. 필터 카드 내에서 오른쪽 위에 있는 화살표를 클릭하여 카드를 축소합니다.

	![그림 58](Linked_image_Files/07-design-report-in-power-bi-desktop_image45.png)

	***필터** 창에 추가된 필드는 슬라이서와 동일한 결과를 가져올 수 있습니다. 한 가지 차이점은 보고서 페이지의 공간을 차지하지 않는다는 것입니다. 또 다른 차이점은 더 복잡한 필터링 요구 사항을 충족하도록 구성할 수 있다는 것입니다.*

12. 다음 각 **제품** 테이블 필드를 **이 페이지의 필터** 웰/영역에 추가하여 **범주** 카드 바로 아래에 각각 축소합니다.

	- Subcategory

	- Product

	- Color

	![그림 60](Linked_image_Files/07-design-report-in-power-bi-desktop_image46.png)

13. Power BI Desktop 파일을 저장합니다.

	*이제 두 번째 페이지의 디자인이 완료되었습니다.*

### **작업 6: 3페이지 디자인**

이 작업에서는 세 번째(마지막) 보고서 페이지를 디자인합니다. 디자인을 완료하면 페이지는 다음과 같은 모습이 됩니다.

![슬라이서 1개와 시각적 개체 3개로 구성된 3페이지의 이미지](Linked_image_Files/07-design-report-in-power-bi-desktop_image47.png)

1. 새 페이지를 만든 다음 이름을 **내 성능**으로 바꿉니다.

1. 행 수준 보안 필터의 성능을 시뮬레이션하기 위해 **Salesperson (Performance) | Salesperson** 필드를 필터 창의 페이지 수준 필터로 끌어옵니다.
	
	![필터 창에 있는 Salesperson 필드의 이미지.](Linked_image_Files/07-design-report-in-power-bi-desktop_image999.png) 

1. **Michael Blythe**를 선택합니다. 이제 **내 실적** 보고서 페이지의 데이터가 Michael Blythe의 데이터만 표시하도록 필터링됩니다.

1. **날짜 | 년** 필드를 기준으로 드롭다운 슬라이서를 추가한 후 크기를 조정하여 페이지 왼쪽 위 모서리에 표시되도록 배치합니다.

	![그림 70](Linked_image_Files/07-design-report-in-power-bi-desktop_image49.png)

1. 슬라이서에서 **FY2019**를 기준으로 필터링되도록 페이지를 설정합니다.

	![그림 71](Linked_image_Files/07-design-report-in-power-bi-desktop_image50.png)

1. **여러 행 카드** 시각적 개체를 추가한 다음 크기를 조정하고 재배치하여 슬라이서 오른쪽에서 페이지의 나머지 너비를 채웁니다.

	![그림 56](Linked_image_Files/07-design-report-in-power-bi-desktop_image51.png)

	![그림 74](Linked_image_Files/07-design-report-in-power-bi-desktop_image52.png)

1. 시각적 개체에 다음 4개의 필드를 추가합니다.

	- Sales | 영업

	- Targets | 대상

	- Targets | 분산

	- Targets | 분산 한계

1. 시각적 개체의 형식을 지정합니다.

	- **데이터 레이블** 그룹에서 **텍스트 크기** 속성을 **28pt**로 늘립니다.

	- **배경** 그룹에서 **색상**을 연한 회색으로 설정합니다.

	![그림 79](Linked_image_Files/07-design-report-in-power-bi-desktop_image53.png)

1. **묶인 막대형 차트** 시각적 개체를 추가한 다음 크기를 조정하고 배치하여 다중 행 카드 시각적 개체 아래에 배치하고 페이지의 나머지 높이와 다중 행 카드 시각적 개체 너비의 절반을 채웁니다.

	![그림 59](Linked_image_Files/07-design-report-in-power-bi-desktop_image54.png)

	![그림 78](Linked_image_Files/07-design-report-in-power-bi-desktop_image55.png)

1. 다음 필드를 시각적 개체 웰/영역에 추가합니다.

	- 축: **Date | Month**

	- 값: **영업 | 영업** 및 **목표 | 대상**

	![그림 80](Linked_image_Files/07-design-report-in-power-bi-desktop_image56.png)

1. 시각적 개체의 복사본을 만들려면 **Ctrl+C**를 누른 다음, **Ctrl+V**를 누릅니다.

1. 새 시각적 개체를 원래 시각적 개체 오른쪽에 배치합니다.

	![그림 82](Linked_image_Files/07-design-report-in-power-bi-desktop_image57.png)

1. **시각화** 창에서 시각화 유형을 수정하려면 **묶은 세로 막대형 차트**를 선택합니다.

	![그림 61](Linked_image_Files/07-design-report-in-power-bi-desktop_image58.png)

	*이제 두 가지 시각화 유형으로 표현된 동일한 데이터를 볼 수 있습니다. 이 방식은 효율적인 보고서 레이아웃 사용 방식이 아닙니다. 하지만 **Power BI Desktop에서 보고서 디자인, 2부** 랩에서 시각적 개체를 겹쳐 표시하는 방식으로 보고서 레이아웃을 개선할 것입니다. 페이지에 단추를 추가하면 보고서 사용자가 두 시각적 개체 중 어느 쪽이 표시되는지 확인할 수 있습니다.*

	*이제 세 번째 페이지(마지막) 페이지의 디자인이 완료되었습니다.*

### **작업 7: 보고서 게시**

이 작업에서는 보고서를 게시합니다.

1. **개요** 페이지를 선택합니다.

2. Power BI Desktop 파일을 저장합니다.

3. **홈** 리본 탭의 **공유** 그룹 내에서 **게시**를 클릭합니다.

	![그림 67](Linked_image_Files/07-design-report-in-power-bi-desktop_image59.png)

4. **Power BI에 게시** 창에서 **내 작업 영역**이 선택된 것을 확인할 수 있습니다.

5. 보고서를 게시하려면 **선택**을 클릭합니다.

	![그림 75](Linked_image_Files/07-design-report-in-power-bi-desktop_image60.png)

6. 게시가 정상적으로 완료되었으면 **확인**을 클릭합니다.

	![그림 76](Linked_image_Files/07-design-report-in-power-bi-desktop_image61.png)

7. Power BI Desktop을 열어 둡니다.

	*다음 연습을 진행하면서 Power BI 서비스에서 보고서를 살펴볼 것입니다.*

## **연습 2: 보고서 살펴보기**

이 연습에서는 Power BI에 게시된 보고서를 살펴봅니다.

### **작업 1: 보고서 살펴보기**

이 작업에서는 Power BI에 게시된 보고서를 살펴봅니다.

1. Microsoft Edge 브라우저 창의 Power BI 서비스 내 **탐색** 창(왼쪽에 위치, 축소 가능함)에서 **내 작업 영역**을 확장합니다.

	![그림 93](Linked_image_Files/07-design-report-in-power-bi-desktop_image62.png)

2. 작업 영역의 내용을 검토하여 **판매 분석** 보고서와 데이터 세트를 확인합니다.

	*Power BI Desktop 파일을 게시할 때 데이터 모델이 데이터 세트로 게시되었습니다.*

	*데이터 세트가 표시되지 않으면 **F5** 키를 눌러 브라우저를 다시 로드한 다음 작업 영역을 다시 확장합니다.*

	![그림 94](Linked_image_Files/07-design-report-in-power-bi-desktop_image63.png)

3. 보고서를 열려면 **판매 분석** 보고서를 클릭합니다.

4. 왼쪽의 **페이지** 창에서 **개요** 페이지를 선택합니다. 

5. **지역** 슬라이서에서 **Ctrl** 키를 누른 채로 여러 지역을 선택합니다.

6. 세로 막대형/꺾은선형 차트에서 월 열을 선택하여 페이지를 교차 필터링합니다.

7. **Ctrl** 키를 누른 채로 추가 월을 선택합니다.

	*기본적으로 교차 필터링은 페이지의 다른 모든 시각적 개체를 필터링합니다.*

8. 가로 막대형 차트가 필터링되고 강조 표시되며, 필터링된 월을 나타내는 가로 막대가 굵게 표시됩니다.

9. 막대형 차트 시각적 개체 위를 커서로 가리킨 다음 오른쪽 위에 있는 필터 아이콘 위를 커서로 가리킵니다.

	![그림 95](Linked_image_Files/07-design-report-in-power-bi-desktop_image64.png)

	*필터 아이콘을 사용하면 다른 시각적 개체의 슬라이서 및 교차 필터를 포함하여 시각적 개체에 적용되는 모든 필터를 이해할 수 있습니다.*

10. 막대 위를 커서로 가리킨 다음 도구 설명 정보를 확인합니다.

11. 교차 필터를 실행 취소하려면 세로 막대형/꺾은선형 차트에서 시각적 개체의 빈 영역을 클릭합니다.

12. 맵 시각적 개체 위를 커서로 가리킨 다음 오른쪽 위에 있는 **포커스 모드** 아이콘을 클릭합니다.

	![그림 96](Linked_image_Files/07-design-report-in-power-bi-desktop_image65.png)

	*포커스 모드에서는 시각적 개체를 전체 페이지 크기로 확대합니다.*

13. 막대형 차트의 다른 세그먼트 위를 커서로 가리켜 도구 설명을 표시합니다.

14. 보고서 페이지로 돌아가려면 왼쪽 상단에 있는 **보고서로 돌아가기**를 클릭합니다.

	![그림 86](Linked_image_Files/07-design-report-in-power-bi-desktop_image66.png)

15. 맵 시각적 개체 위를 다시 커서로 가리킨 후 오른쪽 위에 있는 줄임표(...)를 클릭하고 메뉴 옵션을 살펴봅니다.

	![그림 97](Linked_image_Files/07-design-report-in-power-bi-desktop_image67.png)

16. **Team에서 채팅**을 제외한 각 옵션을 적용해 봅니다.

17. 왼쪽의 **페이지** 창에서 **수익** 페이지를 선택합니다.

	![그림 84](Linked_image_Files/07-design-report-in-power-bi-desktop_image68.png)

18. **지역** 슬라이서는 **개요** 페이지의 **지역** 슬라이서와는 다음 선택 옵션을 포함합니다.

	*슬라이서가 동기화되지 않았습니다. **Power BI Desktop에서 보고서 디자인, 2부** 랩에서 보고서 디자인을 수정하여 슬라이서가 페이지 간에 동기화되는지 확인할 것입니다.*

19. 오른쪽에 있는 **필터** 창에서 필터 카드를 확장하고 일부 필터를 적용합니다.

	***필터** 창을 사용하면 페이지에 표시될 수 있는 것보다 더 많은 필터를 슬라이서로 정의할 수 있습니다.*

20. 행렬 시각적 개체에서 더하기(+) 단추를 사용하여 **회계** 계층 구조로 드릴합니다.

21. **내 실적** 페이지를 선택합니다.

	![그림 89](Linked_image_Files/07-design-report-in-power-bi-desktop_image69.png)

22. 메뉴 모음의 오른쪽 상단에서 **뷰**를 클릭한 다음 **전체 화면**을 선택합니다.

	![그림 98](Linked_image_Files/07-design-report-in-power-bi-desktop_image70.png)

23. 슬라이서를 수정하여 페이지와 상호 작용하고 페이지를 교차 필터링합니다.

24. 창 아래쪽에서 페이지를 변경하거나, 페이지 간을 정방향이나 역방향으로 이동하거나, 전체 화면 모드를 종료하는 명령을 확인합니다.

25. 왼쪽 아이콘을 클릭하여 전체 화면 모드를 종료합니다.

	![그림 91](Linked_image_Files/07-design-report-in-power-bi-desktop_image71.png)

### **작업 2: 완료**

이 작업에서는 랩을 완료합니다.

1. 작업 영역으로 돌아오려면 창 웹 페이지에 가로로 표시된 배너에서 **내 작업 영역**을 클릭합니다.

	![그림 99](Linked_image_Files/07-design-report-in-power-bi-desktop_image72.png)

2. Microsoft Edge 브라우저 창을 열어 둡니다.

	***Power BI Desktop에서 보고서 디자인, 2부** 랩에서 고급 기능을 사용하여 보고서 디자인을 개선할 것입니다.*
