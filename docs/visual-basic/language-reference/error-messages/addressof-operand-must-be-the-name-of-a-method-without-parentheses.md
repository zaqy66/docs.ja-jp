---
title: '&#39;AddressOf&#39;オペランドは (かっこ) を使用せず、メソッドの名前を指定する必要があります'
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 6f9827d885996ffab8bdab91d0f774a57073e4a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565151"
---
# <a name="39addressof39-operand-must-be-the-name-of-a-method-without-parentheses"></a><span data-ttu-id="ef56b-102">&#39;AddressOf&#39;オペランドは (かっこ) を使用せず、メソッドの名前を指定する必要があります</span><span class="sxs-lookup"><span data-stu-id="ef56b-102">&#39;AddressOf&#39; operand must be the name of a method (without parentheses)</span></span>
<span data-ttu-id="ef56b-103">`AddressOf` 演算子は、特定のプロシージャを参照するプロシージャ デリゲート インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ef56b-103">The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.</span></span> <span data-ttu-id="ef56b-104">構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ef56b-104">The syntax is as follows.</span></span>  
  
 <span data-ttu-id="ef56b-105">`AddressOf` `procedurename`</span><span class="sxs-lookup"><span data-stu-id="ef56b-105">`AddressOf` `procedurename`</span></span>  
  
 <span data-ttu-id="ef56b-106">かっこで囲んで引数以下を挿入した`AddressOf`none は必要に応じて、します。</span><span class="sxs-lookup"><span data-stu-id="ef56b-106">You inserted parentheses around the argument following `AddressOf`, where none are needed.</span></span>  
  
 <span data-ttu-id="ef56b-107">**エラー ID:** BC30577</span><span class="sxs-lookup"><span data-stu-id="ef56b-107">**Error ID:** BC30577</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ef56b-108">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="ef56b-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="ef56b-109">次の引数を囲むかっこを削除`AddressOf`します。</span><span class="sxs-lookup"><span data-stu-id="ef56b-109">Remove the parentheses around the argument following `AddressOf`.</span></span>  
  
2.  <span data-ttu-id="ef56b-110">引数がメソッド名を確認します。</span><span class="sxs-lookup"><span data-stu-id="ef56b-110">Make sure the argument is a method name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef56b-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef56b-111">See also</span></span>
- [<span data-ttu-id="ef56b-112">AddressOf 演算子</span><span class="sxs-lookup"><span data-stu-id="ef56b-112">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="ef56b-113">デリゲート</span><span class="sxs-lookup"><span data-stu-id="ef56b-113">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
