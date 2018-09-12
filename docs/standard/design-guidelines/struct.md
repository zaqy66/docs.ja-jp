---
title: 構造体のデザイン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- deallocating structures
- allocating structures
- value types, structures
- structure design
- type design guidelines, structures
- structures [.NET Framework], design guidelines
ms.assetid: 1f48b2d8-608c-4be6-9ba4-d8f203ed9f9f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3879dc3f0270a56132b44882a74c50d05914ff89
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44709572"
---
# <a name="struct-design"></a>構造体のデザイン
ほとんどの場合、汎用的な値の型は構造体、c# のキーワードと呼ばれます。 このセクションでは、一般的な構造体のデザインのガイドラインを示します。  
  
 **X DO NOT** 構造体の既定のコンス トラクターを提供します。  
  
 このガイドラインに従うには、配列の各項目に対して、コンス トラクターを実行することがなく作成する構造体の配列が使用できます。 C# で許可しないことを既定のコンス トラクターがある構造体に注意してください。  
  
 **X DO NOT** 変更可能な値の型を定義します。  
  
 変更可能な値の型には、いくつかの問題があります。 たとえば、プロパティ get アクセス操作子が値型を返すときに、呼び出し元は、コピーを受け取ります。 コピーが暗黙的に作成されるため、開発者があります、コピー、および元の値ではなくを変更することに注意してくださかった。 また、(動的言語、特に) の一部の言語では、ローカル変数を逆参照時にも、コピーできるようにするために、変更可能な値の型を使用して問題があります。  
  
 **✓ DO** すべてのインスタンス データの状態が 0 に設定されている、false の場合、または null (該当する場合) が有効であることを確認します。  
  
 構造体の配列が作成されたときに、無効なインスタンスの偶発的な作成ができないようにします。  
  
 **✓ DO** 実装<xref:System.IEquatable%601>を値の型。  
  
 <xref:System.Object.Equals%2A?displayProperty=nameWithType>値型のメソッドとボックス化、および既定の実装がリフレクションを使用しているために、非常に効率的です。 <xref:System.IEquatable%601.Equals%2A> 優れたパフォーマンスを持つことができ、ボックス化が発生しないように実装することができます。  
  
 **X DO NOT** 明示的に拡張<xref:System.ValueType>です。 実際、ほとんどの言語は、これを回避します。  
  
 一般に、構造体は非常に役に立ちますが、頻繁には手書きされませんが小さく、1 つ、不変の値にのみ使用する必要があります。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [型デザインのガイドライン](../../../docs/standard/design-guidelines/type.md)  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [クラスまたは構造体の選択](../../../docs/standard/design-guidelines/choosing-between-class-and-struct.md)
