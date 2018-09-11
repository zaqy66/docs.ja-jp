---
title: メンバーのデザインのガイドライン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- member design guidelines [.NET Framework], about member design guidelines
- members [.NET Framework], design guidelines
- class library design guidelines [.NET Framework], members
- member design guidelines [.NET Framework]
ms.assetid: 0ce93180-1d7b-4f8c-9306-f828b2d66b8f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d1598ac63af38f1ca3e11104bc8e1cd6323d35ed
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44259968"
---
# <a name="member-design-guidelines"></a>メンバーのデザインのガイドライン
メソッド、プロパティ、イベント、コンス トラクター、およびフィールドは、メンバーとしてまとめて呼ばれます。 メンバーが、最終的に、フレームワークのエンドユーザーに、フレームワークの機能が公開されていることを意味します。  
  
 メンバーは、仮想または非仮想、具象か抽象クラスで静的メソッドまたはインスタンスにできるし、ユーザー補助機能のいくつかの異なるスコープを持つことができます。 さまざまな種類すべてでは、驚異的な表現力を提供しますが、同時に、framework デザイナー側注意が必要です。  
  
 この章では、任意の型のメンバーを設計するときに従う必要がありますの基本的なガイドラインを提供します。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [メンバーのオーバーロード](../../../docs/standard/design-guidelines/member-overloading.md)  
 [プロパティのデザイン](../../../docs/standard/design-guidelines/property.md)  
 [コンストラクターのデザイン](../../../docs/standard/design-guidelines/constructor.md)  
 [イベントのデザイン](../../../docs/standard/design-guidelines/event.md)  
 [フィールドのデザイン](../../../docs/standard/design-guidelines/field.md)  
 [拡張メソッド](../../../docs/standard/design-guidelines/extension-methods.md)  
 [演算子のオーバーロード](../../../docs/standard/design-guidelines/operator-overloads.md)  
 [パラメーターのデザイン](../../../docs/standard/design-guidelines/parameter-design.md)  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
