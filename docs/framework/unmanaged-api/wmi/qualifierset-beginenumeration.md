---
title: "QualifierSet_BeginEnumeration 函式 （Unmanaged API 參考）"
description: "QualifierSet_BeginEnumeration 函式會重設物件的辨識符號的列舉值。"
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: QualifierSet_BeginEnumeration
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: QualifierSet_BeginEnumeration
helpviewer_keywords: QualifierSet_BeginEnumeration function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f66df772032b8e96b4956f3ed9a5818e961bd919
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/15/2017
---
# <a name="qualifiersetbeginenumeration-function"></a><span data-ttu-id="2317f-103">QualifierSet_BeginEnumeration 函式</span><span class="sxs-lookup"><span data-stu-id="2317f-103">QualifierSet_BeginEnumeration function</span></span>
<span data-ttu-id="2317f-104">將物件的辨識符號的列舉值重設列舉的開頭。</span><span class="sxs-lookup"><span data-stu-id="2317f-104">Resets an enumerator of the qualifiers of an object to the beginning of the enumeration.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="2317f-105">語法</span><span class="sxs-lookup"><span data-stu-id="2317f-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_BeginEnumeration (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LONG                 lFlags
); 
```  

## <a name="parameters"></a><span data-ttu-id="2317f-106">參數</span><span class="sxs-lookup"><span data-stu-id="2317f-106">Parameters</span></span>

`vFunc`   
<span data-ttu-id="2317f-107">[in]未使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2317f-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="2317f-108">[in]指標[IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx)執行個體。</span><span class="sxs-lookup"><span data-stu-id="2317f-108">[in] A pointer to an [IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) instance.</span></span>

`lFlags`   
<span data-ttu-id="2317f-109">[in]旗標或描述中值的位元組合[備註](#remarks)區段，指定要包含在列舉中的限定詞。</span><span class="sxs-lookup"><span data-stu-id="2317f-109">[in] A bitwise combination of the flags or values described in the [Remarks](#remarks) section that specifies the qualifiers to include in the enumeration.</span></span>

## <a name="return-value"></a><span data-ttu-id="2317f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2317f-110">Return value</span></span>

<span data-ttu-id="2317f-111">這個函式傳回下列值會定義在*WbemCli.h*標頭檔，或者您可以定義它們以常數的形式在程式碼中：</span><span class="sxs-lookup"><span data-stu-id="2317f-111">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="2317f-112">常數</span><span class="sxs-lookup"><span data-stu-id="2317f-112">Constant</span></span>  |<span data-ttu-id="2317f-113">值</span><span class="sxs-lookup"><span data-stu-id="2317f-113">Value</span></span>  |<span data-ttu-id="2317f-114">說明</span><span class="sxs-lookup"><span data-stu-id="2317f-114">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="2317f-115">0x80041008</span><span class="sxs-lookup"><span data-stu-id="2317f-115">0x80041008</span></span> | <span data-ttu-id="2317f-116">`lFlags`參數無效。</span><span class="sxs-lookup"><span data-stu-id="2317f-116">The `lFlags` parameter is not valid.</span></span> |
|`WBEM_E_UNEXPECTED` | <span data-ttu-id="2317f-117">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="2317f-117">0x8004101d</span></span> | <span data-ttu-id="2317f-118">第二個呼叫`QualifierSet_BeginEnumeration`所沒有的中間呼叫[ `QualifierSet_EndEnumeration` ](qualifierset-endenumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="2317f-118">A second call to `QualifierSet_BeginEnumeration` was made without an intervening call to [`QualifierSet_EndEnumeration`](qualifierset-endenumeration.md).</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="2317f-119">0x80041006</span><span class="sxs-lookup"><span data-stu-id="2317f-119">0x80041006</span></span> | <span data-ttu-id="2317f-120">使用開始新的列舉型別沒有足夠的記憶體。</span><span class="sxs-lookup"><span data-stu-id="2317f-120">Not enough memory is available to begin a new enumeration.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="2317f-121">0</span><span class="sxs-lookup"><span data-stu-id="2317f-121">0</span></span> | <span data-ttu-id="2317f-122">函式呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="2317f-122">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="2317f-123">備註</span><span class="sxs-lookup"><span data-stu-id="2317f-123">Remarks</span></span>

<span data-ttu-id="2317f-124">此函式會包裝呼叫[IWbemQualifierSet::BeginEnumeration](https://msdn.microsoft.com/library/aa391861(v=vs.85).aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="2317f-124">This function wraps a call to the [IWbemQualifierSet::BeginEnumeration](https://msdn.microsoft.com/library/aa391861(v=vs.85).aspx) method.</span></span>

<span data-ttu-id="2317f-125">若要列舉所有的物件上的限定詞，必須呼叫這個方法的第一個呼叫之前[QualifierSet_Next](qualifierset-next.md)。</span><span class="sxs-lookup"><span data-stu-id="2317f-125">To enumerate all of the qualifiers on an object, this method must be called before the first call to [QualifierSet_Next](qualifierset-next.md).</span></span> <span data-ttu-id="2317f-126">限定詞會列舉中的順序被保證能夠針對指定的列舉型別而異。</span><span class="sxs-lookup"><span data-stu-id="2317f-126">The order in which qualifiers are enumerated is guaranteed to be invariant for a given enumeration.</span></span>

<span data-ttu-id="2317f-127">可以做為傳遞的旗標`lEnumFlags`引數中所定義*WbemCli.h*標頭檔，或者您可以定義它們以常數的形式在程式碼中。</span><span class="sxs-lookup"><span data-stu-id="2317f-127">The flags that can be passed as the `lEnumFlags` argument are defined in the *WbemCli.h* header file, or you can define them as constants in your code.</span></span>   

|<span data-ttu-id="2317f-128">常數</span><span class="sxs-lookup"><span data-stu-id="2317f-128">Constant</span></span>  |<span data-ttu-id="2317f-129">值</span><span class="sxs-lookup"><span data-stu-id="2317f-129">Value</span></span>  |<span data-ttu-id="2317f-130">描述</span><span class="sxs-lookup"><span data-stu-id="2317f-130">Description</span></span>  |
|---------|---------|---------|
|  | <span data-ttu-id="2317f-131">0</span><span class="sxs-lookup"><span data-stu-id="2317f-131">0</span></span> | <span data-ttu-id="2317f-132">傳回所有限定詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="2317f-132">Return the names of all qualifiers.</span></span> |
| `WBEM_FLAG_LOCAL_ONLY` | <span data-ttu-id="2317f-133">0x10</span><span class="sxs-lookup"><span data-stu-id="2317f-133">0x10</span></span> | <span data-ttu-id="2317f-134">傳回目前的屬性或物件特定限定詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="2317f-134">Return only the names of qualifiers specific to the current property or object.</span></span> <br/> <span data-ttu-id="2317f-135">屬性： 返回 （包括覆寫） 的屬性特定辨識符號，並不是這些限定詞傳播從類別定義。</span><span class="sxs-lookup"><span data-stu-id="2317f-135">For a property: Return only the qualifiers specific to the property (including overrides), and not those qualifiers propagated from the class definition.</span></span> <br/> <span data-ttu-id="2317f-136">執行個體： 傳回只可使用特定執行個體的限定詞名稱。</span><span class="sxs-lookup"><span data-stu-id="2317f-136">For an instance: Return only instance-specific qualifier names.</span></span> <br/> <span data-ttu-id="2317f-137">類別： 返回衍生的類別 beiong 特定只限定詞。</span><span class="sxs-lookup"><span data-stu-id="2317f-137">For a class: Return only qualifiers specific to the class beiong derived.</span></span>
|`WBEM_FLAG_PROPAGATED_ONLY` | <span data-ttu-id="2317f-138">0x20</span><span class="sxs-lookup"><span data-stu-id="2317f-138">0x20</span></span> | <span data-ttu-id="2317f-139">傳回的傳播限定詞的名稱，從另一個物件。</span><span class="sxs-lookup"><span data-stu-id="2317f-139">Return only the names of qualifiers propagated from another object.</span></span> <br/> <span data-ttu-id="2317f-140">屬性： 傳回僅限定詞傳播給這個屬性從類別定義中，而不從本身的屬性。</span><span class="sxs-lookup"><span data-stu-id="2317f-140">For a property: Return only the qualifiers propagated to this property from the class definition, and not those from the property itself.</span></span> <br/> <span data-ttu-id="2317f-141">執行個體： 傳回傳播這些辨識符號，從類別定義。</span><span class="sxs-lookup"><span data-stu-id="2317f-141">For an instance: Return only those qualifiers propagated from the class definition.</span></span> <br/> <span data-ttu-id="2317f-142">類別： 傳回繼承自父類別的只有這些限定詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="2317f-142">For a class: Return only those qualifier names inherited from the parent classes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="2317f-143">需求</span><span class="sxs-lookup"><span data-stu-id="2317f-143">Requirements</span></span>  
 <span data-ttu-id="2317f-144">**平台：**看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2317f-144">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2317f-145">**標頭：** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="2317f-145">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="2317f-146">**.NET framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2317f-146">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2317f-147">請參閱</span><span class="sxs-lookup"><span data-stu-id="2317f-147">See also</span></span>  
[<span data-ttu-id="2317f-148">WMI 和效能計數器 （Unmanaged API 參考）</span><span class="sxs-lookup"><span data-stu-id="2317f-148">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)