---
title: '&lt;移除&gt;schemeSettings （Uri 設定） 的項目'
ms.date: 03/30/2017
ms.assetid: 4095ba51-de20-4f87-b562-018abe422c91
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 3f4e3dbdc3dae425e44cd1c0890e8fef9d42a780
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2018
ms.locfileid: "48028392"
---
# <a name="ltremovegt-element-for-schemesettings-uri-settings"></a>&lt;移除&gt;schemeSettings （Uri 設定） 的項目
移除結構描述設定的配置名稱。  
  
 \<configuration>  
\<uri >  
\<schemeSettings >  
\<remove>  
  
## <a name="syntax"></a>語法  
  
```xml  
<remove
  name="http|https"
/>
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|名稱|這項設定適用於配置名稱。 僅支援的值為名稱 ="http"和名稱 ="https"。|  
  
### <a name="child-elements"></a>子元素  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<schemeSettings> 項目 (URI 設定)](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|指定如何針對特定配置剖析 <xref:System.Uri>。|  
  
## <a name="remarks"></a>備註  
 根據預設，<xref:System.Uri?displayProperty=nameWithType>類別取消逸出百分比編碼路徑分隔符號，然後再執行路徑壓縮。 這被實作為安全性機制，抵禦攻擊，如下所示：  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 如果這個 URI 會傳遞到模組不會處理百分比編碼字元正確，可能會造成伺服器正在執行下列命令：  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 基於這個理由，<xref:System.Uri?displayProperty=nameWithType>類別第一個取消逸出路徑分隔符號，然後再套用路徑壓縮。 傳遞至以上惡意 URL 的結果<xref:System.Uri?displayProperty=nameWithType>類別建構函式結果，在下列 URI:  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 此預設行為可以修改為不取消逸出百分比編碼的路徑分隔符號使用 schemeSettings 組態選項的特定結構描述中。  
  
## <a name="configuration-files"></a>組態檔  
 此項目可以用於應用程式組態檔或電腦組態檔 (Machine.config)。  
  
## <a name="example"></a>範例  
 下列範例顯示所使用的組態<xref:System.Uri>移除 http 配置的任何配置設定的類別。  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <remove name="http"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>  
 <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>  
 <xref:System.GenericUriParserOptions?displayProperty=nameWithType>  
 <xref:System.Uri?displayProperty=nameWithType>  
 [網路設定結構描述](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
