---
title: 抽象クラスのデザイン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, abstract classes
- abstract classes, design guidelines
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], abstract
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d3646e6d-5c1f-4922-8fb0-ec5effb30d60
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5b9dacc4995a126e1ee3f6062dca796194d4882
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44128525"
---
# <a name="abstract-class-design"></a>抽象クラスのデザイン
**X DO NOT** 抽象型の public または protected のコンス トラクター内部を定義します。  
  
 コンス トラクターは、ユーザーが、型のインスタンスを作成する必要がある場合にのみパブリックである必要があります。 抽象型のインスタンスを作成することはできません、ため、パブリック コンス トラクターを持つ抽象型は正しく設計で、ユーザーに誤解を招きます。  
  
 **✓ DO** 抽象クラス内で、保護されているか、内部のコンス トラクターを定義します。  
  
 プロテクト コンス トラクターより一般的なサブタイプが作成されたときに、独自の初期化を実行する基本クラスでは。  
  
 アセンブリのクラスを定義する抽象クラスの具象実装を制限する、内部コンス トラクターを使用できます。  
  
 **✓ DO** を出荷する各の抽象クラスから継承する少なくとも 1 つの具象型を提供します。  
  
 これによって、抽象クラスのデザインを検証するを実行します。 たとえば、<xref:System.IO.FileStream?displayProperty=nameWithType>の実装には、<xref:System.IO.Stream?displayProperty=nameWithType>抽象クラス。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [型デザインのガイドライン](../../../docs/standard/design-guidelines/type.md)  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
