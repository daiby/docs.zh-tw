---
title: 執行緒 (C#)
ms.date: 07/20/2015
ms.assetid: 236d157d-37c0-4ee8-89fc-721e6c596325
ms.openlocfilehash: c90816a14bfbcd2ddd469c1240e94d99bfbbb5e5
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/06/2018
ms.locfileid: "48844874"
---
# <a name="threading-c"></a>執行緒 (C#)
C# 程式可以透過執行緒執行並行處理，讓您可以一次執行多項作業。 例如，您可以使用執行緒監視使用者的輸入、執行背景工作，以及處理同時的輸入資料流。  
  
 執行緒具有下列特性：  
  
-   執行緒可讓您的程式執行並行處理。  
  
-   .NET Framework <xref:System.Threading> 命名空間讓執行緒更方便使用。  
  
-   執行緒會共用應用程式的資源。 如需詳細資訊，請參閱 [Using Threads and Threading](../../../../../docs/standard/threading/using-threads-and-threading.md) (使用 Thread 與 Threading)。  
  
 根據預設，C# 程式都有一個執行緒。 但您可以建立輔助執行緒來與主要執行緒一起並行執行程式碼。 這些執行緒通常稱為*背景工作執行緒*。  
  
 背景工作執行緒可用於執行耗時或時間要求嚴格的工作，但不會佔用主要執行緒。 例如，伺服器應用程式中通常會使用背景工作執行緒來滿足傳入的要求，而且無須等待前一個要求完成就能達成。 背景工作執行緒在桌面應用程式中也可用於執行「背景」工作，讓驅動使用者介面項目的主要執行緒能夠持續回應使用者動作。  
  
 執行緒可以解決輸送量與回應性的問題，但也可能會引發資源共用的問題，像是死結及競爭狀況。 多執行緒最適合需要不同資源的工作，例如檔案控制及網路連線。 為單一資源指派多個執行緒除可能會導致同步問題之外，還可能經常因為等候其他執行緒戰勝使用多執行的目標而造成執行緒受阻無法執行。  
  
 常見的策略是使用背景工作處理序來執行耗時或時間要求嚴格，但又不需要太多其他執行緒所用之資源的工作。 當然，您程式中的一些資源仍須能夠讓多執行緒存取。 對於這些情況，<xref:System.Threading>命名空間提供了一些類別可用於同步執行緒。 這些類別包括 <xref:System.Threading.Mutex>、<xref:System.Threading.Monitor>、<xref:System.Threading.Interlocked>、<xref:System.Threading.AutoResetEvent> 及 <xref:System.Threading.ManualResetEvent>。  
  
 您可以其中一些類別來同步多執行緒的活動，但有一些執行緒的支援則來自 C# 語言。 例如 [Lock 陳述式](../../../../csharp/language-reference/keywords/lock-statement.md)可以透過隱含使用<xref:System.Threading.Monitor>來提供同步功能。  
  
> [!NOTE]
>  自 [!INCLUDE[net_v40_long](~/includes/net-v40-long-md.md)] 起，多執行緒程式設計因為 <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType> 及 <xref:System.Threading.Tasks.Task?displayProperty=nameWithType> 類別、[平行 LINQ (PLINQ)](../../../../standard/parallel-programming/parallel-linq-plinq.md)、<xref:System.Collections.Concurrent?displayProperty=nameWithType> 命名空間中的新並行集合類別，以及以工作 (而非執行緒) 概念為基礎的新程式設計模型而獲得大幅簡化。 如需詳細資訊，請參閱[平行程式設計](../../../../../docs/standard/parallel-programming/index.md)。  
  
## <a name="related-topics"></a>相關主題  
  
|標題|描述|  
|-----------|-----------------|  
|[執行緒處理](../../../../../docs/standard/threading/index.md)|說明如何在.NET Framework 中實作執行緒。|
