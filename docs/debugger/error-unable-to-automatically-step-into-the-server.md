---
title: '오류: 자동으로 한 단계씩 코드 실행 서버에 없습니다. | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.causality_no_server_response
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, notification error
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a8c79669da0e20bc7376d68c4ea782d280eb6df3
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31471660"
---
# <a name="error-unable-to-automatically-step-into-the-server"></a>오류: 서버에 대해 자동으로 한 단계씩 코드를 실행할 수 없습니다.
이 오류 메시지는 다음과 같습니다.  
  
 서버에 대해 자동으로 한 단계씩 코드를 실행할 수 없습니다. 원격 프로시저가 실행되기 전에 디버거에 알리지 않았습니다.  
  
 이 오류는 웹 서비스를 한 단계씩 실행하려 할 때 발생할 수 있습니다. [한 단계씩 XML Web Services 실행](http://msdn.microsoft.com/en-us/8e67de38-bf5f-41cc-a457-1b88ce63d764)을 참조하세요. 이 오류는 [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] 이 잘못 설정된 경우에 발생할 수 있습니다.  
  
 가능한 원인은 다음과 같습니다.  
  
-   [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] 응용 프로그램의 web.config 파일에서 디버그 모드를 "true"로 설정하지 않았습니다. [ASP.NET 응용 프로그램의 디버그 모드](../debugger/how-to-enable-debugging-for-aspnet-applications.md)를 참조하세요.  
  
-   Visual Studio가 설치된 후 [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] 버전이 설치되었습니다. [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] 은 Visual Studio보다 먼저 설치해야 합니다. 이 문제를 해결 하려면 Windows를 사용 하 여 **제어판 > 프로그램 및 기능** Visual Studio 설치를 복구 해야 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [원격 디버깅 오류 및 문제 해결](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [원격 디버깅](../debugger/remote-debugging.md)