---
title: DataView
ms.date: 03/30/2017
ms.assetid: 0fe5dfa2-c1cd-435f-90b6-b4dd2e3ef34b
ms.openlocfilehash: 75719e91daba189c1d93491a1db26acc80100bea
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43514753"
---
# <a name="dataviews"></a><span data-ttu-id="a9c80-102">DataView</span><span class="sxs-lookup"><span data-stu-id="a9c80-102">DataViews</span></span>
<span data-ttu-id="a9c80-103"><xref:System.Data.DataView> では、<xref:System.Data.DataTable> に格納されているデータのさまざまなビューを作成できます。この機能は、データ連結アプリケーションで頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9c80-103">A <xref:System.Data.DataView> enables you to create different views of the data stored in a <xref:System.Data.DataTable>, a capability that is often used in data-binding applications.</span></span> <span data-ttu-id="a9c80-104">使用して、 **DataView**、さまざまな並べ替え順序、テーブル内のデータを公開して、によって行の状態やフィルター式に基づいてデータをフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="a9c80-104">Using a **DataView**, you can expose the data in a table with different sort orders, and you can filter the data by row state or based on a filter expression.</span></span>  
  
 <span data-ttu-id="a9c80-105">A **DataView** 、基になるデータの動的なビューを提供します。 **DataTable**: コンテンツ、並べ替え、およびメンバーシップ発生時に変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-105">A **DataView** provides a dynamic view of data in the underlying **DataTable**: the content, ordering, and membership reflect changes as they occur.</span></span> <span data-ttu-id="a9c80-106">この動作は異なります、**選択**のメソッド、 **DataTable**、返された、<xref:System.Data.DataRow>特定のフィルターまたは並べ替え順序に基づいて、テーブルからの配列: thiscontent への変更が反映されます、テーブルが、メンバーシップを基になると、順序付けは、静的なままです。</span><span class="sxs-lookup"><span data-stu-id="a9c80-106">This behavior differs from the **Select** method of the **DataTable**, which returns a <xref:System.Data.DataRow> array from a table based on a particular filter and/or sort order: thiscontent reflects changes to the underlying table, but its membership and ordering remain static.</span></span> <span data-ttu-id="a9c80-107">動的機能、 **DataView**データ バインド アプリケーションに最適です。</span><span class="sxs-lookup"><span data-stu-id="a9c80-107">The dynamic capabilities of the **DataView** make it ideal for data-binding applications.</span></span>  
  
 <span data-ttu-id="a9c80-108">A **DataView**では、さまざまな並べ替えやフィルター処理条件を適用できる、データベース ビューと同様に、データの 1 つのセットの動的な表示。</span><span class="sxs-lookup"><span data-stu-id="a9c80-108">A **DataView** provides you with a dynamic view of a single set of data, much like a database view, to which you can apply different sorting and filtering criteria.</span></span> <span data-ttu-id="a9c80-109">ただし、データベース ビューとは異なり、 **DataView**テーブルとして扱うことはできませんし、結合テーブルのビューを提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="a9c80-109">Unlike a database view, however, a **DataView** cannot be treated as a table and cannot provide a view of joined tables.</span></span> <span data-ttu-id="a9c80-110">また、ソース テーブルの既存の列を除外したり、ソース テーブルにない列 (計算列など) を追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="a9c80-110">You also cannot exclude columns that exist in the source table, nor can you append columns, such as computational columns, that do not exist in the source table.</span></span>  
  
 <span data-ttu-id="a9c80-111">使用することができます、<xref:System.Data.DataView.DataViewManager%2A>内のすべてのテーブルの表示設定を管理する、**データセット**します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-111">You can use a <xref:System.Data.DataView.DataViewManager%2A> to manage view settings for all the tables in a **DataSet**.</span></span> <span data-ttu-id="a9c80-112">**DataViewManager**の各テーブルの既定のビュー設定を管理する便利な方法です。</span><span class="sxs-lookup"><span data-stu-id="a9c80-112">The **DataViewManager** provides you with a convenient way to manage default view settings for each table.</span></span> <span data-ttu-id="a9c80-113">1 つ以上のテーブルにコントロールをバインドするときに、**データセット**連結する、 **DataViewManager**は理想的な選択肢です。</span><span class="sxs-lookup"><span data-stu-id="a9c80-113">When binding a control to more than one table of a **DataSet**, binding to a **DataViewManager** is the ideal choice.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="a9c80-114">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="a9c80-114">In This Section</span></span>  
 [<span data-ttu-id="a9c80-115">DataView の作成</span><span class="sxs-lookup"><span data-stu-id="a9c80-115">Creating a DataView</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/creating-a-dataview.md)  
 <span data-ttu-id="a9c80-116">作成する方法について説明します、 **DataView**の**DataTable**します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-116">Describes how to create a **DataView** for a **DataTable**.</span></span>  
  
 [<span data-ttu-id="a9c80-117">データの並べ替えとフィルター処理</span><span class="sxs-lookup"><span data-stu-id="a9c80-117">Sorting and Filtering Data</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/sorting-and-filtering-data.md)  
 <span data-ttu-id="a9c80-118">プロパティを設定する方法について説明します、 **DataView**特定のフィルター条件を満たす、データ行のサブセットを返すか、特定の並べ替え順序でデータを返します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-118">Describes how to set the properties of a **DataView** to return subsets of data rows meeting specific filter criteria, or to return data in a particular sort order.</span></span>  
  
 [<span data-ttu-id="a9c80-119">DataRow および DataRowView</span><span class="sxs-lookup"><span data-stu-id="a9c80-119">DataRows and DataRowViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datarows-and-datarowviews.md)  
 <span data-ttu-id="a9c80-120">によって公開されているデータにアクセスする方法について説明します、 **DataView**します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-120">Describes how to access the data exposed by the **DataView**.</span></span>  
  
 [<span data-ttu-id="a9c80-121">行の検索</span><span class="sxs-lookup"><span data-stu-id="a9c80-121">Finding Rows</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/finding-rows.md)  
 <span data-ttu-id="a9c80-122">特定の行を検索する方法について説明します、 **DataView**します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-122">Describes how to find a particular row in a **DataView**.</span></span>  
  
 [<span data-ttu-id="a9c80-123">ChildView とリレーション</span><span class="sxs-lookup"><span data-stu-id="a9c80-123">ChildViews and Relations</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/childviews-and-relations.md)  
 <span data-ttu-id="a9c80-124">使用して、親子リレーションシップからデータのビューを作成する方法について説明します、 **DataView**します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-124">Describes how to create views of data from a parent-child relationship using a **DataView**.</span></span>  
  
 [<span data-ttu-id="a9c80-125">DataView の変更</span><span class="sxs-lookup"><span data-stu-id="a9c80-125">Modifying DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/modifying-dataviews.md)  
 <span data-ttu-id="a9c80-126">基になるデータを変更する方法について説明します**DataTable**を使用して、 **DataView**などを有効にするまたは更新プログラムを無効にします。</span><span class="sxs-lookup"><span data-stu-id="a9c80-126">Describes how to modify the data in the underlying **DataTable** via the **DataView**, including enabling or disabling updates.</span></span>  
  
 [<span data-ttu-id="a9c80-127">DataView イベントの処理</span><span class="sxs-lookup"><span data-stu-id="a9c80-127">Handling DataView Events</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/handling-dataview-events.md)  
 <span data-ttu-id="a9c80-128">使用する方法について説明します、 **ListChanged**イベント通知を受信するときに内容またはの順序を**DataView**が更新されています。</span><span class="sxs-lookup"><span data-stu-id="a9c80-128">Describes how to use the **ListChanged** event to receive notification when the contents or order of a **DataView** is being updated.</span></span>  
  
 [<span data-ttu-id="a9c80-129">DataViews の管理</span><span class="sxs-lookup"><span data-stu-id="a9c80-129">Managing DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/managing-dataviews.md)  
 <span data-ttu-id="a9c80-130">使用する方法について説明します、 **DataViewManager**を管理する**DataView**内の各テーブルの設定、**データセット**します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-130">Describes how to use a **DataViewManager** to manage **DataView** settings for each table in a **DataSet**.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="a9c80-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9c80-131">Related Sections</span></span>  
 [<span data-ttu-id="a9c80-132">ASP.NET Web アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a9c80-132">ASP.NET Web Applications</span></span>](https://msdn.microsoft.com/library/a812d7b7-049e-4234-a4c2-6acf690301f6)  
 <span data-ttu-id="a9c80-133">ASP.NET アプリケーション、Web フォームおよび Web サービスを作成する場合の概要と詳細なステップごとの手順を示します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-133">Provides overviews and detailed, step-by-step procedures for creating ASP.NET applications, Web Forms, and Web Services.</span></span>  
  
 [<span data-ttu-id="a9c80-134">Windows アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a9c80-134">Windows Applications</span></span>](https://msdn.microsoft.com/library/a6bb2180-09b1-4738-b9fd-7fb05fc92f23)  
 <span data-ttu-id="a9c80-135">Windows フォームおよびコンソール アプリケーションの操作に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-135">Provides detailed information about working with Windows Forms and console applications.</span></span>  
  
 [<span data-ttu-id="a9c80-136">DataSet、DataTable、および DataView</span><span class="sxs-lookup"><span data-stu-id="a9c80-136">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 <span data-ttu-id="a9c80-137">について説明します、**データセット**オブジェクトと使用してアプリケーション データを管理する方法。</span><span class="sxs-lookup"><span data-stu-id="a9c80-137">Describes the **DataSet** object and how you can use it to manage application data.</span></span>  
  
 [<span data-ttu-id="a9c80-138">DataTables</span><span class="sxs-lookup"><span data-stu-id="a9c80-138">DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)  
 <span data-ttu-id="a9c80-139">について説明します、 **DataTable**オブジェクトと使用して単独でまたはの一部としてアプリケーション データを管理する方法、**データセット**します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-139">Describes the **DataTable** object and how you can use it to manage application data by itself or as part of a **DataSet**.</span></span>  
  
 [<span data-ttu-id="a9c80-140">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="a9c80-140">ADO.NET</span></span>](../../../../../docs/framework/data/adonet/index.md)  
 <span data-ttu-id="a9c80-141">ADO.NET のアーキテクチャとコンポーネントについて説明し、ADO.NET を使用して既存のデータ ソースにアクセスしたり、アプリケーション データを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9c80-141">Describes the ADO.NET architecture and components, and how to use ADO.NET to access existing data sources and manage application data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9c80-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9c80-142">See Also</span></span>  
 [<span data-ttu-id="a9c80-143">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="a9c80-143">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
