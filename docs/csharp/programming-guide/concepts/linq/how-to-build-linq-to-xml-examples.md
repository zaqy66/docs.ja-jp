---
title: '方法: LINQ to XML の例をビルドする (C#)'
ms.date: 07/20/2015
ms.assetid: e5d18fa1-2704-48fe-a44b-1564f97c9e9c
ms.openlocfilehash: da0d85db22de6bcb2038cbe0608983d39bd66383
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44176677"
---
# <a name="how-to-build-linq-to-xml-examples-c"></a><span data-ttu-id="25f4a-102">方法: LINQ to XML の例をビルドする (C#)</span><span class="sxs-lookup"><span data-stu-id="25f4a-102">How to: Build LINQ to XML Examples (C#)</span></span>
<span data-ttu-id="25f4a-103">このドキュメントに含まれている各種のスニペットおよびコード例では、さまざまな名前空間のクラスと型が使用されます。</span><span class="sxs-lookup"><span data-stu-id="25f4a-103">The various snippets and examples in this documentation use classes and types from a variety of namespaces.</span></span> <span data-ttu-id="25f4a-104">C# のコードをコンパイルする場合は、適切な `using` ディレクティブを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25f4a-104">When compiling C# code, you need to supply appropriate `using` directives.</span></span>  
  
## <a name="example"></a><span data-ttu-id="25f4a-105">例</span><span class="sxs-lookup"><span data-stu-id="25f4a-105">Example</span></span>  
 <span data-ttu-id="25f4a-106">次のコードには、C# のコード例をビルドおよび実行するために必要な `using` ディレクティブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="25f4a-106">The following code contains the `using` directives that the C# examples require to build and run.</span></span> <span data-ttu-id="25f4a-107">すべての `using` ディレクティブがすべてのコード例で必要になるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="25f4a-107">Not all `using` directives are required for every example.</span></span>  
  
```csharp  
using System;  
using System.Diagnostics;  
using System.Collections;  
using System.Collections.Generic;  
using System.Collections.Specialized;  
using System.Text;  
using System.Linq;  
using System.Xml;  
using System.Xml.Linq;  
using System.Xml.Schema;  
using System.Xml.XPath;  
using System.Xml.Xsl;  
using System.IO;  
using System.Threading;  
using System.Reflection;  
using System.IO.Packaging;  
```  
  
## <a name="see-also"></a><span data-ttu-id="25f4a-108">参照</span><span class="sxs-lookup"><span data-stu-id="25f4a-108">See Also</span></span>

- [<span data-ttu-id="25f4a-109">LINQ to XML プログラミングの概要 (C#)</span><span class="sxs-lookup"><span data-stu-id="25f4a-109">LINQ to XML Programming Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-programming-overview.md)
