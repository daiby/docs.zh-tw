---
title: 編譯 Interop 專案
ms.date: 03/30/2017
helpviewer_keywords:
- interoperation with unmanaged code, compiling
- COM interop, compiling
- exposing COM components to .NET Framework
- compiling interop projects
- interoperation with unmanaged code, exposing COM components
- COM interop, exposing COM components
ms.assetid: 6fcf6588-5e25-41af-b4ae-780974f2c3df
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8a6099764fb98604726da99ef71b9c82e9a931bd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33388498"
---
# <a name="compiling-an-interop-project"></a>編譯 Interop 專案
會編譯參考一或多個包含已匯入 COM 類型之組件的 COM Interop 專案，就像任何其他 Managed 專案一樣。 您可以參考 Visual Studio 這類開發環境中的 Interop 組件，也可以在使用命令列編譯器時參考它們。 在任一情況下，若要正常編譯，則 Interop 組件必須與其他專案檔位於相同的目錄中。  
  
 有兩種方法可以參考 Interop 組件：  
  
-   內嵌的 Interop 類型：從 [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] 和 [!INCLUDE[vs_dev10_long](../../../includes/vs-dev10-long-md.md)] 開始，您可以指示編譯器將 Interop 組件的類型資訊內嵌到可執行檔。 這是建議使用的技巧。  
  
-   部署 Interop 組件：您可以建立 Interop 組件的標準參考。 在此情況下，Interop 組件必須與您的應用程式一起部署。  
  
 [在 Managed 程式碼中使用 COM 類型](https://msdn.microsoft.com/library/1a95a8ca-c8b8-4464-90b0-5ee1a1135b66(v=vs.100))會更詳細討論這兩種技術之間的差異。  
  
 [逐步解說：從 Microsoft Office 組件內嵌類型資訊](https://msdn.microsoft.com/library/85b55e05-bc5e-4665-b6ae-e1ada9299fd3(v=vs.100))和 [Walkthrough: Embedding Types from Managed Assemblies](https://msdn.microsoft.com/library/b28ec92c-1867-4847-95c0-61adfe095e21) (逐步解說：從 Managed 組件內嵌類型) 示範如何使用 Visual Studio 內嵌 Interop 類型。  
  
 若要參考具有命令列編譯器的 Interop 組件，以及在可執行檔中內嵌類型資訊，請使用 [/link (C# 編譯器選項)](../../csharp/language-reference/compiler-options/link-compiler-option.md) 或 [/link (Visual Basic)](../../visual-basic/reference/command-line-compiler/link.md) 編譯器參數，並指定 Interop 組件的名稱。  
  
> [!NOTE]
>  Visual C++ 應用程式無法內嵌類型資訊，但可以與執行的應用程式或增益集交互操作。  
  
 若要在部署包含主要 Interop 組件的應用程式時進行編譯，請使用 **/reference** 編譯器參數，並指定 Interop 組件的名稱。  
  
## <a name="see-also"></a>請參閱  
 [將 COM 元件公開給 .NET Framework](exposing-com-components.md)  
 [語言獨立性以及與語言無關的元件](../../standard/language-independence-and-language-independent-components.md)  
 [在受控程式碼中使用 COM 類型](https://msdn.microsoft.com/library/1a95a8ca-c8b8-4464-90b0-5ee1a1135b66(v=vs.100))  
 [逐步解說：從 Microsoft Office 組件內嵌類型資訊](https://msdn.microsoft.com/library/85b55e05-bc5e-4665-b6ae-e1ada9299fd3(v=vs.100))  
 [逐步解說：從 Managed 組件內嵌類型](https://msdn.microsoft.com/library/b28ec92c-1867-4847-95c0-61adfe095e21)  
 [匯入類型程式庫做為組件](importing-a-type-library-as-an-assembly.md)
