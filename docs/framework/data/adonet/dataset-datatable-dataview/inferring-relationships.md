---
title: リレーションシップの推論
ms.date: 03/30/2017
ms.assetid: 8fa86a9d-6545-4a9d-b1f5-58d9742179c7
ms.openlocfilehash: 2d25160b8dae8b8dc883abb589551782925ca325
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536283"
---
# <a name="inferring-relationships"></a><span data-ttu-id="6dc43-102">リレーションシップの推論</span><span class="sxs-lookup"><span data-stu-id="6dc43-102">Inferring Relationships</span></span>
<span data-ttu-id="6dc43-103">テーブルとして推論される要素に、同じくテーブルとして推論される子の要素が含まれている場合には、2 つのテーブル間に <xref:System.Data.DataRelation> が作成されます。</span><span class="sxs-lookup"><span data-stu-id="6dc43-103">If an element that is inferred as a table has a child element that is also inferred as a table, a <xref:System.Data.DataRelation> will be created between the two tables.</span></span> <span data-ttu-id="6dc43-104">新しい列の名前を持つ**ParentTableName_Id**親要素に対して作成されたテーブルと子要素に対して作成されたテーブルの両方に追加されます。</span><span class="sxs-lookup"><span data-stu-id="6dc43-104">A new column with a name of **ParentTableName_Id** will be added to both the table created for the parent element, and the table created for the child element.</span></span> <span data-ttu-id="6dc43-105">**ColumnMapping**この id 列のプロパティに設定する**MappingType.Hidden**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-105">The **ColumnMapping** property of this identity column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="6dc43-106">列の場合は、親テーブルの自動インクリメントのプライマリ キーとに使用される、 **DataRelation** 2 つのテーブル。</span><span class="sxs-lookup"><span data-stu-id="6dc43-106">The column will be an auto-incrementing primary key for the parent table, and will be used for the **DataRelation** between the two tables.</span></span> <span data-ttu-id="6dc43-107">追加される id 列のデータ型になります**System.Int32**、これは他のすべての推論された列のデータ型とは異なり**System.String**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-107">The data type of the added identity column will be **System.Int32**, unlike the data type of all other inferred columns, which is **System.String**.</span></span> <span data-ttu-id="6dc43-108">A<xref:System.Data.ForeignKeyConstraint>で**DeleteRule** = **Cascade**親と子の両方のテーブルに新しい列を使用しても作成されます。</span><span class="sxs-lookup"><span data-stu-id="6dc43-108">A <xref:System.Data.ForeignKeyConstraint> with **DeleteRule** = **Cascade** will also be created using the new column in both the parent and child tables.</span></span>  
  
 <span data-ttu-id="6dc43-109">たとえば、次のような XML があるとします。</span><span class="sxs-lookup"><span data-stu-id="6dc43-109">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1 attr1="value1" attr2="value2"/>  
    <ChildElement2>Text2</ChildElement2>  
  </Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="6dc43-110">推論プロセスでは、2 つのテーブルを生成します。**Element1**と**ChildElement1**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-110">The inference process will produce two tables: **Element1** and **ChildElement1**.</span></span>  
  
 <span data-ttu-id="6dc43-111">**Element1**テーブルが 2 つの列が必要があります。**Element1_Id**と**ChildElement2**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-111">The **Element1** table will have two columns: **Element1_Id** and **ChildElement2**.</span></span> <span data-ttu-id="6dc43-112">**ColumnMapping**のプロパティ、 **Element1_Id**列に設定する**MappingType.Hidden**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-112">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="6dc43-113">**ColumnMapping**のプロパティ、 **ChildElement2**列に設定する**MappingType.Element**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-113">The **ColumnMapping** property of the **ChildElement2** column will be set to **MappingType.Element**.</span></span> <span data-ttu-id="6dc43-114">**Element1_Id**としての主キー列が設定されます、 **Element1**テーブル。</span><span class="sxs-lookup"><span data-stu-id="6dc43-114">The **Element1_Id** column will be set as the primary key of the **Element1** table.</span></span>  
  
 <span data-ttu-id="6dc43-115">**ChildElement1**テーブルは 3 つの列になります: **attr1**、 **attr2**と**Element1_Id**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-115">The **ChildElement1** table will have three columns: **attr1**, **attr2** and **Element1_Id**.</span></span> <span data-ttu-id="6dc43-116">**ColumnMapping**プロパティを**attr1**と**attr2**列を設定することは**MappingType.Attribute**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-116">The **ColumnMapping** property for the **attr1** and **attr2** columns will be set to **MappingType.Attribute**.</span></span> <span data-ttu-id="6dc43-117">**ColumnMapping**のプロパティ、 **Element1_Id**列に設定する**MappingType.Hidden**します。</span><span class="sxs-lookup"><span data-stu-id="6dc43-117">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span>  
  
 <span data-ttu-id="6dc43-118">A **DataRelation**と**ForeignKeyConstraint**を使用して作成は、 **Element1_Id**両方のテーブルの列。</span><span class="sxs-lookup"><span data-stu-id="6dc43-118">A **DataRelation** and **ForeignKeyConstraint** will be created using the **Element1_Id** columns from both tables.</span></span>  
  
 <span data-ttu-id="6dc43-119">**データセット:** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="6dc43-119">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="6dc43-120">**テーブル:** Element1</span><span class="sxs-lookup"><span data-stu-id="6dc43-120">**Table:** Element1</span></span>  
  
|<span data-ttu-id="6dc43-121">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="6dc43-121">Element1_Id</span></span>|<span data-ttu-id="6dc43-122">ChildElement2</span><span class="sxs-lookup"><span data-stu-id="6dc43-122">ChildElement2</span></span>|  
|------------------|-------------------|  
|<span data-ttu-id="6dc43-123">0</span><span class="sxs-lookup"><span data-stu-id="6dc43-123">0</span></span>|<span data-ttu-id="6dc43-124">Text2</span><span class="sxs-lookup"><span data-stu-id="6dc43-124">Text2</span></span>|  
  
 <span data-ttu-id="6dc43-125">**テーブル:** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="6dc43-125">**Table:** ChildElement1</span></span>  
  
|<span data-ttu-id="6dc43-126">attr1</span><span class="sxs-lookup"><span data-stu-id="6dc43-126">attr1</span></span>|<span data-ttu-id="6dc43-127">attr2</span><span class="sxs-lookup"><span data-stu-id="6dc43-127">attr2</span></span>|<span data-ttu-id="6dc43-128">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="6dc43-128">Element1_Id</span></span>|  
|-----------|-----------|------------------|  
|<span data-ttu-id="6dc43-129">value1</span><span class="sxs-lookup"><span data-stu-id="6dc43-129">value1</span></span>|<span data-ttu-id="6dc43-130">value2</span><span class="sxs-lookup"><span data-stu-id="6dc43-130">value2</span></span>|<span data-ttu-id="6dc43-131">0</span><span class="sxs-lookup"><span data-stu-id="6dc43-131">0</span></span>|  
  
 <span data-ttu-id="6dc43-132">**DataRelation:** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="6dc43-132">**DataRelation:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="6dc43-133">**ParentTable:** Element1</span><span class="sxs-lookup"><span data-stu-id="6dc43-133">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="6dc43-134">**ParentColumn:** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="6dc43-134">**ParentColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="6dc43-135">**ChildTable:** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="6dc43-135">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="6dc43-136">**ChildColumn:** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="6dc43-136">**ChildColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="6dc43-137">**入れ子になった。** True</span><span class="sxs-lookup"><span data-stu-id="6dc43-137">**Nested:** True</span></span>  
  
 <span data-ttu-id="6dc43-138">**ForeignKeyConstraint:** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="6dc43-138">**ForeignKeyConstraint:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="6dc43-139">**列:** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="6dc43-139">**Column:** Element1_Id</span></span>  
  
 <span data-ttu-id="6dc43-140">**ParentTable:** Element1</span><span class="sxs-lookup"><span data-stu-id="6dc43-140">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="6dc43-141">**ChildTable:** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="6dc43-141">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="6dc43-142">**DeleteRule:** Cascade</span><span class="sxs-lookup"><span data-stu-id="6dc43-142">**DeleteRule:** Cascade</span></span>  
  
 <span data-ttu-id="6dc43-143">**AcceptRejectRule:** なし</span><span class="sxs-lookup"><span data-stu-id="6dc43-143">**AcceptRejectRule:** None</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6dc43-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="6dc43-144">See also</span></span>
- [<span data-ttu-id="6dc43-145">XML からの DataSet リレーショナル構造の推論</span><span class="sxs-lookup"><span data-stu-id="6dc43-145">Inferring DataSet Relational Structure from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="6dc43-146">XML からの DataSet の読み込み</span><span class="sxs-lookup"><span data-stu-id="6dc43-146">Loading a DataSet from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [<span data-ttu-id="6dc43-147">XML の DataSet スキーマ情報の読み込み</span><span class="sxs-lookup"><span data-stu-id="6dc43-147">Loading DataSet Schema Information from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="6dc43-148">DataRelation の入れ子化</span><span class="sxs-lookup"><span data-stu-id="6dc43-148">Nesting DataRelations</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/nesting-datarelations.md)
- [<span data-ttu-id="6dc43-149">DataSet での XML の使用</span><span class="sxs-lookup"><span data-stu-id="6dc43-149">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [<span data-ttu-id="6dc43-150">DataSet、DataTable、および DataView</span><span class="sxs-lookup"><span data-stu-id="6dc43-150">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="6dc43-151">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="6dc43-151">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
