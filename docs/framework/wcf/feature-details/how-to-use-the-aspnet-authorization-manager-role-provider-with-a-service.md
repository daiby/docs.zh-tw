---
title: "HOW TO：使用 ASP.NET 授權管理員角色提供者搭配服務 | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f21deb81-91ef-49ef-94d6-494785143271
caps.latest.revision: 6
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 6
---
# HOW TO：使用 ASP.NET 授權管理員角色提供者搭配服務
當 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 主控 Web 服務時，您可以將授權管理員整合至應用程式，以提供授權給服務。  授權管理員可讓應用程式開發人員定義個別作業，以便將作業分組，進而形成工作。  接著，系統管理員可以授權角色來執行特定工作或個別作業。  授權管理員會以 Microsoft Management Console \(MMC\) 嵌入式管理單元的形式提供系統管理工具，以管理角色、工作、作業和使用者。  系統管理員會在 XML 檔案、Active Directory 或「Active Directory 應用程式模式」\(ADAM\) 存放區中設定授權管理員原則存放區。  
  
 將授權管理員整合至應用程式的方式是，針對主控 Web 服務的 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 應用程式，設定授權管理員 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 角色提供者。  就像其他 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 角色提供者，授權管理員 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 角色提供者也是使用 \<`providers`\> 項目來設定。  
  
 下列程式碼範例是將授權管理員整合至應用程式之 Web 服務組態檔的一部分。  
  
```  
<system.web>  
    <roleManager enabled="true" defaultProvider="AzManRoleProvider">  
      <providers>  
        <add name="AzManRoleProvider"  
             type="System.Web.Security.AuthorizationStoreRoleProvider, System.Web, Version=2.0.0.0, Culture=neutral, publicKeyToken=b03f5f7f11d50a3a"  
             connectionStringName="AzManPolicyStoreConnectionString"   
             applicationName="SecureService"/>  
      </providers>  
    </roleManager>  
</system.web>  
```  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)] 以 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] 應用程式整合 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 角色提供者，請參閱[HOW TO：使用 ASP.NET 角色提供者搭配服務](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)。  [!INCLUDE[crabout](../../../../includes/crabout-md.md)] 搭配 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 使用授權管理員的詳細資訊，請參閱 [如何：搭配 ASP.NET 2.0 使用授權管理員 \(AzMan\)](http://go.microsoft.com/fwlink/?LinkId=71303)。  
  
## 請參閱  
 [HOW TO：使用 ASP.NET 角色提供者搭配服務](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)