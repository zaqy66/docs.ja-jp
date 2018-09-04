---
title: ポリモーフィック クエリを実行する方法
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2f05da1e-845b-4f14-83e4-c6353a850553
ms.openlocfilehash: ae491d0eeda7f8703dca174bdf4c5c847f78e675
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519083"
---
# <a name="how-to-execute-a-polymorphic-query"></a><span data-ttu-id="fe9f9-102">ポリモーフィック クエリを実行する方法</span><span class="sxs-lookup"><span data-stu-id="fe9f9-102">How to: Execute a Polymorphic Query</span></span>
<span data-ttu-id="fe9f9-103">このトピックでは、ポリモーフィックなを実行する方法を示しています。[!INCLUDE[esql](../../../../../includes/esql-md.md)]クエリを使用して、 [OFTYPE](../../../../../docs/framework/data/adonet/ef/language-reference/oftype-entity-sql.md)演算子。</span><span class="sxs-lookup"><span data-stu-id="fe9f9-103">This topic shows how to execute a polymorphic [!INCLUDE[esql](../../../../../includes/esql-md.md)] query using the [OFTYPE](../../../../../docs/framework/data/adonet/ef/language-reference/oftype-entity-sql.md) operator.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="fe9f9-104">この例のコードを実行するには</span><span class="sxs-lookup"><span data-stu-id="fe9f9-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="fe9f9-105">追加、 [School モデル](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac)をプロジェクトに Entity Framework を使用してプロジェクトを構成するとします。</span><span class="sxs-lookup"><span data-stu-id="fe9f9-105">Add the [School Model](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac) to your project and configure your project to use the Entity Framework.</span></span> <span data-ttu-id="fe9f9-106">詳細については、次を参照してください。[方法: Entity Data Model ウィザードを使用して、](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)します。</span><span class="sxs-lookup"><span data-stu-id="fe9f9-106">For more information, see [How to: Use the Entity Data Model Wizard](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span></span>  
  
2.  <span data-ttu-id="fe9f9-107">アプリケーションのコード ページで、次の `using` ステートメント (Visual Basic の場合は `Imports`) を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe9f9-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3.  <span data-ttu-id="fe9f9-108">次の手順に従ってテーブル-hierrachy ごとの継承を有効にして、概念モデルを変更[チュートリアル: 継承のマッピング-Table-per-hierarchy](https://msdn.microsoft.com/library/49b685cf-9db8-4d6d-b885-8837ed238f55)します。</span><span class="sxs-lookup"><span data-stu-id="fe9f9-108">Modify the conceptual model to have a table-per-hierrachy inheritance by following the steps in [Walkthrough: Mapping Inheritance - Table-per-Hierarchy](https://msdn.microsoft.com/library/49b685cf-9db8-4d6d-b885-8837ed238f55).</span></span>  
  
## <a name="example"></a><span data-ttu-id="fe9f9-109">例</span><span class="sxs-lookup"><span data-stu-id="fe9f9-109">Example</span></span>  
 <span data-ttu-id="fe9f9-110">次の例では、OFTYPE 演算子を使用し、`OnsiteCourses` のコレクションから `Courses` のコレクションだけを取得して表示します。</span><span class="sxs-lookup"><span data-stu-id="fe9f9-110">The following example uses an OFTYPE operator to get and display a collection of only `OnsiteCourses` from a collection of `Courses`.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#PolymorphicQuery](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#polymorphicquery)]
 [!code-vb[DP EntityServices Concepts#PolymorphicQuery](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#polymorphicquery)]  
  
## <a name="see-also"></a><span data-ttu-id="fe9f9-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe9f9-111">See Also</span></span>  
 [<span data-ttu-id="fe9f9-112">Entity Framework 用の EntityClient プロバイダー</span><span class="sxs-lookup"><span data-stu-id="fe9f9-112">EntityClient Provider for the Entity Framework</span></span>](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)  
 [<span data-ttu-id="fe9f9-113">Entity SQL 言語</span><span class="sxs-lookup"><span data-stu-id="fe9f9-113">Entity SQL Language</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)
