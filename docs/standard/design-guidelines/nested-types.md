---
title: 入れ子にされた型
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- types, nested
- public nested types
- type design guidelines, nested types
- nested types
- members [.NET Framework], type
- class library design guidelines [.NET Framework], nested types
ms.assetid: 12feb7f0-b793-4d96-b090-42d6473bab8c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2593b85dd4747a3fbe365994c3e5d9beae3e3406
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44188148"
---
# <a name="nested-types"></a>入れ子にされた型
入れ子になった型は、それを囲む型と呼ばれる別の型のスコープ内で定義されている型です。 入れ子にされた型が、その外側の型のすべてのメンバーにアクセスします。 たとえば、それを囲む型のすべての先祖で定義されているフィールドを保護して、外側の型で定義されてプライベート フィールドにアクセス権があります。  
  
 一般に、控えめ入れ子にされた型に使用する必要があります。 直接呼び出すべきではないいくつかの理由があります。 一部の開発者の概念を熟知していません。 これらの開発者では、入れ子にされた型の変数の宣言の構文に問題があるなどがあります。 入れ子にされた型は、その外側の型でも非常に緊密に結合されていて、そのため、汎用型であることには適していません。  
  
 入れ子にされた型は、それを囲む型の実装の詳細をモデル化するために最適です。 エンドユーザーは、入れ子にされた型の変数を宣言する必要はほとんどとほとんどない、入れ子にされた型を明示的にインスタンス化する必要があります。 たとえば、コレクションの列挙子は、そのコレクションの入れ子にされた型にできます。 列挙子がその外側の型でインスタンス化は、通常、列挙子変数に、エンドユーザーが宣言することはほとんどありませんがあるため、多くの言語では、foreach ステートメントをサポート、.  
  
 **✓ DO** 入れ子にされた型とその外側の型間の関係のあるメンバーのアクセシビリティのセマンティクスは次のことをお勧めときに、入れ子にされた型を使用します。  
  
 **X DO NOT** 論理的なグループとしてパブリック入れ子にされた型を使用して構築以外の場合はこの名前空間を使用します。  
  
 **X AVOID** 入れ子にされた型をパブリックに公開します。 唯一の例外は、入れ子にされた型の変数をサブクラスまたはその他の高度なカスタマイズ シナリオなどのまれなシナリオでのみ宣言する必要があるかどうかです。  
  
 **X DO NOT** 型が、含んでいる型の外部で参照されている可能性が高い場合は、入れ子にされた型を使用します。  
  
 たとえば、クラスで定義されたメソッドに渡される列挙型はクラスの入れ子にされた型として定義されませんする必要があります。  
  
 **X DO NOT** クライアント コードでインスタンス化する必要がある場合は、入れ子にされた型を使用します。  型のパブリック コンス トラクターの場合する必要がありますネストいない可能性があります。  
  
 型が、独自のフレームワーク内の場所を示すために思えます型をインスタンス化する場合 (できます作成し、それに伴う作業し、これまで、外部型を使用せず、それを破棄)、そのため、ネストいない必要があります。 内部型する必要がありますいない広範囲に再利用、リレーションシップがない場合は、外側の型の外部で外側の型にもします。  
  
 **X DO NOT** インターフェイスのメンバーとして入れ子にされた型を定義します。 多くの言語は、そのようなコンストラクトをサポートしていません。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [型デザインのガイドライン](../../../docs/standard/design-guidelines/type.md)  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
