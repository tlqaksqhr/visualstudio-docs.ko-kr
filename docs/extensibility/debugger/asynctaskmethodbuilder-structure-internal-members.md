---
title: AsyncTaskMethodBuilder 구조-내부 멤버 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debug engines, AsyncTaskMethodBuilder structure [.NET Framework]
- AsyncTaskMethodBuilder structure [.NET Framework debug engines]
ms.assetid: f32f5857-7ef8-45fd-8b5a-7f644eb98b11
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 130a3236752fba85c611619fb3cae70e00c76ec9
ms.sourcegitcommit: 0e5289414d90a314ca0d560c0c3fe9c88cb2217c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/19/2018
ms.locfileid: "39150968"
---
# <a name="asynctaskmethodbuilder-structure---internal-members"></a>AsyncTaskMethodBuilder 구조-내부 멤버
내부 멤버에 설명 합니다 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder> 클래스입니다. 이 클래스에 대 한 일반 정보에 대 한 참조를 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder> 참조 항목입니다.  
  
 **Namespace:** <xref:System.Runtime.CompilerServices?displayProperty=fullName>  
  
 **어셈블리:** mscorlib (mscorlib.dll)  
  
 .NET Framework에서 이러한 내부 멤버에 액세스할 수 없는 때문에 다음 구문은 공통 중간 언어 (CIL) 제공 됩니다.  
  
## <a name="syntax"></a>구문  
  
```csharp  
.class public sequential ansi sealed beforefieldinit System.Runtime.CompilerServices.AsyncTaskMethodBuilder  
       extends System.ValueType  
       implements System.Runtime.CompilerServices.IAsyncMethodBuilder  
```  
  
## <a name="internal-members"></a>내부 멤버  
  
|name|설명|  
|----------|-----------------|  
|[ObjectIdForDebugger 속성](../../extensibility/debugger/asynctaskmethodbuilder-objectidfordebugger-property.md)|이 작성기 디버거를 고유 하 게 식별 하는 데 사용할 수 있는 개체를 가져옵니다.|  
|[m_builder 필드](../../extensibility/debugger/asynctaskmethodbuilder-m-builder-field.md)|제네릭이 아닌 인스턴스가 대리자는 제네릭 작성기 개체를 나타냅니다.|  
  
## <a name="see-also"></a>참고자료  
 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder>   
 [.NET Framework에 대 한 병렬 확장 기능 내부](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)