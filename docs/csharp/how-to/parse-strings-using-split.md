---
title: "如何：使用 String.Split 剖析字串 (C# 指南)"
description: "String.Split 會傳回從一組分隔符號分割的字串陣列。 它容易剖析字串。"
ms.date: 01/03/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- splitting strings [C#]
- Split method [C#]
- strings [C#], splitting
- parse strings
ms.assetid: 729c2923-4169-41c6-9c90-ef176c1e2953
author: BillWagner
ms.author: wiwagn
ms.custom: mvc
ms.openlocfilehash: 9dd5b1204986bd9b181c033d254bb41e8cc894da
ms.sourcegitcommit: f28752eab00d2bd97e971542c0f49ce63cfbc239
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2018
---
# <a name="how-to-parse-strings-using-stringsplit-c-guide"></a><span data-ttu-id="f900b-104">如何：使用 String.Split 剖析字串 (C# 指南)</span><span class="sxs-lookup"><span data-stu-id="f900b-104">How to: Parse Strings Using String.Split (C# Guide)</span></span>

<span data-ttu-id="f900b-105"><xref:System.String.Split%2A?displayProperty=nameWithType> 方法會根據一或多個分隔符號來分割輸入字串，以建立子字串陣列。</span><span class="sxs-lookup"><span data-stu-id="f900b-105">The <xref:System.String.Split%2A?displayProperty=nameWithType> method creates an array of substrings by splitting the input string based on one or more delimiters.</span></span> <span data-ttu-id="f900b-106">這通常是分隔字組界限上字串的最簡單方式。</span><span class="sxs-lookup"><span data-stu-id="f900b-106">It is often the easiest way to separate a string on word boundaries.</span></span> <span data-ttu-id="f900b-107">它也用來分割其他特定字元或字串上的字串。</span><span class="sxs-lookup"><span data-stu-id="f900b-107">It is also used to split strings on other specific characters or strings.</span></span>

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

<span data-ttu-id="f900b-108">下列程式碼將常用詞語分割成每個字組的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="f900b-108">The following code splits a common phrase into an array of strings for each word.</span></span>

[!code-csharp-interactive[split strings on word boundaries](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#1)]

<span data-ttu-id="f900b-109">每個分隔符號字元執行個體都會產生已傳回陣列中的值。</span><span class="sxs-lookup"><span data-stu-id="f900b-109">Every instance of a separator character produces a value in the returned array.</span></span> <span data-ttu-id="f900b-110">連續分隔符號字元會產生空字串，作為已傳回陣列中的值。</span><span class="sxs-lookup"><span data-stu-id="f900b-110">Consecutive separator characters produce the empty string as a value in the returned array.</span></span>  <span data-ttu-id="f900b-111">您可以在下列範例中看到這個項目，其使用空格作為分隔符號：</span><span class="sxs-lookup"><span data-stu-id="f900b-111">You can see this in the following example, which uses space as a separator:</span></span>

[!code-csharp-interactive[split strings with repeated separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#2)]

<span data-ttu-id="f900b-112">此行為可以更輕鬆地使用格式，例如代表表格式資料的逗號分隔值 (CSV) 檔案。</span><span class="sxs-lookup"><span data-stu-id="f900b-112">This behavior makes it easier for formats like comma separated values (CSV) files representing tabular data.</span></span> <span data-ttu-id="f900b-113">連續的逗號表示空白資料行。</span><span class="sxs-lookup"><span data-stu-id="f900b-113">Consecutive commas represent a blank column.</span></span>

<span data-ttu-id="f900b-114">您可以傳遞選擇性 <xref:System.StringSplitOptions.RemoveEmptyEntries?displayProperty=fullName> 參數，以排除已傳回陣列中的任何空字串。</span><span class="sxs-lookup"><span data-stu-id="f900b-114">You can pass an optional <xref:System.StringSplitOptions.RemoveEmptyEntries?displayProperty=fullName> parameter to exclude any empty strings in the returned array.</span></span> <span data-ttu-id="f900b-115">針對更複雜處理的已傳回集合，您可以使用 [LINQ](../programming-guide/concepts/linq/index.md) 來操作結果序列。</span><span class="sxs-lookup"><span data-stu-id="f900b-115">For more complicated processing of the returned collection, you can use [LINQ](../programming-guide/concepts/linq/index.md) to manipulate the result sequence.</span></span>    

<span data-ttu-id="f900b-116"><xref:System.String.Split%2A?displayProperty=nameWithType> 可以使用多個分隔符號字元。</span><span class="sxs-lookup"><span data-stu-id="f900b-116"><xref:System.String.Split%2A?displayProperty=nameWithType> can use multiple separator characters.</span></span> <span data-ttu-id="f900b-117">下列範例會使用空格、逗號、句號、冒號和定位點，全部以包含這些分隔符號的陣列傳遞至 <xref:System.String.Split%2A>。</span><span class="sxs-lookup"><span data-stu-id="f900b-117">The following example uses spaces, commas, periods, colons, and tabs, all passed in an array containing these separating characters, to <xref:System.String.Split%2A>.</span></span>  <span data-ttu-id="f900b-118">程式碼底部的迴圈會顯示所傳回陣列中的每個字組。</span><span class="sxs-lookup"><span data-stu-id="f900b-118">The loop at the bottom of the code displays each of the words in the returned array.</span></span>  

[!code-csharp-interactive[split strings using multiple separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#3)]

<span data-ttu-id="f900b-119">任何分隔符號的連續執行個體都會產生輸出陣列中的空字串：</span><span class="sxs-lookup"><span data-stu-id="f900b-119">Consecutive instances of any separator produce the empty string in the output array:</span></span>

[!code-csharp-interactive[split strings using multiple consecutive separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#4)]

<span data-ttu-id="f900b-120"><xref:System.String.Split%2A?displayProperty=nameWithType> 可以採用字串陣列 (作為分隔符號以剖析目標字串的字元序列，而不是單一字元)。</span><span class="sxs-lookup"><span data-stu-id="f900b-120"><xref:System.String.Split%2A?displayProperty=nameWithType> can take an array of strings (character sequences that act as separators for parsing the target string, instead of single characters).</span></span>  
  
[!code-csharp-interactive[split strings using strings as separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#5)]

<span data-ttu-id="f900b-121">您可以查看 [GitHub 存放庫](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings)中的程式碼，來嘗試這些範例</span><span class="sxs-lookup"><span data-stu-id="f900b-121">You can try these samples by looking at the code in our [GitHub repository](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings)</span></span>

## <a name="see-also"></a><span data-ttu-id="f900b-122">請參閱</span><span class="sxs-lookup"><span data-stu-id="f900b-122">See Also</span></span>  
 [<span data-ttu-id="f900b-123">C# 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="f900b-123">C# Programming Guide</span></span>](../programming-guide/index.md)  
 [<span data-ttu-id="f900b-124">字串</span><span class="sxs-lookup"><span data-stu-id="f900b-124">Strings</span></span>](../programming-guide/strings/index.md)  
 [<span data-ttu-id="f900b-125">.NET Framework 規則運算式</span><span class="sxs-lookup"><span data-stu-id="f900b-125">.NET Framework Regular Expressions</span></span>](https://msdn.microsoft.com/library/hs600312)