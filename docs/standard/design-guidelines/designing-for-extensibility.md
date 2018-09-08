---
title: 機能拡張のデザイン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- extending class libraries
- extensibility with class libraries in .NET Framework
- class library design guidelines [.NET Framework], extensibility
- class library extensibility [.NET Framework]
ms.assetid: 1cdb8740-871a-456c-9bd9-db96ca8d79b3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c1690d0cdf1f57eaf0a794d6e71babfa4fa6425
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44199883"
---
# <a name="designing-for-extensibility"></a>機能拡張のデザイン
フレームワークの設計の 1 つの重要な側面は、フレームワークの拡張性を慎重に検討することを確認して行っています。 これは、コストとメリットに関連付けられたさまざまな機能拡張メカニズムを理解することが必要です。 この章では、拡張メカニズムを判断するのに役立ちます: サブクラス化、イベント、仮想メンバー、コールバック、および、-、framework の要件を満たす最適なことができます。  
  
 フレームワークで機能拡張を可能にする方法はたくさんあります。 コストが非常に強力なするよりも低コストの範囲です。 任意の特定の機能拡張要件の要件を満たす最低コストのかかる機能拡張メカニズムを選択してください。 重大な変更を導入することがなくすぐ実行しないことができますが、通常は、後で、複数の機能拡張を追加することは覚えておいてください。  
  
## <a name="in-this-section"></a>このセクションの内容  
 [シールされていないクラス](../../../docs/standard/design-guidelines/unsealed-classes.md)  
 [プロテクト メンバー](../../../docs/standard/design-guidelines/protected-members.md)  
 [イベントとコールバック](../../../docs/standard/design-guidelines/events-and-callbacks.md)  
 [仮想メンバー](../../../docs/standard/design-guidelines/virtual-members.md)  
 [抽象化 (抽象型およびインターフェイス)](../../../docs/standard/design-guidelines/abstractions-abstract-types-and-interfaces.md)  
 [抽象化の実装用の基本クラス](../../../docs/standard/design-guidelines/base-classes-for-implementing-abstractions.md)  
 [シール](../../../docs/standard/design-guidelines/sealing.md)  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
