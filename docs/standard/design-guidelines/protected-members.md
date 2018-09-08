---
title: プロテクト メンバー
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- members [.NET Framework], protected
- protected members
- classes [.NET Framework], unsealed
- classes [.NET Framework], protected members
- unsealed classes
- customizing class behavior
ms.assetid: aa0b58ee-3956-494d-ab48-471ae5db8740
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4574dffc3f9dd1b60d655bfde33a4ddc1a81d350
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44140945"
---
# <a name="protected-members"></a>プロテクト メンバー
単独で保護されたメンバーでは任意の拡張機能は提供しませんより強力なサブクラス化による拡張性を作成することができます。 これらは、メインのパブリック インターフェイスを不必要に複雑にせず、高度なカスタマイズ オプションを公開する使用できます。  
  
 フレームワークの設計者は、「保護」の名前は、セキュリティの誤った認識を与えることができますので、保護されたメンバーには注意する必要があります。 すべてのユーザーは、封印されていないクラスのサブクラスとメンバーへのアクセスが保護されていることと、防御的なコーディング手法がパブリック メンバーの使用が保護されたメンバーに適用するため、同じ。  
  
 **✓ CONSIDER** 高度なカスタマイズのメンバーを使用して保護されています。  
  
 **✓ DO** セキュリティ、ドキュメント、および互換性分析するためにパブリックと封印されていないクラスにプロテクト メンバーを処理します。  
  
 クラスから継承するすべてのユーザーし、プロテクト メンバーにアクセスできます。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [機能拡張のデザイン](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
