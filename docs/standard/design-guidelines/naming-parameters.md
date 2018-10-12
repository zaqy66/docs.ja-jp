---
title: パラメーターに名前を付ける
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- parameters, names
- names [.NET Framework], parameters
ms.assetid: ca3c956e-725a-441b-b4e3-eab5d472f41c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8e6a8a1dcdcb8fa3311b040c72987f0f76e681fc
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44086473"
---
# <a name="naming-parameters"></a>パラメーターに名前を付ける
はっきりした理由の読みやすさを超えるパラメーターは、そのビジュアル デ ザイン ツール Intellisense および参照機能クラスを提供するときにドキュメントでは、デザイナーで表示されるため、パラメーター名のガイドラインに従う重要です。  
  
 **✓ DO** パラメーター名の camel 表記を使用します。  
  
 **✓ DO** わかりやすいパラメーター名を使用します。  
  
 **✓ CONSIDER** パラメーターの型ではなく、パラメーターの意味に基づく名前を使用します。  
  
### <a name="naming-operator-overload-parameters"></a>演算子のオーバー ロードのパラメーターの名前を付ける  
 **✓ DO** 使用`left`と`right`のパラメーターに意味がない場合は、二項演算子のオーバー ロード パラメーター名にします。  
  
 **✓ DO** 使用`value`で単項演算子のオーバー ロード パラメーター名はパラメーターに意味がない場合。  
  
 **✓ CONSIDER** 演算子にわかりやすい名前オーバー ロードのパラメーターの場合は重要な価値が追加されます。  
  
 **X DO NOT** 使用の省略形または数値の添字演算子のオーバー ロードのパラメーターの名前。  
  
 *Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*  
  
 *2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*  
  
## <a name="see-also"></a>関連項目

- [フレームワーク デザインのガイドライン](../../../docs/standard/design-guidelines/index.md)  
- [名前付けのガイドライン](../../../docs/standard/design-guidelines/naming-guidelines.md)
