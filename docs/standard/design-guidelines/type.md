---
title: 型のデザインのガイドライン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines
- type design guidelines, about type design guidelines
- class library design guidelines [.NET Framework], type design guidelines
- types [.NET Framework], design guidelines
ms.assetid: 6b49314e-8bba-43ea-97ca-4e0255812f95
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7fb9964d0e542c0937c55ae65bd88b3f7149fa8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44187940"
---
# <a name="type-design-guidelines"></a>型のデザインのガイドライン
CLR の観点からは、型の 2 つのカテゴリがあります: 参照型と値の型: フレームワークの設計に関する詳細については、するために、それぞれに独自の特定のデザイン規則より論理的にグループの種類を分割しますが、します。  
  
 クラスは、参照型の一般的なケースです。 ほとんどのフレームワークの型の大部分を構成します。 クラスは、豊富なオブジェクト指向の機能がサポートされるを設定して、一般的な適用性を人気を助かりました。 基底クラスと抽象クラスは、拡張機能に関連する、特殊な論理グループです。  
  
 インターフェイスは、参照型と値の型の両方で実装できる型です。 したがって、参照型と値の型のポリモーフィックな階層のルートとして使用ができます。 さらに、インターフェイスは、CLR によってネイティブでサポートされていない複数の継承をシミュレートするために使用できます。  
  
 構造体の値型の一般的なケースは、小規模で単純な種類、言語プリミティブのように予約されている必要があります。  
  
 列挙型は、週、コンソールの色の日などの値の短いセットを定義するのに使用される値型の特殊なケースです。  
  
 静的クラスは、型の静的メンバーのコンテナーを意図したものです。 その他の操作へのショートカットを提供するよく使用されます。  
  
 デリゲート、例外、属性、配列、およびコレクションは、特定の用途のためのもので、参照型のすべての特殊なケースと、この書籍での設計と使用法のガイドラインは別の場所について説明します。  
  
 **✓ DO** 各型が適切に定義された一連の関連するメンバーは、関連付けられていない機能のランダムなコレクションだけでなくであることを確認します。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [クラスまたは構造体の選択](../../../docs/standard/design-guidelines/choosing-between-class-and-struct.md)  
 [抽象クラスのデザイン](../../../docs/standard/design-guidelines/abstract-class.md)  
 [静的クラスのデザイン](../../../docs/standard/design-guidelines/static-class.md)  
 [インターフェイスのデザイン](../../../docs/standard/design-guidelines/interface.md)  
 [構造体のデザイン](../../../docs/standard/design-guidelines/struct.md)  
 [列挙型デザイン](../../../docs/standard/design-guidelines/enum.md)  
 [入れ子にされた型](../../../docs/standard/design-guidelines/nested-types.md)  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
