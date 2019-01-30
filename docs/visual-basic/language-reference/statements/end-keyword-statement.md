---
title: End&lt;keyword&gt;ステートメント (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.EndDefinition
helpviewer_keywords:
- End keyword [Visual Basic]
ms.assetid: 42d6e088-ab0f-4cda-88e8-fdce3e5fcf4f
ms.openlocfilehash: d65c921a1631cd38c4d0d1ab9b34db3d7e43a97e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654842"
---
# <a name="end-ltkeywordgt-statement-visual-basic"></a><span data-ttu-id="dec10-102">End&lt;keyword&gt;ステートメント (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dec10-102">End &lt;keyword&gt; Statement (Visual Basic)</span></span>

<span data-ttu-id="dec10-103">その他のキーワードの後に、そのキーワードによって導入されるステートメント ブロックの定義を終了します。</span><span class="sxs-lookup"><span data-stu-id="dec10-103">When followed by an additional keyword, terminates the definition of the statement block introduced by that keyword.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec10-104">構文</span><span class="sxs-lookup"><span data-stu-id="dec10-104">Syntax</span></span>

```vb
End AddHandler
End Class
End Enum
End Event
End Function
End Get
End If
End Interface
End Module
End Namespace
End Operator
End Property
End RaiseEvent  
End RemoveHandler  
End Select
End Set
End Structure
End Sub
End SyncLock
End Try
End While
End With  
```  
  
## <a name="parts"></a><span data-ttu-id="dec10-105">指定項目</span><span class="sxs-lookup"><span data-stu-id="dec10-105">Parts</span></span>

|<span data-ttu-id="dec10-106">パーツ</span><span class="sxs-lookup"><span data-stu-id="dec10-106">Part</span></span>|<span data-ttu-id="dec10-107">説明</span><span class="sxs-lookup"><span data-stu-id="dec10-107">Description</span></span>|
|---|---|
|`End`|<span data-ttu-id="dec10-108">必須。</span><span class="sxs-lookup"><span data-stu-id="dec10-108">Required.</span></span> <span data-ttu-id="dec10-109">プログラミング要素の定義を終了します。</span><span class="sxs-lookup"><span data-stu-id="dec10-109">Terminates the definition of the programming element.</span></span>|
|`AddHandler`|<span data-ttu-id="dec10-110">終了するために必要な`AddHandler`アクセサーを照合することによって開始された`AddHandler`カスタム ステートメント[Event ステートメント](event-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-110">Required to terminate an `AddHandler` accessor begun by a matching `AddHandler` statement in a custom [Event Statement](event-statement.md).</span></span>|
|`Class`|<span data-ttu-id="dec10-111">照合することによって開始されたクラス定義を終了するために必要な[Class ステートメント](class-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-111">Required to terminate a class definition begun by a matching [Class Statement](class-statement.md).</span></span>|
|`Enum`|<span data-ttu-id="dec10-112">照合することによって開始された列挙の定義を終了するために必要な[Enum ステートメント](enum-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-112">Required to terminate an enumeration definition begun by a matching [Enum Statement](enum-statement.md).</span></span>|
|`Event`|<span data-ttu-id="dec10-113">終了するために必要な`Custom`を照合することによって開始されたイベント定義[Event ステートメント](event-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-113">Required to terminate a `Custom` event definition begun by a matching [Event Statement](event-statement.md).</span></span>|  
|`Function`|<span data-ttu-id="dec10-114">終了するために必要な`Function`プロシージャの定義を照合することによって開始された[Function ステートメント](function-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-114">Required to terminate a `Function` procedure definition begun by a matching [Function Statement](function-statement.md).</span></span> <span data-ttu-id="dec10-115">実行されると、`End Function`ステートメントでは、呼び出し元のコードに制御が戻ります。</span><span class="sxs-lookup"><span data-stu-id="dec10-115">If execution encounters an `End Function` statement, control returns to the calling code.</span></span>|
|`Get`|<span data-ttu-id="dec10-116">終了するために必要な`Property`プロシージャの定義を照合することによって開始された[Get ステートメント](get-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-116">Required to terminate a `Property` procedure definition begun by a matching [Get Statement](get-statement.md).</span></span> <span data-ttu-id="dec10-117">実行されると、`End Get`ステートメントでは、プロパティの値を要求するステートメントに制御が戻ります。</span><span class="sxs-lookup"><span data-stu-id="dec10-117">If execution encounters an `End Get` statement, control returns to the statement requesting the property's value.</span></span>|
|`If`|<span data-ttu-id="dec10-118">終了するために必要な`If`.`Then`...`Else`ブロックを照合することによって開始された定義`If`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="dec10-118">Required to terminate an `If`...`Then`...`Else` block definition begun by a matching `If` statement.</span></span> <span data-ttu-id="dec10-119">参照してください[If...Then...Else ステートメント](if-then-else-statement.md)です。</span><span class="sxs-lookup"><span data-stu-id="dec10-119">See [If...Then...Else Statement](if-then-else-statement.md).</span></span>|
|`Interface`|<span data-ttu-id="dec10-120">照合することによって開始されたインターフェイス定義を終了するために必要な[Interface ステートメント](interface-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-120">Required to terminate an interface definition begun by a matching [Interface Statement](interface-statement.md).</span></span>|
|`Module`|<span data-ttu-id="dec10-121">照合することによって開始されたモジュールの定義を終了するために必要な[Module ステートメント](module-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-121">Required to terminate a module definition begun by a matching [Module Statement](module-statement.md).</span></span>|
|`Namespace`|<span data-ttu-id="dec10-122">照合することによって開始された名前空間の定義を終了するために必要な[Namespace ステートメント](namespace-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-122">Required to terminate a namespace definition begun by a matching [Namespace Statement](namespace-statement.md).</span></span>|
|`Operator`|<span data-ttu-id="dec10-123">照合することによって開始された演算子の定義を終了するために必要な[Operator Statement](operator-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-123">Required to terminate an operator definition begun by a matching [Operator Statement](operator-statement.md).</span></span>|
|`Property`|<span data-ttu-id="dec10-124">照合することによって開始されたプロパティの定義を終了するために必要な[Property ステートメント](property-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-124">Required to terminate a property definition begun by a matching [Property Statement](property-statement.md).</span></span>|
|`RaiseEvent`|<span data-ttu-id="dec10-125">終了するために必要な`RaiseEvent`アクセサーを照合することによって開始された`RaiseEvent`カスタム ステートメント[Event ステートメント](event-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-125">Required to terminate a `RaiseEvent` accessor begun by a matching `RaiseEvent` statement in a custom [Event Statement](event-statement.md).</span></span>|
|`RemoveHandler`|<span data-ttu-id="dec10-126">終了するために必要な`RemoveHandler`アクセサーを照合することによって開始された`RemoveHandler`カスタム ステートメント[Event ステートメント](event-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-126">Required to terminate a `RemoveHandler` accessor begun by a matching `RemoveHandler` statement in a custom [Event Statement](event-statement.md).</span></span>|
|`Select`|<span data-ttu-id="dec10-127">終了するために必要な`Select`.`Case`ブロックを照合することによって開始された定義`Select`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="dec10-127">Required to terminate a `Select`...`Case` block definition begun by a matching `Select` statement.</span></span> <span data-ttu-id="dec10-128">参照してください[Select...Case ステートメント](select-case-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-128">See [Select...Case Statement](select-case-statement.md).</span></span>  
|`Set`|<span data-ttu-id="dec10-129">終了するために必要な`Property`プロシージャの定義を照合することによって開始された[Set ステートメント](set-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-129">Required to terminate a `Property` procedure definition begun by a matching [Set Statement](set-statement.md).</span></span> <span data-ttu-id="dec10-130">実行されると、`End Set`ステートメントでは、プロパティの値を設定するステートメントに制御が戻ります。</span><span class="sxs-lookup"><span data-stu-id="dec10-130">If execution encounters an `End Set` statement, control returns to the statement setting the property's value.</span></span>  
|`Structure`|<span data-ttu-id="dec10-131">照合することによって開始された構造体の定義を終了するために必要な[Structure ステートメント](structure-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-131">Required to terminate a structure definition begun by a matching [Structure Statement](structure-statement.md).</span></span>  
|`Sub`|<span data-ttu-id="dec10-132">終了するために必要な`Sub`プロシージャの定義を照合することによって開始された[Sub ステートメント](sub-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-132">Required to terminate a `Sub` procedure definition begun by a matching [Sub Statement](sub-statement.md).</span></span> <span data-ttu-id="dec10-133">実行されると、`End Sub`ステートメントでは、呼び出し元のコードに制御が戻ります。</span><span class="sxs-lookup"><span data-stu-id="dec10-133">If execution encounters an `End Sub` statement, control returns to the calling code.</span></span>  
|`SyncLock`|<span data-ttu-id="dec10-134">終了するために必要な`SyncLock`ブロックを照合することによって開始された定義`SyncLock`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="dec10-134">Required to terminate a `SyncLock` block definition begun by a matching `SyncLock` statement.</span></span> <span data-ttu-id="dec10-135">参照してください[SyncLock ステートメント](synclock-statement.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-135">See [SyncLock Statement](synclock-statement.md).</span></span>  
|`Try`|<span data-ttu-id="dec10-136">終了するために必要な`Try`.`Catch`...`Finally`ブロックを照合することによって開始された定義`Try`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="dec10-136">Required to terminate a `Try`...`Catch`...`Finally` block definition begun by a matching `Try` statement.</span></span> <span data-ttu-id="dec10-137">[Try...Catch...Finally ステートメント](try-catch-finally-statement.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dec10-137">See [Try...Catch...Finally Statement](try-catch-finally-statement.md).</span></span>  
|`While`|<span data-ttu-id="dec10-138">終了するために必要な`While`ループの定義を照合することによって開始された`While`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="dec10-138">Required to terminate a `While` loop definition begun by a matching `While` statement.</span></span> <span data-ttu-id="dec10-139">参照してください[While...End While ステートメント](while-end-while-statement.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dec10-139">See [While...End While Statement](while-end-while-statement.md).</span></span>  
|`With`| <span data-ttu-id="dec10-140">終了するために必要な`With`ブロックを照合することによって開始された定義`With`ステートメント。</span><span class="sxs-lookup"><span data-stu-id="dec10-140">Required to terminate a `With` block definition begun by a matching `With` statement.</span></span> <span data-ttu-id="dec10-141">[With...End With ステートメント](with-end-with-statement.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dec10-141">See [With...End With Statement](with-end-with-statement.md).</span></span>  
|||
  
## <a name="directives"></a><span data-ttu-id="dec10-142">ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="dec10-142">Directives</span></span>

<span data-ttu-id="dec10-143">シャープ記号に続く場合 (`#`)、`End`キーワードに対応するディレクティブによって導入されるプリプロセッサ ブロックが終了します。</span><span class="sxs-lookup"><span data-stu-id="dec10-143">When preceded by a number sign (`#`), the `End` keyword terminates a preprocessing block introduced by the corresponding directive.</span></span>  

```vb
#End ExternalSource
#End If
#End Region
```

|<span data-ttu-id="dec10-144">パーツ</span><span class="sxs-lookup"><span data-stu-id="dec10-144">Part</span></span>|<span data-ttu-id="dec10-145">説明</span><span class="sxs-lookup"><span data-stu-id="dec10-145">Description</span></span>|
|---|---|
|`#End`|<span data-ttu-id="dec10-146">必須。</span><span class="sxs-lookup"><span data-stu-id="dec10-146">Required.</span></span> <span data-ttu-id="dec10-147">処理前のブロックの定義を終了します。</span><span class="sxs-lookup"><span data-stu-id="dec10-147">Terminates the definition of the preprocessing block.</span></span>|
|`ExternalSource`|<span data-ttu-id="dec10-148">照合することによって開始された、外部ソース ブロックを終了するために必要な[#ExternalSource ディレクティブ](../directives/externalsource-directive.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-148">Required to terminate an external source block begun by a matching [#ExternalSource Directive](../directives/externalsource-directive.md).</span></span>|
|`If`|<span data-ttu-id="dec10-149">照合することによって開始された条件付きコンパイル ブロックを終了するために必要な`#If`ディレクティブ。</span><span class="sxs-lookup"><span data-stu-id="dec10-149">Required to terminate a conditional compilation block begun by a matching `#If` directive.</span></span> <span data-ttu-id="dec10-150">参照してください[#If.Then... #Else ディレクティブ](../directives/if-then-else-directives.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-150">See [#If...Then...#Else Directives](../directives/if-then-else-directives.md).</span></span>|
|`Region`|<span data-ttu-id="dec10-151">照合することによって開始されたソース リージョンのブロックを終了するために必要な[#Region ディレクティブ](../directives/region-directive.md)します。</span><span class="sxs-lookup"><span data-stu-id="dec10-151">Required to terminate a source region block begun by a matching [#Region Directive](../directives/region-directive.md).</span></span>|
|||

## <a name="remarks"></a><span data-ttu-id="dec10-152">Remarks</span><span class="sxs-lookup"><span data-stu-id="dec10-152">Remarks</span></span>

<span data-ttu-id="dec10-153">[End ステートメント](end-statement.md)をその他のキーワードを使用せずにすぐに実行を終了します。</span><span class="sxs-lookup"><span data-stu-id="dec10-153">The [End Statement](end-statement.md), without an additional keyword, terminates execution immediately.</span></span>

## <a name="smart-device-developer-notes"></a><span data-ttu-id="dec10-154">スマート デバイスの開発者向け注意事項</span><span class="sxs-lookup"><span data-stu-id="dec10-154">Smart Device Developer Notes</span></span>  

<span data-ttu-id="dec10-155">`End`その他のキーワードを使用せず、ステートメントはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="dec10-155">The `End` statement, without an additional keyword, is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dec10-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="dec10-156">See also</span></span>

- [<span data-ttu-id="dec10-157">End ステートメント</span><span class="sxs-lookup"><span data-stu-id="dec10-157">End Statement</span></span>](end-statement.md)
