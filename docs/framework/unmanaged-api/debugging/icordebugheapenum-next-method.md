---
title: "ICorDebugHeapEnum::Next 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugHeapEnum.Next
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugHeapEnum::Next
helpviewer_keywords:
- ICorDebugHeapEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugHeapEnum interface [.NET Framework debugging]
ms.assetid: 2221fd06-9e27-4113-972e-2530db8c3594
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a15637f925401f23f9da34e33583c9bc5c014dd3
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugheapenumnext-method"></a><span data-ttu-id="1ee6c-102">ICorDebugHeapEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="1ee6c-102">ICorDebugHeapEnum::Next Method</span></span>
<span data-ttu-id="1ee6c-103">取得指定的數目[COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md)包含 managed 堆積上物件的相關資訊的執行個體。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-103">Gets the specified number of [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instances that contain information about objects on the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ee6c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ee6c-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG celt,    [out, size_is(celt), length_is(*pceltFetched)] COR_HEAPOBJECT  objects[],   
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1ee6c-105">參數</span><span class="sxs-lookup"><span data-stu-id="1ee6c-105">Parameters</span></span>  
 <span data-ttu-id="1ee6c-106">celt</span><span class="sxs-lookup"><span data-stu-id="1ee6c-106">celt</span></span>  
 <span data-ttu-id="1ee6c-107">[in] 要擷取的物件數目。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-107">[in] The number of objects to be retrieved.</span></span>  
  
 <span data-ttu-id="1ee6c-108">物件</span><span class="sxs-lookup"><span data-stu-id="1ee6c-108">objects</span></span>  
 <span data-ttu-id="1ee6c-109">[out]陣列的指標，其中每個指向[COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md)提供 managed 堆積物件的相關資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-109">[out] An array of pointers, each of which points to a [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) object that provides information about an object on the managed heap.</span></span>  
  
 <span data-ttu-id="1ee6c-110">pceltFetched</span><span class="sxs-lookup"><span data-stu-id="1ee6c-110">pceltFetched</span></span>  
 <span data-ttu-id="1ee6c-111">[out]數目的指標[COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md)中實際傳回的物件`objects`。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-111">[out] A pointer to the number of [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) objects actually returned in `objects`.</span></span> <span data-ttu-id="1ee6c-112">如果 `celt` 為 1，則這個值可能是 `null`。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-112">This value may be `null` if `celt` is 1.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ee6c-113">備註</span><span class="sxs-lookup"><span data-stu-id="1ee6c-113">Remarks</span></span>  
 <span data-ttu-id="1ee6c-114">`COR_HEAPOBJECT.type` 欄位是計算巢狀參考數目之 COM 介面的識別項。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-114">The `COR_HEAPOBJECT.type` field is the identifier of a nested reference-counted COM interface.</span></span> <span data-ttu-id="1ee6c-115">這個參考必須由 `ICorDebugHeapEnum::Next` 的呼叫者釋放。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-115">This reference must be released by the caller of `ICorDebugHeapEnum::Next`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ee6c-116">需求</span><span class="sxs-lookup"><span data-stu-id="1ee6c-116">Requirements</span></span>  
 <span data-ttu-id="1ee6c-117">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1ee6c-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ee6c-118">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1ee6c-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1ee6c-119">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1ee6c-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1ee6c-120">**.NET framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ee6c-120">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ee6c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ee6c-121">See Also</span></span>  
 [<span data-ttu-id="1ee6c-122">ICorDebugHeapEnum 介面</span><span class="sxs-lookup"><span data-stu-id="1ee6c-122">ICorDebugHeapEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapenum-interface.md)  
 [<span data-ttu-id="1ee6c-123">偵錯介面</span><span class="sxs-lookup"><span data-stu-id="1ee6c-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)