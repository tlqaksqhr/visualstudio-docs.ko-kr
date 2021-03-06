---
title: 프로세스 속성 대화 상자, 메모리 탭 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: reference
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: a70785f2-5997-40ec-a90f-80a52449768b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b43dd047e4ebdb145092dc3b9f37098b8db6322e
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/18/2018
ms.locfileid: "31474621"
---
# <a name="memory-tab-process-properties-dialog-box"></a>프로세스 속성 대화 상자, 메모리 탭
사용 하 여는 **메모리** 프로세스 메모리를 사용 하는 방법을 보여 줍니다.를 탭 합니다. 표시 하는 [프로세스 속성 대화 상자](../debugger/process-properties-dialog-box.md), 포커스를 이동 하는 [프로세스 뷰](../debugger/processes-view.md) 창. 트리에서 프로세스 노드를 선택한 후 선택 **속성** 에서 **보기** 메뉴.  
  
 다음 설정은에 사용할 수는 **메모리** 탭:  
  
|입력|설명|  
|-----------|-----------------|  
|**가상 바이트**|프로세스에서 사용 중인 가상 주소 공간의 현재 크기 (바이트)에 있습니다. 가상 주소 공간의 사용 반드시 해당 디스크 또는 주 메모리 페이지를 사용을 의미 하지 않습니다. 그러나 가상 공간이 한정 되어 있으므로 너무 많이 라이브러리를 로드 하는 프로세스의 기능 제한할 수 있습니다를 사용 하 여 합니다.|  
|**최대 가상 바이트**|한 번에 사용한 프로세스 가상 주소 공간의 바이트의 최대 수입니다.|  
|**작업 집합**|프로세스의 스레드가 최근에 작업 한 메모리 페이지의 집합입니다. 컴퓨터에서 사용 가능한 메모리가 임계값 보다 크면, 페이지는 사용 중에서이 아니라도 프로세스의 작업 집합에 남아 있습니다. 사용 가능한 메모리가 임계값 미만이 때 페이지는 작업 집합에서 지워집니다. 필요할 경우 됩니다 다시 작업 집합에 소프트 오류 처리 주 메모리 전에.|  
|**최대 작업 집합**|어느 시점에서이 프로세스의 작업 집합에서 페이지의 최대 수입니다.|  
|**페이징된 풀 바이트**|프로세스에서 할당 한 페이징된 풀의 현재 시간. 페이징된 풀은 지정된 된 작업을 수행할 때 운영 체제 구성 요소가 그 공간을 확보 하는 시스템 메모리 영역입니다. 페이징된 풀 페이지 지속된 기간에 대 한 시스템에서 액세스 하지 않을 때 페이징 파일에 페이지 아웃할 수 있습니다.|  
|**비페이징된 풀 바이트**|현재 프로세스에 의해 할당 된 비페이징된 풀의 바이트 수입니다. 비페이징된 풀은 지정된 된 작업을 수행할 때 운영 체제 구성 요소에서 공간 확보는 시스템 메모리 영역입니다. 페이징 파일;에 비페이징된 풀 페이지 아웃 호출 될 수 없습니다. 할당 된 상태로 주 메모리에 유지 합니다.|  
|**전용 바이트**|이 프로세스가 할당 하는 바이트 수가 현재 다른 프로세스와 공유할 수 없습니다.|  
|**사용 가능한 바이트**|이 프로세스의 총 사용 하지 않는 가상 주소 공간입니다.|  
|**예약 된 바이트**|이 프로세스에서 사용 하도록 예약 하는 가상 메모리의 총 양입니다.|  
|**사용 가능한 이미지 바이트**|이 프로세스 내에서 이미지에 의해 예약 또는 사용에서 하지 않은 가상 주소 공간의 크기입니다.|  
|**예약 된 이미지 바이트**|이 프로세스 내에서 실행 되는 이미지에서 예약 된 모든 가상 메모리의 합계입니다.|