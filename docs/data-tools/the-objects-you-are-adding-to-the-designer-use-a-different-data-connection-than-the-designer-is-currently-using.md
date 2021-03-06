---
title: 디자이너에 추가하려는 개체가 현재 디자이너가 사용 중인 것과 다른 데이터 연결을 사용합니다.
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.technology: vs-data-tools
ms.workload:
- data-storage
ms.openlocfilehash: a2fb26fa8960c652feefa157fb04c31b9ed7abb9
ms.sourcegitcommit: f37affbc1b885dfe246d4b2c295a6538b383a0ca
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/02/2018
ms.locfileid: "37174197"
---
# <a name="the-objects-you-are-adding-to-the-designer-use-a-different-data-connection-than-the-designer"></a>디자이너에 추가 하려는 개체가 디자이너 보다 다양 한 데이터 연결을 사용 하 여

디자이너에 추가하려는 개체가 디자이너에서 현재 사용 중인 데이터 연결이 아닌 다른 데이터 연결을 사용합니다. 디자이너에서 사용 중인 연결을 바꾸시겠습니까?

항목을 추가 하는 경우는 **Object Relational Designer** (**O/R 디자이너**), 모든 항목이 하나의 공유 데이터 연결을 사용 합니다. 디자인 화면에는 화면의 모든 개체에 대해 하나의 연결을 사용하는 <xref:System.Data.Linq.DataContext>가 표시됩니다. 디자이너에서 현재 사용하는 데이터 연결과 다른 데이터 연결을 사용하는 디자이너에 개체를 추가하면 이 메시지가 나타납니다. 이 오류를 해결하려면 기존 연결 유지를 선택하세요. 이 항목을 선택하면 선택한 개체가 추가되지 않습니다. 또는 개체를 추가 하 고 재설정을 선택할 수는 <xref:System.Data.Linq.DataContext> 새 연결에 연결 합니다.

> [!NOTE]
> 클릭 하면 **예**, 모든 엔터티 클래스에 **O/R 디자이너** 새 연결에 매핑됩니다.

## <a name="to-replace-the-existing-connection-with-the-connection-used-by-the-selected-object"></a>기존 연결을 선택한 개체에서 사용하는 연결로 대체하려면

- **예**를 클릭합니다.

    선택한 개체에 추가 됩니다는 **O/R 디자이너**, 및 *datacontext.connection이* 새 연결으로 설정 됩니다.

## <a name="to-continue-to-use-the-existing-connection-and-cancel-adding-the-selected-object"></a>기존 연결을 계속 사용하고 선택한 개체 추가를 취소하려면

- **아니요**를 클릭합니다.

    작업이 취소됩니다.  합니다 *datacontext.connection이* 기존 연결으로 설정 됩니다.

## <a name="see-also"></a>참고자료

- [O/R 디자이너 메시지](../data-tools/o-r-designer-messages.md)
- [Visual Studio에서 LINQ to SQL 도구](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
