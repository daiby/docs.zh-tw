---
title: IMetaDataEmit::SetCustomAttributeValue 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetCustomAttributeValue
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetCustomAttributeValue
helpviewer_keywords:
- SetCustomAttributeValue method [.NET Framework metadata]
- IMetaDataEmit::SetCustomAttributeValue method [.NET Framework metadata]
ms.assetid: f721c863-9642-4e64-917a-65f9e55c25b9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6b699539df52bda9206191dd89c0f95de69140a5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443882"
---
# <a name="imetadataemitsetcustomattributevalue-method"></a>IMetaDataEmit::SetCustomAttributeValue 方法
設定或更新先前呼叫所定義的自訂屬性的值[imetadataemit:: Definecustomattribute](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definecustomattribute-method.md)。  
  
## <a name="syntax"></a>語法  
  
```  
HRESULT SetCustomAttributeValue (   
    [in]  mdCustomAttribute       pcv,   
    [in]  void const              *pCustomAttribute,    
    [in]  ULONG                   cbCustomAttribute   
);  
```  
  
#### <a name="parameters"></a>參數  
 `pcv`  
 [in]目標的自訂屬性的語彙基元。  
  
 `pCustomAttribute`  
 [in]包含自訂屬性的陣列指標。  
  
 `cbCustomAttribute`  
 [in]以位元組為單位，自訂屬性的大小。  
  
## <a name="requirements"></a>需求  
 **平台：** 看到[系統需求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **標頭：** Cor.h  
  
 **程式庫：** 做為 MSCorEE.dll 中的資源  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另請參閱  
 [IMetaDataEmit 介面](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2 介面](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
