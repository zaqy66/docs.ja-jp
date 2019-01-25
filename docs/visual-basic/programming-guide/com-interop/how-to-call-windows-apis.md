---
title: '方法: Windows Api (Visual Basic) を呼び出す'
ms.date: 07/20/2015
helpviewer_keywords:
- API calls [Visual Basic]
- Windows API, calling
- API calls [Visual Basic], platform invoke
- calls [Visual Basic], stored procedures
ms.assetid: 27d75f0a-54ab-4ee1-b91d-43513a19b12d
ms.openlocfilehash: 5db6e299012982024f34d46906de1a3be9b20ff1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650695"
---
# <a name="how-to-call-windows-apis-visual-basic"></a><span data-ttu-id="1cf34-102">方法: Windows Api (Visual Basic) を呼び出す</span><span class="sxs-lookup"><span data-stu-id="1cf34-102">How to: Call Windows APIs (Visual Basic)</span></span>
<span data-ttu-id="1cf34-103">この例を定義し、呼び出し、 `MessageBox` user32.dll 内の関数に文字列を渡します。</span><span class="sxs-lookup"><span data-stu-id="1cf34-103">This example defines and calls the `MessageBox` function in user32.dll and then passes a string to it.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1cf34-104">例</span><span class="sxs-lookup"><span data-stu-id="1cf34-104">Example</span></span>  
 [!code-vb[VbVbalrInterop#1](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/how-to-call-windows-apis_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1cf34-105">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="1cf34-105">Compiling the Code</span></span>  
 <span data-ttu-id="1cf34-106">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1cf34-106">This example requires:</span></span>  
  
-   <span data-ttu-id="1cf34-107"><xref:System> 名前空間への参照</span><span class="sxs-lookup"><span data-stu-id="1cf34-107">A reference to the <xref:System> namespace.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="1cf34-108">信頼性の高いプログラミング</span><span class="sxs-lookup"><span data-stu-id="1cf34-108">Robust Programming</span></span>  
 <span data-ttu-id="1cf34-109">次の条件を満たす場合は、例外が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1cf34-109">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="1cf34-110">メソッドが静的でないするには、抽象クラスでは、または以前に定義します。</span><span class="sxs-lookup"><span data-stu-id="1cf34-110">The method is not static, is abstract, or has been previously defined.</span></span> <span data-ttu-id="1cf34-111">親の種類がインターフェイス、またはの長さ*名前*または*dllName*は 0 です。</span><span class="sxs-lookup"><span data-stu-id="1cf34-111">The parent type is an interface, or the length of *name* or *dllName* is zero.</span></span> <span data-ttu-id="1cf34-112">(<xref:System.ArgumentException>)</span><span class="sxs-lookup"><span data-stu-id="1cf34-112">(<xref:System.ArgumentException>)</span></span>  
  
-   <span data-ttu-id="1cf34-113">*名前*または*dllName*は`Nothing`します。</span><span class="sxs-lookup"><span data-stu-id="1cf34-113">The *name* or *dllName* is `Nothing`.</span></span> <span data-ttu-id="1cf34-114">(<xref:System.ArgumentNullException>)</span><span class="sxs-lookup"><span data-stu-id="1cf34-114">(<xref:System.ArgumentNullException>)</span></span>  
  
-   <span data-ttu-id="1cf34-115">含んでいる型が `CreateType` を使用して以前に作成されています。</span><span class="sxs-lookup"><span data-stu-id="1cf34-115">The containing type has been previously created using `CreateType`.</span></span> <span data-ttu-id="1cf34-116">(<xref:System.InvalidOperationException>)</span><span class="sxs-lookup"><span data-stu-id="1cf34-116">(<xref:System.InvalidOperationException>)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cf34-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cf34-117">See also</span></span>

- [<span data-ttu-id="1cf34-118">プラットフォーム呼び出しの詳細</span><span class="sxs-lookup"><span data-stu-id="1cf34-118">A Closer Look at Platform Invoke</span></span>](../../../framework/interop/consuming-unmanaged-dll-functions.md#a-closer-look-at-platform-invoke)
- [<span data-ttu-id="1cf34-119">プラットフォーム呼び出しの例</span><span class="sxs-lookup"><span data-stu-id="1cf34-119">Platform Invoke Examples</span></span>](../../../framework/interop/platform-invoke-examples.md)
- [<span data-ttu-id="1cf34-120">アンマネージ DLL 関数の処理</span><span class="sxs-lookup"><span data-stu-id="1cf34-120">Consuming Unmanaged DLL Functions</span></span>](../../../framework/interop/consuming-unmanaged-dll-functions.md)
- [<span data-ttu-id="1cf34-121">出力のリフレクションを使用してメソッドを定義します。</span><span class="sxs-lookup"><span data-stu-id="1cf34-121">Defining a Method with Reflection Emit</span></span>](https://msdn.microsoft.com/library/84fd3bf6-628f-41aa-83d9-b990cf926e81)
- [<span data-ttu-id="1cf34-122">チュートリアル: Windows API の呼び出し</span><span class="sxs-lookup"><span data-stu-id="1cf34-122">Walkthrough: Calling Windows APIs</span></span>](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
- [<span data-ttu-id="1cf34-123">COM 相互運用</span><span class="sxs-lookup"><span data-stu-id="1cf34-123">COM Interop</span></span>](../../../visual-basic/programming-guide/com-interop/index.md)
