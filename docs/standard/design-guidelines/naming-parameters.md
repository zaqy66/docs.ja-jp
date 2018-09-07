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
# <a name="naming-parameters"></a><span data-ttu-id="71088-102">パラメーターに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="71088-102">Naming Parameters</span></span>
<span data-ttu-id="71088-103">はっきりした理由の読みやすさを超えるパラメーターは、そのビジュアル デ ザイン ツール Intellisense および参照機能クラスを提供するときにドキュメントでは、デザイナーで表示されるため、パラメーター名のガイドラインに従う重要です。</span><span class="sxs-lookup"><span data-stu-id="71088-103">Beyond the obvious reason of readability, it is important to follow the guidelines for parameter names because parameters are displayed in documentation and in the designer when visual design tools provide Intellisense and class browsing functionality.</span></span>  
  
 <span data-ttu-id="71088-104">**✓ DO** パラメーター名の camel 表記を使用します。</span><span class="sxs-lookup"><span data-stu-id="71088-104">**✓ DO** use camelCasing in parameter names.</span></span>  
  
 <span data-ttu-id="71088-105">**✓ DO** わかりやすいパラメーター名を使用します。</span><span class="sxs-lookup"><span data-stu-id="71088-105">**✓ DO** use descriptive parameter names.</span></span>  
  
 <span data-ttu-id="71088-106">**✓ CONSIDER** パラメーターの型ではなく、パラメーターの意味に基づく名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="71088-106">**✓ CONSIDER** using names based on a parameter’s meaning rather than the parameter’s type.</span></span>  
  
### <a name="naming-operator-overload-parameters"></a><span data-ttu-id="71088-107">演算子のオーバー ロードのパラメーターの名前を付ける</span><span class="sxs-lookup"><span data-stu-id="71088-107">Naming Operator Overload Parameters</span></span>  
 <span data-ttu-id="71088-108">**✓ DO** 使用`left`と`right`のパラメーターに意味がない場合は、二項演算子のオーバー ロード パラメーター名にします。</span><span class="sxs-lookup"><span data-stu-id="71088-108">**✓ DO** use `left` and `right` for binary operator overload parameter names if there is no meaning to the parameters.</span></span>  
  
 <span data-ttu-id="71088-109">**✓ DO** 使用`value`で単項演算子のオーバー ロード パラメーター名はパラメーターに意味がない場合。</span><span class="sxs-lookup"><span data-stu-id="71088-109">**✓ DO** use `value` for unary operator overload parameter names if there is no meaning to the parameters.</span></span>  
  
 <span data-ttu-id="71088-110">**✓ CONSIDER** 演算子にわかりやすい名前オーバー ロードのパラメーターの場合は重要な価値が追加されます。</span><span class="sxs-lookup"><span data-stu-id="71088-110">**✓ CONSIDER** meaningful names for operator overload parameters if doing so adds significant value.</span></span>  
  
 <span data-ttu-id="71088-111">**X DO NOT** 使用の省略形または数値の添字演算子のオーバー ロードのパラメーターの名前。</span><span class="sxs-lookup"><span data-stu-id="71088-111">**X DO NOT** use abbreviations or numeric indices for operator overload parameter names.</span></span>  
  
 <span data-ttu-id="71088-112">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="71088-112">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="71088-113">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="71088-113">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71088-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="71088-114">See also</span></span>

- [<span data-ttu-id="71088-115">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="71088-115">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
- [<span data-ttu-id="71088-116">名前付けのガイドライン</span><span class="sxs-lookup"><span data-stu-id="71088-116">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
