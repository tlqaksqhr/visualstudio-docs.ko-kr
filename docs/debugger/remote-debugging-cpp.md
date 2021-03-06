---
title: 원격 Visual c + + 프로젝트를 디버그 | Microsoft Docs
ms.custom: remotedebugging
ms.date: 08/14/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
- FSharp
- CSharp
- JScript
- VB
helpviewer_keywords:
- remote debugging, setup
ms.assetid: 8b8eca0d-122f-4eda-848a-cf0945f207d0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- cplusplus
ms.openlocfilehash: 334a0b964033282458c211d69af30aad20dbd6bc
ms.sourcegitcommit: c57ae28181ffe14a30731736661bf59c3eff1211
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/11/2018
ms.locfileid: "38781947"
---
# <a name="remote-debugging-a-visual-c-project-in-visual-studio"></a>Visual Studio에서 Visual c + + 프로젝트 원격 디버그
다른 컴퓨터에 Visual Studio 응용 프로그램을 디버깅 설치 하 고 앱을 배포할 컴퓨터의 원격 도구를 실행 하려면 Visual Studio에서 원격 컴퓨터에 연결 및 다음 배포 하 고 앱을 실행 하도록 프로젝트를 구성 합니다.

![원격 디버거 구성 요소](../debugger/media/remote-debugger-client-apps.png "Remote_debugger_components")

원격 디버깅 유니버설 Windows 앱 (UWP)에 대 한 정보를 참조 하세요 [설치 된 앱 패키지 디버그](debug-installed-app-package.md)합니다.

## <a name="requirements"></a>요구 사항

원격 디버거는 Windows 7에서 지원 되며 최신 (phone 있는 경우) 및 Windows Server 2008 서비스 팩 2부터 Windows Server의 버전입니다. 요구 사항의 전체 목록은 참조 하세요 [요구 사항](../debugger/remote-debugging.md#requirements_msvsmon)합니다.

> [!NOTE]
> 프록시를 통해 연결 하는 두 컴퓨터 간에 디버깅이 지원 되지 않습니다. 국가 간 높은 대기 시간 또는 낮은 대역폭 연결에서는 인터넷에 접속 등을 통해 또는 인터넷을 통해 디버깅 권장 되지 않습니다 및 실패 하거나 느리고 수 있습니다.
  
## <a name="download-and-install-the-remote-tools"></a>원격 도구 다운로드 및 설치

[!INCLUDE [remote-debugger-download](../debugger/includes/remote-debugger-download.md)]
  
> [!TIP]
> 일부 시나리오에서는 파일 공유에서 원격 디버거를 실행 하는 것이 가장 효율적일 수 있습니다. 자세한 내용은 [파일 공유에서 원격 디버거 실행](../debugger/remote-debugging.md#fileshare_msvsmon)합니다.
  
## <a name="BKMK_setup"></a> 원격 디버거 설정

[!INCLUDE [remote-debugger-configuration](../debugger/includes/remote-debugger-configuration.md)]

> [!NOTE]
> 추가 사용자에 대 한 사용 권한을 추가 하는 인증 모드를 변경 하거나 원격 디버거의 포트 번호에 필요한 경우 참조 [원격 디버거 구성](../debugger/remote-debugging.md#configure_msvsmon)합니다.

## <a name="remote_cplusplus"></a> Visual c + + 프로젝트 원격 디버그  
 다음 절차에서는 이름 및 프로젝트의 경로 C:\remotetemp\MyMfc이 고 원격 컴퓨터의 이름이 **MJO DL**합니다.  
  
1.  명명 된 MFC 응용 프로그램 만들기 **mymfc 합니다.**  
  
2.  쉽게 도달할 수 있는, 예를 응용 프로그램의 어딘가에 중단점을 설정 **MainFrm.cpp**를 시작할 때 `CMainFrame::OnCreate`합니다.  
  
3.  솔루션 탐색기에서 마우스 오른쪽 단추로 클릭 프로젝트를 마우스 **속성**합니다. 엽니다는 **디버깅** 탭 합니다.  
  
4.  설정 된 **실행할 디버거** 하 **원격 Windows 디버거**합니다.  
  
     ![RemoteDebuggingCPlus](../debugger/media/remotedebuggingcplus.png "RemoteDebuggingCPlus")  
  
5.  다음과 같이 속성을 변경합니다.  
  
    |설정|값|
    |-|-|  
    |원격 명령|C:\remotetemp\mymfc.exe|  
    |작업 디렉터리|C:\remotetemp|  
    |원격 서버 이름|MJO DL:*portnumber*|  
    |연결|Windows 인증을 사용한 원격|  
    |디버거 형식|네이티브 전용|  
    |배포 디렉터리|C:\remotetemp.|  
    |배포할 추가 파일|C:\data\mymfcdata.txt.|  
  
     추가 파일 (선택 사항)을 배포 하는 경우 두 컴퓨터 모두에서 폴더가 있어야 합니다.  
  
6.  솔루션 탐색기에서 솔루션을 마우스 오른쪽 단추로 클릭 하 고 선택 **Configuration Manager**합니다.  
  
7.  에 대 한 합니다 **디버그** 구성을 선택 합니다 **배포** 확인란 합니다.  
  
     ![RemoteDebugCplusDeploy](../debugger/media/remotedebugcplusdeploy.png "RemoteDebugCplusDeploy")  
  
8.  디버깅을 시작 (**디버그 > 디버깅 시작**, 또는 **F5**).  
  
9. 실행 파일이 원격 컴퓨터에 자동으로 배포됩니다.  
  
10. 메시지가 표시 되 면 원격 컴퓨터에 연결할 네트워크 자격 증명을 입력 합니다.  
  
     필요한 자격 증명은 네트워크의 보안 구성에 적용 됩니다. 예를 들어, 도메인 컴퓨터에서 보안 인증서를 선택 하면 또는 도메인 이름 및 암호를 입력 합니다. 도메인이 아닌 컴퓨터에서 입력할 수 있습니다 컴퓨터 이름 및 유효한 사용자 계정 이름 같은 **MJO-DL\name@something.com**, 올바른 암호와 함께 합니다.  
  
11. Visual Studio 컴퓨터에서 실행이 중단점에서 중지된 것이 표시됩니다.  
  
    > [!TIP]
    >  또는 별도의 단계로 파일을 배포할 수 있습니다. 에 **솔루션 탐색기** 마우스 오른쪽 단추로 클릭 합니다 **mymfc** 노드를 선택한 후 **배포**.  
  
 응용 프로그램에서 사용해야 하는 비코드 파일이 있는 경우 Visual Studio 프로젝트에 포함해야 합니다. 추가 파일을 프로젝트 폴더를 만듭니다 (에 **솔루션 탐색기**, 클릭 **추가 > 새 폴더**.) 다음 폴더에 파일 추가 (에 **솔루션 탐색기**, 클릭 **추가 > 기존 항목**, 파일을 선택). 에 **속성** 각 파일에 대 한 페이지에서 설정 **출력 디렉터리로 복사** 하 **항상 복사**합니다.
  
## <a name="set-up-debugging-with-remote-symbols"></a>원격 기호를 사용한 디버깅 설정 

[!INCLUDE [remote-debugger-symbols](../debugger/includes/remote-debugger-symbols.md)] 
  
## <a name="see-also"></a>참고 항목  
 [Visual Studio의 디버깅](../debugger/index.md)  
 [디버거 기능 둘러보기](../debugger/debugger-feature-tour.md)   
 [원격 디버깅용 Windows 방화벽 구성](../debugger/configure-the-windows-firewall-for-remote-debugging.md)   
 [원격 디버거 포트 할당](../debugger/remote-debugger-port-assignments.md)   
 [원격 IIS 컴퓨터의 원격 디버깅 ASP.NET](../debugger/remote-debugging-aspnet-on-a-remote-iis-computer.md)  
 [원격 디버깅 오류 및 문제 해결](../debugger/remote-debugging-errors-and-troubleshooting.md)