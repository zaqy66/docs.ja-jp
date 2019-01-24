---
title: プロシージャのオーバーロード (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- signatures
- Overloads keyword [Visual Basic]
- hiding by signature
- Visual Basic code, procedures
- procedures [Visual Basic], signatures for
- procedures [Visual Basic], overloading
- procedures [Visual Basic], multiple versions
- parameters [Visual Basic], lists
- signatures [Visual Basic], procedure
- parameter lists [Visual Basic]
- Visual Basic code, parameter lists
- Shadows keyword [Visual Basic]
- procedure overloading
- procedures [Visual Basic], parameter lists
ms.assetid: fbc7fb18-e3b2-48b6-b554-64c00ed09d2a
ms.openlocfilehash: 3cb11079241da4815c6e7bde4a76123965a95514
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54712523"
---
# <a name="procedure-overloading-visual-basic"></a><span data-ttu-id="ec1cc-102">プロシージャのオーバーロード (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ec1cc-102">Procedure Overloading (Visual Basic)</span></span>
<span data-ttu-id="ec1cc-103">*オーバー ロード*プロシージャでは、異なるパラメーター リストが同じ名前を使用して、複数のバージョンを定義することを意味します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-103">*Overloading* a procedure means defining it in multiple versions, using the same name but different parameter lists.</span></span> <span data-ttu-id="ec1cc-104">オーバー ロードの目的では、名前で区別せずに密接に関連するいくつかのバージョンのプロシージャを定義します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-104">The purpose of overloading is to define several closely related versions of a procedure without having to differentiate them by name.</span></span> <span data-ttu-id="ec1cc-105">パラメーター リストをさまざまなこれを行います。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-105">You do this by varying the parameter list.</span></span>  
  
## <a name="overloading-rules"></a><span data-ttu-id="ec1cc-106">オーバー ロードの規則</span><span class="sxs-lookup"><span data-stu-id="ec1cc-106">Overloading Rules</span></span>  
 <span data-ttu-id="ec1cc-107">プロシージャをオーバー ロードする場合は、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-107">When you overload a procedure, the following rules apply:</span></span>  
  
-   <span data-ttu-id="ec1cc-108">**同じ名前**します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-108">**Same Name**.</span></span> <span data-ttu-id="ec1cc-109">各オーバー ロードされたバージョンでは、同じプロシージャ名を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-109">Each overloaded version must use the same procedure name.</span></span>  
  
-   <span data-ttu-id="ec1cc-110">**異なる署名**します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-110">**Different Signature**.</span></span> <span data-ttu-id="ec1cc-111">各オーバー ロードされたバージョンは、次のうちの少なくとも 1 つにその他のすべてのオーバー ロードされたバージョンと異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-111">Each overloaded version must differ from all other overloaded versions in at least one of the following respects:</span></span>  
  
    -   <span data-ttu-id="ec1cc-112">パラメーターの数</span><span class="sxs-lookup"><span data-stu-id="ec1cc-112">Number of parameters</span></span>  
  
    -   <span data-ttu-id="ec1cc-113">パラメーターの順序</span><span class="sxs-lookup"><span data-stu-id="ec1cc-113">Order of the parameters</span></span>  
  
    -   <span data-ttu-id="ec1cc-114">パラメーターのデータ型</span><span class="sxs-lookup"><span data-stu-id="ec1cc-114">Data types of the parameters</span></span>  
  
    -   <span data-ttu-id="ec1cc-115">(ジェネリック プロシージャの場合) の型パラメーターの数</span><span class="sxs-lookup"><span data-stu-id="ec1cc-115">Number of type parameters (for a generic procedure)</span></span>  
  
    -   <span data-ttu-id="ec1cc-116">戻り値の型 (変換演算子) の場合のみ</span><span class="sxs-lookup"><span data-stu-id="ec1cc-116">Return type (only for a conversion operator)</span></span>  
  
     <span data-ttu-id="ec1cc-117">プロシージャ名、と共に、上記の項目は、総称、*署名*プロシージャのです。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-117">Together with the procedure name, the preceding items are collectively called the *signature* of the procedure.</span></span> <span data-ttu-id="ec1cc-118">オーバー ロードされたプロシージャを呼び出すときに、コンパイラは、呼び出しが、定義を正しくと一致することを確認するのに署名を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-118">When you call an overloaded procedure, the compiler uses the signature to check that the call correctly matches the definition.</span></span>  
  
-   <span data-ttu-id="ec1cc-119">**シグネチャの一部ではない項目**します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-119">**Items Not Part of Signature**.</span></span> <span data-ttu-id="ec1cc-120">シグネチャを変更せず、プロシージャをオーバー ロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-120">You cannot overload a procedure without varying the signature.</span></span> <span data-ttu-id="ec1cc-121">具体的には、プロシージャをオーバー ロードするだけで、次のものの 1 つ以上ことはできません。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-121">In particular, you cannot overload a procedure by varying only one or more of the following items:</span></span>  
  
    -   <span data-ttu-id="ec1cc-122">プロシージャ修飾子キーワードなど`Public`、`Shared`と `Static`</span><span class="sxs-lookup"><span data-stu-id="ec1cc-122">Procedure modifier keywords, such as `Public`, `Shared`, and `Static`</span></span>  
  
    -   <span data-ttu-id="ec1cc-123">パラメーターまたは型パラメーター名</span><span class="sxs-lookup"><span data-stu-id="ec1cc-123">Parameter or type parameter names</span></span>  
  
    -   <span data-ttu-id="ec1cc-124">(ジェネリック プロシージャの場合) の型パラメーターの制約</span><span class="sxs-lookup"><span data-stu-id="ec1cc-124">Type parameter constraints (for a generic procedure)</span></span>  
  
    -   <span data-ttu-id="ec1cc-125">パラメーター修飾子キーワードなど`ByRef`と `Optional`</span><span class="sxs-lookup"><span data-stu-id="ec1cc-125">Parameter modifier keywords, such as `ByRef` and `Optional`</span></span>  
  
    -   <span data-ttu-id="ec1cc-126">値を返すかどうか</span><span class="sxs-lookup"><span data-stu-id="ec1cc-126">Whether it returns a value</span></span>  
  
    -   <span data-ttu-id="ec1cc-127">(変換演算子) を除く、戻り値のデータ型</span><span class="sxs-lookup"><span data-stu-id="ec1cc-127">The data type of the return value (except for a conversion operator)</span></span>  
  
     <span data-ttu-id="ec1cc-128">上記のリスト項目は、シグネチャの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-128">The items in the preceding list are not part of the signature.</span></span> <span data-ttu-id="ec1cc-129">オーバー ロードされたバージョンを区別するために、それらを使用することはできませんは、そのシグネチャで区別する、オーバー ロードされたバージョン間で異なることができます。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-129">Although you cannot use them to differentiate between overloaded versions, you can vary them among overloaded versions that are properly differentiated by their signatures.</span></span>  
  
-   <span data-ttu-id="ec1cc-130">**遅延バインディング引数**します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-130">**Late-Bound Arguments**.</span></span> <span data-ttu-id="ec1cc-131">として適切なパラメーターを宣言する必要があります、オーバー ロードされたバージョンに遅延バインディング オブジェクト変数を渡す場合は、<xref:System.Object>します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-131">If you intend to pass a late bound object variable to an overloaded version, you must declare the appropriate parameter as <xref:System.Object>.</span></span>  
  
## <a name="multiple-versions-of-a-procedure"></a><span data-ttu-id="ec1cc-132">プロシージャの複数のバージョン</span><span class="sxs-lookup"><span data-stu-id="ec1cc-132">Multiple Versions of a Procedure</span></span>  
 <span data-ttu-id="ec1cc-133">作成すると、`Sub`に対して顧客のバランスでは、トランザクションをポストするプロシージャが名またはアカウントの数のいずれかを顧客に参照することができるようにします。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-133">Suppose you are writing a `Sub` procedure to post a transaction against a customer's balance, and you want to be able to refer to the customer either by name or by account number.</span></span> <span data-ttu-id="ec1cc-134">これに合わせて、2 つの異なる定義できます`Sub`手順については、次の例のように。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-134">To accommodate this, you can define two different `Sub` procedures, as in the following example:</span></span>  
  
 [!code-vb[VbVbcnProcedures#73](./codesnippet/VisualBasic/procedure-overloading_1.vb)]  
  
### <a name="overloaded-versions"></a><span data-ttu-id="ec1cc-135">オーバー ロードされたバージョン</span><span class="sxs-lookup"><span data-stu-id="ec1cc-135">Overloaded Versions</span></span>  
 <span data-ttu-id="ec1cc-136">別の方法では、1 つのプロシージャ名をオーバー ロードします。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-136">An alternative is to overload a single procedure name.</span></span> <span data-ttu-id="ec1cc-137">使用することができます、[オーバー ロード](../../../../visual-basic/language-reference/modifiers/overloads.md)キーワードを次のように各パラメーター一覧については、プロシージャのバージョンを定義します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-137">You can use the [Overloads](../../../../visual-basic/language-reference/modifiers/overloads.md) keyword to define a version of the procedure for each parameter list, as follows:</span></span>  
  
 [!code-vb[VbVbcnProcedures#72](./codesnippet/VisualBasic/procedure-overloading_2.vb)]  
  
#### <a name="additional-overloads"></a><span data-ttu-id="ec1cc-138">追加のオーバー ロード</span><span class="sxs-lookup"><span data-stu-id="ec1cc-138">Additional Overloads</span></span>  
 <span data-ttu-id="ec1cc-139">いずれかでトランザクションの量をそのまま使用したい場合`Decimal`または`Single`、オーバー ロードすることがさらに`post`このバリエーションの 1 つを許可します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-139">If you also wanted to accept a transaction amount in either `Decimal` or `Single`, you could further overload `post` to allow for this variation.</span></span> <span data-ttu-id="ec1cc-140">これを実行した場合に上記の例ではオーバー ロードごとに、4 つ必要がある`Sub`4 つの異なるシグネチャを持つが、同じ名前のすべての手順。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-140">If you did this to each of the overloads in the preceding example, you would have four `Sub` procedures, all with the same name but with four different signatures.</span></span>  
  
## <a name="advantages-of-overloading"></a><span data-ttu-id="ec1cc-141">オーバー ロードの利点</span><span class="sxs-lookup"><span data-stu-id="ec1cc-141">Advantages of Overloading</span></span>  
 <span data-ttu-id="ec1cc-142">プロシージャのオーバー ロードの利点は、呼び出しの柔軟性です。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-142">The advantage of overloading a procedure is in the flexibility of the call.</span></span> <span data-ttu-id="ec1cc-143">使用する、`post`プロシージャ宣言の前の例では、呼び出し元のコードは、いずれか、顧客 id を取得できます、`String`または`Integer`、いずれの場合も同じ手順を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-143">To use the `post` procedure declared in the preceding example, the calling code can obtain the customer identification as either a `String` or an `Integer`, and then call the same procedure in either case.</span></span> <span data-ttu-id="ec1cc-144">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-144">The following example illustrates this:</span></span>  
  
 [!code-vb[VbVbcnProcedures#56](./codesnippet/VisualBasic/procedure-overloading_3.vb)]  
  
 [!code-vb[VbVbcnProcedures#57](./codesnippet/VisualBasic/procedure-overloading_4.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="ec1cc-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec1cc-145">See also</span></span>
- [<span data-ttu-id="ec1cc-146">プロシージャ</span><span class="sxs-lookup"><span data-stu-id="ec1cc-146">Procedures</span></span>](./index.md)
- [<span data-ttu-id="ec1cc-147">方法: 複数のバージョンのプロシージャを定義します。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-147">How to: Define Multiple Versions of a Procedure</span></span>](./how-to-define-multiple-versions-of-a-procedure.md)
- [<span data-ttu-id="ec1cc-148">方法: オーバー ロードされたプロシージャを呼び出す</span><span class="sxs-lookup"><span data-stu-id="ec1cc-148">How to: Call an Overloaded Procedure</span></span>](./how-to-call-an-overloaded-procedure.md)
- [<span data-ttu-id="ec1cc-149">方法: 省略可能なパラメーターを受け取るプロシージャをオーバー ロードします。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-149">How to: Overload a Procedure that Takes Optional Parameters</span></span>](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [<span data-ttu-id="ec1cc-150">方法: 不特定数のパラメーターを受け取るプロシージャをオーバー ロードします。</span><span class="sxs-lookup"><span data-stu-id="ec1cc-150">How to: Overload a Procedure that Takes an Indefinite Number of Parameters</span></span>](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)
- [<span data-ttu-id="ec1cc-151">プロシージャのオーバーロードに関する注意事項</span><span class="sxs-lookup"><span data-stu-id="ec1cc-151">Considerations in Overloading Procedures</span></span>](./considerations-in-overloading-procedures.md)
- [<span data-ttu-id="ec1cc-152">オーバーロードの解決</span><span class="sxs-lookup"><span data-stu-id="ec1cc-152">Overload Resolution</span></span>](./overload-resolution.md)
- [<span data-ttu-id="ec1cc-153">オーバーロード</span><span class="sxs-lookup"><span data-stu-id="ec1cc-153">Overloads</span></span>](../../../../visual-basic/language-reference/modifiers/overloads.md)
- [<span data-ttu-id="ec1cc-154">Visual Basic におけるジェネリック型</span><span class="sxs-lookup"><span data-stu-id="ec1cc-154">Generic Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
