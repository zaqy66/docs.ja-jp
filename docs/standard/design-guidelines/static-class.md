---
title: 静的クラスのデザイン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c3a0a51fc6055190f9a0189de2e17d98f88036ea
ms.sourcegitcommit: 700b9003ea6bdd83a53458bbc436c9b5778344f1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2018
ms.locfileid: "48261577"
---
# <a name="static-class-design"></a>静的クラスのデザイン
静的クラスは、静的メンバーのみを含んでいるクラスとして定義されます (から継承されたインスタンス メンバーだけでなくもちろん<xref:System.Object?displayProperty=nameWithType>とコンス トラクターはプライベート可能性があります)。 一部の言語では、静的クラスの組み込みサポートを提供します。 C# 2.0 以降では、クラスが静的に宣言されると、これはシール、抽象クラスで、インスタンス メンバーをオーバーライドまたは宣言されていることができます。  
  
 静的クラスは、純粋なオブジェクト指向設計と単純さのバランスです。 その他の操作へのショートカットを提供によく使用されます (など<xref:System.IO.File?displayProperty=nameWithType>)、拡張メソッド、または完全なオブジェクト指向ラッパーが保証されているいない機能の保持者 (など<xref:System.Environment?displayProperty=nameWithType>)。  
  
 **✓ DO** 静的クラスを慎重に使用します。  
  
 静的クラスは、オブジェクト指向のコア フレームワークのサポート クラスとしてのみ使用する必要があります。  
  
 **X DO NOT** 静的クラスをその他のバケットとして扱います。  
  
 **X DO NOT** 宣言または静的クラスでインスタンス メンバーをオーバーライドします。  
  
 **✓ DO** として、シールされた抽象クラスで静的クラスを宣言し、使用するプログラミング言語には静的クラスの組み込みサポートがない場合は、プライベート インスタンス コンス トラクターを追加します。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [型デザインのガイドライン](../../../docs/standard/design-guidelines/type.md)  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
