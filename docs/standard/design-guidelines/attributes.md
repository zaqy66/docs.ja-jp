---
title: Attributes1
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- attributes [.NET Framework], about
- class library design guidelines [.NET Framework], attributes
ms.assetid: ee0038ef-b247-4747-a650-3c5c5cd58d8b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51aa91b1acbae9f1a15ac12441090dd4c1c2dcb1
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43869144"
---
# <a name="attributes"></a>属性
<xref:System.Attribute?displayProperty=nameWithType> カスタム属性を定義するために使用する基本クラス。  
  
 属性は、アセンブリ、型、メンバー、およびパラメーターなどのプログラミング要素に追加できる注釈です。 アセンブリのメタデータに格納されていて、リフレクション Api を使用して実行時にアクセスできます。 たとえば、フレームワークを定義、 <xref:System.ObsoleteAttribute>、型またはメンバーは推奨されていることを示す、型またはメンバーに適用できます。  
  
 属性には、1 つ以上のプロパティ、属性に関連する追加のデータを受け渡すことができます。 たとえば、`ObsoleteAttribute`のリリースに関する追加情報を実行することが、型またはメンバーが非推奨とし、廃止された API を置き換える新しい Api の説明。  
  
 属性が適用されるときに、属性の一部のプロパティを指定する必要があります。 これらと呼びます必要なプロパティまたは必須の引数を位置指定コンス トラクターのパラメーターとして表されるためです。 たとえば、<xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A>のプロパティ、<xref:System.Diagnostics.ConditionalAttribute>は必要なプロパティです。  
  
 属性を適用した場合に指定する必ずしもプロパティは省略可能なプロパティ (または省略可能な引数) と呼ばれます。 設定可能なプロパティで表されます。 コンパイラは、属性が適用されるときに、これらのプロパティを設定する特別な構文を提供します。 たとえば、<xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType>プロパティは省略可能な引数を表します。  
  
 **✓ DO** 「属性」サフィックスを持つカスタム属性クラスの名前  
  
 **✓ DO** 適用、<xref:System.AttributeUsageAttribute>カスタム属性にします。  
  
 **✓ DO** 省略可能な引数の設定可能なプロパティを提供します。  
  
 **✓ DO** 必須の引数の取得専用のプロパティを提供します。  
  
 **✓ DO** 必須の引数に対応するプロパティを初期化するコンス トラクターのパラメーターを指定します。 各パラメーターは、対応するプロパティとして (大文字小文字が異なる) には、同じ名前が必要です。  
  
 **X AVOID** 省略可能な引数に対応するプロパティを初期化するコンス トラクターのパラメーターを指定します。  
  
 つまり、コンス トラクターと setter の両方で設定できるプロパティがありません。 このガイドラインでは非常に明示的などの引数は省略可能ですし、これは必須であり、2 つの方法で同じことを行う必要はなくなります。  
  
 **X AVOID** カスタム属性のコンス トラクターのオーバー ロードします。  
  
 コンス トラクターの 1 つだけのことを明確に伝達をユーザーにどの引数が必要ですし、これは省略可能です。  
  
 **✓ DO** 可能であれば、カスタム属性クラスをシールします。 これにより、属性の参照、高速化。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [使用方法のガイドライン](../../../docs/standard/design-guidelines/usage-guidelines.md)
