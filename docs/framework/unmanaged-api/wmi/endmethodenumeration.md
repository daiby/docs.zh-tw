---
title: "EndMethodEnumeration 函式 （Unmanaged API 參考）"
description: "EndMethodEnumeration 函式會終止方法列舉序列。"
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: EndMethodEnumeration
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: EndMethodEnumeration
helpviewer_keywords: EndMethodEnumeration function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d1b768292811a752e7a319f853ca8eff85f1bb08
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2017
---
# <a name="endmethodenumeration-function"></a><span data-ttu-id="4a460-103">EndMethodEnumeration 函式</span><span class="sxs-lookup"><span data-stu-id="4a460-103">EndMethodEnumeration function</span></span>
<span data-ttu-id="4a460-104">結束呼叫啟動列舉順序[BeginMethodEnumeration 函式](beginmethodenumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="4a460-104">Terminates an enumeration sequence started with a call to the [BeginMethodEnumeration function](beginmethodenumeration.md).</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="4a460-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a460-105">Syntax</span></span>  
  
```  
HRESULT EndMethodEnumeration (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr 
); 
```  

## <a name="parameters"></a><span data-ttu-id="4a460-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a460-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="4a460-107">[in]未使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="4a460-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="4a460-108">[in]指標[IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx)執行個體。</span><span class="sxs-lookup"><span data-stu-id="4a460-108">[in] A pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a460-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a460-109">Return value</span></span>

<span data-ttu-id="4a460-110">這個函式傳回下列值會定義在*WbemCli.h*標頭檔，或者您可以定義它們以常數的形式在程式碼中：</span><span class="sxs-lookup"><span data-stu-id="4a460-110">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="4a460-111">常數</span><span class="sxs-lookup"><span data-stu-id="4a460-111">Constant</span></span>  |<span data-ttu-id="4a460-112">值</span><span class="sxs-lookup"><span data-stu-id="4a460-112">Value</span></span>  |<span data-ttu-id="4a460-113">說明</span><span class="sxs-lookup"><span data-stu-id="4a460-113">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_UNEXPECTED` | <span data-ttu-id="4a460-114">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="4a460-114">0x8004101d</span></span> | <span data-ttu-id="4a460-115">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a460-115">An internal error occurred.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="4a460-116">0</span><span class="sxs-lookup"><span data-stu-id="4a460-116">0</span></span> | <span data-ttu-id="4a460-117">函式呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="4a460-117">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="4a460-118">備註</span><span class="sxs-lookup"><span data-stu-id="4a460-118">Remarks</span></span>

<span data-ttu-id="4a460-119">此函式會包裝呼叫[IWbemClassObject::EndMethodEnumeration](https://msdn.microsoft.com/library/aa391441(v=vs.85).aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="4a460-119">This function wraps a call to the [IWbemClassObject::EndMethodEnumeration](https://msdn.microsoft.com/library/aa391441(v=vs.85).aspx) method.</span></span>

<span data-ttu-id="4a460-120">呼叫者開始列舉順序使用[BeginMethodEnumeration 函式](beginmethodenumeration.md)，然後再呼叫[NextMethod 函式](nextmethod.md )直到該方法傳回`WBEM_S_NO_MORE_DATA`。</span><span class="sxs-lookup"><span data-stu-id="4a460-120">The caller begins the enumeration sequence using [BeginMethodEnumeration function](beginmethodenumeration.md), and then calls the [NextMethod function](nextmethod.md )until the method  returns `WBEM_S_NO_MORE_DATA`.</span></span> <span data-ttu-id="4a460-121">呼叫端 （選擇性） 藉由呼叫完成順序`EndMethodEnumeration`。</span><span class="sxs-lookup"><span data-stu-id="4a460-121">The caller optionally finishes the sequence by calling `EndMethodEnumeration`.</span></span> <span data-ttu-id="4a460-122">呼叫端可能會提早終止列舉型別，藉由呼叫`EndMethodEnumeration`在任何時間。</span><span class="sxs-lookup"><span data-stu-id="4a460-122">The caller may terminate the enumeration early by calling `EndMethodEnumeration` at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a460-123">需求</span><span class="sxs-lookup"><span data-stu-id="4a460-123">Requirements</span></span>  
 <span data-ttu-id="4a460-124">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4a460-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a460-125">**標頭：** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="4a460-125">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="4a460-126">**.NET framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4a460-126">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a460-127">請參閱</span><span class="sxs-lookup"><span data-stu-id="4a460-127">See also</span></span>  
[<span data-ttu-id="4a460-128">WMI 和效能計數器 （Unmanaged API 參考）</span><span class="sxs-lookup"><span data-stu-id="4a460-128">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)