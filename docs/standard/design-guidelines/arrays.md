---
title: 配列
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], arrays
- arrays [.NET Framework], usage guidelines
- empty arrays
ms.assetid: 66a1b3d8-6f3f-4715-b235-e1ff95e32d8e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1ac7e28c3172f2ed68d402e1d04a1664644c7f25
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2018
ms.locfileid: "45658722"
---
# <a name="arrays"></a>配列
**✓ DO** パブリック Api で配列にコレクションの使用を優先します。 [コレクション](../../../docs/standard/design-guidelines/guidelines-for-collections.md)セクション コレクションと配列の間で選択する方法について詳しく説明します。  
  
 **X DO NOT** 読み取り専用配列フィールドを使用します。 フィールド自体は読み取り専用と、変更できない配列内の要素を変更することができます。  
  
 **✓ CONSIDER** 多次元配列ではなくジャグ配列を使用します。  
  
 ジャグ配列は、要素も配列を含む配列です。 配列の要素を構成するには、多次元配列と比較データ (スパース マトリックスなど) のいくつかのセットに対して無駄な小さい領域に、さまざまなサイズを指定できます。 さらに、いくつかのシナリオで実行時パフォーマンスの向上を発生する可能性がありますので、CLR は、ジャグ配列のインデックス操作を最適化します。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- <xref:System.Array>  
- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [使用方法のガイドライン](../../../docs/standard/design-guidelines/usage-guidelines.md)
