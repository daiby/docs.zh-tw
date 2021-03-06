---
title: '&lt;cryptographySettings&gt;項目'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptographySettings
helpviewer_keywords:
- cryptographySettings element
- <cryptographySettings> element
ms.assetid: 6201b7da-bcb7-49f7-b9f5-ba1fe05573b9
author: mcleblanc
ms.author: markl
ms.openlocfilehash: dc55acd7a698ef37d45e8a412db684c13a3b8b16
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2018
ms.locfileid: "48025439"
---
# <a name="ltcryptographysettingsgt-element"></a>&lt;cryptographySettings&gt;項目
包含密碼編譯設定。  
  
 \<configuration>  
\<mscorlib >  
\<cryptographySettings >  
  
## <a name="syntax"></a>語法  
  
```xml  
      <cryptographySettings>   
</cryptographySettings>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
 無。  
  
### <a name="child-elements"></a>子元素  
  
|項目|描述|  
|-------------|-----------------|  
|[\<cryptoNameMapping >](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)|包含易記名稱的類別對應。|  
|[\<oidMap >](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)|包含類別的 ASN.1 物件識別碼 (OID) 對應。|  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|`configuration`|通用語言執行平台和 .NET Framework 應用程式所使用之每個組態檔中的根項目。|  
|`mscorlib`|包含`cryptographySettings`項目。|  
  
## <a name="example"></a>範例  
 下列範例示範如何使用 **\<cryptographySettings >** 包含密碼編譯名稱對應和 OID 對應的項目。 這個範例會設定執行階段，讓<xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType>會傳回`MyHashClass`物件和`MyCryptoClass`類別會對應至物件識別元 1.3.36.2.1。  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyHash="MyHashClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="System.Security.Cryptography.HashAlgorithm"  
                       class="MyHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a>另請參閱  
 [組態檔結構描述](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [密碼編譯設定結構描述](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [密碼編譯服務](../../../../../docs/standard/security/cryptographic-services.md)
