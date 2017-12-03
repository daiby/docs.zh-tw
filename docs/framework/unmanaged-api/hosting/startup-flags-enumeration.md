---
title: "STARTUP_FLAGS 列舉"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: STARTUP_FLAGS
api_location: mscoree.dll
api_type: COM
f1_keywords: STARTUP_FLAGS
helpviewer_keywords: STARTUP_FLAGS enumeration [.NET Framework hosting]
ms.assetid: 4f043594-0c45-4bc6-988e-a6793f0d8d06
topic_type: apiref
caps.latest.revision: "22"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ebfb45e6d568b4fa1db209264e02332df636474f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="startupflags-enumeration"></a><span data-ttu-id="fb08f-102">STARTUP_FLAGS 列舉</span><span class="sxs-lookup"><span data-stu-id="fb08f-102">STARTUP_FLAGS Enumeration</span></span>
<span data-ttu-id="fb08f-103">包含值，表示啟動行為的 common language runtime (CLR)。</span><span class="sxs-lookup"><span data-stu-id="fb08f-103">Contains values that indicate the startup behavior of the common language runtime (CLR).</span></span> <span data-ttu-id="fb08f-104">根據預設，記憶體回收是非並行，而且只基底類別程式庫載入定義域中性區域。</span><span class="sxs-lookup"><span data-stu-id="fb08f-104">By default, garbage collection is non-concurrent, and only the base class library is loaded into the domain-neutral area.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb08f-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb08f-105">Syntax</span></span>  
  
```  
typedef enum {  
    STARTUP_CONCURRENT_GC                         = 0x1,  
    STARTUP_LOADER_OPTIMIZATION_MASK              = 0x3<<1,  
    STARTUP_LOADER_OPTIMIZATION_SINGLE_DOMAIN     = 0x1<<1,  
    STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN      = 0x2<<1,  
    STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN_HOST = 0x3<<1,  
  
    STARTUP_LOADER_SAFEMODE                       = 0x10,  
    STARTUP_LOADER_SETPREFERENCE                  = 0x100,  
  
    STARTUP_SERVER_GC                             = 0x1000,  
    STARTUP_HOARD_GC_VM                           = 0x2000,  
  
    STARTUP_SINGLE_VERSION_HOSTING_INTERFACE      = 0x4000,  
    STARTUP_LEGACY_IMPERSONATION                  = 0x10000,  
    STARTUP_DISABLE_COMMITTHREADSTACK             = 0x20000,  
    STARTUP_ALWAYSFLOW_IMPERSONATION              = 0x40000,  
    STARTUP_TRIM_GC_COMMIT                        = 0x80000,  
  
    STARTUP_ETW                                   = 0x100000,  
    STARTUP_ARM                                   = 0x400000  
} STARTUP_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="fb08f-106">成員</span><span class="sxs-lookup"><span data-stu-id="fb08f-106">Members</span></span>  
  
|<span data-ttu-id="fb08f-107">成員</span><span class="sxs-lookup"><span data-stu-id="fb08f-107">Member</span></span>|<span data-ttu-id="fb08f-108">說明</span><span class="sxs-lookup"><span data-stu-id="fb08f-108">Description</span></span>|  
|------------|-----------------|  
|`STARTUP_CONCURRENT_GC`|<span data-ttu-id="fb08f-109">指定應該使用並行記憶體回收。</span><span class="sxs-lookup"><span data-stu-id="fb08f-109">Specifies that concurrent garbage collection should be used.</span></span> <span data-ttu-id="fb08f-110">如果呼叫端要求的伺服器組建和並行記憶體回收在單一處理器電腦上，但是工作站組建和非並行記憶體回收會改為執行。</span><span class="sxs-lookup"><span data-stu-id="fb08f-110">If the caller asks for the server build and concurrent garbage collection on a single-processor machine, the workstation build and non-concurrent garbage collection are run instead.</span></span> <span data-ttu-id="fb08f-111">**注意：** WOW64 執行的應用程式中不支援並行記憶體回收 x86 實作 （之前稱為 ia-64） 的 Intel Itanium 架構的 64 位元系統上的模擬器。</span><span class="sxs-lookup"><span data-stu-id="fb08f-111">**Note:**  Concurrent garbage collection is not supported in applications that are running the WOW64 x86 emulator on 64-bit systems that implement the Intel Itanium architecture (formerly called IA-64).</span></span> <span data-ttu-id="fb08f-112">如需使用 WOW64 在 64 位元 Windows 系統上的詳細資訊，請參閱[執行 32 位元應用程式](http://msdn.microsoft.com/library/windows/desktop/aa384249.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fb08f-112">For more information about using WOW64 on 64-bit Windows systems, see [Running 32-bit Applications](http://msdn.microsoft.com/library/windows/desktop/aa384249.aspx).</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_MASK`|<span data-ttu-id="fb08f-113">指定應該發生的載入器最佳化。</span><span class="sxs-lookup"><span data-stu-id="fb08f-113">Specifies that loader optimization shall occur.</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_SINGLE_DOMAIN`|<span data-ttu-id="fb08f-114">指定不以定義域中性方式載入任何組件。</span><span class="sxs-lookup"><span data-stu-id="fb08f-114">Specifies that no assemblies are loaded as domain-neutral.</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN`|<span data-ttu-id="fb08f-115">指定的所有組件以定義域中性方式載入。</span><span class="sxs-lookup"><span data-stu-id="fb08f-115">Specifies that all assemblies are loaded as domain-neutral.</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN_HOST`|<span data-ttu-id="fb08f-116">指定所有的強式名稱組件會以定義域中性方式載入。</span><span class="sxs-lookup"><span data-stu-id="fb08f-116">Specifies that all strong-named assemblies are loaded as domain-neutral.</span></span>|  
|`STARTUP_LOADER_SAFEMODE`|<span data-ttu-id="fb08f-117">指定 CLR 版本原則不會套用到傳入的版本。</span><span class="sxs-lookup"><span data-stu-id="fb08f-117">Specifies that CLR version policy will not be applied to the version passed in.</span></span> <span data-ttu-id="fb08f-118">將載入指定的 clr 的正確版本。</span><span class="sxs-lookup"><span data-stu-id="fb08f-118">The exact version specified of the CLR will be loaded.</span></span> <span data-ttu-id="fb08f-119">填充碼不會評估原則，以判斷最新的相容版本。</span><span class="sxs-lookup"><span data-stu-id="fb08f-119">The shim does not evaluate policy to determine the latest compatible version.</span></span>|  
|`STARTUP_LOADER_SETPREFERENCE`|<span data-ttu-id="fb08f-120">指定慣用的執行階段會設定，但實際上不會啟動。</span><span class="sxs-lookup"><span data-stu-id="fb08f-120">Specifies that the preferred runtime will be set, but not actually started.</span></span>|  
|`STARTUP_SERVER_GC`|<span data-ttu-id="fb08f-121">指定將會使用伺服器記憶體回收。</span><span class="sxs-lookup"><span data-stu-id="fb08f-121">Specifies that the server garbage collection will be used.</span></span>|  
|`STARTUP_HOARD_GC_VM`|<span data-ttu-id="fb08f-122">指定回收將保留用的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="fb08f-122">Specifies that garbage collection will keep the virtual address used.</span></span>|  
|`STARTUP_SINGLE_VERSION_HOSTING_INTERFACE`|<span data-ttu-id="fb08f-123">指定不會允許混用裝載介面。</span><span class="sxs-lookup"><span data-stu-id="fb08f-123">Specifies that mixing a hosting interface will not be allowed.</span></span>|  
|`STARTUP_LEGACY_IMPERSONATION`|<span data-ttu-id="fb08f-124">指定的模擬不應該流經非同步點預設。</span><span class="sxs-lookup"><span data-stu-id="fb08f-124">Specifies that impersonation should not flow across asynchronous points by default.</span></span>|  
|`STARTUP_DISABLE_COMMITTHREADSTACK`|<span data-ttu-id="fb08f-125">指定完整執行緒堆疊不應該認可執行緒開始執行時。</span><span class="sxs-lookup"><span data-stu-id="fb08f-125">Specifies that the full thread stack should not be committed when the thread starts running.</span></span>|  
|`STARTUP_ALWAYSFLOW_IMPERSONATION`|<span data-ttu-id="fb08f-126">指定受管理的模擬和模擬透過平台叫用會流經非同步點。</span><span class="sxs-lookup"><span data-stu-id="fb08f-126">Specifies that managed impersonations and impersonations achieved through platform invoke will flow across asynchronous points.</span></span> <span data-ttu-id="fb08f-127">根據預設，只有受管理的模擬會流經非同步點。</span><span class="sxs-lookup"><span data-stu-id="fb08f-127">By default, only managed impersonations will flow across asynchronous points.</span></span>|  
|`STARTUP_TRIM_GC_COMMIT`|<span data-ttu-id="fb08f-128">指定記憶體回收在系統記憶體偏低時，將使用較不認可的空間。</span><span class="sxs-lookup"><span data-stu-id="fb08f-128">Specifies that garbage collection will use less committed space when system memory is low.</span></span> <span data-ttu-id="fb08f-129">請參閱`gcTrimCommitOnLowMemory`中[共用的 Web 裝載的最佳化](../../../../docs/standard/garbage-collection/optimization-for-shared-web-hosting.md)。</span><span class="sxs-lookup"><span data-stu-id="fb08f-129">See `gcTrimCommitOnLowMemory` in [Optimization for Shared Web Hosting](../../../../docs/standard/garbage-collection/optimization-for-shared-web-hosting.md).</span></span>|  
|`STARTUP_ETW`|<span data-ttu-id="fb08f-130">指定 common language runtime 事件，會啟用事件追蹤 Windows (ETW)。</span><span class="sxs-lookup"><span data-stu-id="fb08f-130">Specifies that event tracing for Windows (ETW) is enabled for common language runtime events.</span></span> <span data-ttu-id="fb08f-131">從 Windows Vista 開始，事件追蹤永遠啟用，所以這個旗標不有任何作用。</span><span class="sxs-lookup"><span data-stu-id="fb08f-131">Beginning with Windows Vista, event tracing is always enabled, so this flag has no effect.</span></span> <span data-ttu-id="fb08f-132">請參閱[控制.NET Framework 記錄](../../../../docs/framework/performance/controlling-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="fb08f-132">See [Controlling .NET Framework Logging](../../../../docs/framework/performance/controlling-logging.md).</span></span>|  
|`STARTUP_ARM`|<span data-ttu-id="fb08f-133">指定啟用應用程式定義域資源監視。</span><span class="sxs-lookup"><span data-stu-id="fb08f-133">Specifies that application domain resource monitoring is enabled.</span></span> <span data-ttu-id="fb08f-134">請參閱<xref:System.AppDomain.MonitoringIsEnabled%2A?displayProperty=nameWithType>屬性和[ \<appDomainResourceMonitoring > 項目](../../../../docs/framework/configure-apps/file-schema/runtime/appdomainresourcemonitoring-element.md)。</span><span class="sxs-lookup"><span data-stu-id="fb08f-134">See the <xref:System.AppDomain.MonitoringIsEnabled%2A?displayProperty=nameWithType> property and [\<appDomainResourceMonitoring> Element](../../../../docs/framework/configure-apps/file-schema/runtime/appdomainresourcemonitoring-element.md).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fb08f-135">需求</span><span class="sxs-lookup"><span data-stu-id="fb08f-135">Requirements</span></span>  
 <span data-ttu-id="fb08f-136">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fb08f-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fb08f-137">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fb08f-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fb08f-138">**程式庫：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fb08f-138">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fb08f-139">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fb08f-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb08f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb08f-140">See Also</span></span>  
 [<span data-ttu-id="fb08f-141">裝載列舉</span><span class="sxs-lookup"><span data-stu-id="fb08f-141">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)