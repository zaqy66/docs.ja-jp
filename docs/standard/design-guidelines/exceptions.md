---
title: 例外のデザインのガイドライン
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- exceptions [.NET Framework], design guidelines
- class library design guidelines [.NET Framework], exceptions
- errors [.NET Framework], exceptions
- reporting errors
ms.assetid: bc177b2f-7528-4ae4-83db-aacfb04b86d0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51cc5296a7b3f6d75b5e56d6bbc74330fa147848
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47232618"
---
# <a name="design-guidelines-for-exceptions"></a><span data-ttu-id="1d75a-102">例外のデザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="1d75a-102">Design Guidelines for Exceptions</span></span>
<span data-ttu-id="1d75a-103">例外処理には戻り値ベースのエラー報告に対する多くの利点です。</span><span class="sxs-lookup"><span data-stu-id="1d75a-103">Exception handling has many advantages over return-value-based error reporting.</span></span> <span data-ttu-id="1d75a-104">適切なフレームワークの設計では、例外の利点を活用するアプリケーション開発者は役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1d75a-104">Good framework design helps the application developer realize the benefits of exceptions.</span></span> <span data-ttu-id="1d75a-105">このセクションでは、例外の利点を説明し、それらを効果的に使用のガイドラインを示します。</span><span class="sxs-lookup"><span data-stu-id="1d75a-105">This section discusses the benefits of exceptions and presents guidelines for using them effectively.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="1d75a-106">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="1d75a-106">In This Section</span></span>  
 [<span data-ttu-id="1d75a-107">例外のスロー</span><span class="sxs-lookup"><span data-stu-id="1d75a-107">Exception Throwing</span></span>](../../../docs/standard/design-guidelines/exception-throwing.md)  
 [<span data-ttu-id="1d75a-108">標準例外型の使用</span><span class="sxs-lookup"><span data-stu-id="1d75a-108">Using Standard Exception Types</span></span>](../../../docs/standard/design-guidelines/using-standard-exception-types.md)  
 [<span data-ttu-id="1d75a-109">例外とパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="1d75a-109">Exceptions and Performance</span></span>](../../../docs/standard/design-guidelines/exceptions-and-performance.md)  
 <span data-ttu-id="1d75a-110">*Portions © 2005, 2009 Microsoft Corporation.All rights reserved.*</span><span class="sxs-lookup"><span data-stu-id="1d75a-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="1d75a-111">*2008 年 10 月 22 日に Microsoft Windows Development シリーズの一部として、Addison-Wesley Professional によって発行された、Krzysztof Cwalina および Brad Abrams による「[Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)」 (フレームワーク デザイン ガイドライン: 再利用可能な .NET ライブラリの規則、用法、パターン、第 2 版) から Pearson Education, Inc. の許可を得て再印刷されています。*</span><span class="sxs-lookup"><span data-stu-id="1d75a-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d75a-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d75a-112">See also</span></span>

- [<span data-ttu-id="1d75a-113">フレームワーク デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="1d75a-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
