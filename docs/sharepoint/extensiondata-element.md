---
title: ExtensionData 요소 | Microsoft Docs
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ExtensionData element
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 9cb80965385d7d258523dc0caf5291791c5ea09a
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36326233"
---
# <a name="extensiondata-element"></a>ExtensionData 요소
  SharePoint 프로젝트 항목에 연관 된 사용자 지정 데이터 항목의 컬렉션을 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```xml  
<ExtensionData>  
  <ExtensionDataItem.../>  
</ExtensionData>  
```  
  
## <a name="attributes-and-elements"></a>특성 및 요소
 다음 단원에서는 특성, 자식 요소 및 부모 요소에 대해 설명합니다.  
  
### <a name="attributes"></a>특성  
 없음  
  
### <a name="child-elements"></a>자식 요소
  
|요소|설명|  
|-------------|-----------------|  
|[ExtensionDataItem](../sharepoint/extensiondataitem-element.md)|선택적 요소입니다.<br /><br /> 키/값 형식의 SharePoint 프로젝트 항목과 연결 된 사용자 지정 데이터 항목을 나타냅니다. 키와 값을 모두 문자열 이어야 합니다.|  
  
### <a name="parent-elements"></a>부모 요소
  
|요소|설명|  
|-------------|-----------------|  
|[프로젝트 항목](../sharepoint/projectitem-element.md)|SharePoint 프로젝트 항목을 나타냅니다. 이 요소는 필수 루트 요소에는 `.spdata` 파일.|  
  
## <a name="remarks"></a>설명  
 사용 하 여 SharePoint 프로젝트 항목을 사용 하 여 사용자 지정 데이터를 연결 하는 경우는 <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> 의 속성은 <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem> 개체, 데이터를 저장 하는 Visual Studio는 **ExtensionData** 요소에는 `.spdata` 프로젝트의 파일 항목입니다. 자세한 내용은 [SharePoint 프로젝트 시스템의 확장에 데이터를 저장](../sharepoint/saving-data-in-extensions-of-the-sharepoint-project-system.md)합니다.  
  
## <a name="element-information"></a>요소 정보
  
|||  
|-|-|  
|**네임스페이스**|http<nolink>: //schemas.microsoft.com/VisualStudio/<br>2010/SharePointTools/SharePointProjectItemModel|  
|**스키마 이름**|SharePoint 프로젝트 항목 스키마|  
|**유효성 검사 파일**|ProjectItemModelSchema.xsd|  
|**비어 있을 수 있습니다.**|아니요|  
  
## <a name="see-also"></a>참고자료
 [SharePoint 프로젝트 항목 스키마 참조](../sharepoint/sharepoint-project-item-schema-reference.md)  
  
  
