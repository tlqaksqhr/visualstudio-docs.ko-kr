---
title: Visual Studio를 사용하여 C#으로 ASP.NET Core 웹앱 만들기
description: C#을 사용하여 단계별로 Visual Studio에서 ASP.NET Core 웹앱을 만드는 방법을 알아봅니다.
ms.custom: mvc
ms.date: 07/20/2018
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: quickstart
author: TerryGLee
ms.author: tglee
manager: douge
dev_langs:
- CSharp
ms.workload:
- aspnet
- dotnetcore
ms.openlocfilehash: cbb43f61aab1df099efca01b56a927cf189a808e
ms.sourcegitcommit: 0cf1e63b6e0e6a0130668278489b21a6e5038084
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39468980"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-aspnet-core-web-app"></a>빠른 시작: Visual Studio를 사용하여 첫 번째 ASP.NET Core 웹앱 만들기

이 5~10분 진행되는 Visual Studio를 사용하는 방법에 대한 소개에서 ASP.NET 프로젝트 템플릿과 C# 프로그래밍 언어를 사용하여 간단한 "Hello World" 웹앱을 만듭니다.

아직 Visual Studio를 설치하지 않은 경우 [Visual Studio 다운로드](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) 페이지로 이동하여 체험용으로 설치합니다.

## <a name="create-a-project"></a>프로젝트 만들기

먼저, ASP.NET Core 웹 응용 프로그램 프로젝트를 만듭니다. 또한 프로젝트 형식에는 어떤 것을 추가하기도 전에 웹앱을 만들 수 있는 모든 템플릿 파일이 함께 제공됩니다!

1. Visual Studio 2017을 엽니다.

1. 메뉴 모음에서 **파일** > **새로 만들기** > **프로젝트**를 차례로 선택합니다.

1. **새 프로젝트** 대화 상자의 왼쪽 창에서 **Visual C#** 을 확장하고 **.NET Core**를 선택합니다. 가운데 창에서 **ASP.NET Core 웹 응용 프로그램**을 선택합니다. 그런 다음, 파일 이름을 `HelloWorld`로 지정하고 **확인**을 선택합니다.

   ![C#용 새 ASP.NET Core 웹 응용 프로그램 프로젝트 만들기](../ide/media/csharp-aspnet-choose-template-name-file.png)

   > [!NOTE]
   > **.NET Core** 프로젝트 템플릿 범주가 표시되지 않으면 왼쪽 창에서 **Visual Studio 설치 관리자 열기** 링크를 선택합니다.
   >
   > ![새 프로젝트 대화 상자에서 Visual Studio 설치 관리자 열기](../ide/media/open-visual-studio-installer.png)
   >
   > Visual Studio 설치 관리자가 시작됩니다. **ASP.NET 및 웹 개발** 워크로드를 선택한 다음 **수정**을 선택합니다.
   >
   > ![VS 설치 관리자에서 ASP.NET 워크로드](../ide/media/quickstart-aspnet-workload.png)
   >
   > (새 워크로드를 계속 설치하려면 먼저 Visual Studio를 닫아야 할 수 있습니다.)

1. **새 ASP.NET Core 웹 응용 프로그램** 대화 상자의 위쪽 드롭다운 메뉴에 **ASP.NET Core 2.0** 이 표시되는지 확인합니다. 그런 다음, **웹 응용 프로그램**을 선택하고 **확인**을 선택합니다.

   ![새 ASP.NET Core 웹 응용 프로그램 대화 상자](../ide/media/quickstart-aspnet-core20.png)

곧 Visual Studio에서 프로젝트 파일이 열립니다.

## <a name="create-the-app"></a>앱 만들기

1. **솔루션 탐색기**에서 **Pages** 폴더를 확장한 다음, **About.cshtml**을 선택합니다.

   ![솔루션 탐색기에서 About.cshtml 파일 선택](../ide/media/csharp-aspnet-about-page-html-file.png)

   이 파일은 웹앱에서 이름이 **정보**로 이름이 지정된 페이지에 해당합니다.

   ![웹앱의 정보 페이지](../ide/media/csharp-aspnet-about-page.png)

   **정보** 페이지의 “추가 정보” 영역에 대한 HTML 코드가 편집기에 표시됩니다.

   ![Visual Studio 편집기의 추가 정보 영역에 대한 HTML 코드](../ide/media/csharp-aspnet-about-cshtml-page.png)

1. “추가 정보” 텍스트를 “**Hello World!**”로 변경합니다.

   ![Visual Studio 편집기에서 추가 정보 영역의 기본 HTML 코드를 변경합니다.](../ide/media/csharp-aspnet-about-cshtml-page-hello-world.png)

1. **솔루션 탐색기**에서 **About.cshtml**을 확장한 다음, **About.cshtml.cs**를 선택합니다. (이 파일은 웹앱의 **정보** 페이지와 일치합니다.)

   ![솔루션 탐색기에서 About.cshtml 파일 선택](../ide/media/csharp-aspnet-about-page-code-file.png)

   **정보** 페이지의 “응용 프로그램 설명” 영역에 대한 텍스트를 포함하는 C# 코드가 편집기에 표시됩니다.

   ![Visual Studio 편집기의 응용 프로그램 설명 영역에 대한 C# 코드](../ide/media/csharp-aspnet-about-cshtml-cs-code.png)

1. “응용 프로그램 설명” 메시지 텍스트를 “**내 메시지란?**”으로 변경합니다.

   ![Visual Studio 편집기에서 응용 프로그램 설명 영역의 기본 메시지 텍스트 변경](../ide/media/csharp-aspnet-about-cshtml-cs-message.png)

## <a name="run-the-app"></a>앱 실행

1. **Ctrl**+**F5**를 눌러 앱을 실행하고 웹 브라우저에서 엽니다.

   > [!NOTE]
   > **‘IIS Express’ 웹 서버에 연결할 수 없습니다**라는 오류 메시지가 발생하면 Visual Studio를 닫은 후 마우스 오른쪽 단추 클릭 또는 상황에 맞는 메뉴에서 **관리자 권한으로 실행** 옵션을 사용하여 엽니다. 그런 다음 응용 프로그램을 다시 실행합니다.

1. 웹 페이지 위쪽에서 **정보**를 선택합니다.

   ![웹 페이지에서 정보 선택](../ide/media/csharp-aspnet-home-page-about.png)

1. **정보** 페이지에 추가한 업데이트된 텍스트를 봅니다.

   ![추가한 텍스트가 포함된 업데이트된 페이지 보기](../ide/media/csharp-aspnet-about-page-hello-world.png)

1. 웹 브라우저를 닫습니다.

이 빠른 시작을 완료한 것을 축하 드립니다! C#, ASP.NET Core 및 Visual Studio IDE(통합 개발 환경)를 이해하는 데 도움이 되었기를 바랍니다.

## <a name="next-steps"></a>다음 단계

자세히 알아보려면 계속 다음 자습서를 사용하세요.

> [!div class="nextstepaction"]
> [Visual Studio에서 C# 및 ASP.NET 시작](tutorial-csharp-aspnet-core.md)

## <a name="see-also"></a>참고 항목

[Visual Studio를 사용하여 Azure App Service에 웹앱 게시](..//deployment/quickstart-deploy-to-azure.md)
