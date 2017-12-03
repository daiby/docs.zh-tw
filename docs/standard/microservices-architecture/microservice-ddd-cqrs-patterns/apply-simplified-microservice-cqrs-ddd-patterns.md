---
title: "套用微服務的簡化的 CQRS 和 DDD 模式"
description: "容器化的.NET 應用程式的.NET Microservices 架構 |套用微服務的簡化的 CQRS 和 DDD 模式"
keywords: "Docker, 微服務, ASP.NET, 容器"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 99fd7ce32039742e23f8e01aa4c33cddd7a9f698
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="applying-simplified-cqrs-and-ddd-patterns-in-a-microservice"></a><span data-ttu-id="62a9d-104">套用微服務的簡化的 CQRS 和 DDD 模式</span><span class="sxs-lookup"><span data-stu-id="62a9d-104">Applying simplified CQRS and DDD patterns in a microservice</span></span>

<span data-ttu-id="62a9d-105">CQRS 會分隔模型來進行讀取和寫入資料的架構模式。</span><span class="sxs-lookup"><span data-stu-id="62a9d-105">CQRS is an architectural pattern that separates the models for reading and writing data.</span></span> <span data-ttu-id="62a9d-106">相關的詞彙[命令查詢分離 (CQS)](https://martinfowler.com/bliki/CommandQuerySeparation.html)原本他活頁簿中定義由 Bertrand 慧君*物件導向軟體建構*。</span><span class="sxs-lookup"><span data-stu-id="62a9d-106">The related term [Command Query Separation (CQS)](https://martinfowler.com/bliki/CommandQuerySeparation.html) was originally defined by Bertrand Meyer in his book *Object Oriented Software Construction*.</span></span> <span data-ttu-id="62a9d-107">基本概念是，您可以將分割分成兩個加深而大幅分隔分類系統的作業：</span><span class="sxs-lookup"><span data-stu-id="62a9d-107">The basic idea is that you can divide a system’s operations into two sharply separated categories:</span></span>

-   <span data-ttu-id="62a9d-108">查詢。</span><span class="sxs-lookup"><span data-stu-id="62a9d-108">Queries.</span></span> <span data-ttu-id="62a9d-109">這些傳回結果，不會變更系統的狀態，而且是免費的副作用。</span><span class="sxs-lookup"><span data-stu-id="62a9d-109">These return a result and do not change the state of the system, and they are free of side effects.</span></span>

-   <span data-ttu-id="62a9d-110">命令。</span><span class="sxs-lookup"><span data-stu-id="62a9d-110">Commands.</span></span> <span data-ttu-id="62a9d-111">這些變更系統狀態。</span><span class="sxs-lookup"><span data-stu-id="62a9d-111">These change the state of a system.</span></span>

<span data-ttu-id="62a9d-112">CQS 是簡單的概念，它是關於相同物件中的方法正在查詢或命令。</span><span class="sxs-lookup"><span data-stu-id="62a9d-112">CQS is a simple concept—it is about methods within the same object being either queries or commands.</span></span> <span data-ttu-id="62a9d-113">每個方法會傳回狀態或狀態，但兩者不會改變。</span><span class="sxs-lookup"><span data-stu-id="62a9d-113">Each method either returns state or mutates state, but not both.</span></span> <span data-ttu-id="62a9d-114">甚至單一的儲存機制模式的物件可以遵守 CQS。</span><span class="sxs-lookup"><span data-stu-id="62a9d-114">Even a single repository pattern object can comply with CQS.</span></span> <span data-ttu-id="62a9d-115">CQS 可以考量的基本原則 CQRS。</span><span class="sxs-lookup"><span data-stu-id="62a9d-115">CQS can be considered a foundational principle for CQRS.</span></span>

<span data-ttu-id="62a9d-116">[命令和查詢責任隔離 (CQRS)](https://martinfowler.com/bliki/CQRS.html)已引進 Greg Young，而且強烈升級 Udi Dahan 等等。</span><span class="sxs-lookup"><span data-stu-id="62a9d-116">[Command and Query Responsibility Segregation (CQRS)](https://martinfowler.com/bliki/CQRS.html) was introduced by Greg Young and strongly promoted by Udi Dahan and others.</span></span> <span data-ttu-id="62a9d-117">它根據 CQS 原則，雖然會更詳細說明。</span><span class="sxs-lookup"><span data-stu-id="62a9d-117">It is based on the CQS principle, although it is more detailed.</span></span> <span data-ttu-id="62a9d-118">它可以視為基礎命令和事件加上選擇性地在非同步訊息模式。</span><span class="sxs-lookup"><span data-stu-id="62a9d-118">It can be considered a pattern based on commands and events plus optionally on asynchronous messages.</span></span> <span data-ttu-id="62a9d-119">在許多情況下，CQRS 與相關的更進階的案例，像是讓不同的實體資料庫的讀取 （查詢） 比寫入 （更新）。</span><span class="sxs-lookup"><span data-stu-id="62a9d-119">In many cases, CQRS is related to more advanced scenarios, like having a different physical database for reads (queries) than for writes (updates).</span></span> <span data-ttu-id="62a9d-120">此外，可能會實作更進化的 CQRS 系統[事件來源 (ES)](http://codebetter.com/gregyoung/2010/02/20/why-use-event-sourcing/)更新資料庫，所以您會只儲存事件中的網域模型，而不是儲存目前的狀態資料。</span><span class="sxs-lookup"><span data-stu-id="62a9d-120">Moreover, a more evolved CQRS system might implement [Event-Sourcing (ES)](http://codebetter.com/gregyoung/2010/02/20/why-use-event-sourcing/) for your updates database, so you would only store events in the domain model instead of storing the current-state data.</span></span> <span data-ttu-id="62a9d-121">不過，這不是使用本指南中; 中的方法我們使用簡單的 CQRS 方法，只要從命令分隔的查詢所組成。</span><span class="sxs-lookup"><span data-stu-id="62a9d-121">However, this is not the approach used in this guide; we are using the simplest CQRS approach, which consists of just separating the queries from the commands.</span></span>

<span data-ttu-id="62a9d-122">CQRS 分離層面被達成分組為一個圖層中的查詢作業和另一個圖層中的命令。</span><span class="sxs-lookup"><span data-stu-id="62a9d-122">The separation aspect of CQRS is achieved by grouping query operations in one layer and commands in another layer.</span></span> <span data-ttu-id="62a9d-123">每個圖層有它自己的資料模型 （請注意我們說模型中，不一定是不同的資料庫），而且會根據您使用自己的模式和技術的組合。</span><span class="sxs-lookup"><span data-stu-id="62a9d-123">Each layer has its own data model (note that we say model, not necessarily a different database) and is built using its own combination of patterns and technologies.</span></span> <span data-ttu-id="62a9d-124">更重要的是，兩個圖層可以是相同的階層或微服務，（排序微服務），例如用於本指南中。</span><span class="sxs-lookup"><span data-stu-id="62a9d-124">More importantly, the two layers can be within the same tier or microservice, as in the example (ordering microservice) used for this guide.</span></span> <span data-ttu-id="62a9d-125">或者，他們可能會實作上不同 microservices 或處理程序，才能最佳化以及向外延展個別而不會影響另一個。</span><span class="sxs-lookup"><span data-stu-id="62a9d-125">Or they could be implemented on different microservices or processes so they can be optimized and scaled out separately without affecting one another.</span></span>

<span data-ttu-id="62a9d-126">CQRS 表示會有兩個物件的讀取/寫入作業，在其他內容中有一個。</span><span class="sxs-lookup"><span data-stu-id="62a9d-126">CQRS means having two objects for a read/write operation where in other contexts there is one.</span></span> <span data-ttu-id="62a9d-127">有原因有反正規化的讀取資料庫，您可以在更進階的 CQRS 文獻中學習。</span><span class="sxs-lookup"><span data-stu-id="62a9d-127">There are reasons to have a denormalized reads database, which you can learn about in more advanced CQRS literature.</span></span> <span data-ttu-id="62a9d-128">但我們不使用以下，該方法的目標在於的查詢，而不是限制與條件約束從 DDD 模式，例如彙總查詢中有更大的彈性。</span><span class="sxs-lookup"><span data-stu-id="62a9d-128">But we are not using that approach here, where the goal is to have more flexibility in the queries instead of limiting the queries with constraints from DDD patterns like aggregates.</span></span>

<span data-ttu-id="62a9d-129">舉例來說，這種服務是從 eShopOnContainers 參考應用程式排序的微服務。</span><span class="sxs-lookup"><span data-stu-id="62a9d-129">An example of this kind of service is the ordering microservice from the eShopOnContainers reference application.</span></span> <span data-ttu-id="62a9d-130">此服務會實作簡單的 CQRS 方法為基礎的微服務。</span><span class="sxs-lookup"><span data-stu-id="62a9d-130">This service implements a microservice based on a simplified CQRS approach.</span></span> <span data-ttu-id="62a9d-131">它會使用單一資料來源或資料庫，但兩個邏輯模型加上 DDD 模式對於交易式的網域，如圖 9-2 所示。</span><span class="sxs-lookup"><span data-stu-id="62a9d-131">It uses a single data source or database, but two logical models plus DDD patterns for the transactional domain, as shown in Figure 9-2.</span></span>

![](./media/image2.png)

<span data-ttu-id="62a9d-132">**圖 9 2**。</span><span class="sxs-lookup"><span data-stu-id="62a9d-132">**Figure 9-2**.</span></span> <span data-ttu-id="62a9d-133">簡化 CQRS 和 DDD 型微服務</span><span class="sxs-lookup"><span data-stu-id="62a9d-133">Simplified CQRS- and DDD-based microservice</span></span>

<span data-ttu-id="62a9d-134">應用程式層都可以是 Web API 本身。</span><span class="sxs-lookup"><span data-stu-id="62a9d-134">The application layer can be the Web API itself.</span></span> <span data-ttu-id="62a9d-135">重要的設計層面以下取自微服務有分割的查詢和 ViewModels （特別是建立用戶端應用程式的資料模型） 命令、 網域模型，與下列 CQRS 模式的交易。</span><span class="sxs-lookup"><span data-stu-id="62a9d-135">The important design aspect here is that the microservice has split the queries and ViewModels (data models especially created for the client applications) from the commands, domain model, and transactions following the CQRS pattern.</span></span> <span data-ttu-id="62a9d-136">這個方法會保留查詢無關的限制與來自 DDD 模式，才有意義的交易與更新，稍後的章節中所述的條件約束。</span><span class="sxs-lookup"><span data-stu-id="62a9d-136">This approach keeps the queries independent from restrictions and constraints coming from DDD patterns that only make sense for transactions and updates, as explained in later sections.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="62a9d-137">[上一個](index.md) [下一步] (eshoponcontainers-cqrs-ddd-microservice.md)</span><span class="sxs-lookup"><span data-stu-id="62a9d-137">[Previous] (index.md) [Next] (eshoponcontainers-cqrs-ddd-microservice.md)</span></span>