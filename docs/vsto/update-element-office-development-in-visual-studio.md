---
title: '&lt;업데이트&gt; 요소 (Visual Studio에서 Office 개발)'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- update element
- <update> element
- application manifests [Office development in Visual Studio], <update> element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: c51a7f79165d421f080d05088418d02a48680b66
ms.sourcegitcommit: 4cd4aef53e7035d23e7d1d0f66f51ac8480622a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/05/2018
ms.locfileid: "34767610"
---
# <a name="ltupdategt-element-office-development-in-visual-studio"></a>&lt;업데이트&gt; 요소 (Visual Studio에서 Office 개발)
  `update` 요소 업데이트에 대 한 솔루션은 확인 간격을 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```xml  
<update  
  enabled>  
  <expiration  
    maximumAge  
    unit  
  />  
</update>  
```  
  
## <a name="elements-and-attributes"></a>요소 및 특성  
 `update` 요소는 필수이며 `vstav3` 네임스페이스에 있습니다.  
  
 `update` 요소에는 다음 특성이 있습니다.  
  
|특성|설명|  
|---------------|-----------------|  
|`enabled`|필수. 다음 값 중 하나를 사용을 설정 합니다.<br /><br /> -   **true 이면** 업데이트를 확인 합니다.<br />-   **false** 를 업데이트를 확인 하지 않습니다.|  
  
 `update` 요소에는 다음 자식 요소가 있습니다.  
  
### <a name="expiration"></a>만료  
 `expiration` 요소는 필수이며 `vstav3` 네임스페이스에 있습니다. 이 요소는 업데이트에 대 한 솔루션을 확인 하는 간격을 지정 합니다.  
  
 `expiration` 요소에는 다음 특성이 있습니다.  
  
|특성|설명|  
|---------------|-----------------|  
|`maximumAge`|   필수. 이 값은 정수로 설정 합니다.|  
|`unit`|필수. 설정 `unit` 를 다음 값 중 하나:<br /><br /> -   **시간**<br />-   **(일)**<br />-   **주**|  
  
## <a name="example-of-always-checking-for-updates"></a>업데이트를 항상 확인의 예  
  
### <a name="description"></a>설명  
 다음 코드 예제는 `update` 항상 Office 솔루션에서 업데이트를 확인 하도록 설정 된 요소입니다.  
  
### <a name="code"></a>코드  
  
```xml  
<vstav3:update enabled="true" />  
```  
  
## <a name="example-of-setting-a-default-update-interval"></a>기본 업데이트 간격을 설정 하는 예  
  
### <a name="description"></a>설명  
 다음 코드 예제는 `update` Office 솔루션에 대 한 응용 프로그램 매니페스트에서 요소입니다. 이 코드 예제는에 제공 된 큰 예제의 일부 [Office 솔루션에 대 한 응용 프로그램 매니페스트](../vsto/application-manifests-for-office-solutions.md)합니다.  
  
### <a name="code"></a>코드  
  
```xml  
<vstav3:update enabled="true">  
    <vstav3:expiration maximumAge="7" unit="days" />  
</vstav3:update>  
```  
  
## <a name="see-also"></a>참고자료  
 [ClickOnce를 사용 하 여 Office 솔루션 배포](../vsto/deploying-an-office-solution-by-using-clickonce.md)   
 [Office 솔루션에 대 한 응용 프로그램 매니페스트](../vsto/application-manifests-for-office-solutions.md)   
 [Office 솔루션의 배포 매니페스트](../vsto/deployment-manifests-for-office-solutions.md)   
 [ClickOnce 응용 프로그램 매니페스트](/visualstudio/deployment/clickonce-application-manifest)  
  
  