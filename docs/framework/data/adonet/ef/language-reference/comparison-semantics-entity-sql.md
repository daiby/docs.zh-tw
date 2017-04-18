---
title: "比較語意 (Entity SQL) | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-ado"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
ms.assetid: b36ce28a-2fe4-4236-b782-e5f7c054deae
caps.latest.revision: 2
author: "JennieHubbard"
ms.author: "jhubbard"
manager: "jhubbard"
caps.handback.revision: 2
---
# 比較語意 (Entity SQL)
執行以下任何 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 運算子都會牽涉到型別執行個體的比較：  
  
## 明確比較  
 相等運算：  
  
-   \=  
  
-   \!\=  
  
 排序作業：  
  
-   \<  
  
-   \<\=  
  
-   \>  
  
-   \>\=  
  
 可為 Null 的運算：  
  
-   IS NULL  
  
-   IS NOT NULL  
  
## 明確區分  
 相等區分：  
  
-   DISTINCT  
  
-   GROUP BY  
  
 排序區分：  
  
-   ORDER BY  
  
## 隱含區分  
 Set 作業和述詞 \(相等\)：  
  
-   UNION  
  
-   INTERSECT  
  
-   EXCEPT  
  
-   SET  
  
-   OVERLAPS  
  
 Item 述詞 \(相等\)：  
  
-   IN  
  
## 支援的組合  
 以下資料表針對每一種型別顯示比較運算子的所有支援組合：  
  
|||||||||  
|-|-|-|-|-|-|-|-|  
|**類型**|**\=**<br /><br /> **\!\=**|**GROUP BY**<br /><br /> **DISTINCT**|**UNION**<br /><br /> **INTERSECT**<br /><br /> **EXCEPT**<br /><br /> **SET**<br /><br /> **OVERLAPS**|**IN**|**\<   \<\=**<br /><br /> **\>   \>\=**|**ORDER BY**|**IS NULL**<br /><br /> **IS NOT NULL**|  
|實體類型|參考<sup>1</sup>|所有屬性<sup>2</sup>|所有屬性<sup>2</sup>|所有屬性<sup>2</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|參考<sup>1</sup>|  
|複雜類型|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|  
|表格列|所有屬性<sup>4</sup>|所有屬性<sup>4</sup>|所有屬性<sup>4</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|所有屬性<sup>4</sup>|擲回<sup>3</sup>|  
|基本型別|提供者特定|提供者特定|提供者特定|提供者特定|提供者特定|提供者特定|提供者特定|  
|多重集|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|  
|參考|是 <sup>5</sup>|是 <sup>5</sup>|是 <sup>5</sup>|是 <sup>5</sup>|Throw|Throw|是 <sup>5</sup>|  
|關聯<br /><br /> 類型|擲回<sup>3</sup>|Throw|Throw|Throw|擲回<sup>3</sup>|擲回<sup>3</sup>|擲回<sup>3</sup>|  
  
 <sup>1</sup>給定實體類型執行個體的參考會以隱含的方式比較，如下列範例所示：  
  
```  
SELECT p1, p2   
FROM AdventureWorksEntities.Product AS p1   
     JOIN AdventureWorksEntities.Product AS p2   
WHERE p1 != p2 OR p1 IS NULL  
```  
  
 實體執行個體無法與明確參考相比較。  如果嘗試進行此作業，就會擲回例外狀況。  例如，下列查詢將會擲回例外狀況：  
  
```  
SELECT p1, p2   
FROM AdventureWorksEntities.Product AS p1   
     JOIN AdventureWorksEntities.Product AS p2   
WHERE p1 != REF(p2)  
```  
  
 <sup>2</sup>複雜類型的屬性會先簡維，然後再送到存放區，以便可加以比較 \(只要其所有屬性都可以比較即可\)。  請參閱 <sup>4</sup>。  
  
 <sup>3</sup>Entity Framework 執行階段會偵測到不支援的案例，並擲回有意義的例外狀況，而不會佔用提供者\/存放區。  
  
 <sup>4</sup>嘗試比較所有的屬性。  如果某個屬性具有無法比較的型別 \(如文字、ntext 或影像\)，可能會擲回伺服器例外狀況。  
  
 <sup>5</sup>參考的所有個別項目都會比較 \(這包括實體集名稱及實體類型的所有 Key 屬性\)。  
  
## 請參閱  
 [Entity SQL 概觀](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)