---
title: "ICorProfilerInfo::GetCodeInfo 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.GetCodeInfo
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::GetCodeInfo
helpviewer_keywords:
- GetCodeInfo method [.NET Framework profiling]
- ICorProfilerInfo::GetCodeInfo method [.NET Framework profiling]
ms.assetid: 90140b0f-a926-4a7e-b6fa-23e05f703cce
topic_type: apiref
caps.latest.revision: "18"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 0b5c7b0d932200f04df0a1a84dd1f747b7945943
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfogetcodeinfo-method"></a><span data-ttu-id="f8f96-102">ICorProfilerInfo::GetCodeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="f8f96-102">ICorProfilerInfo::GetCodeInfo Method</span></span>
<span data-ttu-id="f8f96-103">取得與指定函式識別碼相關聯的機器碼範圍。</span><span class="sxs-lookup"><span data-stu-id="f8f96-103">Gets the extent of native code associated with the specified function ID.</span></span>  
  
 <span data-ttu-id="f8f96-104">這個方法已過時。</span><span class="sxs-lookup"><span data-stu-id="f8f96-104">This method is obsolete.</span></span> <span data-ttu-id="f8f96-105">使用[icorprofilerinfo2:: Getcodeinfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md)方法改為。</span><span class="sxs-lookup"><span data-stu-id="f8f96-105">Use the [ICorProfilerInfo2::GetCodeInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getcodeinfo2-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8f96-106">語法</span><span class="sxs-lookup"><span data-stu-id="f8f96-106">Syntax</span></span>  
  
```  
HRESULT GetCodeInfo(  
    [in]  FunctionID functionId,  
    [out] LPCBYTE    *pStart,  
    [out] ULONG      *pcSize);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f8f96-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8f96-107">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="f8f96-108">[in] 與機器碼關聯的函式識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8f96-108">[in] The ID of the function with which the native code is associated.</span></span>  
  
 `pStart`  
 <span data-ttu-id="f8f96-109">[out] 構成函式機器碼的位元組陣列指標。</span><span class="sxs-lookup"><span data-stu-id="f8f96-109">[out] A pointer to an array of bytes that compose the native code of the function.</span></span>  
  
 `pcSize`  
 <span data-ttu-id="f8f96-110">[out] 整數的指標，此整數指定機器碼的大小，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="f8f96-110">[out] A pointer to an integer that specifies the size, in bytes, of the native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f8f96-111">備註</span><span class="sxs-lookup"><span data-stu-id="f8f96-111">Remarks</span></span>  
 <span data-ttu-id="f8f96-112">為了最佳化效能，.NET Framework 2.0 版中的執行階段會將先行編譯的函式機器碼分割成多個區域。</span><span class="sxs-lookup"><span data-stu-id="f8f96-112">To optimize performance, the runtime in the .NET Framework version 2.0 splits the precompiled, native code of a function into multiple regions.</span></span> <span data-ttu-id="f8f96-113">因此，`GetCodeInfo` 方法在 .NET Framework 2.0 中已過時，因為它無法處理函式機器碼的範圍。</span><span class="sxs-lookup"><span data-stu-id="f8f96-113">Consequently, the `GetCodeInfo` method is obsolete in the .NET Framework 2.0 because it is unable to handle the extent of a function's native code.</span></span> <span data-ttu-id="f8f96-114">分析工具應改為使用較為通用的 `ICorProfilerInfo2::GetCodeInfo2` 方法。</span><span class="sxs-lookup"><span data-stu-id="f8f96-114">Profilers should switch to using the more general `ICorProfilerInfo2::GetCodeInfo2` method instead.</span></span>  
  
 <span data-ttu-id="f8f96-115">這個函式會使用呼叫端配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f8f96-115">This function uses caller-allocated buffers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8f96-116">需求</span><span class="sxs-lookup"><span data-stu-id="f8f96-116">Requirements</span></span>  
 <span data-ttu-id="f8f96-117">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f8f96-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8f96-118">**標頭：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f8f96-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f8f96-119">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f8f96-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f8f96-120">**.NET framework 版本：** 1.0</span><span class="sxs-lookup"><span data-stu-id="f8f96-120">**.NET Framework Versions:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8f96-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8f96-121">See Also</span></span>  
 [<span data-ttu-id="f8f96-122">ICorProfilerInfo 介面</span><span class="sxs-lookup"><span data-stu-id="f8f96-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="f8f96-123">分析介面</span><span class="sxs-lookup"><span data-stu-id="f8f96-123">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="f8f96-124">程式碼剖析</span><span class="sxs-lookup"><span data-stu-id="f8f96-124">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)