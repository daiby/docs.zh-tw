---
title: 如何：呼叫 Windows API (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- API calls [Visual Basic]
- Windows API, calling
- API calls [Visual Basic], platform invoke
- calls [Visual Basic], stored procedures
ms.assetid: 27d75f0a-54ab-4ee1-b91d-43513a19b12d
ms.openlocfilehash: 081f4242ef5883a8b25b8819ba3aff835b1e6ac7
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2018
ms.locfileid: "44208266"
---
# <a name="how-to-call-windows-apis-visual-basic"></a>如何：呼叫 Windows API (Visual Basic)
此範例定義和呼叫`MessageBox`在 user32.dll 中的函式，然後將字串傳遞給它。  
  
## <a name="example"></a>範例  
 [!code-vb[VbVbalrInterop#1](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/how-to-call-windows-apis_1.vb)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 這個範例需要：  
  
-   <xref:System> 命名空間的參考。  
  
## <a name="robust-programming"></a>穩固程式設計  
 以下條件可能會造成例外狀況：  
  
-   此方法不是靜態、 是抽象的或先前已定義。 父類型是介面或長度*名稱*或是*dllName*為零。 (<xref:System.ArgumentException>)  
  
-   *名稱*或是*dllName*是`Nothing`。 (<xref:System.ArgumentNullException>)  
  
-   之前已使用 `CreateType` 建立包含類型。 (<xref:System.InvalidOperationException>)  
  
## <a name="see-also"></a>另請參閱

- [詳述平台叫用](../../../framework/interop/consuming-unmanaged-dll-functions.md#a-closer-look-at-platform-invoke)  
- [平台叫用範例](../../../framework/interop/platform-invoke-examples.md)  
- [使用 Unmanaged DLL 函式](../../../framework/interop/consuming-unmanaged-dll-functions.md)  
- [定義方法，以使用反映發出](https://msdn.microsoft.com/library/84fd3bf6-628f-41aa-83d9-b990cf926e81)  
- [逐步解說：呼叫 Windows API](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)  
- [COM Interop](../../../visual-basic/programming-guide/com-interop/index.md)
