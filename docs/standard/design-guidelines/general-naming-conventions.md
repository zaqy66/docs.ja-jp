---
title: 一般的な名前付け規則
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], conflicts
- type names, conflicts
- language-specific type names
- names [.NET Framework], about naming guidelines
- names [.NET Framework], abbreviations
- abbreviation naming guidelines
- acronym naming guidelines
- Hungarian notation
- names [.NET Framework], type names
- names [.NET Framework], acronyms
ms.assetid: d3a77ea1-75d2-4969-a8c3-3e1e3e1aaedc
author: KrzysztofCwalina
ms.openlocfilehash: 9febc7eed7d6dedad6655b51a96694b72b78711b
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147282"
---
# <a name="general-naming-conventions"></a>一般的な名前付け規則
このセクションでは、一般的な名前付け規則、単語の選択に関連する言語固有の名前を使用しないようにする方法の省略形と頭字語、および推奨事項の使用に関するガイドラインについて説明します。  
  
## <a name="word-choice"></a>単語の選択  
 **✓ DO** 読みやすい識別子の名前を選択します。  
  
 たとえば、という名前のプロパティ`HorizontalAlignment`英語 - よりも読みやすく、`AlignmentHorizontal`します。  
  
 **✓ DO** 簡潔さよりも読みやすさを優先します。  
  
 プロパティ名`CanScrollHorizontally`よりは`ScrollableX`(x 軸にあいまいな参照)。  
  
 **X DO NOT** アンダー スコア、ハイフン、またはその他の英数字以外の文字を使用します。  
  
 **X DO NOT** ハンガリアン記法を使用します。  
  
 **X AVOID** 広くのキーワードと競合する識別子を使用してプログラミング言語を使用します。  
  
 に従って規則 4 の共通言語仕様 (CLS) に準拠しているすべての言語はその言語のキーワードを識別子として使用する名前付きの項目へのアクセスを許可するメカニズムを提供する必要があります。 C# の場合は、たとえば、使用して、@ 記号にエスケープ メカニズムとして。 ただしはよりもなしで 1 つのエスケープ シーケンスでメソッドを使用するより難しいために、一般的なキーワードを回避することはお勧めもします。  
  
## <a name="using-abbreviations-and-acronyms"></a>省略形と頭字語を使用します。  
 **X DO NOT** 識別子名の一部としての省略形または短縮形を使用します。  
  
 たとえば、使用して`GetWindow`なく`GetWin`します。  
  
 **X DO NOT** 広く受け入れられていると偶数の場合は、必要な場合にのみではない任意の頭字語を使用します。  
  
## <a name="avoiding-language-specific-names"></a>言語固有の名前を回避します。  
 **✓ DO** 型名に言語固有のキーワードではなく、意味的にわかりやすい名前を使用します。  
  
 たとえば、`GetLength`よりもよい名前は、`GetInt`します。  
  
 **✓ DO** まれなケース識別子には、その型以外の意味があるない場合に言語固有の名前ではなく、汎用の CLR 型名を使用します。  
  
 たとえば、メソッドに変換する<xref:System.Int64>名前を指定する必要があります`ToInt64`ではなく、 `ToLong` (ため<xref:System.Int64>(C#) CLR 名は、-固有のエイリアス`long`)。 次の表は、CLR の型名 (およびその c#、Visual Basic、および C++ の対応する型名) を使用していくつかの基本データ型を表示します。  
  
|C#|Visual Basic|C++|CLR|  
|---------|------------------|-----------|---------|  
|**sbyte**|**SByte**|**char**|**SByte**|  
|**byte**|**Byte**|**unsigned char**|**Byte**|  
|**short**|**Short**|**short**|**Int16**|  
|**ushort**|**UInt16**|**unsigned short**|**UInt16**|  
|**int**|**Integer**|**int**|**Int32**|  
|**uint**|**UInt32**|**unsigned int**|**UInt32**|  
|**long**|**Long**|**__int64**|**Int64**|  
|**ulong**|**UInt64**|**unsigned __int64**|**UInt64**|  
|**float**|**Single**|**float**|**Single**|  
|**double**|**Double**|**double**|**Double**|  
|**bool**|**Boolean**|**bool**|**Boolean**|  
|**char**|**Char**|**wchar_t**|**Char**|  
|**string**|**String**|**String**|**String**|  
|**object**|**Object**|**Object**|**Object**|  
  
 **✓ DO** など、共通名を使用して`value`または`item`、まれなケース識別子は特別な意味を持たないし、パラメーターの型が重要でないときに、型名を繰り返しではなくです。  
  
## <a name="naming-new-versions-of-existing-apis"></a>既存の Api の新しいバージョンの名前を付ける  
 **✓ DO** 既存の API の新しいバージョンを作成するときに、古い API への名前を使用します。  
  
 これにより、Api の間のリレーションシップを強調表示します。  
  
 **✓ DO** を既存の API の新しいバージョンを示すプレフィックスではなく、サフィックスを追加することを希望します。  
  
 ドキュメントについてを参照するときに検出を支援はこれまたは IntelliSense を使用します。 古いバージョンの API はほとんどのブラウザーと IntelliSense は、アルファベット順に識別子を表示するための新しい Api の近くに編成します。  
  
 **✓ CONSIDER** サフィックスまたはプリフィックスを追加する代わりに、まったく新しいが意味のある識別子を使用します。  
  
 **✓ DO** の数値のサフィックスを使用して、既存の API の新しいバージョンを指定する、API の既存の名前 (つまり、業界標準である) 場合は、意味のある唯一の名前は、どの意味を追加する場合は、サフィックス (または、名前を変更する) アプリの場合に特にropriate オプション。  
  
 **X DO NOT** "Ex"(または類似した) を使用して、同じ API の以前のバージョンと区別する識別子のサフィックスです。  
  
 **✓ DO** 32 ビット整数の代わりに 64 ビット整数 (長整数) で動作する Api のバージョンを導入するときに、「64」サフィックスを使用します。 既存の 32 ビットの API が存在する場合は、この手法を採用するだけで済みますしないため、64 ビット バージョンのみで新しい Api を行います。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *Pearson Education, Inc. からのアクセス許可によって了承を得て転載[Framework デザイン ガイドライン。規則、手法、および再利用可能な .NET ライブラリの第 2 版のパターン](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)Krzysztof Cwalina、Brad 内容では、Microsoft Windows の開発シリーズの一部として、Addison-wesley Professional、2008 年 10 月 22日を公開します。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [名前付けのガイドライン](../../../docs/standard/design-guidelines/naming-guidelines.md)
