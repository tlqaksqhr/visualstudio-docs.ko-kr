---
title: '방법: 응용 프로그램 아이콘 지정(Visual Basic, C#)'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- icons [Visual Studio], application
- application properties [Visual Studio], icons
- application icons [Visual Studio]
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 8da1de87031db962ede178a742325d9206e808c3
ms.sourcegitcommit: e13e61ddea6032a8282abe16131d9e136a927984
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/26/2018
ms.locfileid: "31945222"
---
# <a name="how-to-specify-an-application-icon-visual-basic-c"></a>방법: 응용 프로그램 아이콘 지정(Visual Basic, C#)

프로젝트에 대한 `Icon` 속성은 컴파일된 응용 프로그램에 대해 **파일 탐색기** 및 Windows 작업 표시줄에서 표시되는 아이콘 파일(*.ico*)을 지정합니다.

`Icon` 속성은 **프로젝트 디자이너**의 **응용 프로그램** 창에서 액세스할 수 있습니다. 이 속성에는 리소스나 콘텐츠 파일로 프로젝트에 추가된 아이콘 목록이 포함되어 있습니다.

> [!NOTE]
> 응용 프로그램에 대한 아이콘 속성을 설정한 후에는 응용 프로그램에서 각 **창** 또는 **폼**의 `Icon` 속성도 설정할 수 있습니다. WPF(Windows Presentation Foundation) 독립 실행형 응용 프로그램의 창 아이콘에 대한 자세한 내용은 <xref:System.Windows.Window.Icon%2A>속성을 참조하세요.

## <a name="to-specify-an-application-icon"></a>응용 프로그램 아이콘을 지정하려면

1. **솔루션 탐색기**에서 프로젝트 노드(**솔루션** 노드 아님)를 선택합니다.

1. 메뉴 모음에서 **프로젝트** > **속성**을 선택합니다.

1. **프로젝트 디자이너**가 나타나면 **응용 프로그램** 탭을 선택합니다.

1. **(Visual Basic)**&mdash; **아이콘** 목록에서 아이콘 파일(*.ico*)을 선택합니다.

    **C#** &mdash; **아이콘** 목록 근처에서 **\<찾아보기...>** 단추를 선택한 다음, 원하는 아이콘 파일의 위치로 이동합니다.

## <a name="see-also"></a>참고 항목

- [응용 프로그램 페이지, 프로젝트 디자이너(Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md)
- [응용 프로그램 페이지, 프로젝트 디자이너(C#)](../ide/reference/application-page-project-designer-csharp.md)