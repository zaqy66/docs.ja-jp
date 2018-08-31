---
title: モデル宣言関数
ms.date: 03/30/2017
ms.assetid: aba87f13-5685-4f6b-ad14-918e8a7d5c2a
ms.openlocfilehash: f92bdfedaefca7182b5de72abae9852965d83ff7
ms.sourcegitcommit: a368166a51e5204c0224fbf5e46476e3ed122817
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2018
ms.locfileid: "43332047"
---
# <a name="model-declared-function"></a><span data-ttu-id="0a079-102">モデル宣言関数</span><span class="sxs-lookup"><span data-stu-id="0a079-102">model-declared function</span></span>
<span data-ttu-id="0a079-103">A*モデル宣言関数*が概念モデルで宣言されていますが、その概念モデルで定義されていない関数です。</span><span class="sxs-lookup"><span data-stu-id="0a079-103">A *model-declared function* is a function that is declared in a conceptual model, but is not defined in that conceptual model.</span></span> <span data-ttu-id="0a079-104">この関数は、ホスト環境またはストレージ環境で定義します。</span><span class="sxs-lookup"><span data-stu-id="0a079-104">The function might be defined in the hosting or storage environment.</span></span> <span data-ttu-id="0a079-105">たとえば、モデル宣言関数は、データベースに定義された関数にマップされ、これによって概念モデルにおけるサーバー側の機能が公開される場合があります。</span><span class="sxs-lookup"><span data-stu-id="0a079-105">For example, a model-declared function might be mapped to a function that is defined in a database, thus exposing server-side functionality in the conceptual model.</span></span>  
  
 <span data-ttu-id="0a079-106">モデル宣言関数の宣言には、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0a079-106">The declaration of a model-declared function contains the following information:</span></span>  
  
-   <span data-ttu-id="0a079-107">関数の名前。</span><span class="sxs-lookup"><span data-stu-id="0a079-107">The name of the function.</span></span> <span data-ttu-id="0a079-108">(必須)</span><span class="sxs-lookup"><span data-stu-id="0a079-108">(Required)</span></span>  
  
-   <span data-ttu-id="0a079-109">戻り値の型。</span><span class="sxs-lookup"><span data-stu-id="0a079-109">The type of the return value.</span></span> <span data-ttu-id="0a079-110">(オプション)。</span><span class="sxs-lookup"><span data-stu-id="0a079-110">(Optional)</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="0a079-111">戻り値が指定されていない場合、戻り値の型は void になります。</span><span class="sxs-lookup"><span data-stu-id="0a079-111">If no return value is specified, the return type is void.</span></span>  
  
-   <span data-ttu-id="0a079-112">パラメーター名と型を含むパラメーター情報。</span><span class="sxs-lookup"><span data-stu-id="0a079-112">Parameter information, including parameter name and type.</span></span> <span data-ttu-id="0a079-113">(オプション)。</span><span class="sxs-lookup"><span data-stu-id="0a079-113">(Optional)</span></span>  
  
## <a name="example"></a><span data-ttu-id="0a079-114">例</span><span class="sxs-lookup"><span data-stu-id="0a079-114">Example</span></span>  
 <span data-ttu-id="0a079-115">[ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md)概念スキーマ定義言語と呼ばれるドメイン固有言語 (DSL) を使用して ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 概念モデルを定義します。</span><span class="sxs-lookup"><span data-stu-id="0a079-115">The [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) to define conceptual models.</span></span> <span data-ttu-id="0a079-116">モデル宣言関数の 1 つの実装は、CSDL で、[関数インポート](https://msdn.microsoft.com/library/125704ae-56c7-4233-80b7-389a10f3a65d)します。</span><span class="sxs-lookup"><span data-stu-id="0a079-116">In CSDL, one implementation of a model-declared function is a [function import](https://msdn.microsoft.com/library/125704ae-56c7-4233-80b7-389a10f3a65d).</span></span> <span data-ttu-id="0a079-117">次の CSDL は、関数インポート定義を含むエンティティ コンテナーを定義しています。</span><span class="sxs-lookup"><span data-stu-id="0a079-117">The following CSDL defines an entity container with a function import definition.</span></span> <span data-ttu-id="0a079-118">戻り値の型が指定されていないため、関数の戻り値の型は void になります。</span><span class="sxs-lookup"><span data-stu-id="0a079-118">Note that the return type for the function is void since no return type is specified.</span></span>  
  
 [!code-xml[EDM_Example_Model#FunctionImport](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#functionimport)]  
  
## <a name="see-also"></a><span data-ttu-id="0a079-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a079-119">See Also</span></span>  
 [<span data-ttu-id="0a079-120">Entity Data Model キーの概念</span><span class="sxs-lookup"><span data-stu-id="0a079-120">Entity Data Model Key Concepts</span></span>](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)  
 [<span data-ttu-id="0a079-121">Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="0a079-121">Entity Data Model</span></span>](../../../../docs/framework/data/adonet/entity-data-model.md)
