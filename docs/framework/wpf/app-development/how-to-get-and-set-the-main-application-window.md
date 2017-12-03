---
title: "如何： 取得和設定主應用程式視窗"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- windows objects [WPF], setting
- setting windows objects [WPF]
- windows objects [WPF], getting
- getting windows objects [WPF]
ms.assetid: ec902bc4-4a59-46f5-8ec1-963b46789356
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0d6bca158172fd3fc31526287c6d4a9928a8ea0c
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-get-and-set-the-main-application-window"></a><span data-ttu-id="2031f-102">如何： 取得和設定主應用程式視窗</span><span class="sxs-lookup"><span data-stu-id="2031f-102">How to: Get and Set the Main Application Window</span></span>
<span data-ttu-id="2031f-103">這個範例示範如何取得及設定主應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="2031f-103">This example shows how to get and set the main application window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2031f-104">範例</span><span class="sxs-lookup"><span data-stu-id="2031f-104">Example</span></span>  
 <span data-ttu-id="2031f-105">第一個<xref:System.Windows.Window>，具現化內[!INCLUDE[TLA#tla_wpf](../../../../includes/tlasharptla-wpf-md.md)]應用程式會自動設定<xref:System.Windows.Application>與主應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="2031f-105">The first <xref:System.Windows.Window> that is instantiated within a [!INCLUDE[TLA#tla_wpf](../../../../includes/tlasharptla-wpf-md.md)] application is automatically set by <xref:System.Windows.Application> as the main application window.</span></span> <span data-ttu-id="2031f-106">第一個<xref:System.Windows.Window>要具現化的會很有可能是指定為啟動視窗[!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)](請參閱<xref:System.Windows.Application.StartupUri%2A>)。</span><span class="sxs-lookup"><span data-stu-id="2031f-106">The first <xref:System.Windows.Window> to be instantiated will most likely be the window that is specified as the startup [!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)] (see <xref:System.Windows.Application.StartupUri%2A>).</span></span>  
  
 <span data-ttu-id="2031f-107">第一個<xref:System.Windows.Window>可能也會使用具現化程式碼。</span><span class="sxs-lookup"><span data-stu-id="2031f-107">The first <xref:System.Windows.Window> could also be instantiated using code.</span></span> <span data-ttu-id="2031f-108">其中一個範例會開啟視窗的應用程式在啟動期間，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2031f-108">One example is opening a window during application startup, like the following:</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#FirstWindowUsingCodeCODEBEHIND](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/App.xaml.cs#firstwindowusingcodecodebehind)]
 [!code-vb[HOWTOWindowManagementSnippets#FirstWindowUsingCodeCODEBEHIND](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/application.xaml.vb#firstwindowusingcodecodebehind)]  
  
 <span data-ttu-id="2031f-109">某些情況下，第一個具現化<xref:System.Windows.Window>如啟動顯示畫面是實際上並不是主應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="2031f-109">Sometimes, the first instantiated <xref:System.Windows.Window> is not actually the main application window e.g. a splash screen.</span></span> <span data-ttu-id="2031f-110">在此情況下，您可以指定主應用程式視窗中，使用標記，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2031f-110">In this case, you can specify the main application window using markup, like the following:</span></span>  
  
 [!code-xaml[ApplicationMainWindowSnippets#SetApplicationMainWindowXAML](../../../../samples/snippets/xaml/VS_Snippets_Wpf/ApplicationMainWindowSnippets/XAML/App.xaml#setapplicationmainwindowxaml)]  
  
 <span data-ttu-id="2031f-111">是否自動或手動指定主視窗，就可以從主視窗<xref:System.Windows.Application.MainWindow%2A>使用下列程式碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2031f-111">Whether the main window is specified automatically or manually, you can get the main window from <xref:System.Windows.Application.MainWindow%2A> using the following code, like the following:</span></span>  
  
 [!code-csharp[ApplicationMainWindowSnippets#GetApplicationMainWindowCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ApplicationMainWindowSnippets/CSharp/App.xaml.cs#getapplicationmainwindowcode)]
 [!code-vb[ApplicationMainWindowSnippets#GetApplicationMainWindowCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ApplicationMainWindowSnippets/visualbasic/application.xaml.vb#getapplicationmainwindowcode)]