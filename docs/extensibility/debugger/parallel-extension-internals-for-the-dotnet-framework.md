---
title: 확장 기능의 내부.NET Framework에 대 한 병렬 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debug engines, internals [.NET Framework]
ms.assetid: 93e07cfa-91fa-464c-b866-8bf5570411df
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 84b4106509f62f1929f20283bc86c7930c22d39b
ms.sourcegitcommit: 71b307ce86c4079cc7ad686d8d5f96a6a123aadd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/25/2018
ms.locfileid: "39251087"
---
# <a name="parallel-extension-internals-for-the-net-framework"></a>.NET Framework에 대 한 병렬 확장 기능 내부
이 섹션에서는 내부 형식, 메서드를 설명 하 고 도움이 되는 클래스의 필드 parallel extensions to.NET Framework에 대 한 사용자 지정 디버거를 구현 합니다.  
  
## <a name="in-this-section"></a>단원 내용  
 [Task 클래스](../../extensibility/debugger/task-class-internal-members.md)  
 내부 데이터 멤버를 설명 합니다 <xref:System.Threading.Tasks.Task?displayProperty=fullName> 클래스입니다.  
  
 [TaskScheduler 클래스](../../extensibility/debugger/taskscheduler-class-internal-members.md)  
 내부 데이터 멤버를 설명 합니다 <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName> 클래스입니다.  
  
 [ContingentProperties 클래스](../../extensibility/debugger/contingentproperties-class-internal-members.md)  
 내부 데이터 멤버를 설명 합니다 `System.Threading.Tasks.ContingentProperties` 클래스입니다.  
  
 [AsyncTaskMethodBuilder 구조](../../extensibility/debugger/asynctaskmethodbuilder-structure-internal-members.md)  
 내부 멤버를 설명 합니다 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder> 구조입니다.  
  
 [AsyncTaskMethodBuilder\<TResult > 구조](../../extensibility/debugger/asynctaskmethodbuilder-tresult-structure-internal-members.md)  
 내부 멤버를 설명 합니다 <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601> 구조입니다.  
  
 [AsyncVoidMethodBuilder 구조](../../extensibility/debugger/asyncvoidmethodbuilder-structure-internal-members.md)  
 내부 멤버를 설명 합니다 <xref:System.Runtime.CompilerServices.AsyncVoidMethodBuilder> 구조입니다.  
  
## <a name="see-also"></a>참고자료  
 <xref:System.Threading.Tasks.Task?displayProperty=fullName>   
 <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName>   
 [Visual Studio 디버거 확장성](../../extensibility/debugger/visual-studio-debugger-extensibility.md)   
 [병렬 프로그래밍](/dotnet/standard/parallel-programming/index)