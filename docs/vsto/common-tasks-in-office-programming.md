---
title: Office 프로그래밍의 일반적인 작업
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office development in Visual Studio, getting started
- FAQs (frequently asked questions) [Office development in Visual Studio]
- Office development in Visual Studio, frequently asked questions
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 2c095b6792b2cde9596e1d955a1ddffbc568c801
ms.sourcegitcommit: 209c2c068ff0975994ed892b62aa9b834a7f6077
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2018
---
# <a name="common-tasks-in-office-programming"></a>Office 프로그래밍의 일반적인 작업
  이 항목은 Visual Studio를 사용하여 Office 솔루션을 프로그래밍하는 방법에 대한 다음 범주의 일반적인 질문에 대해 답변을 찾을 수 있도록 설계되었습니다.  
  
-   [설치 및 일반 작업](#projects)  
  
-   [사용자 인터페이스 사용자 지정 작업](#ui)  
  
-   [Excel 자동화 작업](#excel)  
  
-   [Word 자동화 작업](#word)  
  
-   [데이터 작업](#data)  
  
-   [서버 쪽 문서 관리 작업](#server)  
  
-   [보안 작업](#security)  
  
-   [배포 작업](#deployment)  
  
##  <a name="projects"></a> 설치 및 일반 작업  
  
-   [방법: Visual Studio에서 Office 프로젝트 만들기](../vsto/how-to-create-office-projects-in-visual-studio.md)합니다.  
  
-   [방법: 업그레이드 Office 솔루션](http://msdn.microsoft.com/en-us/a269e539-b717-4680-a568-2152b070347e)합니다.  
  
-   [방법: 설치 Office 주 interop 어셈블리](../vsto/how-to-install-office-primary-interop-assemblies.md)합니다.  
  
-   [방법: 주 interop 어셈블리를 통해 대상 Office 응용 프로그램](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md)합니다.  
  
-   [방법: Office 프로젝트의 이벤트 처리기 만들기](../vsto/how-to-create-event-handlers-in-office-projects.md)합니다.  
  
-   [방법: 코드를 실행 하지 않고 열기 Office 솔루션](../vsto/how-to-open-office-solutions-without-running-code.md)합니다.  
  
-   [방법: Office 솔루션에 대 한 구성 정보를 설정](../vsto/how-to-set-up-configuration-information-for-an-office-solution.md)합니다.  
  
-   [방법: 리본에 개발자 탭 표시](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md)합니다.  
  
-   [방법: 사용자 인터페이스 오류 표시 추가 기능인](../vsto/how-to-show-add-in-user-interface-errors.md)합니다.  
  
##  <a name="ui"></a> 사용자 인터페이스 사용자 지정 작업  
  
### <a name="controls-on-documents-and-worksheets"></a>문서 및 워크시트에 컨트롤  
  
-   [방법: Office 문서에 Windows Forms 컨트롤을 추가](../vsto/how-to-add-windows-forms-controls-to-office-documents.md)합니다.  
  
-   [방법: 워크시트에 NamedRange 컨트롤 추가](../vsto/how-to-add-namedrange-controls-to-worksheets.md)합니다.  
  
-   [방법: 워크시트에 ListObject 컨트롤 추가](../vsto/how-to-add-listobject-controls-to-worksheets.md)합니다.  
  
-   [방법: Office 문서에 Windows Forms 컨트롤을 추가](../vsto/how-to-add-windows-forms-controls-to-office-documents.md)합니다.  
  
-   [방법: 콘텐츠를 추가 합니다. Word 문서에 컨트롤](../vsto/how-to-add-content-controls-to-word-documents.md)합니다.  
  
-   [방법: Word 문서에 책갈피 컨트롤 추가](../vsto/how-to-add-bookmark-controls-to-word-documents.md)합니다.  
  
### <a name="task-panes-in-document-level-customizations"></a>문서 수준 사용자 지정의 작업창  
  
-   [방법: Word 문서에 작업 창 추가 또는 Excel 통합 문서](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md)합니다.  
  
### <a name="task-panes-in-vsto-add-ins"></a>VSTO 추가 기능에서 작업창  
  
-   [방법: 응용 프로그램에 사용자 지정 작업창 추가](../vsto/how-to-add-a-custom-task-pane-to-an-application.md)합니다.  
  
### <a name="ribbon-customizations"></a>리본 메뉴 사용자 지정  
  
-   [방법: 리본 메뉴 사용자 지정 시작](../vsto/how-to-get-started-customizing-the-ribbon.md)합니다.  
  
-   [방법: 리본의 탭 위치 변경](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md)합니다.  
  
-   [방법: 기본 제공 탭 사용자 지정](../vsto/how-to-customize-a-built-in-tab.md)합니다.  
  
-   [방법: Backstage 보기에 컨트롤 추가](../vsto/how-to-add-controls-to-the-backstage-view.md)합니다.  
  
-   [How to: Export a Ribbon from the Ribbon Designer to Ribbon XML](../vsto/how-to-export-a-ribbon-from-the-ribbon-designer-to-ribbon-xml.md).  
  
### <a name="outlook-form-regions"></a>Outlook 양식 영역  
  
-   [방법: Outlook 추가 기능 프로젝트에 양식 영역 추가](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md)합니다.  
  
-   [방법: Outlook에서 양식 영역 표시 하지 않기](../vsto/how-to-prevent-outlook-from-displaying-a-form-region.md)합니다.  
  
### <a name="custom-menus"></a>사용자 지정 메뉴  
  
-   [방법: 바로 가기 메뉴에 명령 추가](../vsto/how-to-add-commands-to-shortcut-menus.md)합니다.  
  
##  <a name="excel"></a> Excel 자동화 작업  
  
-   [방법: 프로그래밍 방식으로 워크시트 셀에 문자열을 표시](../vsto/how-to-programmatically-display-a-string-in-a-worksheet-cell.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 새 통합 문서를 만들](../vsto/how-to-programmatically-create-new-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 통합 문서를 열고](../vsto/how-to-programmatically-open-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 통합 문서를 저장](../vsto/how-to-programmatically-save-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 통합 문서를 닫기](../vsto/how-to-programmatically-close-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 통합 문서에 새 워크시트 추가](../vsto/how-to-programmatically-add-new-worksheets-to-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 워크시트 숨기기](../vsto/how-to-programmatically-hide-worksheets.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 통합 문서 내에서 워크시트를 이동](../vsto/how-to-programmatically-move-worksheets-within-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 통합 문서를 보호](../vsto/how-to-programmatically-protect-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 코드에서 워크시트 범위 참조](../vsto/how-to-programmatically-refer-to-worksheet-ranges-in-code.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 통합 문서에서 범위에 스타일을 적용할](../vsto/how-to-programmatically-apply-styles-to-ranges-in-workbooks.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 선택한 셀이 포함 된 워크시트 행의 서식 변경](../vsto/how-to-programmatically-change-formatting-in-worksheet-rows-containing-selected-cells.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 워크시트 범위에서 텍스트 검색](../vsto/how-to-programmatically-search-for-text-in-worksheet-ranges.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 워크시트를 인쇄](../vsto/how-to-programmatically-print-worksheets.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 Excel 계산 실행](../vsto/how-to-programmatically-run-excel-calculations-programmatically.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 워크시트에서 데이터 정렬](../vsto/how-to-programmatically-sort-data-in-worksheets.md)합니다.  
  
##  <a name="word"></a> Word 자동화 작업  
  
-   [방법: 프로그래밍 방식으로 새 문서를 만들](../vsto/how-to-programmatically-create-new-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 기존 문서 열기](../vsto/how-to-programmatically-open-existing-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 문서를 저장](../vsto/how-to-programmatically-save-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 문서를 닫기](../vsto/how-to-programmatically-close-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 Word 문서에 텍스트 삽입](../vsto/how-to-programmatically-insert-text-into-word-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 정의 하 고 문서에서 범위 선택](../vsto/how-to-programmatically-define-and-select-ranges-in-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 Word 문서의 범위 다시 설정](../vsto/how-to-programmatically-reset-ranges-in-word-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 문서의 텍스트 서식 지정](../vsto/how-to-programmatically-format-text-in-documents.md)합니다.  
  
-   [방법: Word 문서에 XMLNode 컨트롤 추가](../vsto/how-to-add-xmlnode-controls-to-word-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 책갈피 텍스트 업데이트](../vsto/how-to-programmatically-update-bookmark-text.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 검색 하 고 문서에서 텍스트를 바꿀](../vsto/how-to-programmatically-search-for-and-replace-text-in-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 문서를 인쇄](../vsto/how-to-programmatically-print-documents.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 Word 표 만들기](../vsto/how-to-programmatically-create-word-tables.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 Word 표에 행과 열을 추가](../vsto/how-to-programmatically-add-rows-and-columns-to-word-tables.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 문서의 문자 수 계산](../vsto/how-to-programmatically-count-characters-in-documents.md)합니다.  
  
##  <a name="data"></a> 데이터 작업  
  
### <a name="data-bound-controls"></a>데이터 바인딩 컨트롤  
  
-   [방법: 데이터베이스의 데이터로 워크시트 채우기](../vsto/how-to-populate-worksheets-with-data-from-a-database.md)합니다.  
  
-   [방법: 데이터베이스의 데이터로 문서 채우기](../vsto/how-to-populate-documents-with-data-from-a-database.md)합니다.  
  
-   [방법: 서비스의 데이터로 문서 채우기](../vsto/how-to-populate-documents-with-data-from-services.md)합니다.  
  
-   [방법: 개체의 데이터로 문서 채우기](../vsto/how-to-populate-documents-with-data-from-objects.md)합니다.  
  
-   [방법: 데이터베이스의 데이터로 문서 채우기](../vsto/how-to-populate-documents-with-data-from-a-database.md)합니다.  
  
-   [방법: 서비스의 데이터로 문서 채우기](../vsto/how-to-populate-documents-with-data-from-services.md)합니다.  
  
-   [방법: 호스트 컨트롤의 데이터로 데이터 소스 업데이트](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)합니다.  
  
### <a name="cached-data-in-document-level-solutions"></a>문서 수준 솔루션의 캐시 된 데이터  
  
-   [방법: 오프 라인 상태가 되거나 서버에 사용 하기 위해 데이터를 캐시](../vsto/how-to-cache-data-for-use-offline-or-on-a-server.md)합니다.  
  
-   [방법: 프로그래밍 방식으로 Office 문서에 데이터 소스를 캐싱](../vsto/how-to-programmatically-cache-a-data-source-in-an-office-document.md)합니다.  
  
-   [방법: 암호로 보호 된 문서에서 데이터를 캐시](../vsto/how-to-cache-data-in-a-password-protected-document.md)합니다.  
  
### <a name="custom-xml-data"></a>사용자 지정 XML 데이터  
  
-   [방법: 문서 수준 사용자 지정에 사용자 지정 XML 부분 추가](../vsto/how-to-add-custom-xml-parts-to-document-level-customizations.md)합니다.  
  
-   [방법: VSTO 추가 기능을 사용 하 여 문서에 사용자 지정 XML 부분 추가](../vsto/how-to-add-custom-xml-parts-to-documents-by-using-vsto-add-ins.md)합니다.  
  
##  <a name="server"></a> 서버 쪽 문서 관리 작업  
  
-   [방법: 문서에서 관리 코드 확장을 제거](../vsto/how-to-remove-managed-code-extensions-from-documents.md)합니다.  
  
-   [방법: 연결 관리 코드 확장이 문서에](../vsto/how-to-attach-managed-code-extensions-to-documents.md)합니다.  
  
##  <a name="security"></a> 보안 작업  
  
-   [방법: Office 솔루션에 서명](../vsto/how-to-sign-office-solutions.md)합니다.  
  
##  <a name="deployment"></a> 배포 작업  
  
-   [방법: ClickOnce를 사용 하 여 Office 솔루션 게시](http://msdn.microsoft.com/en-us/2b6c247e-bc04-4ce4-bb64-c4e79bb3d5b8)합니다.  
  
-   [방법: ClickOnce를 사용 하 여 SharePoint 서버에 문서 수준의 Office 솔루션 게시](http://msdn.microsoft.com/en-us/2408e809-fb78-42a1-9152-00afa1522e58)합니다.  
  
-   [방법: ClickOnce Office 솔루션 설치](http://msdn.microsoft.com/en-us/14702f48-9161-4190-994c-78211fe18065)합니다.  
  
-   [방법: Office 솔루션을 실행 하려면 최종 사용자 컴퓨터에서 필수 구성 요소 설치](http://msdn.microsoft.com/en-us/74dd2c52-838f-4abf-b2b4-4d7b0c2a0a98)합니다.  
  
-   [방법: Office 솔루션 배포를 위해 IIS 준비](http://msdn.microsoft.com/en-us/f62bce70-81d4-4f8b-86e6-2f2afec5d9b4)합니다.  
  
-   [방법: 배포 된 Office 솔루션 업데이트](http://msdn.microsoft.com/en-us/be96db53-b6ea-46ab-b8d9-b76b098b3b13)합니다.  
  
-   [방법: Office 솔루션의 설치 경로 변경](http://msdn.microsoft.com/en-us/d0eaa07b-2d72-4902-899f-2f9fb165b8fd)합니다.  
  
## <a name="see-also"></a>참고자료  
 [시작 하려면 &#40;Visual Studio에서 Office 개발&#41;](../vsto/getting-started-office-development-in-visual-studio.md)   
 [Office 응용 프로그램 및 프로젝트 형식으로 사용할 수 있는 기능](../vsto/features-available-by-office-application-and-project-type.md)   
 [Office 개발 샘플 및 연습](../vsto/office-development-samples-and-walkthroughs.md)  
  
  