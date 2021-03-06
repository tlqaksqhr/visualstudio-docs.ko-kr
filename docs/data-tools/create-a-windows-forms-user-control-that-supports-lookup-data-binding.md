---
title: 데이터 바인딩-Windows Forms 컨트롤의에서 조회 테이블 사용 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data binding, user controls
- LookupBindingPropertiesAttribute class, examples
- user controls [Visual Basic], creating
ms.assetid: c48b4d75-ccfc-4950-8b14-ff8adbfe4208
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: e79d4ba6db70876539aa2e85f0579953937cab14
ms.sourcegitcommit: 30f653d9625ba763f6b58f02fb74a24204d064ea
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/25/2018
ms.locfileid: "36756326"
---
# <a name="create-a-windows-forms-user-control-that-supports-lookup-data-binding"></a>조회 데이터 바인딩을 지 원하는 Windows Forms 사용자 컨트롤 만들기
Windows Forms에서 데이터를 표시할 때 기존 컨트롤에서 선택할 수 있습니다 합니다 **도구 상자**, 또는 응용 프로그램에 표준 컨트롤에서 사용할 수 없는 기능이 필요한 경우 사용자 지정 컨트롤을 작성할 수 있습니다. 이 연습에서는 <xref:System.ComponentModel.LookupBindingPropertiesAttribute>를 구현하는 컨트롤을 만드는 방법을 보여줍니다. <xref:System.ComponentModel.LookupBindingPropertiesAttribute>를 구현하는 컨트롤은 데이터에 바인딩할 수 있는 속성 3개를 포함할 수 있습니다. 이러한 컨트롤은 <xref:System.Windows.Forms.ComboBox>와 비슷합니다.

 컨트롤 작성에 대 한 자세한 내용은 참조 하세요. [디자인 타임에 Windows Forms 개발 컨트롤](/dotnet/framework/winforms/controls/developing-windows-forms-controls-at-design-time)합니다.

 데이터 바인딩 시나리오에 사용할 컨트롤을 작성할 때는 다음 데이터 바인딩 특성 중 하나를 구현해야 합니다.

|데이터 바인딩 특성 사용법|
|-----------------------------------|
|단일 데이터 열이나 속성을 표시하는 <xref:System.ComponentModel.DefaultBindingPropertyAttribute> 등의 단순 컨트롤에 대해 <xref:System.Windows.Forms.TextBox>를 구현합니다. 자세한 내용은 [단순 데이터 바인딩을 지 원하는 Windows Forms 사용자 컨트롤 만들기](../data-tools/create-a-windows-forms-user-control-that-supports-simple-data-binding.md)합니다.|
|데이터 목록 또는 테이블을 표시하는 <xref:System.ComponentModel.ComplexBindingPropertiesAttribute> 등의 컨트롤에 대해 <xref:System.Windows.Forms.DataGridView>를 구현합니다. 자세한 내용은 [복잡 한 데이터 바인딩을 지 원하는 Windows Forms 사용자 컨트롤 만들기](../data-tools/create-a-windows-forms-user-control-that-supports-complex-data-binding.md)합니다.|
|데이터 목록 또는 테이블을 표시하는 동시에 단일 열이나 속성도 제공해야 하는 <xref:System.ComponentModel.LookupBindingPropertiesAttribute> 등의 컨트롤에 대해 <xref:System.Windows.Forms.ComboBox>를 구현합니다. 이 연습 페이지에서 해당 프로세스에 대해 설명합니다.|

 이 연습에서는 두 테이블의 데이터에 바인딩되는 조회 컨트롤을 만듭니다. 이 예에서는 Northwind 샘플 데이터베이스의 `Customers` 및 `Orders` 테이블을 사용합니다. 조회 컨트롤에 바인딩되어 합니다 `CustomerID` 필드는 `Orders` 테이블입니다. 이 값을 사용 하 여 조회 하는 `CompanyName` 에서 `Customers` 테이블입니다.

 이 연습에서는 다음 작업을 수행하는 방법을 배웁니다.

-   새 **Windows Forms 응용 프로그램**합니다.

-   새 **사용자 정의 컨트롤** 프로젝트입니다.

-   사용자 컨트롤을 시각적으로 디자인합니다.

-   `LookupBindingProperty` 특성을 구현합니다.

-   사용 하 여 데이터 집합을 만들 합니다 **데이터 원본 구성** 마법사.

-   설정 합니다 **CustomerID** 열에는 **주문** 테이블의 경우는 **데이터 원본** 창에서 새 컨트롤을 사용 하려면.

-   새 컨트롤에 데이터를 표시할 폼을 만듭니다.

## <a name="prerequisites"></a>전제 조건

이 연습에서는 Northwind 샘플 데이터베이스 및 SQL Server Express LocalDB를 사용 합니다.

1.  SQL Server Express LocalDB가 없는 경우 설치에서 [SQL Server Express 다운로드 페이지](https://www.microsoft.com/sql-server/sql-server-editions-express), 또는 합니다 **Visual Studio 설치 관리자**합니다. 에 **Visual Studio 설치 관리자**의 일부로 SQL Server Express LocalDB를 설치할 수 있습니다는 **데이터 저장 및 처리** 워크 로드 또는 개별 구성 요소로 합니다.

2.  다음이 단계를 수행 하 여 Northwind 샘플 데이터베이스를 설치 합니다.

    1. Visual Studio에서 엽니다는 **SQL Server 개체 탐색기** 창입니다. (SQL Server 개체 탐색기의 일부로 설치 되는 **데이터 저장소 및 처리** Visual Studio 설치 관리자에서 작업 합니다.) 확장 된 **SQL Server** 노드. LocalDB 인스턴스를 마우스 오른쪽 단추로 클릭 하 고 선택 **새 쿼리**합니다.

       쿼리 편집기 창이 열립니다.

    2. 복사 합니다 [Northwind Transact SQL 스크립트](https://github.com/MicrosoftDocs/visualstudio-docs/blob/master/docs/data-tools/samples/northwind.sql?raw=true) 클립보드에 있습니다. 이 T-SQL 스크립트부터에서 Northwind 데이터베이스를 만들고 데이터로 채웁니다.

    3. T-SQL 스크립트, 쿼리 편집기에 붙여넣고 선택한 합니다 **Execute** 단추입니다.

       짧은 시간 후 쿼리 실행이 완료 하 고 Northwind 데이터베이스 생성 됩니다.

## <a name="create-a-windows-forms-application"></a>Windows Forms 응용 프로그램 만들기
 첫 번째 단계를 만드는 것을 **Windows Forms 응용 프로그램**합니다.

#### <a name="to-create-the-new-windows-project"></a>새 Windows 프로젝트를 만들려면

1. Visual Studio에서에 **파일** 메뉴에서 **새로 만들기** > **프로젝트**합니다.

2. 확장 **Visual C#** 하거나 **Visual Basic** 왼쪽 창에서 선택한 **Windows Desktop**합니다.

3. 가운데 창에서 선택 합니다 **Windows Forms 앱** 형식 프로젝션 합니다.

4. 프로젝트 이름을 **LookupControlWalkthrough**를 선택한 후 **확인**합니다.

     합니다 **LookupControlWalkthrough** 프로젝트에 추가한 만들어지면 **솔루션 탐색기**합니다.

## <a name="add-a-user-control-to-the-project"></a>사용자 컨트롤을 프로젝트에 추가
 이 연습에서 조회 컨트롤을 만듭니다는 **사용자 정의 컨트롤**, 추가 **사용자 정의 컨트롤** 항목을 합니다 **LookupControlWalkthrough** 프로젝트.

#### <a name="to-add-a-user-control-to-the-project"></a>프로젝트에 사용자 컨트롤을 추가하려면

1.  **프로젝트** 메뉴에서 **사용자 정의 컨트롤 추가**합니다.

2.  형식 `LookupBox` 에 **이름** 영역에서 마우스 클릭 **추가**합니다.

     합니다 **LookupBox** 컨트롤을 추가할 **솔루션 탐색기**, 디자이너에서 엽니다.

## <a name="design-the-lookupbox-control"></a>LookupBox 컨트롤 디자인

#### <a name="to-design-the-lookupbox-control"></a>LookupBox 컨트롤을 디자인하려면

-   끌어서를 <xref:System.Windows.Forms.ComboBox> 에서 합니다 **도구 상자** 사용자 컨트롤의 디자인 화면으로 합니다.

## <a name="add-the-required-data-binding-attribute"></a>필요한 데이터 바인딩 특성 추가
 데이터 바인딩을 지원하는 조회 컨트롤에 대해 <xref:System.ComponentModel.LookupBindingPropertiesAttribute>를 구현할 수 있습니다.

#### <a name="to-implement-the-lookupbindingproperties-attribute"></a>LookupBindingProperties 특성을 구현하려면

1.  스위치를 **LookupBox** 코드 보기를 제어 합니다. (에 **뷰** 메뉴 선택 **코드**.)

2.  `LookupBox`의 코드를 다음 코드로 바꿉니다.

     [!code-vb[VbRaddataDisplaying#5](../data-tools/codesnippet/VisualBasic/create-a-windows-forms-user-control-that-supports-lookup-data-binding_1.vb)]
     [!code-csharp[VbRaddataDisplaying#5](../data-tools/codesnippet/CSharp/create-a-windows-forms-user-control-that-supports-lookup-data-binding_1.cs)]

3.  **빌드** 메뉴에서 **솔루션 빌드**를 선택합니다.

## <a name="create-a-data-source-from-your-database"></a>데이터베이스에서 데이터 원본 만들기
이 단계에서는 사용 하 여 데이터 소스를 **데이터 소스 구성** 를 기반으로 마법사를 `Customers` 및 `Orders` Northwind 샘플 데이터베이스의 테이블입니다.

#### <a name="to-create-the-data-source"></a>데이터 소스를 만들려면

1.  **데이터** 메뉴에서 **데이터 소스 표시**를 클릭합니다.

2.  에 **데이터 원본** 창에서 **새 데이터 소스 추가** 시작 하는 **데이터 소스 구성** 마법사.

3.  **데이터 소스 형식 선택** 페이지에서 **데이터베이스** 를 선택하고 **다음**을 클릭합니다.

4.  에 **데이터 연결 선택** 페이지 중 하나를 수행 합니다.

    -   Northwind 샘플 데이터베이스에 대한 데이터 연결이 드롭다운 목록에 표시되면 해당 연결을 선택합니다.

    -   선택 **새 연결** 시작 하는 **연결 추가/수정** 대화 상자.

5.  데이터베이스에서 암호를 요구 하는 경우 중요 한 데이터를 포함 한 다음 클릭 옵션을 선택 **다음**합니다.

6.  에 **응용 프로그램 구성 파일에 연결 문자열을 저장** 페이지에서 클릭 **다음**합니다.

7.  에 **데이터베이스 개체 선택** 페이지에서 확장을 **테이블** 노드.

8.  선택 합니다 `Customers` 하 고 `Orders` 테이블과 클릭 **완료**.

     **NorthwindDataSet** 프로젝트에 추가 됩니다 및 `Customers` 및 `Orders` 의 테이블에 표시 된 **데이터 원본** 창.

## <a name="set-the-customerid-column-of-the-orders-table-to-use-the-lookupbox-control"></a>LookupBox 컨트롤을 사용 하 여 Orders 테이블의 CustomerID 열 설정
 내 합니다 **데이터 원본** 창에서 폼으로 항목 끌기 전에 만들 컨트롤을 설정할 수 있습니다.

#### <a name="to-set-the-customerid-column-to-bind-to-the-lookupbox-control"></a>LookupBox 컨트롤에 바인딩되도록 CustomerID 열을 설정하려면

1.  오픈 **Form1** 디자이너에서 합니다.

2.  확장 된 **고객** 에서 노드를 **데이터 원본** 창.

3.  확장을 **주문** 노드 (있는 **고객** 노드 아래 합니다 **팩스** 열).

4.  드롭다운 화살표를 클릭 합니다 **주문을** 노드를 선택 하 고 **세부 정보** 컨트롤 목록에서.

5.  드롭다운 화살표를 클릭 합니다 **CustomerID** 열 (에 **주문** 노드), 선택한 **사용자 지정**합니다.

6.  선택 된 **LookupBox** 목록에서 **연결 된 컨트롤** 에 **데이터 UI 사용자 지정 옵션** 대화 상자.

7.  **확인**을 클릭합니다.

8.  드롭다운 화살표를 클릭 합니다 **CustomerID** 열에서 선택한 **LookupBox**합니다.

## <a name="add-controls-to-the-form"></a>폼에 컨트롤 추가
 항목을 끌어 데이터 바인딩된 컨트롤을 만들 수는 **데이터 원본** 창만 **Form1**합니다.

#### <a name="to-create-data-bound-controls-on-the-windows-form"></a>Windows Form에서 데이터 바인딩된 컨트롤을 만들려면

-   끌어서를 **주문** 에서 노드를 **데이터 원본** 창에서 Windows 폼을 하 고 있는지 확인 합니다 **LookupBox** 컨트롤은 데이터를 표시 하는 데 사용는 `CustomerID` 열입니다.

## <a name="bind-the-control-to-look-up-companyname-from-the-customers-table"></a>Customers 테이블에서 CompanyName을 조회 하도록 컨트롤 바인딩

#### <a name="to-setup-the-lookup-bindings"></a>조회 바인딩을 설정하려면

-   주 **고객** 에서 노드를 **데이터 원본** 창과 끌어서 콤보 상자에 **CustomerIDLookupBox** 에서 **Form1** .

     표시할 데이터 바인딩을 설정 합니다 `CompanyName` 에서 `Customers` 유지 관리 하는 동안 테이블을 `CustomerID` 에서 값는 `Orders` 테이블입니다.

## <a name="running-the-application"></a>응용 프로그램 실행

#### <a name="to-run-the-application"></a>응용 프로그램을 실행하려면

-   **F5** 키를 눌러 응용 프로그램을 실행합니다.

-   일부 레코드를 탐색 하 고 있는지 확인 합니다 `CompanyName` 나타나는 `LookupBox` 제어 합니다.

## <a name="see-also"></a>참고자료

- [Visual Studio에서 데이터에 Windows Forms 컨트롤 바인딩](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)