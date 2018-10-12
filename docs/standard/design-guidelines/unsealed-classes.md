---
title: シールされていないクラス
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ef0f1c4c9b2d1928d6f96d62ab12df9786756498
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43891378"
---
# <a name="unsealed-classes"></a>シールされていないクラス
シール クラスから継承することはできませんし、機能拡張は、します。 これに対し、封印されていないクラスから継承できるクラスと呼びます。  
  
 **✓ CONSIDER** 安価なを提供するのにまだ高く評価されたフレームワークを拡張機能として、仮想またはプロテクト メンバーを追加なしで封印されていないクラスを使用します。  
  
 多くの場合、開発者はカスタム コンス トラクター、新しいメソッドは、メソッドのオーバー ロードなどの便利なメンバーを追加するための封印されていないクラスから継承したいと考えているとします。 たとえば、`System.Messaging.MessageQueue`が封印されていないと、できるので、ユーザーがその既定値を特定のキューのパスにカスタムのキューを作成する特定のシナリオ用の API を簡略化するカスタム メソッドを追加します。  
  
 既定ではほとんどのプログラミング言語でクラスが封印されていないし、これは、推奨された既定のフレームワークのほとんどのクラスにもします。 封印されていない型によって提供される拡張機能は、フレームワークのユーザーによって非常にありがたいと封印されていない型に関連付けられている相対的に低いテスト コストのために提供する非常に低コストです。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [機能拡張のデザイン](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
- [シール](../../../docs/standard/design-guidelines/sealing.md)
