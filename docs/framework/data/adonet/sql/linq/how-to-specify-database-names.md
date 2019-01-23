---
title: '方法: データベース名を指定します。'
ms.date: 03/30/2017
ms.assetid: b80f0fd2-7f75-45fe-9e12-496f80f183df
ms.openlocfilehash: a1198a294cd4921728919981bae213c0ee891da6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54556376"
---
# <a name="how-to-specify-database-names"></a><span data-ttu-id="3509c-102">方法: データベース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="3509c-102">How to: Specify Database Names</span></span>
<span data-ttu-id="3509c-103"><xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> 属性の <xref:System.Data.Linq.Mapping.DatabaseAttribute> プロパティを使用すると、接続によってデータベースの名前が提供されない場合に、名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3509c-103">Use the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property on a <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute to specify the name of a database when a name is not supplied by the connection.</span></span>  
  
 <span data-ttu-id="3509c-104">コード例については、「<xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3509c-104">For code samples, see <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A>.</span></span>  
  
### <a name="to-specify-the-name-of-the-database"></a><span data-ttu-id="3509c-105">データベースの名前を指定するには</span><span class="sxs-lookup"><span data-stu-id="3509c-105">To specify the name of the database</span></span>  
  
1.  <span data-ttu-id="3509c-106">データベースのクラス宣言に <xref:System.Data.Linq.Mapping.DatabaseAttribute> 属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="3509c-106">Add the <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute to the class declaration for the database.</span></span>  
  
2.  <span data-ttu-id="3509c-107"><xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> 属性に <xref:System.Data.Linq.Mapping.DatabaseAttribute> プロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="3509c-107">Add the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property to the <xref:System.Data.Linq.Mapping.DatabaseAttribute> attribute.</span></span>  
  
3.  <span data-ttu-id="3509c-108"><xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> プロパティ値を目的の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="3509c-108">Set the <xref:System.Data.Linq.Mapping.DatabaseAttribute.Name%2A> property value to the name that you want to specify.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3509c-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="3509c-109">See also</span></span>
- [<span data-ttu-id="3509c-110">LINQ to SQL オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="3509c-110">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [<span data-ttu-id="3509c-111">方法: コード エディターを使用してエンティティ クラスをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="3509c-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
