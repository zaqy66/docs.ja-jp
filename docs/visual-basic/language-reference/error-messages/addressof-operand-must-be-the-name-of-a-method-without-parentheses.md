---
title: "'AddressOf' オペランドはメソッドの名前でなければなりません。かっこは不要です。"
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 37b02ab76730458b757835fda37b8cb145ed93ad
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262115"
---
# <a name="addressof-operand-must-be-the-name-of-a-method-without-parentheses"></a><span data-ttu-id="c97e2-102">'AddressOf' オペランドはメソッドの名前でなければなりません。かっこは不要です。</span><span class="sxs-lookup"><span data-stu-id="c97e2-102">'AddressOf' operand must be the name of a method (without parentheses)</span></span>
<span data-ttu-id="c97e2-103">`AddressOf` 演算子は、特定のプロシージャを参照するプロシージャ デリゲート インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="c97e2-103">The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.</span></span> <span data-ttu-id="c97e2-104">構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c97e2-104">The syntax is as follows.</span></span>  
  
 <span data-ttu-id="c97e2-105">`AddressOf` `procedurename`</span><span class="sxs-lookup"><span data-stu-id="c97e2-105">`AddressOf` `procedurename`</span></span>  
  
 <span data-ttu-id="c97e2-106">かっこで囲んで引数以下を挿入した`AddressOf`none は必要に応じて、します。</span><span class="sxs-lookup"><span data-stu-id="c97e2-106">You inserted parentheses around the argument following `AddressOf`, where none are needed.</span></span>  
  
 <span data-ttu-id="c97e2-107">**エラー ID:** BC30577</span><span class="sxs-lookup"><span data-stu-id="c97e2-107">**Error ID:** BC30577</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c97e2-108">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="c97e2-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="c97e2-109">次の引数を囲むかっこを削除`AddressOf`します。</span><span class="sxs-lookup"><span data-stu-id="c97e2-109">Remove the parentheses around the argument following `AddressOf`.</span></span>  
  
2.  <span data-ttu-id="c97e2-110">引数がメソッド名を確認します。</span><span class="sxs-lookup"><span data-stu-id="c97e2-110">Make sure the argument is a method name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c97e2-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="c97e2-111">See also</span></span>
- [<span data-ttu-id="c97e2-112">AddressOf 演算子</span><span class="sxs-lookup"><span data-stu-id="c97e2-112">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="c97e2-113">デリゲート</span><span class="sxs-lookup"><span data-stu-id="c97e2-113">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
