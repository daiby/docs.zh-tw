---
title: "ICorDebugInstanceFieldSymbol::GetName 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: d9c12b1f-9c1d-4943-8e9e-93b55faf085f
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: cfd56230d391c44343bdb3f575247b07af1e98ee
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="icordebuginstancefieldsymbolgetname-method"></a><span data-ttu-id="b82a9-102">ICorDebugInstanceFieldSymbol::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="b82a9-102">ICorDebugInstanceFieldSymbol::GetName Method</span></span>
<span data-ttu-id="b82a9-103">取得執行個體欄位的名稱。</span><span class="sxs-lookup"><span data-stu-id="b82a9-103">Gets the name of the instance field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b82a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="b82a9-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,   
   [out] ULONG32 *pcchName,   
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b82a9-105">參數</span><span class="sxs-lookup"><span data-stu-id="b82a9-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="b82a9-106">[in] `szName` 緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="b82a9-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="b82a9-107">[out] 實際寫入 `szName` 緩衝區的字元數指標。</span><span class="sxs-lookup"><span data-stu-id="b82a9-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="b82a9-108">[out] 會儲存傳回的名稱之字元陣列。</span><span class="sxs-lookup"><span data-stu-id="b82a9-108">[out] A character array that stores the returned name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b82a9-109">備註</span><span class="sxs-lookup"><span data-stu-id="b82a9-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b82a9-110">這個方法僅適用於 .NET 原生。</span><span class="sxs-lookup"><span data-stu-id="b82a9-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b82a9-111">需求</span><span class="sxs-lookup"><span data-stu-id="b82a9-111">Requirements</span></span>  
 <span data-ttu-id="b82a9-112">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b82a9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b82a9-113">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b82a9-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b82a9-114">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b82a9-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b82a9-115">**.NET framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b82a9-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b82a9-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b82a9-116">See Also</span></span>  
 [<span data-ttu-id="b82a9-117">ICorDebugInstanceFieldSymbol 介面</span><span class="sxs-lookup"><span data-stu-id="b82a9-117">ICorDebugInstanceFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-interface.md)  
 [<span data-ttu-id="b82a9-118">偵錯介面</span><span class="sxs-lookup"><span data-stu-id="b82a9-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)