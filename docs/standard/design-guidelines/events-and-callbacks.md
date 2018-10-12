---
title: イベントとコールバック
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- events [.NET Framework], extensibility
- methods [.NET Framework], callback
- callback methods
- callbacks
ms.assetid: 48b55c60-495f-4089-9396-97f9122bba7c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 390c12af7107bb78fc261c55ea15390cf9eaa5b7
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43862950"
---
# <a name="events-and-callbacks"></a>イベントとコールバック
コールバックは、機能拡張ポイントがデリゲートからのユーザー コードにコールバックするためのフレームワークです。 これらのデリゲートは、メソッドのパラメーターでは、通常、フレームワークに渡されます。  
  
 イベントは、コールバックのデリゲート (イベント ハンドラー) を提供するための便利で一貫した構文をサポートする特殊なケースです。 さらに、Visual Studio のステートメント入力候補およびデザイナーは、イベント ベースの Api を使用してヘルプを提供します。 (を参照してください[イベント デザイン](../../../docs/standard/design-guidelines/event.md))。  
  
 **✓ CONSIDER** コールバックを使用して、フレームワークによって実行されるカスタム コードを提供できるようにします。  
  
 **✓ CONSIDER** イベントを使用したオブジェクト指向設計を理解することがなくてもフレームワークの動作をカスタマイズできるようにします。  
  
 **✓ DO** 幅広い開発者になじみのあるは、ステートメント入力候補の Visual Studio と統合されたために、イベントを単純なコールバックよりも優先されます。  
  
 **X AVOID** パフォーマンス重視の Api でのコールバックを使用します。  
  
 **✓ DO** 新しい`Func<...>`、 `Action<...>`、または`Expression<...>`コールバックで Api を定義するときに、カスタム デリゲートではなく型です。  
  
 `Func<...>` `Action<...>`汎用デリゲートを表します。 `Expression<...>` コンパイルと、その後もできますが、実行時に呼び出されることができます関数定義を表すシリアル化およびリモート プロセスに渡されます。  
  
 **✓ DO** を測定しを使用するパフォーマンスの影響について理解する`Expression<...>`、使用する代わりに`Func<...>`と`Action<...>`デリゲート。  
  
 `Expression<...>` ほとんどの場合と論理的に等価では型が`Func<...>`と`Action<...>`デリゲート。 主な違いは、デリゲートはローカル プロセスのシナリオで使用するものであります。式は、有益なリモート プロセスまたはマシンで式を評価することである場合を対象としています。  
  
 **✓ DO** するデリゲートを呼び出すことによって実行している任意のコードを理解し、セキュリティ、正確性、および互換性への影響を与える可能性です。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [機能拡張のデザイン](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)
