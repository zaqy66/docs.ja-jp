---
title: コレクション初期化子を使用してディクショナリを初期化する方法 (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [C#], with Dictionary
ms.assetid: 25283922-f8ee-40dc-a639-fac30804ec71
ms.openlocfilehash: ca2f508e5500cc135b2712362bcfb71778a664c1
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44227338"
---
# <a name="how-to-initialize-a-dictionary-with-a-collection-initializer-c-programming-guide"></a>コレクション初期化子を使用してディクショナリを初期化する方法 (C# プログラミング ガイド)

<xref:System.Collections.Generic.Dictionary%602> にはキーと値のペアのコレクションが含まれています。 その <xref:System.Collections.Generic.Dictionary%602.Add*> メソッドは、それぞれキーと値に対する 2 つのパラメーターを受け取ります。 `Add` メソッドが複数のパラメーターを受け取る <xref:System.Collections.Generic.Dictionary%602> またはコレクションを初期化するには、次の例に示すように、各パラメーターのセットを中かっこで囲みます。

## <a name="example"></a>例

次のコード例では、<xref:System.Collections.Generic.Dictionary%602> が型 `StudentName` のインスタンスで初期化されています。  
  
[!code-csharp[csProgGuideLINQ#34](../../../csharp/programming-guide/arrays/codesnippet/CSharp/how-to-initialize-a-dictionary-with-a-collection-initializer_1.cs)]

コレクションの各要素の中かっこの 2 つのペアに注目してください。 最も内側の中かっこは `StudentName` のオブジェクト初期化子を囲み、最も外側の中かっこは、`students` <xref:System.Collections.Generic.Dictionary%602> に追加されるキーと値のペアの初期化子を囲んでいます。 最後に、ディクショナリのコレクション初期化子全体が中かっこで囲まれています。

## <a name="compiling-the-code"></a>コードのコンパイル

このコードを実行するには、クラスをコピーし、Visual Studio で作成した Visual C# コンソール アプリケーション プロジェクトに貼り付けます。 既定では、このプロジェクトは、[!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] のバージョン 3.5 を対象としており、System.Core.dll への参照と System.Linq の using ディレクティブが含まれます。 これらの要件のうち 1 つまたは複数を満たしていないプロジェクトの場合は、手動で追加することができます。

## <a name="see-also"></a>関連項目

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)
- [オブジェクト初期化子とコレクション初期化子](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)
