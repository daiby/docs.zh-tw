---
title: 轉換運算子 (C# 程式設計手冊)
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, conversion operators
- conversion operators [C#]
- operators [C#], conversion
- user-defined conversions [C#]
ms.assetid: c5ad73a3-d57b-4d2b-b4c9-24e3c2856efc
ms.openlocfilehash: cbf6a83d43a1b3a69e82a35d5d0875f62422cd3f
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2018
ms.locfileid: "44183310"
---
# <a name="conversion-operators-c-programming-guide"></a>轉換運算子 (C# 程式設計手冊)
C# 可讓程式設計人員宣告類別或結構轉換，使類別或結構能夠與其他類別、結構或基本類型相互轉換。 轉換的定義方式類似運算子，並會以轉換的目標類型命名。 在引數所要轉換的目標類型或轉換的結果類型中，必須有一個是包含類型，但不能兩者都是。  
  
 [!code-csharp[csProgGuideStatements#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/conversion-operators_1.cs)]  
  
## <a name="conversion-operators-overview"></a>轉換運算子概觀  
 轉換運算子具有下列屬性：  
  
-   宣告為 `implicit` 的轉換會在必要時自動發生。  
  
-   宣告為 `explicit` 的轉換需要呼叫轉換。  
  
-   所有轉換都必須宣告為 `static`。  
  
## <a name="related-sections"></a>相關章節  
 如需詳細資訊：  
  
-   [使用轉換運算子](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md)  
  
-   [轉換和型別轉換](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
  
-   [如何：在結構之間實作使用者定義的轉換](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)  
  
-   [explicit](../../../csharp/language-reference/keywords/explicit.md)  
  
-   [implicit](../../../csharp/language-reference/keywords/implicit.md)  
  
-   [static](../../../csharp/language-reference/keywords/static.md)  
  
## <a name="see-also"></a>請參閱

- <xref:System.Convert>  
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)  
- [C# 中鏈結的使用者定義明確轉換](https://blogs.msdn.microsoft.com/ericlippert/2007/04/16/chained-user-defined-explicit-conversions-in-c/)
