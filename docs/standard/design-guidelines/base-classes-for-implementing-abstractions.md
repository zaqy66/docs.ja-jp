---
title: 抽象化の実装用の基本クラス
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- abstractions [.NET Framework]
- base classes, abstractions
ms.assetid: 37a2d9a4-9721-482a-a40f-eee2c1d97875
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f326ee895251678c7a23ea84a11e83951edf2cc
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44078640"
---
# <a name="base-classes-for-implementing-abstractions"></a>抽象化の実装用の基本クラス
厳密に言えば、別のクラスがそこから派生する場合、クラスは、基底クラスになります。 ここでは、ただし、基本クラスは、共通の抽象化を提供または一部を再利用するには、他のクラスの既定の実装が継承する主な目的としたクラス。 通常、基底クラスは、階層のルートにある抽象化と下部にあるいくつかのカスタム実装の間の継承階層の途中で配置されています。  
  
 これらは、抽象化を実装するための実装のヘルパーとして機能します。 たとえば、項目の順序付けられたコレクションのフレームワークの抽象化の 1 つは、<xref:System.Collections.Generic.IList%601>インターフェイス。 実装する<xref:System.Collections.Generic.IList%601>、簡単ではありませんし、そのため、いくつかの基本クラスは、フレームワークなど<xref:System.Collections.ObjectModel.Collection%601>と<xref:System.Collections.ObjectModel.KeyedCollection%602>、カスタム コレクションを実装するためのヘルパーとして機能します。  
  
 基底クラスは、通常は、単独で抽象化として機能するのに適したが多すぎるの実装を格納する傾向があるためです。 たとえば、`Collection<T>`基底クラスには、大量非ジェネリックが実装しているという事実に関連する実装にはが含まれています`IList`(非ジェネリック コレクションでより適切に統合) へのインターフェイスとは、という事実に格納された項目のコレクション。そのフィールドのいずれかでメモリ。  
  
 既に説明したようの基本クラスは抽象化を実装する必要があるユーザーにご協力を提供することができますが、同時に重大な責任になることができます。 継承階層の深さを増やすし、したがって概念的には、フレームワークが複雑になる、サーフェス領域を追加します。 そのため、フレームワークのユーザーに大きな価値を提供する場合にのみ、基本クラスを使用する必要があります。 これらを基本クラスから継承ではなく内部の実装への委任で大文字と小文字をことを検討するフレームワークの実装時にのみ値を提供する場合に避ける必要があります。  
  
 **✓ CONSIDER** 抽象メンバーが含まれている場合でも、基本クラスの抽象です。 これをユーザーに明確に伝達する、クラスが継承するためだけに設計されています。  
  
 **✓ CONSIDER** 主要なシナリオの種類から別の名前空間の基本クラスを配置することです。 定義上、基底クラスは高度な機能拡張シナリオのためのものし、そのため、多くのユーザーにとって重要ではありません。  
  
 **X AVOID** クラスは、パブリック Api で使用する場合は、"Base"サフィックスを持つ基本クラスを名前付けします。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [機能拡張のデザイン](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
