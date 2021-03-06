---
title: 如何：投影查詢結果(WCF 資料服務)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- projection [WCF Data Services]
- WCF Data Services, projection
- query projection [WCF Data Services]
- WCF Data Services, querying
ms.assetid: 474ac625-8770-43ba-8320-d3315ea9530f
ms.openlocfilehash: c1eb2618e14f0e02aa5e1a2e91aa93fe0831c7c7
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2018
ms.locfileid: "43508740"
---
# <a name="how-to-project-query-results-wcf-data-services"></a>如何：投影查詢結果(WCF 資料服務)
投影提供一種機制，可藉由指定回應中僅傳回特定實體屬性的方式降低查詢傳回的資料量。 您可以執行的結果投影[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)]查詢藉由使用`$select`查詢選項或使用[選取](~/docs/csharp/language-reference/keywords/select-clause.md)子句 ([選取](~/docs/visual-basic/language-reference/queries/select-clause.md)Visual Basic 中) 在 LINQ 查詢中。 如需詳細資訊，請參閱 <<c0> [ 查詢資料服務](../../../../docs/framework/data/wcf/querying-the-data-service-wcf-data-services.md)。  
  
 本主題中的範例使用 Northwind 範例資料服務和自動產生的用戶端資料服務類別。 當您完成建立這項服務和用戶端資料類別[WCF Data Services 快速入門](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md)。  
  
## <a name="example"></a>範例  
 下列範例顯示會將 Customers 實體投射至新的 CustomerAddress 類型之 LINQ 查詢，其中僅包含位址專用屬性加上識別屬性。 這個 `CustomerAddress` 類別已在用戶端上定義並屬性化，如此用戶端程式庫便能將它辨認為實體類型。  
  
 [!code-csharp[Astoria Northwind Client#SelectCustomerAddress](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#selectcustomeraddress)]
 [!code-vb[Astoria Northwind Client#SelectCustomerAddress](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#selectcustomeraddress)]  
  
## <a name="example"></a>範例  
 下列範例顯示會將傳回之 Customers 實體投射至新的 CustomerAddressNonEntity 類型之 LINQ 查詢，其中僅包含位址專用屬性但不包含識別屬性。 這個 `CustomerAddressNonEntity` 類別已在用戶端上定義，但並未屬性化為實體類型。  
  
 [!code-csharp[Astoria Northwind Client#SelectCustomerAddressNonEntity](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#selectcustomeraddressnonentity)]
 [!code-vb[Astoria Northwind Client#SelectCustomerAddressNonEntity](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#selectcustomeraddressnonentity)]  
  
## <a name="example"></a>範例  
 下列範例顯示的定義`CustomerAddress`和`CustomerAddressNonEntity`前一個範例中所用的類型。  
  
 [!code-csharp[Astoria Northwind Client#CustomerAddressDefinition](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/customeraddress.cs#customeraddressdefinition)]
 [!code-vb[Astoria Northwind Client#CustomerAddressDefinition](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/customeraddress.vb#customeraddressdefinition)]
