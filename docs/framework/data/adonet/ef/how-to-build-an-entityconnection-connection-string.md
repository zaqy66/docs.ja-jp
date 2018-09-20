---
title: EntityConnection の接続文字列を作成する方法
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5bd1a748-3df7-4d0a-a607-14f25e3175e9
ms.openlocfilehash: a35a0bf54d7850e4b10e59c259e4ee512bc93aad
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2018
ms.locfileid: "45529793"
---
# <a name="how-to-build-an-entityconnection-connection-string"></a><span data-ttu-id="47394-102">EntityConnection の接続文字列を作成する方法</span><span class="sxs-lookup"><span data-stu-id="47394-102">How to: Build an EntityConnection Connection String</span></span>
<span data-ttu-id="47394-103">このトピックでは、<xref:System.Data.EntityClient.EntityConnection> を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="47394-103">This topic provides an example of how to build an <xref:System.Data.EntityClient.EntityConnection>.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="47394-104">この例のコードを実行するには</span><span class="sxs-lookup"><span data-stu-id="47394-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="47394-105">追加、 [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832)をプロジェクトに使用するプロジェクトを構成して、[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]します。</span><span class="sxs-lookup"><span data-stu-id="47394-105">Add the [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="47394-106">詳細については、次を参照してください。[方法: Entity Data Model ウィザードを使用して、](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)します。</span><span class="sxs-lookup"><span data-stu-id="47394-106">For more information, see [How to: Use the Entity Data Model Wizard](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span></span>  
  
2.  <span data-ttu-id="47394-107">アプリケーションのコード ページで、次の `using` ステートメント (Visual Basic の場合は `Imports`) を追加します。</span><span class="sxs-lookup"><span data-stu-id="47394-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="47394-108">例</span><span class="sxs-lookup"><span data-stu-id="47394-108">Example</span></span>  
 <span data-ttu-id="47394-109">次の例では、基になるプロバイダーの <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=nameWithType> を初期化した後、<xref:System.Data.EntityClient.EntityConnectionStringBuilder?displayProperty=nameWithType> オブジェクトを初期化して、このオブジェクトを <xref:System.Data.EntityClient.EntityConnection> のコンストラクターに渡しています。</span><span class="sxs-lookup"><span data-stu-id="47394-109">The following example initializes the <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=nameWithType> for the underlying provider, then initializes the <xref:System.Data.EntityClient.EntityConnectionStringBuilder?displayProperty=nameWithType> object and passes this object to the constructor of the <xref:System.Data.EntityClient.EntityConnection>.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#BuildingConnectionStringWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#buildingconnectionstringwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#BuildingConnectionStringWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#buildingconnectionstringwithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="47394-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="47394-110">See Also</span></span>  
 [<span data-ttu-id="47394-111">方法: オブジェクト コンテキストで EntityConnection を使用</span><span class="sxs-lookup"><span data-stu-id="47394-111">How to: Use EntityConnection with an Object Context</span></span>](https://msdn.microsoft.com/library/2140fe7b-b88b-47c8-a749-d7f142eb1080)  
 [<span data-ttu-id="47394-112">Entity Framework 用の EntityClient プロバイダー</span><span class="sxs-lookup"><span data-stu-id="47394-112">EntityClient Provider for the Entity Framework</span></span>](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
