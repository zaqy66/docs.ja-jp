---
title: 型 <typename> は CLS に準拠していません。
ms.date: 07/20/2015
f1_keywords:
- bc40041
- vbc40041
helpviewer_keywords:
- BC40041
ms.assetid: 634132c2-5646-44aa-98c6-f773e2e63882
ms.openlocfilehash: 243f51b3e6c798c82fdbe7b28557c4f96c728bf2
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55281724"
---
# <a name="type-typename-is-not-cls-compliant"></a><span data-ttu-id="2a5fe-102">型\<typename > CLS 準拠ではありません</span><span class="sxs-lookup"><span data-stu-id="2a5fe-102">Type \<typename> is not CLS-compliant</span></span>
<span data-ttu-id="2a5fe-103">変数、プロパティ、または関数の戻り値は、CLS 準拠でないデータ型で宣言されています。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-103">A variable, property, or function return is declared with a data type that is not CLS-compliant.</span></span>  
  
 <span data-ttu-id="2a5fe-104">準拠するアプリケーションの[Language Independence and Language-independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS) に CLS 準拠型のみを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-104">For an application to be compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS), it must use only CLS-compliant types.</span></span>  
  
 <span data-ttu-id="2a5fe-105">次の Visual Basic データ型は CLS 準拠ではありません。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-105">The following Visual Basic data types are not CLS-compliant:</span></span>  
  
-   [<span data-ttu-id="2a5fe-106">SByte データ型</span><span class="sxs-lookup"><span data-stu-id="2a5fe-106">SByte Data Type</span></span>](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [<span data-ttu-id="2a5fe-107">UInteger データ型</span><span class="sxs-lookup"><span data-stu-id="2a5fe-107">UInteger Data Type</span></span>](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [<span data-ttu-id="2a5fe-108">ULong データ型</span><span class="sxs-lookup"><span data-stu-id="2a5fe-108">ULong Data Type</span></span>](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [<span data-ttu-id="2a5fe-109">UShort データ型</span><span class="sxs-lookup"><span data-stu-id="2a5fe-109">UShort Data Type</span></span>](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 <span data-ttu-id="2a5fe-110">**エラー ID:** BC40041</span><span class="sxs-lookup"><span data-stu-id="2a5fe-110">**Error ID:** BC40041</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="2a5fe-111">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="2a5fe-111">To correct this error</span></span>  
  
-   <span data-ttu-id="2a5fe-112">アプリケーションは、CLS に準拠する必要がある、最も近い CLS 準拠型にこの要素のデータ型を変更します。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-112">If your application needs to be CLS-compliant, change the data type of this element to the closest CLS-compliant type.</span></span> <span data-ttu-id="2a5fe-113">たとえば、2,147,483,647 を超える値の範囲が不要な場合は、 `UInteger` の代わりに `Integer` を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-113">For example, in place of `UInteger` you might be able to use `Integer` if you do not need the value range above 2,147,483,647.</span></span> <span data-ttu-id="2a5fe-114">拡張範囲が必要な場合は、 `UInteger` の代わりに `Long`を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-114">If you do need the extended range, you can replace `UInteger` with `Long`.</span></span>  
  
-   <span data-ttu-id="2a5fe-115">場合は、アプリケーションは、CLS に準拠する必要はありません、何も変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-115">If your application does not need to be CLS-compliant, you do not need to change anything.</span></span> <span data-ttu-id="2a5fe-116">おく必要がある、コンプライアンス非対応意識ただしします。</span><span class="sxs-lookup"><span data-stu-id="2a5fe-116">You should be aware of its noncompliance, however.</span></span>