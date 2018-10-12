---
title: 相互運用性 (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- COM interop
- interoperability
- platform invoke, accessing APIs with C#
- C# language, interoperability
ms.assetid: 238bb95a-e962-4026-bbd5-197055bdb8ee
ms.openlocfilehash: f1befaf6fe5b553f8049385b95a9f541cf0d57a7
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43506125"
---
# <a name="interoperability-c-programming-guide"></a>相互運用性 (C# プログラミング ガイド)
相互運用性は、アンマネージ コードへの既存の投資を保持して活用できるようにします。 共通言語ランタイム (CLR) の制御下で実行されるコードは*マネージド コード*と呼ばれ、CLR の外部で実行されるコードは*アンマネージド コード*と呼ばれます。 アンマネージ コードの例は、COM、COM +、C++ コンポーネント、ActiveX コンポーネント、および Microsoft Win32 API です。  
  
 [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] では、プラットフォーム呼び出しサービス、<xref:System.Runtime.InteropServices> 名前空間、C++ 相互運用性、および COM 相互運用性 (COM 相互運用機能) を通して、アンマネージ コードの相互運用を可能にしています。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [相互運用性の概要](../../../csharp/programming-guide/interop/interoperability-overview.md)  
 C# のマネージド コードとアンマネージド コードの間で相互運用する方法について説明します。  
  
 [方法: Visual C# の機能を使用して Office 相互運用オブジェクトにアクセスする](../../../csharp/programming-guide/interop/how-to-access-office-onterop-objects.md)  
 Office のプログラミングを容易にするために Visual C# に導入されている機能について説明します。  
  
 [方法: COM 相互運用機能を使用したプログラミングでインデックス付きプロパティを使用する](../../../csharp/programming-guide/interop/how-to-use-indexed-properties-in-com-interop-rogramming.md)  
 インデックス付きプロパティを使用して、パラメーターを持つ COM プロパティにアクセスする方法について説明します。  
  
 [方法: プラットフォーム呼び出しを使用して Wave ファイルを再生する](../../../csharp/programming-guide/interop/how-to-use-platform-invoke-to-play-a-wave-file.md)  
 プラットフォーム呼び出しサービスを使用して、Windows オペレーティング システム上の .wav サウンド ファイルを再生する方法について説明します。  
  
 [チュートリアル: Office のプログラミング](../../../csharp/programming-guide/interop/walkthrough-office-programming.md)  
 Excel ブックと、ブックへのリンクを含む Word 文書を作成する方法を示します。  
  
 [COM クラスの例](../../../csharp/programming-guide/interop/example-com-class.md)  
 C# クラスを COM オブジェクトとして公開する方法を示します。  
  
## <a name="c-language-specification"></a>C# 言語仕様  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>参照

- <xref:System.Runtime.InteropServices.Marshal.ReleaseComObject%2A?displayProperty=nameWithType>  
- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [アンマネージ コードとの相互運用](../../../../docs/framework/interop/index.md)  
- [チュートリアル: Office のプログラミング](../../../csharp/programming-guide/interop/walkthrough-office-programming.md)
