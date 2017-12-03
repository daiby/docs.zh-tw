---
title: "ICLRRuntimeInfo::GetVersionString 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRRuntimeInfo.GetVersionString
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRRuntimeInfo::GetVersionString
helpviewer_keywords:
- ICLRRuntimeInfo::GetVersionString method [.NET Framework hosting]
- GetVersionString method, ICLRRuntimeInfo interface [.NET Framework hosting]
ms.assetid: 98b097ef-2276-4dd9-8551-b03c972e8179
topic_type: apiref
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 170b144c642463f6030e033cb5f5aaaf9755d4e2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="iclrruntimeinfogetversionstring-method"></a><span data-ttu-id="16bde-102">ICLRRuntimeInfo::GetVersionString 方法</span><span class="sxs-lookup"><span data-stu-id="16bde-102">ICLRRuntimeInfo::GetVersionString Method</span></span>
<span data-ttu-id="16bde-103">取得 common language runtime (CLR) 版本資訊與相關給定[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)介面。</span><span class="sxs-lookup"><span data-stu-id="16bde-103">Gets common language runtime (CLR) version information associated with a given [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="16bde-104">這個方法會取代以下函數：</span><span class="sxs-lookup"><span data-stu-id="16bde-104">This method supersedes the following functions:</span></span>  
  
-   [<span data-ttu-id="16bde-105">GetRequestedRuntimeInfo</span><span class="sxs-lookup"><span data-stu-id="16bde-105">GetRequestedRuntimeInfo</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)  
  
-   [<span data-ttu-id="16bde-106">GetRequestedRuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="16bde-106">GetRequestedRuntimeVersion</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)  
  
## <a name="syntax"></a><span data-ttu-id="16bde-107">語法</span><span class="sxs-lookup"><span data-stu-id="16bde-107">Syntax</span></span>  
  
```  
HRESULT GetVersionString(  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out]  DWORD *pcchBuffer);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="16bde-108">參數</span><span class="sxs-lookup"><span data-stu-id="16bde-108">Parameters</span></span>  
 `pwzBuffer`  
 <span data-ttu-id="16bde-109">[out].NET Framework 編譯版本，格式為"v*A*。*B*[。*X*]"。</span><span class="sxs-lookup"><span data-stu-id="16bde-109">[out] The .NET Framework compilation version in the format "v*A*.*B*[.*X*]".</span></span> <span data-ttu-id="16bde-110">*A*， *B*，和*X*是對應至主要版本、 次要版本和組建編號的十進位數字。</span><span class="sxs-lookup"><span data-stu-id="16bde-110">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="16bde-111">*X*是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="16bde-111">*X* is optional.</span></span> <span data-ttu-id="16bde-112">如果*X*已不存在，沒有結尾週期。</span><span class="sxs-lookup"><span data-stu-id="16bde-112">If *X* is not present, there is no trailing period.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="16bde-113">C:\Windows\Microsoft.NET\Framework 底下所顯示的樣子，這個參數必須符合.NET Framework 版本的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="16bde-113">This parameter must match the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="16bde-114">範例值是"v1.0.3705"、"v1.1.4322"、"v2.0.50727，"和"v4.0。*x*"，其中*x*取決於已安裝的組建編號。</span><span class="sxs-lookup"><span data-stu-id="16bde-114">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*x*", where *x* depends on the build number installed.</span></span> <span data-ttu-id="16bde-115">請注意，"v"前置詞是強制性。</span><span class="sxs-lookup"><span data-stu-id="16bde-115">Note that the "v" prefix is mandatory.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="16bde-116">[in、 out]指定的大小`pwzBuffer`以避免緩衝區滿溢。</span><span class="sxs-lookup"><span data-stu-id="16bde-116">[in, out] Specifies the size of `pwzBuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="16bde-117">如果`pwzBuffer`是`null`，`pchBuffer`傳回的所需的大小`pwzBuffer`允許 preallocation。</span><span class="sxs-lookup"><span data-stu-id="16bde-117">If `pwzBuffer` is `null`, `pchBuffer` returns the required size of `pwzBuffer` to allow preallocation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="16bde-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="16bde-118">Return Value</span></span>  
 <span data-ttu-id="16bde-119">這個方法會傳回下列特定的 HRESULT 以及 HRESULT 錯誤，以指出方法失敗。</span><span class="sxs-lookup"><span data-stu-id="16bde-119">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="16bde-120">HRESULT</span><span class="sxs-lookup"><span data-stu-id="16bde-120">HRESULT</span></span>|<span data-ttu-id="16bde-121">描述</span><span class="sxs-lookup"><span data-stu-id="16bde-121">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="16bde-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="16bde-122">S_OK</span></span>|<span data-ttu-id="16bde-123">已成功完成命令。</span><span class="sxs-lookup"><span data-stu-id="16bde-123">The method completed successfully.</span></span>|  
|<span data-ttu-id="16bde-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="16bde-124">E_POINTER</span></span>|<span data-ttu-id="16bde-125">`pwzBuffer` 或 `pchBuffer` 為 null。</span><span class="sxs-lookup"><span data-stu-id="16bde-125">`pwzBuffer` or `pchBuffer` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="16bde-126">需求</span><span class="sxs-lookup"><span data-stu-id="16bde-126">Requirements</span></span>  
 <span data-ttu-id="16bde-127">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="16bde-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16bde-128">**標頭：** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="16bde-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="16bde-129">**程式庫：**包含做為 MSCorEE.dll 中的資源</span><span class="sxs-lookup"><span data-stu-id="16bde-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="16bde-130">**.NET framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16bde-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16bde-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16bde-131">See Also</span></span>  
 [<span data-ttu-id="16bde-132">ICLRRuntimeInfo 介面</span><span class="sxs-lookup"><span data-stu-id="16bde-132">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="16bde-133">裝載介面</span><span class="sxs-lookup"><span data-stu-id="16bde-133">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="16bde-134">在.NET Framework 4 和 4.5 加入的 CLR 裝載介面</span><span class="sxs-lookup"><span data-stu-id="16bde-134">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)  
 [<span data-ttu-id="16bde-135">裝載</span><span class="sxs-lookup"><span data-stu-id="16bde-135">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)