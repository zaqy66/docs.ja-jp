---
title: '方法: エンティティをシリアル化可能にします。'
ms.date: 03/30/2017
ms.assetid: a6c5bf6e-064a-4f77-b74c-76b3a5dec309
ms.openlocfilehash: 9b4ff81b4a779b474097de1a69e65f4864e08691
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604216"
---
# <a name="how-to-make-entities-serializable"></a><span data-ttu-id="1daaa-102">方法: エンティティをシリアル化可能にします。</span><span class="sxs-lookup"><span data-stu-id="1daaa-102">How to: Make Entities Serializable</span></span>
<span data-ttu-id="1daaa-103">コードを作成するときに、エンティティをシリアル化可能にできます。</span><span class="sxs-lookup"><span data-stu-id="1daaa-103">You can make entities serializable when you generate your code.</span></span> <span data-ttu-id="1daaa-104">エンティティ クラスは <xref:System.Runtime.Serialization.DataContractAttribute> 属性で装飾し、列は <xref:System.Runtime.Serialization.DataMemberAttribute> 属性で装飾します。</span><span class="sxs-lookup"><span data-stu-id="1daaa-104">Entity classes are decorated with the <xref:System.Runtime.Serialization.DataContractAttribute> attribute, and columns with the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute.</span></span>  
  
 <span data-ttu-id="1daaa-105">Visual Studio を使用して開発者が使用できる、[!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)]この目的のためです。</span><span class="sxs-lookup"><span data-stu-id="1daaa-105">Developers using Visual Studio can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] for this purpose.</span></span>  
  
 <span data-ttu-id="1daaa-106">SQLMetal コマンド ライン ツールを使用している場合は、使用、 **/serialization**オプションは、`unidirectional`引数。</span><span class="sxs-lookup"><span data-stu-id="1daaa-106">If you are using the SQLMetal command-line tool, use the **/serialization** option with the `unidirectional` argument.</span></span> <span data-ttu-id="1daaa-107">詳しくは、「[SqlMetal.exe (コード生成ツール)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="1daaa-107">For more information, see [SqlMetal.exe (Code Generation Tool)](../../../../../../docs/framework/tools/sqlmetal-exe-code-generation-tool.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1daaa-108">例</span><span class="sxs-lookup"><span data-stu-id="1daaa-108">Example</span></span>  
 <span data-ttu-id="1daaa-109">次の SQLMetal コマンド ラインでは、シリアル化可能なエンティティを持つファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="1daaa-109">The following SQLMetal command lines produce files that have serializable entities.</span></span>  
  
```  
sqlmetal /code:nwserializable.vb /language:vb "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
```  
sqlmetal /code:nwserializable.cs /language:csharp "c:\northwnd.mdf" /sprocs /functions /pluralize /serialization:unidirectional  
```  
  
## <a name="see-also"></a><span data-ttu-id="1daaa-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="1daaa-110">See also</span></span>
- [<span data-ttu-id="1daaa-111">シリアル化</span><span class="sxs-lookup"><span data-stu-id="1daaa-111">Serialization</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/serialization.md)
- [<span data-ttu-id="1daaa-112">オブジェクト モデルの作成</span><span class="sxs-lookup"><span data-stu-id="1daaa-112">Creating the Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/creating-the-object-model.md)
