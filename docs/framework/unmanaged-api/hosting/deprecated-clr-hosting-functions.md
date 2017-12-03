---
title: "已被取代的 CLR 裝載函式"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- .NET Framework 1.1, hosting global static functions
- global static functions [.NET Framework hosting], version 2.0
- .NET Framework 2.0, hosting global static functions
- hosting global static functions [.NET Framework], version 2.0
ms.assetid: 91fbbb35-e543-4814-b806-371cebae8c5a
caps.latest.revision: "20"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 9530fecb4f2ca6f59d165e49c282320966fd2fa8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2017
---
# <a name="deprecated-clr-hosting-functions"></a><span data-ttu-id="53ddc-102">已被取代的 CLR 裝載函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-102">Deprecated CLR Hosting Functions</span></span>
<span data-ttu-id="53ddc-103">本章節描述的 unmanaged 全域靜態函式使用舊版的裝載 API。</span><span class="sxs-lookup"><span data-stu-id="53ddc-103">This section describes the unmanaged global static functions that earlier versions of the hosting API used.</span></span>  
  
 <span data-ttu-id="53ddc-104">基礎結構功能除外 (`_Cor*`函式)，這僅供.NET Framework 中，這些函式已被取代[!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]。</span><span class="sxs-lookup"><span data-stu-id="53ddc-104">With the exception of the infrastructure functions (`_Cor*` functions), which are used only by the .NET Framework, these functions have been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="activation-functions"></a><span data-ttu-id="53ddc-105">啟用函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-105">Activation functions</span></span>  
 [<span data-ttu-id="53ddc-106">ClrCreateManagedInstance 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-106">ClrCreateManagedInstance Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/clrcreatemanagedinstance-function.md)  
 <span data-ttu-id="53ddc-107">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-107">Deprecated.</span></span> <span data-ttu-id="53ddc-108">建立指定的 managed 型別的執行個體。</span><span class="sxs-lookup"><span data-stu-id="53ddc-108">Creates an instance of the specified managed type.</span></span>  
  
 [<span data-ttu-id="53ddc-109">CoInitializeCor 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-109">CoInitializeCor Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/coinitializecor-function.md)  
 <span data-ttu-id="53ddc-110">已過時。</span><span class="sxs-lookup"><span data-stu-id="53ddc-110">Obsolete.</span></span> <span data-ttu-id="53ddc-111">若要初始化 common language runtime (CLR)，請使用[CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)或[CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md)。</span><span class="sxs-lookup"><span data-stu-id="53ddc-111">To initialize the common language runtime (CLR), use either [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).</span></span>  
  
 [<span data-ttu-id="53ddc-112">CoInitializeEE 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-112">CoInitializeEE Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/coinitializeee-function.md)  
 <span data-ttu-id="53ddc-113">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-113">Deprecated.</span></span> <span data-ttu-id="53ddc-114">確保 CLR 執行引擎載入處理序。</span><span class="sxs-lookup"><span data-stu-id="53ddc-114">Ensures that the CLR execution engine is loaded into a process.</span></span> <span data-ttu-id="53ddc-115">使用[iclrruntimehost:: Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md)方法改為。</span><span class="sxs-lookup"><span data-stu-id="53ddc-115">Use the [ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) method instead.</span></span>  
  
 [<span data-ttu-id="53ddc-116">CorBindToCurrentRuntime 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-116">CorBindToCurrentRuntime Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md)  
 <span data-ttu-id="53ddc-117">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-117">Deprecated.</span></span> <span data-ttu-id="53ddc-118">載入處理序的 common language runtime (CLR) 使用 XML 檔案中儲存的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="53ddc-118">Loads the common language runtime (CLR) into a process by using version information stored in an XML file.</span></span>  
  
 [<span data-ttu-id="53ddc-119">CorBindToRuntime 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-119">CorBindToRuntime Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md)  
 <span data-ttu-id="53ddc-120">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-120">Deprecated.</span></span> <span data-ttu-id="53ddc-121">可讓 unmanaged 的主機將 CLR 載入處理序。</span><span class="sxs-lookup"><span data-stu-id="53ddc-121">Enables unmanaged hosts to load the CLR into a process.</span></span>  
  
 [<span data-ttu-id="53ddc-122">CorBindToRuntimeByCfg 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-122">CorBindToRuntimeByCfg Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md)  
 <span data-ttu-id="53ddc-123">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-123">Deprecated.</span></span> <span data-ttu-id="53ddc-124">載入處理序的 CLR 使用會從 XML 檔案讀取的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="53ddc-124">Loads the CLR into a process by using version information that is read from an XML file.</span></span>  
  
 [<span data-ttu-id="53ddc-125">CorBindToRuntimeEx 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-125">CorBindToRuntimeEx Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)  
 <span data-ttu-id="53ddc-126">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-126">Deprecated.</span></span> <span data-ttu-id="53ddc-127">可讓 unmanaged 的主機將 CLR 載入處理序，並可讓您設定旗標來指定 CLR 的行為。</span><span class="sxs-lookup"><span data-stu-id="53ddc-127">Enables unmanaged hosts to load the CLR into a process, and allows you to set flags to specify the behavior of the CLR.</span></span>  
  
 [<span data-ttu-id="53ddc-128">CorBindToRuntimeHost 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-128">CorBindToRuntimeHost Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md)  
 <span data-ttu-id="53ddc-129">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-129">Deprecated.</span></span> <span data-ttu-id="53ddc-130">可讓主機處理程序中載入指定的 clr 版本。</span><span class="sxs-lookup"><span data-stu-id="53ddc-130">Enables hosts to load a specified version of the CLR into a process.</span></span>  
  
 [<span data-ttu-id="53ddc-131">GetCORRequiredVersion 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-131">GetCORRequiredVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getcorrequiredversion-function.md)  
 <span data-ttu-id="53ddc-132">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-132">Deprecated.</span></span> <span data-ttu-id="53ddc-133">取得必要的 CLR 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="53ddc-133">Gets the required CLR version number.</span></span>  
  
 [<span data-ttu-id="53ddc-134">GetCORSystemDirectory 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-134">GetCORSystemDirectory Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getcorsystemdirectory-function.md)  
 <span data-ttu-id="53ddc-135">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-135">Deprecated.</span></span> <span data-ttu-id="53ddc-136">傳回 CLR 載入到處理程序的安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="53ddc-136">Returns the installation directory of the CLR that is loaded into the process.</span></span>  
  
 [<span data-ttu-id="53ddc-137">GetRealProcAddress 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-137">GetRealProcAddress Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md)  
 <span data-ttu-id="53ddc-138">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-138">Deprecated.</span></span> <span data-ttu-id="53ddc-139">取得最新安裝的 CLR 版本從匯出的指定函式的位址。</span><span class="sxs-lookup"><span data-stu-id="53ddc-139">Gets the address of the specified function that is exported from the latest installed version of the CLR.</span></span>  
  
 [<span data-ttu-id="53ddc-140">GetRequestedRuntimeInfo 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-140">GetRequestedRuntimeInfo Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)  
 <span data-ttu-id="53ddc-141">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-141">Deprecated.</span></span> <span data-ttu-id="53ddc-142">取得有關應用程式所要求的 CLR 版本和目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="53ddc-142">Gets version and directory information about the CLR requested by an application.</span></span>  
  
## <a name="clr-version-functions"></a><span data-ttu-id="53ddc-143">CLR 版本函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-143">CLR version functions</span></span>  
 <span data-ttu-id="53ddc-144">本節中的函式傳回 CLR 版本;它們沒有啟動 CLR。</span><span class="sxs-lookup"><span data-stu-id="53ddc-144">The functions in this section return a CLR version; they do not activate the CLR.</span></span>  
  
 [<span data-ttu-id="53ddc-145">GetCORVersion 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-145">GetCORVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getcorversion-function.md)  
 <span data-ttu-id="53ddc-146">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-146">Deprecated.</span></span> <span data-ttu-id="53ddc-147">傳回目前的處理序中執行的 clr 版本編號。</span><span class="sxs-lookup"><span data-stu-id="53ddc-147">Returns the version number of the CLR that is running in the current process.</span></span>  
  
 [<span data-ttu-id="53ddc-148">GetFileVersion 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-148">GetFileVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getfileversion-function.md)  
 <span data-ttu-id="53ddc-149">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-149">Deprecated.</span></span> <span data-ttu-id="53ddc-150">取得指定的檔案，使用指定的緩衝區的 CLR 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="53ddc-150">Gets the CLR version information of the specified file, using the specified buffer.</span></span>  
  
 [<span data-ttu-id="53ddc-151">GetRequestedRuntimeVersion 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-151">GetRequestedRuntimeVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)  
 <span data-ttu-id="53ddc-152">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-152">Deprecated.</span></span> <span data-ttu-id="53ddc-153">取得所指定的應用程式要求的 CLR 的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="53ddc-153">Gets the version number of the CLR requested by the specified application.</span></span> <span data-ttu-id="53ddc-154">如果未安裝該版本，取得要求的版本之前安裝的最新版本。</span><span class="sxs-lookup"><span data-stu-id="53ddc-154">If that version is not installed, gets the most recent version that is installed before the requested version.</span></span>  
  
 [<span data-ttu-id="53ddc-155">GetRequestedRuntimeVersionForCLSID 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-155">GetRequestedRuntimeVersionForCLSID Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversionforclsid-function.md)  
 <span data-ttu-id="53ddc-156">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-156">Deprecated.</span></span> <span data-ttu-id="53ddc-157">取得具有指定的 CLSID 之類別的適當 CLR 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="53ddc-157">Gets the appropriate CLR version information for the class with the specified CLSID.</span></span>  
  
 [<span data-ttu-id="53ddc-158">GetVersionFromProcess 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-158">GetVersionFromProcess Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md)  
 <span data-ttu-id="53ddc-159">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-159">Deprecated.</span></span> <span data-ttu-id="53ddc-160">取得與指定的處理序控制代碼相關聯之 CLR 的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="53ddc-160">Gets the version number of the CLR that is associated with the specified process handle.</span></span>  
  
 [<span data-ttu-id="53ddc-161">LockClrVersion 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-161">LockClrVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md)  
 <span data-ttu-id="53ddc-162">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-162">Deprecated.</span></span> <span data-ttu-id="53ddc-163">可讓主機判斷處理序中先明確初始化 CLR 使用的 clr 版本。</span><span class="sxs-lookup"><span data-stu-id="53ddc-163">Allows the host to determine which version of the CLR will be used within the process before explicitly initializing the CLR.</span></span>  
  
## <a name="hosting-functions"></a><span data-ttu-id="53ddc-164">裝載函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-164">Hosting functions</span></span>  
 [<span data-ttu-id="53ddc-165">CallFunctionShim 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-165">CallFunctionShim Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/callfunctionshim-function.md)  
 <span data-ttu-id="53ddc-166">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-166">Deprecated.</span></span> <span data-ttu-id="53ddc-167">會指定程式庫中有指定的名稱和參數的函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="53ddc-167">Makes a call to the function that has the specified name and parameters in the specified library.</span></span>  
  
 [<span data-ttu-id="53ddc-168">CoEEShutDownCOM 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-168">CoEEShutDownCOM Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/coeeshutdowncom-function.md)  
 <span data-ttu-id="53ddc-169">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-169">Deprecated.</span></span> <span data-ttu-id="53ddc-170">卸載從處理序的 COM 組件。</span><span class="sxs-lookup"><span data-stu-id="53ddc-170">Unloads a COM assembly from the process.</span></span>  
  
 [<span data-ttu-id="53ddc-171">CorExitProcess 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-171">CorExitProcess Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md)  
 <span data-ttu-id="53ddc-172">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-172">Deprecated.</span></span> <span data-ttu-id="53ddc-173">關閉目前未受管理的程序。</span><span class="sxs-lookup"><span data-stu-id="53ddc-173">Shuts down the current unmanaged process.</span></span>  
  
 [<span data-ttu-id="53ddc-174">CorLaunchApplication 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-174">CorLaunchApplication Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corlaunchapplication-function.md)  
 <span data-ttu-id="53ddc-175">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-175">Deprecated.</span></span> <span data-ttu-id="53ddc-176">啟動指定的網路路徑，使用指定的資訊清單和其他應用程式資料在應用程式。</span><span class="sxs-lookup"><span data-stu-id="53ddc-176">Starts the application at the specified network path, using the specified manifests and other application data.</span></span>  
  
 [<span data-ttu-id="53ddc-177">CorMarkThreadInThreadPool 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-177">CorMarkThreadInThreadPool Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/cormarkthreadinthreadpool-function.md)  
 <span data-ttu-id="53ddc-178">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-178">Deprecated.</span></span> <span data-ttu-id="53ddc-179">標記目前正在執行的執行緒集區執行緒，以便執行 managed 程式碼。</span><span class="sxs-lookup"><span data-stu-id="53ddc-179">Marks the currently executing thread-pool thread for the execution of managed code.</span></span> <span data-ttu-id="53ddc-180">從.NET Framework 2.0 版開始，此函式沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="53ddc-180">Starting with the .NET Framework version 2.0, this function has no effect.</span></span> <span data-ttu-id="53ddc-181">它不是必要項目，並可以從您的程式碼中移除。</span><span class="sxs-lookup"><span data-stu-id="53ddc-181">It is not required, and can be removed from your code.</span></span>  
  
 [<span data-ttu-id="53ddc-182">CoUninitializeCor 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-182">CoUninitializeCor Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/couninitializecor-function.md)  
 <span data-ttu-id="53ddc-183">已過時。</span><span class="sxs-lookup"><span data-stu-id="53ddc-183">Obsolete.</span></span> <span data-ttu-id="53ddc-184">CLR 無法從處理序卸載。</span><span class="sxs-lookup"><span data-stu-id="53ddc-184">The CLR cannot be unloaded from a process.</span></span>  
  
 [<span data-ttu-id="53ddc-185">CoUninitializeEE 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-185">CoUninitializeEE Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/couninitializeee-function.md)  
 <span data-ttu-id="53ddc-186">已過時。</span><span class="sxs-lookup"><span data-stu-id="53ddc-186">Obsolete.</span></span>  
  
 [<span data-ttu-id="53ddc-187">CreateDebuggingInterfaceFromVersion 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-187">CreateDebuggingInterfaceFromVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/createdebugginginterfacefromversion-function.md)  
 <span data-ttu-id="53ddc-188">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-188">Deprecated.</span></span> <span data-ttu-id="53ddc-189">建立[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)物件會根據指定的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="53ddc-189">Creates an [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) object based on the specified version information.</span></span>  
  
 [<span data-ttu-id="53ddc-190">CreateICeeFileGen 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-190">CreateICeeFileGen Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/createiceefilegen-function.md)  
 <span data-ttu-id="53ddc-191">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-191">Deprecated.</span></span> <span data-ttu-id="53ddc-192">建立[ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md)物件。</span><span class="sxs-lookup"><span data-stu-id="53ddc-192">Creates an [ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md) object.</span></span>  
  
 [<span data-ttu-id="53ddc-193">DestroyICeeFileGen 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-193">DestroyICeeFileGen Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/destroyiceefilegen-function.md)  
 <span data-ttu-id="53ddc-194">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-194">Deprecated.</span></span> <span data-ttu-id="53ddc-195">終結[ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md)物件。</span><span class="sxs-lookup"><span data-stu-id="53ddc-195">Destroys an [ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md) object.</span></span>  
  
 [<span data-ttu-id="53ddc-196">FExecuteInAppDomainCallback 函式指標</span><span class="sxs-lookup"><span data-stu-id="53ddc-196">FExecuteInAppDomainCallback Function Pointer</span></span>](../../../../docs/framework/unmanaged-api/hosting/fexecuteinappdomaincallback-function-pointer.md)  
 <span data-ttu-id="53ddc-197">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-197">Deprecated.</span></span> <span data-ttu-id="53ddc-198">指向以 CLR 執行 managed 程式碼呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="53ddc-198">Points to a function that the CLR calls to execute managed code.</span></span>  
  
 [<span data-ttu-id="53ddc-199">FLockClrVersionCallback 函式指標</span><span class="sxs-lookup"><span data-stu-id="53ddc-199">FLockClrVersionCallback Function Pointer</span></span>](../../../../docs/framework/unmanaged-api/hosting/flockclrversioncallback-function-pointer.md)  
 <span data-ttu-id="53ddc-200">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-200">Deprecated.</span></span> <span data-ttu-id="53ddc-201">指向 CLR 會呼叫以通知主機的函式初始設定已啟動，或是已完成。</span><span class="sxs-lookup"><span data-stu-id="53ddc-201">Points to a function that the CLR calls to notify the host that initialization has either started or completed.</span></span>  
  
 [<span data-ttu-id="53ddc-202">GetCLRIdentityManager 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-202">GetCLRIdentityManager Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getclridentitymanager-function.md)  
 <span data-ttu-id="53ddc-203">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-203">Deprecated.</span></span> <span data-ttu-id="53ddc-204">取得可讓管理身分識別 CLR 的介面指標。</span><span class="sxs-lookup"><span data-stu-id="53ddc-204">Gets a pointer to an interface that allows the CLR to manage identities.</span></span>  
  
 [<span data-ttu-id="53ddc-205">LoadLibraryShim 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-205">LoadLibraryShim Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md)  
 <span data-ttu-id="53ddc-206">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-206">Deprecated.</span></span> <span data-ttu-id="53ddc-207">載入指定的版本的.NET Framework DLL。</span><span class="sxs-lookup"><span data-stu-id="53ddc-207">Loads a specified version of a .NET Framework DLL.</span></span>  
  
 [<span data-ttu-id="53ddc-208">LoadStringRC 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-208">LoadStringRC Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/loadstringrc-function.md)  
 <span data-ttu-id="53ddc-209">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-209">Deprecated.</span></span> <span data-ttu-id="53ddc-210">使用目前執行緒的預設文化特性，將 HRESULT 值轉譯成錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="53ddc-210">Translates an HRESULT value into an error message by using the default culture of the current thread.</span></span>  
  
 [<span data-ttu-id="53ddc-211">LoadStringRCEx 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-211">LoadStringRCEx Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/loadstringrcex-function.md)  
 <span data-ttu-id="53ddc-212">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-212">Deprecated.</span></span> <span data-ttu-id="53ddc-213">HRESULT 值轉譯成適當的錯誤訊息指定的文化特性。</span><span class="sxs-lookup"><span data-stu-id="53ddc-213">Translates an HRESULT value to an appropriate error message for the specified culture.</span></span>  
  
 [<span data-ttu-id="53ddc-214">LPOVERLAPPED_COMPLETION_ROUTINE 函式指標</span><span class="sxs-lookup"><span data-stu-id="53ddc-214">LPOVERLAPPED_COMPLETION_ROUTINE Function Pointer</span></span>](../../../../docs/framework/unmanaged-api/hosting/lpoverlapped-completion-routine-function-pointer.md)  
 <span data-ttu-id="53ddc-215">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-215">Deprecated.</span></span> <span data-ttu-id="53ddc-216">指向某個函式以通知主機重疊時 (也就是非同步) 至裝置的 I/O 已完成。</span><span class="sxs-lookup"><span data-stu-id="53ddc-216">Points to a function that notifies the host when an overlapped (that is, asynchronous) I/O to a device has completed.</span></span>  
  
 [<span data-ttu-id="53ddc-217">LPTHREAD_START_ROUTINE 函式指標</span><span class="sxs-lookup"><span data-stu-id="53ddc-217">LPTHREAD_START_ROUTINE Function Pointer</span></span>](../../../../docs/framework/unmanaged-api/hosting/lpthread-start-routine-function-pointer.md)  
 <span data-ttu-id="53ddc-218">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-218">Deprecated.</span></span> <span data-ttu-id="53ddc-219">指向以通知主機在執行緒已開始執行的函式。</span><span class="sxs-lookup"><span data-stu-id="53ddc-219">Points to a function that notifies the host that a thread has started to execute.</span></span>  
  
 [<span data-ttu-id="53ddc-220">RunDll32ShimW 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-220">RunDll32ShimW Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/rundll32shimw-function.md)  
 <span data-ttu-id="53ddc-221">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-221">Deprecated.</span></span> <span data-ttu-id="53ddc-222">執行指定命令。</span><span class="sxs-lookup"><span data-stu-id="53ddc-222">Executes the specified command.</span></span>  
  
 [<span data-ttu-id="53ddc-223">WAITORTIMERCALLBACK 函式指標</span><span class="sxs-lookup"><span data-stu-id="53ddc-223">WAITORTIMERCALLBACK Function Pointer</span></span>](../../../../docs/framework/unmanaged-api/hosting/waitortimercallback-function-pointer.md)  
 <span data-ttu-id="53ddc-224">已取代。</span><span class="sxs-lookup"><span data-stu-id="53ddc-224">Deprecated.</span></span> <span data-ttu-id="53ddc-225">指向以通知主機，等候控制代碼已收到信號或逾時的函式。</span><span class="sxs-lookup"><span data-stu-id="53ddc-225">Points to a function that notifies the host that a wait handle has either been signaled or timed out.</span></span>  
  
## <a name="infrastructure-functions"></a><span data-ttu-id="53ddc-226">基礎結構函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-226">Infrastructure functions</span></span>  
 <span data-ttu-id="53ddc-227">本節中的函式是.NET Framework 所使用。</span><span class="sxs-lookup"><span data-stu-id="53ddc-227">The functions in this section are for use by the .NET Framework only.</span></span>  
  
 [<span data-ttu-id="53ddc-228">_CorDllMain 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-228">_CorDllMain Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/cordllmain-function.md)  
 <span data-ttu-id="53ddc-229">初始化 CLR 中，找出 managed 的進入點 DLL 組件的 CLR 標頭，並開始執行。</span><span class="sxs-lookup"><span data-stu-id="53ddc-229">Initializes the CLR, locates the managed entry point in the DLL assembly's CLR header, and begins execution.</span></span>  
  
 [<span data-ttu-id="53ddc-230">_CorExeMain 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-230">_CorExeMain Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corexemain-function.md)  
 <span data-ttu-id="53ddc-231">初始化 CLR 中，找出 managed 的進入點中可執行組件的 CLR 標頭，並開始執行。</span><span class="sxs-lookup"><span data-stu-id="53ddc-231">Initializes the CLR, locates the managed entry point in the executable assembly's CLR header, and begins execution.</span></span>  
  
 [<span data-ttu-id="53ddc-232">_CorExeMain2 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-232">_CorExeMain2 Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corexemain2-function.md)  
 <span data-ttu-id="53ddc-233">指定記憶體對應程式碼中執行的進入點。</span><span class="sxs-lookup"><span data-stu-id="53ddc-233">Executes the entry point in the specified memory-mapped code.</span></span> <span data-ttu-id="53ddc-234">作業系統載入器會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="53ddc-234">This function is called by the operating system loader.</span></span>  
  
 [<span data-ttu-id="53ddc-235">_CorImageUnloading 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-235">_CorImageUnloading Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corimageunloading-function.md)  
 <span data-ttu-id="53ddc-236">卸載 managed 的模組映像時，請通知載入器。</span><span class="sxs-lookup"><span data-stu-id="53ddc-236">Notifies the loader when the managed module images are unloaded.</span></span>  
  
 [<span data-ttu-id="53ddc-237">_CorValidateImage 函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-237">_CorValidateImage Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/corvalidateimage-function.md)  
 <span data-ttu-id="53ddc-238">驗證 managed 的模組映像，並已經載入後，通知作業系統載入器。</span><span class="sxs-lookup"><span data-stu-id="53ddc-238">Validates managed module images, and notifies the operating system loader after they have been loaded.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53ddc-239">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53ddc-239">See Also</span></span>  
 [<span data-ttu-id="53ddc-240">.NET framework 4 裝載全域靜態函式</span><span class="sxs-lookup"><span data-stu-id="53ddc-240">.NET Framework 4 Hosting Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/net-framework-4-hosting-global-static-functions.md) 