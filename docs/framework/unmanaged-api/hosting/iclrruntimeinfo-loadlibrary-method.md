---
title: "ICLRRuntimeInfo::LoadLibrary 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRRuntimeInfo.LoadLibrary
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRRuntimeInfo::LoadLibrary
helpviewer_keywords:
- ICLRRuntimeInfo::LoadLibrary method [.NET Framework hosting]
- LoadLibrary method [.NET Framework hosting]
ms.assetid: 4517ada3-4417-4ac5-a150-73da7a87c686
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c1d943f45a4e665836f376bddf65d84329c1900e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="iclrruntimeinfoloadlibrary-method"></a><span data-ttu-id="8a5eb-102">ICLRRuntimeInfo::LoadLibrary 方法</span><span class="sxs-lookup"><span data-stu-id="8a5eb-102">ICLRRuntimeInfo::LoadLibrary Method</span></span>
<span data-ttu-id="8a5eb-103">.NET Framework 程式庫載入 common language runtime (CLR) 所表示從[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)介面。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-103">Loads a .NET Framework library from the common language runtime (CLR) represented by an [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="8a5eb-104">這個方法會取代[LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md)函式。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-104">This method supersedes the [LoadLibraryShim](../../../../docs/framework/unmanaged-api/hosting/loadlibraryshim-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a5eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="8a5eb-105">Syntax</span></span>  
  
```  
HRESULT LoadLibrary(  
     [in]  LPCWSTR pwzDllName,  
     [out, retval] HMODULE *phndModule);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8a5eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a5eb-106">Parameters</span></span>  
 `pwzDllName`  
 <span data-ttu-id="8a5eb-107">[in]要載入之組件名稱。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-107">[in] The name of the assembly to be loaded.</span></span>  
  
 `phndModule`  
 <span data-ttu-id="8a5eb-108">[out]載入的組件控制代碼。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-108">[out] A handle to the loaded assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8a5eb-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a5eb-109">Return Value</span></span>  
 <span data-ttu-id="8a5eb-110">這個方法會傳回下列特定的 HRESULT 以及 HRESULT 錯誤，以指出方法失敗。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="8a5eb-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8a5eb-111">HRESULT</span></span>|<span data-ttu-id="8a5eb-112">描述</span><span class="sxs-lookup"><span data-stu-id="8a5eb-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8a5eb-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a5eb-113">S_OK</span></span>|<span data-ttu-id="8a5eb-114">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="8a5eb-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="8a5eb-115">E_POINTER</span></span>|<span data-ttu-id="8a5eb-116">`pwzDllName` 或 `phndModule` 為 null。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-116">`pwzDllName` or `phndModule` is null.</span></span>|  
|<span data-ttu-id="8a5eb-117">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8a5eb-117">E_OUTOFMEMORY</span></span>|<span data-ttu-id="8a5eb-118">沒有足夠的記憶體是可用來處理要求。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-118">Not enough memory is available to handle the request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8a5eb-119">備註</span><span class="sxs-lookup"><span data-stu-id="8a5eb-119">Remarks</span></span>  
 <span data-ttu-id="8a5eb-120">這個方法只會載入 Dll 包含在.NET Framework 可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-120">This method only loads DLLs included in the .NET Framework redistributable package.</span></span> <span data-ttu-id="8a5eb-121">它無法載入使用者產生的組件。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-121">It can not load user-generated assemblies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a5eb-122">需求</span><span class="sxs-lookup"><span data-stu-id="8a5eb-122">Requirements</span></span>  
 <span data-ttu-id="8a5eb-123">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8a5eb-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a5eb-124">**標頭：** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="8a5eb-124">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="8a5eb-125">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="8a5eb-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8a5eb-126">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a5eb-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a5eb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a5eb-127">See Also</span></span>  
 [<span data-ttu-id="8a5eb-128">ICLRRuntimeInfo 介面</span><span class="sxs-lookup"><span data-stu-id="8a5eb-128">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="8a5eb-129">裝載介面</span><span class="sxs-lookup"><span data-stu-id="8a5eb-129">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="8a5eb-130">裝載</span><span class="sxs-lookup"><span data-stu-id="8a5eb-130">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)