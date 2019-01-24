---
title: アソシエーション セット End
ms.date: 03/30/2017
ms.assetid: fe4bf1d3-047a-4a37-98c5-a66e70811346
ms.openlocfilehash: 9a71fd434bea87a75e259a3d5caa902fbecf8a57
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701639"
---
# <a name="association-set-end"></a><span data-ttu-id="cc311-102">アソシエーション セット End</span><span class="sxs-lookup"><span data-stu-id="cc311-102">association set end</span></span>
<span data-ttu-id="cc311-103">*アソシエーション セット end*識別、[エンティティ型](../../../../docs/framework/data/adonet/entity-type.md)と[エンティティ セット](../../../../docs/framework/data/adonet/entity-set.md)の最後に、[アソシエーション セット](../../../../docs/framework/data/adonet/association-set.md)します。</span><span class="sxs-lookup"><span data-stu-id="cc311-103">An *association set end* identifies the [entity type](../../../../docs/framework/data/adonet/entity-type.md) and the [entity set](../../../../docs/framework/data/adonet/entity-set.md) at the end of an [association set](../../../../docs/framework/data/adonet/association-set.md).</span></span> <span data-ttu-id="cc311-104">アソシエーション セット End はアソシエーション セットの一部として定義されます。アソシエーション セットには、アソシエーション セット End が 2 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="cc311-104">Association set ends are defined as part of an association set; an association set must have exactly two association set ends.</span></span>  
  
 <span data-ttu-id="cc311-105">アソシエーション セット End の定義には、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cc311-105">An association set end definition contains the following information:</span></span>  
  
-   <span data-ttu-id="cc311-106">アソシエーション セットに含まれるエンティティ型の 1 つ。</span><span class="sxs-lookup"><span data-stu-id="cc311-106">One of the entity types involved in the association set.</span></span> <span data-ttu-id="cc311-107">(必須)</span><span class="sxs-lookup"><span data-stu-id="cc311-107">(Required)</span></span>  
  
-   <span data-ttu-id="cc311-108">アソシエーション セットに含まれるエンティティ型のエンティティ セット。</span><span class="sxs-lookup"><span data-stu-id="cc311-108">The entity set for the entity type involved in the association set.</span></span> <span data-ttu-id="cc311-109">(必須)</span><span class="sxs-lookup"><span data-stu-id="cc311-109">(Required)</span></span>  
  
## <a name="example"></a><span data-ttu-id="cc311-110">例</span><span class="sxs-lookup"><span data-stu-id="cc311-110">Example</span></span>  
 <span data-ttu-id="cc311-111">下のダイアグラムは、`WrittenBy` および `PublishedBy` という 2 つのアソシエーションの概念モデルを示しています。</span><span class="sxs-lookup"><span data-stu-id="cc311-111">The diagram below shows a conceptual model with two associations: `WrittenBy` and `PublishedBy`.</span></span>  
  
 <span data-ttu-id="cc311-112">![モデルの例](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")</span><span class="sxs-lookup"><span data-stu-id="cc311-112">![Example Model](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")</span></span>  
  
 <span data-ttu-id="cc311-113">次のダイアグラムには、上の概念モデルに基づくアソシエーション セット (`PublishedBy`) と 2 つのエンティティ セット (`Books` および `Publishers`) を示しています。</span><span class="sxs-lookup"><span data-stu-id="cc311-113">The following diagram shows an association set (`PublishedBy`) and two entity sets (`Books` and `Publishers`) based on the conceptual model shown above.</span></span> <span data-ttu-id="cc311-114">アソシエーション セット End は `Books` および `Publishers` エンティティ セットです。</span><span class="sxs-lookup"><span data-stu-id="cc311-114">The association set ends are the `Books` and `Publishers` entity sets.</span></span> <span data-ttu-id="cc311-115">Bi、`Books`エンティティ セットのインスタンスを表し、`Book`実行時にエンティティ型。</span><span class="sxs-lookup"><span data-stu-id="cc311-115">Bi in the `Books` entity set represents an instance of the `Book` entity type at run time.</span></span> <span data-ttu-id="cc311-116">同様に、Pj を表す、`Publisher`インスタンス、`Publishers`エンティティ セット。</span><span class="sxs-lookup"><span data-stu-id="cc311-116">Similarly, Pj represents a `Publisher` instance in the `Publishers` entity set.</span></span> <span data-ttu-id="cc311-117">BiPj がのインスタンスを表し、`PublishedBy`のアソシエーション、`PublishedBy`アソシエーション セット。</span><span class="sxs-lookup"><span data-stu-id="cc311-117">BiPj represents an instance of the `PublishedBy` association in the `PublishedBy` association set.</span></span>  
  
 <span data-ttu-id="cc311-118">![設定例](../../../../docs/framework/data/adonet/media/setsexample.gif "SetsExample")</span><span class="sxs-lookup"><span data-stu-id="cc311-118">![Sets Example](../../../../docs/framework/data/adonet/media/setsexample.gif "SetsExample")</span></span>  
  
 <span data-ttu-id="cc311-119">[ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md)概念スキーマ定義言語と呼ばれる DSL を使用して ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 概念モデルを定義します。</span><span class="sxs-lookup"><span data-stu-id="cc311-119">The [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) uses a DSL called conceptual schema definition language ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) to define conceptual models.</span></span> <span data-ttu-id="cc311-120">次の CSDL は、上のダイアグラムの各アソシエーションに対して 1 つのアソシエーション セットを持つエンティティ コンテナーを定義しています。</span><span class="sxs-lookup"><span data-stu-id="cc311-120">The following CSDL defines an entity container with one association set for each association in the diagram above.</span></span> <span data-ttu-id="cc311-121">アソシエーション セット End はアソシエーション セット定義の一部として定義されています。</span><span class="sxs-lookup"><span data-stu-id="cc311-121">Note that association set ends are defined as part of each association set definition.</span></span>  
  
 [!code-xml[EDM_Example_Model#EntityContainerExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entitycontainerexample)]  
  
## <a name="see-also"></a><span data-ttu-id="cc311-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc311-122">See also</span></span>
- [<span data-ttu-id="cc311-123">Entity Data Model キーの概念</span><span class="sxs-lookup"><span data-stu-id="cc311-123">Entity Data Model Key Concepts</span></span>](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [<span data-ttu-id="cc311-124">Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="cc311-124">Entity Data Model</span></span>](../../../../docs/framework/data/adonet/entity-data-model.md)
