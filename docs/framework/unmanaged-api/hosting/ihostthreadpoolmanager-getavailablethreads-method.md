---
title: "IHostThreadPoolManager::GetAvailableThreads 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostThreadPoolManager.GetAvailableThreads
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostThreadPoolManager::GetAvailableThreads
helpviewer_keywords:
- GetAvailableThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
- IHostThreadPoolManager::GetAvailableThreads method [.NET Framework hosting]
ms.assetid: 61d26dfd-7f24-4e7d-a63e-b30a463f08e1
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 11cd8de264a332cd553ad44a35355bf45039ab84
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="ihostthreadpoolmanagergetavailablethreads-method"></a><span data-ttu-id="ccfd5-102">IHostThreadPoolManager::GetAvailableThreads 方法</span><span class="sxs-lookup"><span data-stu-id="ccfd5-102">IHostThreadPoolManager::GetAvailableThreads Method</span></span>
<span data-ttu-id="ccfd5-103">取得目前未處理的工作項目之執行緒集區中的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-103">Gets the number of threads in the thread pool that are not currently processing work items.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccfd5-104">語法</span><span class="sxs-lookup"><span data-stu-id="ccfd5-104">Syntax</span></span>  
  
```  
HRESULT GetAvailableThreads (  
    [out] DWORD *pdwAvailableWorkerThreads  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ccfd5-105">參數</span><span class="sxs-lookup"><span data-stu-id="ccfd5-105">Parameters</span></span>  
 `pdwAvailableWorkerThreads`  
 <span data-ttu-id="ccfd5-106">[out]目前未處理的工作項目中的執行緒集區的執行緒數目的指標。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-106">[out] Pointer to the number of threads in the thread pool that are not currently processing work items.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ccfd5-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccfd5-107">Return Value</span></span>  
  
|<span data-ttu-id="ccfd5-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ccfd5-108">HRESULT</span></span>|<span data-ttu-id="ccfd5-109">描述</span><span class="sxs-lookup"><span data-stu-id="ccfd5-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ccfd5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccfd5-110">S_OK</span></span>|<span data-ttu-id="ccfd5-111">`GetAvailableThreads`已成功傳回。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-111">`GetAvailableThreads` returned successfully.</span></span>|  
|<span data-ttu-id="ccfd5-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ccfd5-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ccfd5-113">Common language runtime (CLR) 尚未載入到處理程序，或 CLR 正在中它無法執行 managed 程式碼，或成功地處理呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ccfd5-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ccfd5-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ccfd5-115">呼叫已逾時。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-115">The call timed out.</span></span>|  
|<span data-ttu-id="ccfd5-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ccfd5-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ccfd5-117">呼叫端未擁有鎖定。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ccfd5-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ccfd5-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ccfd5-119">事件已取消時封鎖的執行緒或 fiber 等候它。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ccfd5-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ccfd5-120">E_FAIL</span></span>|<span data-ttu-id="ccfd5-121">發生未知的嚴重失敗。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ccfd5-122">方法會傳回 E_FAIL CLR 已不再可用的處理序內。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ccfd5-123">裝載方法的後續呼叫會傳回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ccfd5-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="ccfd5-124">E_NOTIMPL</span></span>|<span data-ttu-id="ccfd5-125">主機並未提供的實作`GetAvailableThreads`。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-125">The host does not provide an implementation of `GetAvailableThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ccfd5-126">備註</span><span class="sxs-lookup"><span data-stu-id="ccfd5-126">Remarks</span></span>  
 <span data-ttu-id="ccfd5-127">如果主機並未提供的實作`GetAvailableThreads`，它應該會傳回 E_NOTIMPL 的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-127">If the host does not provide an implementation of `GetAvailableThreads`, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ccfd5-128">需求</span><span class="sxs-lookup"><span data-stu-id="ccfd5-128">Requirements</span></span>  
 <span data-ttu-id="ccfd5-129">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ccfd5-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ccfd5-130">**標頭：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ccfd5-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ccfd5-131">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="ccfd5-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ccfd5-132">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ccfd5-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccfd5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccfd5-133">See Also</span></span>  
 <xref:System.Threading.ThreadPool.GetAvailableThreads%2A>  
 <xref:System.Threading.ThreadPool>  
 [<span data-ttu-id="ccfd5-134">IHostThreadPoolManager 介面</span><span class="sxs-lookup"><span data-stu-id="ccfd5-134">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)