---
title: メンバーのオーバーロード
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- default arguments
- members [.NET Framework], overloaded
- member design guidelines [.NET Framework], overloading
- overloaded members
- signatures, members
ms.assetid: 964ba19e-8b94-4b5b-b1e3-5a0b531a0bb1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2127497d294cbfd4e1bb24d033f432378627ff13
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44129803"
---
# <a name="member-overloading"></a>メンバーのオーバーロード
メンバーのオーバー ロードでは、数またはのパラメーターの型でのみ異なるが、同じ名前を持つ同じ型に 2 つ以上のメンバーの作成を意味します。 たとえば、以下では、`WriteLine`メソッドがオーバー ロードします。  
  
```  
public static class Console {  
    public void WriteLine();  
    public void WriteLine(string value);  
    public void WriteLine(bool value);  
    ...  
}  
```  
  
 メソッド、コンス トラクター、およびインデックス付きプロパティは、パラメーターを持つことができます、ため、これらのメンバーだけがオーバー ロードできます。  
  
 オーバー ロードでは、使いやすさ、生産性、および再利用可能なライブラリの読みやすさを向上させるための最も重要な手法の 1 つです。 パラメーターの数のオーバー ロードできるようになりますコンス トラクターとメソッドの単純なバージョンを提供します。 パラメーターの型のオーバー ロードできるようになります同じメンバーの選択したさまざまな種類のセットで同じ操作を実行する名前を使用します。  
  
 **✓ DO** 短いオーバー ロードで使用される既定値を示すためにわかりやすいパラメーター名を使用しようとしています。  
  
 **X AVOID** オーバー ロードのパラメーター名は任意で変更します。 1 つのオーバー ロードのパラメーターは、別のオーバー ロードのパラメーターとして、同じ入力を表している場合、パラメーターは、同じ名前が必要です。  
  
 **X AVOID** メンバーをオーバー ロードされているのパラメーターの順序で一貫していません。 同じ名前のパラメーターは、すべてのオーバー ロード内の同じ位置に表示されます。  
  
 **✓ DO** (拡張機能が必要な場合)、最長のオーバー ロードだけの仮想を作成します。 短いオーバー ロードは、長いオーバー ロードに単にを通じてを呼び出す必要があります。  
  
 **X DO NOT** 使用`ref`または`out`メンバーをオーバー ロードする修飾子です。  
  
 一部の言語では、このようなオーバー ロードの呼び出しを解決できません。 さらに、このようなオーバー ロード、通常は完全に異なるセマンティクスを持つ可能性がありますされないをオーバー ロードが 2 つの個別のメソッド代わりにします。  
  
 **X DO NOT** 同じ位置と類似した種類のパラメーターを使用してまだセマンティクスが異なるオーバー ロードがあります。  
  
 **✓ DO** 許可`null`省略可能な引数に渡されます。  
  
 **✓ DO** メンバーの既定の引数を持つメンバーを定義するのではなく、オーバー ロードを使用します。  
  
 既定の引数は、CLS 準拠ではありません。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [メンバーのデザインのガイドライン](../../../docs/standard/design-guidelines/member.md)  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
