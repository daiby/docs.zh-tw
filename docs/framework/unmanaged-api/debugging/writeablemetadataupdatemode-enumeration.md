---
title: "WriteableMetadataUpdateMode 列舉"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs: cpp
api_name: WriteableMetadataUpdateMode
api_location: mscordbi.dll
api_type: COM
ms.assetid: 6758f4d3-6bc7-4c99-8582-e9be00566784
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 001d80a2232f5b6fbfb43b9de5deafb3317e426d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/21/2017
---
# <a name="writeablemetadataupdatemode-enumeration"></a><span data-ttu-id="44996-102">WriteableMetadataUpdateMode 列舉</span><span class="sxs-lookup"><span data-stu-id="44996-102">WriteableMetadataUpdateMode Enumeration</span></span>
<span data-ttu-id="44996-103">[在 .NET Framework 4.5.2 及更新版本中支援]</span><span class="sxs-lookup"><span data-stu-id="44996-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="44996-104">提供值來指定偵錯工具是否可以看見對中繼資料的記憶體中更新。</span><span class="sxs-lookup"><span data-stu-id="44996-104">Provides values that specify whether in-memory updates to metadata are visible to a debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44996-105">語法</span><span class="sxs-lookup"><span data-stu-id="44996-105">Syntax</span></span>  
  
```cpp
typedef enum WriteableMetadataUpdateMode {  
   LegacyCompatPolicy,  
   AlwaysShowUpdates  
} WriteableMetadataUpdateMode;  
```  
  
## <a name="members"></a><span data-ttu-id="44996-106">成員</span><span class="sxs-lookup"><span data-stu-id="44996-106">Members</span></span>  
  
|<span data-ttu-id="44996-107">成員名稱</span><span class="sxs-lookup"><span data-stu-id="44996-107">Member name</span></span>|<span data-ttu-id="44996-108">描述</span><span class="sxs-lookup"><span data-stu-id="44996-108">Description</span></span>|  
|-----------------|-----------------|  
|`LegacyCompatPolicy`|<span data-ttu-id="44996-109">在對中繼資料可見性進行記憶體中更新時，維護與舊版 .NET Framework 的相容性。</span><span class="sxs-lookup"><span data-stu-id="44996-109">Maintain compatibility with previous versions of the .NET Framework when making in-memory updates to metadata visible.</span></span> <span data-ttu-id="44996-110">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="44996-110">See the Remarks section for more information.</span></span>|  
|`AlwaysShowUpdates`|<span data-ttu-id="44996-111">針對可讓偵錯工具看見的中繼資料進行記憶體中更新。</span><span class="sxs-lookup"><span data-stu-id="44996-111">Make in-memory updates to metadata visible to the debugger.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="44996-112">備註</span><span class="sxs-lookup"><span data-stu-id="44996-112">Remarks</span></span>  
 <span data-ttu-id="44996-113">成員`WriteableMetadataUpdateMode`列舉可以傳遞至[SetWriteableMetadataUpdateMode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess7-setwriteablemetadataupdatemode-method.md)方法，以控制是否在記憶體中更新目標處理序中的中繼資料會顯示偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="44996-113">A member of the `WriteableMetadataUpdateMode` enumeration can be passed to the [SetWriteableMetadataUpdateMode](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess7-setwriteablemetadataupdatemode-method.md) method to control whether in-memory updates to metadata in the target process are visible to the debugger.</span></span>  
  
 <span data-ttu-id="44996-114">`LegacyCompatPolicy` 選項會強制執行與 .NET Framework 4.5.2 之前版本中相同的行為。</span><span class="sxs-lookup"><span data-stu-id="44996-114">The `LegacyCompatPolicy` option enforces the same behavior as in versions of the .NET Framework before 4.5.2.</span></span> <span data-ttu-id="44996-115">這通常就表示看不到更新的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="44996-115">This often means that metadata from updates is not visible.</span></span> <span data-ttu-id="44996-116">不過，呼叫數個偵錯方法會將偵錯工具隱含強制轉型為可看見更新。</span><span class="sxs-lookup"><span data-stu-id="44996-116">However, calls to a number of debugging methods implicitly coerce the debugger to make updates visible.</span></span> <span data-ttu-id="44996-117">例如，如果偵錯工具傳遞[icordebugilframe:: Getlocalvariable](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getlocalvariable-method.md)中找不到方法的原始中繼資料，所有中繼資料的模組會更新為符合目前狀態的快照集之變數的索引程序。</span><span class="sxs-lookup"><span data-stu-id="44996-117">For example, if the debugger passes [ICorDebugILFrame::GetLocalVariable](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getlocalvariable-method.md) the index of a variable not found in the method's original metadata, all metadata for the module is updated to a snapshot matching the current state of the process.</span></span> <span data-ttu-id="44996-118">換句話說，若使用 `LegacyCompatPolicy` 選項，偵錯工具可能看不到、看到部分或所有可用的中繼資料更新，取決於其使用 Unmanaged 偵錯 API 其他部分的方式。</span><span class="sxs-lookup"><span data-stu-id="44996-118">In other words, with the `LegacyCompatPolicy` option, the debugger might see none, some, or all of the available metadata updates, depending on how it uses other parts of the unmanaged debugging API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44996-119">需求</span><span class="sxs-lookup"><span data-stu-id="44996-119">Requirements</span></span>  
 <span data-ttu-id="44996-120">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="44996-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44996-121">**標頭：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="44996-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="44996-122">**程式庫：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="44996-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="44996-123">**.NET framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44996-123">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44996-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44996-124">See Also</span></span>  
 [<span data-ttu-id="44996-125">偵錯列舉</span><span class="sxs-lookup"><span data-stu-id="44996-125">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [<span data-ttu-id="44996-126">SetWriteableMetadataUpdateMode 方法</span><span class="sxs-lookup"><span data-stu-id="44996-126">SetWriteableMetadataUpdateMode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess7-setwriteablemetadataupdatemode-method.md)