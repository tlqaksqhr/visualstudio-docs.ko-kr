---
title: 프로젝트 구성 개체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- project configurations, object
- objects, project configuration
ms.assetid: 877756c9-4261-43d9-9f32-51bf06b4219f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7385a5f7768a57fd1a3d9688df152fd60a1ea130
ms.sourcegitcommit: 6a9d5bd75e50947659fd6c837111a6a547884e2a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2018
ms.locfileid: "31136031"
---
# <a name="project-configuration-object"></a>프로젝트 구성 개체
프로젝트 구성 개체 관리 UI에 구성 정보를 표시 합니다.  
  
 ![Visual Studio 프로젝트 구성](../../extensibility/internals/media/vsprojectcfg.gif "vsProjectCfg")  
프로젝트 구성 속성 페이지  
  
 프로젝트 구성 공급자 프로젝트 구성을 관리합니다. 환경 및 다른 패키지를 액세스 하려면 프로젝트의 구성에 대 한 정보를 검색 하 고, 프로젝트 구성 공급자 개체에 연결 된 인터페이스를 호출 합니다.  
  
> [!NOTE]
>  만들 하거나 솔루션 구성 파일을 프로그래밍 방식으로 편집할 수 없습니다. 사용 해야 `DTE.SolutionBuilder`합니다. 참조 [솔루션 구성](../../extensibility/internals/solution-configuration.md) 자세한 정보에 대 한 합니다.  
  
 구성 UI에서에서 사용할 표시 이름에 게시 하려면 프로젝트를 구현 해야 <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfg.get_DisplayName%2A>합니다. 환경 <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2.GetCfgs%2A>의 목록을 반환 하는 `IVsCfg` 환경 UI에 표시할 구성 및 플랫폼 정보에 대 한 디스플레이 이름을 하는 데 사용할 수 있는 포인터입니다. 활성 구성 및 플랫폼 활성 솔루션 구성에 저장 된 프로젝트의 구성에 의해 결정 됩니다. <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionBuildManager.FindActiveProjectCfg%2A> 메서드를 사용 하 여 활성 프로젝트 구성을 검색할 수 있습니다.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfgProvider> 개체에 선택적으로 구현할 수 있습니다는 <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2> 개체는 <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProviderEventsHelper> 검색할 수 있도록 하는 개체는 `IVsProjectCfg2` 정식 프로젝트 구성 이름에 따라 개체입니다.  
  
 프로젝트 구성에 액세스할 수 있는 다른 프로젝트 및 환경을 제공 하는 다른 방법은의 구현을 제공 하는 프로젝트에 대해는 `IVsCfgProvider2::GetCfgs` 메서드를 하나 이상 구성 개체를 반환 합니다. 프로젝트 구현할 수도 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectCfg2>에서 상속 되 `IVsProjectCfg` 함으로써에서 `IVsCfg`, 구성 관련 정보를 제공 합니다. <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider2> 추가, 삭제 및 프로젝트 구성 이름 바꾸기에 대 한 플랫폼 및 기능을 지원 합니다.  
  
> [!NOTE]
>  Visual Studio는 두 가지 구성 유형을 제한 더 이상, 구성을 처리 하는 코드 작성 하지 않아야 가정을와 구성의 숫자에 대 한 또는 가정에 쓸 수 해야 하므로 하나만 지정 된 프로젝트 구성이는 디버그 또는 소매 반드시 되었습니다. 이렇게 하면 사용 <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfg.get_IsReleaseOnly%2A> 및 <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfg.get_IsDebugOnly%2A> 사용 되지 않습니다.  
  
 호출 `QueryInterface` 에서 반환 된 개체에`IVsGetCfgProvider::GetCfgProvider` 검색 `IVsCfgProvider2`합니다. 경우 `IVsGetCfgProvider` 호출 하 여 찾을 수 없습니다 `QueryInterface` 에 `IVsProject3` 프로젝트 개체를 호출 하 여 구성 공급자 개체를 액세스할 수 있습니다 `QueryInterface` 에 대해 반환 되는 개체에 대 한 계층 루트 브라우저 개체에 `IVsHierarchy::GetProperty(VSITEM_ROOT, VSHPROPID_BrowseObject)`, 또는 에 대해 반환 되는 구성 공급자에 대 한 포인터 `IVsHierarchy::GetProperty(VSITEM_ROOT, VSHPROPID_ConfigurationProvider)`합니다.  
  
 `IVsProjectCfg2` 주로 빌드, 디버깅에 대 한 액세스 및 배포 관리 개체를 제공 하 고 프로젝트 출력 그룹 수를 허용 합니다. 메서드 `IVsProjectCfg` 및 `IVsProjectCfg2` 구현 하는 데 사용 될 <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildableProjectCfg> 빌드 프로세스를 관리 및 <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputGroup> 구성의 출력 그룹에 대 한 포인터입니다.  
  
 프로젝트는 동일한 수의 그룹 포함 된 출력 수 구성 구성에서 다를 수 있습니다 하는 경우에 지원 되는 각 구성에 대 한 그룹을 반환 해야 합니다. 그룹도 있어야 합니다 (정식 이름, 표시 이름 및 그룹 정보) 동일한 식별자 정보 구성에서 구성 프로젝트 내에서. 자세한 내용은 참조 [출력에 대 한 프로젝트 구성](../../extensibility/internals/project-configuration-for-output.md)합니다.  
  
 디버깅을 사용 하 여 구성을 구현 해야 <xref:Microsoft.VisualStudio.Shell.Interop.IVsDebuggableProjectCfg>합니다. `IVsDebuggableProjectCfg` 디버거가 구성을 시작할 수 있도록 허용 하는 프로젝트에서 구현 되는 선택적 인터페이스 이며로 구성 개체에서 구현 되는 `IVsCfg` 및 `IVsProjectCfg`합니다. 환경 f5 키를 눌러 디버거를 시작 하는 사용자가 호출 됩니다.  
  
 `ISpecifyPropertyPages` 및 `IDispatch` 속성 페이지와 함께에서 검색 하 고 사용자에 게 구성에 종속 된 정보를 표시 하는 데 사용 됩니다. 자세한 내용은 참조 [속성 페이지](../../extensibility/internals/property-pages.md)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [구성 옵션을 관리](../../extensibility/internals/managing-configuration-options.md)   
 [만들기에 대 한 프로젝트 구성](../../extensibility/internals/project-configuration-for-building.md)   
 [출력에 대 한 프로젝트 구성](../../extensibility/internals/project-configuration-for-output.md)   
 [속성 페이지](../../extensibility/internals/property-pages.md)   
 [솔루션 구성](../../extensibility/internals/solution-configuration.md)