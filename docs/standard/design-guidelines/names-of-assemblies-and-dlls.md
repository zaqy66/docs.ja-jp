---
title: アセンブリと DLL の名前
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], DLLs
- names [.NET Framework], assemblies
- assemblies [.NET Framework], names
- DLLs, names
ms.assetid: e800b610-31b4-4949-9c14-cb60e9f254be
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 97bd152cff53fb1c2edb107b6d6b34bd91ca1c49
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44366948"
---
# <a name="names-of-assemblies-and-dlls"></a>アセンブリと DLL の名前
アセンブリは、展開およびマネージ コード アプリケーションの id の単位です。 アセンブリは、1 つまたは複数のファイルにまたがることができます、通常このアセンブリは DLL と 1 対 1 をマップします。 そのため、このセクションでは、のみ DLL の名前付け規則、アセンブリの名前付け規則にマップできますがについて説明します。  
  
 **✓ DO** アセンブリ System.Data などの機能の大きなチャンクを提案する Dll の名前を選択します。  
  
 アセンブリと DLL の名前が名前空間の名前に対応する必要はありませんが、アセンブリの名前を付けるときは、名前空間の名前を次に適切です。 適切な経験則では、アセンブリに含まれている名前空間の共通のプレフィックスに基づいた DLL の名前です。 たとえば、2 つの名前空間を持つアセンブリ`MyCompany.MyTechnology.FirstFeature`と`MyCompany.MyTechnology.SecondFeature`、呼び出すことができます`MyCompany.MyTechnology.dll`します。  
  
 **✓ CONSIDER** Dll を次のパターンに従って名前付け。  
  
 `<Company>.<Component>.dll`  
  
 場所`<Component>`ドットで区切られた 1 つ以上の句が含まれています。 例えば:  
  
 `Litware.Controls.dll`。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [名前付けのガイドライン](../../../docs/standard/design-guidelines/naming-guidelines.md)
