---
title: '방법: 프로파일링 도구 호출 추적 보고서 만들기 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- performance tools, viewing ETW data
- ETW [Visual Studio ALM], viewing data
ms.assetid: 7640520a-7d3c-456c-b184-872a5d2f82f3
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a363554dfab8463ed91a82ffae9dea4f52d435d4
ms.sourcegitcommit: 1b9c1e333c2f096d35cfc77e846116f8e5054557
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34815732"
---
# <a name="how-to-create-a-profiling-tools-call-trace-report"></a>방법: 프로파일링 도구 호출 추적 보고서 만들기
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 프로파일링 도구에 대한 *호출 추적 보고서*는 응용 프로그램의 함수에 대한 각 진입 지점 및 종료 지점에 대한 타이밍 정보와 함수로 다른 함수에 대한 각 호출을 나열합니다. 호출 추적 보고서는 계측 방법으로 수집된 경우에만 프로파일링 데이터에 사용할 수 있습니다.  
  
> [!NOTE]
>  [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]에서 호출 추적 보고서를 표시할 수 없습니다. **VSPerfReport** 명령줄 도구를 사용하여 쉼표로 구분된 값(.*csv*) 또는 .*xml* 파일을 생성해야 합니다. 이 도구에 대한 자세한 내용은 [VSPerfReport](../profiling/vsperfreport.md)를 참조하세요.  
  
### <a name="to-create-a-call-trace-report"></a>호출 추적 보고서를 만들려면  
  
1.  **명령 프롬프트** 창을 엽니다.  
  
2.  명령 프롬프트에 다음 명령을 입력합니다.  
  
     *ToolsPath* **VSPerfReport** *VSPFile*  **/CallTrace [/Xml]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|프로파일링 도구 명령줄 도구의 경로입니다. 자세한 내용은 [명령줄 도구의 경로 지정](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)을 참조하세요.|  
    |*VSPFile*|프로파일링 데이터(.*vsp* 또는 .*vsps*) 파일입니다. 전체 및 부분 경로를 사용할 수 있습니다.|  
    |Xml|XML 형식의 보고서를 생성합니다.|  

  
## <a name="see-also"></a>참고 항목  
 [방법: ETW(Windows용 이벤트 추적) 데이터 수집](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)   
 [프로파일링 도구 API](../profiling/profiling-tools-apis.md)
