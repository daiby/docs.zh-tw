---
title: "GetDemultiplexedStub 函式 （Unmanaged API 參考）"
description: "GetDemultiplexedStub 函式會建立物件轉寄站接收可協助用戶端從 Windows 管理接收非同步呼叫。"
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: GetDemultiplexedStub
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: GetDemultiplexedStub
helpviewer_keywords: GetDemultiplexedStub function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a81101acbf65546ea068e6b5a0e8d9045aaadc71
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2017
---
# <a name="getdemultiplexedstub-function"></a><span data-ttu-id="c5418-103">GetDemultiplexedStub 函式</span><span class="sxs-lookup"><span data-stu-id="c5418-103">GetDemultiplexedStub function</span></span>
<span data-ttu-id="c5418-104">建立物件轉寄站接收可協助用戶端從 Windows 管理接收非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="c5418-104">Creates an object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="c5418-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5418-105">Syntax</span></span>  
  
```  
HRESULT GetDemultiplexedStub (
   [in] IUnknown*    pObject, 
   [in] boolean      isLocal, 
   [out] IUnknown**  ppObject
); 
```  

## <a name="parameters"></a><span data-ttu-id="c5418-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5418-106">Parameters</span></span>

`pObject`  
<span data-ttu-id="c5418-107">[in]用戶端的程序中實作的指標[IWbemObjectSink](https://msdn.microsoft.com/en-us/library/aa391787(v=vs.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="c5418-107">[in] A pointer to the client's in-process implementation of [IWbemObjectSink](https://msdn.microsoft.com/en-us/library/aa391787(v=vs.85).aspx).</span></span>

`isLocal`  
<span data-ttu-id="c5418-108">[in]指出事件是否位於本機的旗標 (`true`)，否則`false`。</span><span class="sxs-lookup"><span data-stu-id="c5418-108">[in] A flag that indicates whether the event is local (`true`); otherwise, `false`.</span></span>

`ppObject`  
<span data-ttu-id="c5418-109">[out]若要協助用戶端從 Windows 管理接收非同步呼叫物件轉寄站接收。</span><span class="sxs-lookup"><span data-stu-id="c5418-109">[out] A object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5418-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5418-110">Return value</span></span>

<span data-ttu-id="c5418-111">如果函式成功，傳回值是`S_OK`(0)。</span><span class="sxs-lookup"><span data-stu-id="c5418-111">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="c5418-112">如果函式失敗，傳回的值就會為非零的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c5418-112">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="c5418-113">若要取得延伸錯誤資訊，請呼叫[GetErrorInfo](geterrorinfo.md)函式。</span><span class="sxs-lookup"><span data-stu-id="c5418-113">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>
    
## <a name="requirements"></a><span data-ttu-id="c5418-114">需求</span><span class="sxs-lookup"><span data-stu-id="c5418-114">Requirements</span></span>  
 <span data-ttu-id="c5418-115">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c5418-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c5418-116">**標頭：** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="c5418-116">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="c5418-117">**.NET framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="c5418-117">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5418-118">請參閱</span><span class="sxs-lookup"><span data-stu-id="c5418-118">See also</span></span>  
[<span data-ttu-id="c5418-119">WMI 和效能計數器 （Unmanaged API 參考）</span><span class="sxs-lookup"><span data-stu-id="c5418-119">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)