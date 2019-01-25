---
title: セキュリティとパブリックの読み取り専用配列フィールド
ms.date: 03/30/2017
helpviewer_keywords:
- security [.NET Framework], public read-only array fields
ms.assetid: 3df28dee-2a9f-40ff-9852-bfdbe59c27f3
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 03f3ce51eaab9e08d5f05932d9360adc4fd2110f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560988"
---
# <a name="security-and-public-read-only-array-fields"></a><span data-ttu-id="25f08-102">セキュリティとパブリックの読み取り専用配列フィールド</span><span class="sxs-lookup"><span data-stu-id="25f08-102">Security and Public Read-only Array Fields</span></span>
<span data-ttu-id="25f08-103">パブリックの読み取り専用の配列フィールドを変更できるため、境界の動作またはアプリケーションのセキュリティを定義するのに、マネージ ライブラリからパブリック読み取り専用の配列フィールドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="25f08-103">Never use read-only public array fields from managed libraries to define the boundary behavior or security of your applications because read-only public array fields can be modified.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="25f08-104">Remarks</span><span class="sxs-lookup"><span data-stu-id="25f08-104">Remarks</span></span>  
 <span data-ttu-id="25f08-105">.NET framework の一部のクラスには、プラットフォーム固有の境界パラメーターが含まれている読み取り専用のパブリック フィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="25f08-105">Some .NET framework classes include read-only public fields that contain platform-specific boundary parameters.</span></span>  <span data-ttu-id="25f08-106">たとえば、<xref:System.IO.Path.InvalidPathChars>フィールドは、ファイル パスの文字列で許可されていない文字を記述する配列。</span><span class="sxs-lookup"><span data-stu-id="25f08-106">For example, the <xref:System.IO.Path.InvalidPathChars> field is an array that describes the characters that are not allowed in a file path string.</span></span>  <span data-ttu-id="25f08-107">.NET Framework 全体で多くの同じフィールドが存在します。</span><span class="sxs-lookup"><span data-stu-id="25f08-107">Many similar fields are present throughout the .NET Framework.</span></span>  
  
 <span data-ttu-id="25f08-108">パブリックの読み取り専用フィールドの値などの<xref:System.IO.Path.InvalidPathChars>コードや、コードのアプリケーション ドメインを共有するコードで変更できます。</span><span class="sxs-lookup"><span data-stu-id="25f08-108">The values of public read-only fields like <xref:System.IO.Path.InvalidPathChars> can be modified by your code or code that shares your code’s application domain.</span></span>  <span data-ttu-id="25f08-109">アプリケーションの境界の動作を定義するのに次のような読み取り専用のパブリックの配列フィールドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="25f08-109">You should not use read-only public array fields like this to define the boundary behavior of your applications.</span></span>  <span data-ttu-id="25f08-110">場合は、悪意のあるコードは、境界の定義を変更し、予期しない方法でコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="25f08-110">If you do, malicious code can alter the boundary definitions and use your code in unexpected ways.</span></span>  
  
 <span data-ttu-id="25f08-111">2.0 と .NET Framework の以降のバージョンでは、パブリックの配列フィールドを使用する代わりに新しい配列を返すメソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="25f08-111">In version 2.0 and later of the .NET Framework, you should use methods that return a new array instead of using public array fields.</span></span>  <span data-ttu-id="25f08-112">使用する代わりに、たとえば、<xref:System.IO.Path.InvalidPathChars>フィールドを使用する必要がある、<xref:System.IO.Path.GetInvalidPathChars%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="25f08-112">For example, instead of using the <xref:System.IO.Path.InvalidPathChars> field, you should use the <xref:System.IO.Path.GetInvalidPathChars%2A> method.</span></span>  
  
 <span data-ttu-id="25f08-113">.NET Framework の型が内部での境界の種類を定義するパブリック フィールドを使用しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="25f08-113">Note that the .NET Framework types do not use the public fields to define boundary types internally.</span></span>  <span data-ttu-id="25f08-114">代わりに、.NET Framework では、別のプライベート フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="25f08-114">Instead, the .NET Framework uses separate private fields.</span></span>  <span data-ttu-id="25f08-115">これらのパブリック フィールドの値を変更しても、.NET Framework 型の動作は変わりません。</span><span class="sxs-lookup"><span data-stu-id="25f08-115">Changing the values of these public fields does not alter the behavior of .NET Framework types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25f08-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="25f08-116">See also</span></span>
- [<span data-ttu-id="25f08-117">安全なコーディングのガイドライン</span><span class="sxs-lookup"><span data-stu-id="25f08-117">Secure Coding Guidelines</span></span>](../../../docs/standard/security/secure-coding-guidelines.md)
