---
title: 等値演算子
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], Equals method
- class library design guidelines [.NET Framework], equality operator
- equality operator (==) [.NET Framework]
- Equals method
- == operator (equality) [.NET Framework]
ms.assetid: bc496a91-fefb-4ce0-ab4c-61f09964119a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27550a8fd8292029cad9c2e699374a190b1a532e
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44511332"
---
# <a name="equality-operators"></a>等値演算子
このセクションでは、等値演算子のオーバー ロードをについて説明しを指す`operator==`と`operator!=`として等値演算子。  
  
 **X DO NOT** 等値演算子および以外のいずれかのオーバー ロードします。  
  
 **✓ DO** いることを確認<xref:System.Object.Equals%2A?displayProperty=nameWithType>等値演算子は、同じセマンティクスと同様のパフォーマンス特性があるとします。  
  
 多くの場合、つまり`Object.Equals`等値演算子はオーバー ロード時にオーバーライドする必要があります。  
  
 **X AVOID** 等値演算子から例外をスローします。  
  
 たとえば、引数のいずれかがスローする代わりに null の場合は false を返す`NullReferenceException`します。  
  
## <a name="equality-operators-on-value-types"></a>値の型で等値演算子  
 **✓ DO** 等しいかどうかがわかりやすい場合は、値型で等値演算子をオーバー ロードします。  
  
 ほとんどのプログラミング言語での既定の実装がない`operator==`値の型。  
  
## <a name="equality-operators-on-reference-types"></a>参照型で等値演算子  
 **X AVOID** 変更可能な参照型で等値演算子のオーバー ロードします。  
  
 多くの言語では、参照型の組み込みの等値演算子があります。 組み込みの演算子は、通常は参照の等価性を実装し、値の等価性を既定の動作が変更されたときに、多くの開発者は驚かします。  
  
 この問題は、不変性をより参照の等価性と値の等価性の間の違いに注意をはるかに困難になるために、変更不可の参照型の軽減されます。  
  
 **X AVOID** 実装では、参照の等価性の場合よりもはるかに低速になる場合は、参照型で等値演算子をオーバー ロードします。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [使用方法のガイドライン](../../../docs/standard/design-guidelines/usage-guidelines.md)
