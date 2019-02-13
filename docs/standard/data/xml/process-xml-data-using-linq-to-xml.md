---
title: LINQ to XML を使用した XML データの処理
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 059d6b9d-63f7-4011-9ba8-8406f0bbae7d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 26d763884cc392a08e8cef7f5321d23f1c52a7fa
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "55903514"
---
# <a name="process-xml-data-using-linq-to-xml"></a><span data-ttu-id="b6ab3-102">LINQ to XML を使用した XML データの処理</span><span class="sxs-lookup"><span data-stu-id="b6ab3-102">Process XML Data Using LINQ to XML</span></span>
<span data-ttu-id="b6ab3-103">LINQ to XML は、XML データの処理を目的とした Microsoft .NET Framework version 3.5 の新しいモデルです。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-103">LINQ to XML is the new model in the .NET Framework version 3.5 for processing XML data.</span></span> <span data-ttu-id="b6ab3-104">LINQ to XML を使用することで、XML ドキュメントのクエリ、変更、作成、保存、シリアル化など、XML データを扱う際に必要な処理をすべて実行できます。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-104">LINQ to XML allows developers to do everything they would expect with XML data: querying, modifying, creating, saving, and serializing XML documents.</span></span> <span data-ttu-id="b6ab3-105">特に、クエリと作成の機能が役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-105">The real advantages lie in the query and creation capabilities.</span></span>  
  
 <span data-ttu-id="b6ab3-106">LINQ to XML のクエリでは、XPath や XQuery よりも SQL に類似した構文が使用され、簡潔で表現力に優れています。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-106">Queries in LINQ to XML are succinct and expressive, using syntax more similar to SQL than to XPath or XQuery.</span></span> <span data-ttu-id="b6ab3-107">クエリの結果を要素や属性のコレクションとして返すことができ、XElement オブジェクトのパラメーターとして使用できるため、XML ツリーの形を簡単に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-107">Because query results can be returned as collections of elements or attributes and can be used as parameters for XElement objects, XML trees can be easily transformed from one shape to another.</span></span>  
  
 <span data-ttu-id="b6ab3-108">LINQ to XML では、.NET Framework version 3.5 の統合言語クエリ (LINQ) テクノロジを利用しています。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-108">LINQ to XML leverages the language-integrated query (LINQ) technology in the .NET Framework version 3.5.</span></span> <span data-ttu-id="b6ab3-109">LINQ は C# および Visual Basic の言語構文を拡張したもので、潜在的には任意のデータ ストアまで拡張できる強力なクエリ機能を備えています。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-109">LINQ extends the language syntax of C# and Visual Basic to provide powerful query capabilities that can be extended to potentially any data store.</span></span>  
  
 <span data-ttu-id="b6ab3-110">その使用方法については、「[LINQ to XML](https://msdn.microsoft.com/library/f0fe21e9-ee43-4a55-b91a-0800e5782c13)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-110">For a detailed discussion of its use, see [LINQ to XML](https://msdn.microsoft.com/library/f0fe21e9-ee43-4a55-b91a-0800e5782c13).</span></span> <span data-ttu-id="b6ab3-111">LINQ フレームワークの概要については、「[統合言語クエリ (LINQ) - C#](../../../csharp/programming-guide/concepts/linq/index.md)」または「[統合言語クエリ (LINQ) - Visual Basic](../../../visual-basic/programming-guide/concepts/linq/index.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6ab3-111">For an overview of the LINQ framework, see [Language-Integrated Query (LINQ) - C#](../../../csharp/programming-guide/concepts/linq/index.md) or [Language-Integrated Query (LINQ) - Visual Basic](../../../visual-basic/programming-guide/concepts/linq/index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6ab3-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6ab3-112">See also</span></span>

- <xref:System.Xml.Linq>
- <xref:System.Linq>
- [<span data-ttu-id="b6ab3-113">LINQ to XML とDOM</span><span class="sxs-lookup"><span data-stu-id="b6ab3-113">LINQ to XML vs. DOM</span></span>](https://msdn.microsoft.com/library/19b5ed02-feb2-455a-8897-f7f0fd76aca3)
- [<span data-ttu-id="b6ab3-114">LINQ to XML とその他の XML テクノロジ</span><span class="sxs-lookup"><span data-stu-id="b6ab3-114">LINQ to XML vs. Other XML Technologies</span></span>](https://msdn.microsoft.com/library/7ba1eecf-f09a-42de-bc80-22ca5b2e42d3)
