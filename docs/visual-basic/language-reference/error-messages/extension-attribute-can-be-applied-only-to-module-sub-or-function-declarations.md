---
title: "'Extension' 属性は 'Module'、'Sub'、または 'Function' の各宣言にのみ適用できます"
ms.date: 07/20/2015
f1_keywords:
- bc36550
- vbc36550
helpviewer_keywords:
- BC36550
ms.assetid: 4387a51f-733c-45d7-abdb-eb64d4f51078
ms.openlocfilehash: e2e2c41d713b0b04b8bc7208a83d059f0d16bf06
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278721"
---
# <a name="extension-attribute-can-be-applied-only-to-module-sub-or-function-declarations"></a><span data-ttu-id="de5da-102">'Extension' 属性は 'Module'、'Sub'、または 'Function' の各宣言にのみ適用できます</span><span class="sxs-lookup"><span data-stu-id="de5da-102">'Extension' attribute can be applied only to 'Module', 'Sub', or 'Function' declarations</span></span>
<span data-ttu-id="de5da-103">Visual Basic でのデータ型を拡張する唯一の方法では、標準のモジュール内で拡張メソッドを定義します。</span><span class="sxs-lookup"><span data-stu-id="de5da-103">The only way to extend a data type in Visual Basic is to define an extension method inside a standard module.</span></span> <span data-ttu-id="de5da-104">拡張メソッドになる、`Sub`プロシージャまたは`Function`プロシージャ。</span><span class="sxs-lookup"><span data-stu-id="de5da-104">The extension method can be a `Sub` procedure or a `Function` procedure.</span></span> <span data-ttu-id="de5da-105">すべての拡張メソッドは、拡張機能の属性でマークする必要があります`<Extension()>`から、<xref:System.Runtime.CompilerServices?displayProperty=nameWithType>名前空間。</span><span class="sxs-lookup"><span data-stu-id="de5da-105">All extension methods must be marked with the extension attribute, `<Extension()>`, from the <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="de5da-106">必要に応じて、拡張メソッドを含むモジュールの場合は、同じ方法でマークされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="de5da-106">Optionally, a module that contains an extension method may be marked in the same way.</span></span> <span data-ttu-id="de5da-107">拡張属性の他の使用が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="de5da-107">No other use of the extension attribute is valid.</span></span>  
  
 <span data-ttu-id="de5da-108">**エラー ID:** BC36550</span><span class="sxs-lookup"><span data-stu-id="de5da-108">**Error ID:** BC36550</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="de5da-109">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="de5da-109">To correct this error</span></span>  
  
-   <span data-ttu-id="de5da-110">拡張属性を削除します。</span><span class="sxs-lookup"><span data-stu-id="de5da-110">Remove the extension attribute.</span></span>  
  
-   <span data-ttu-id="de5da-111">外側のモジュールで定義されている、方法として、拡張機能を再設計します。</span><span class="sxs-lookup"><span data-stu-id="de5da-111">Redesign your extension as a method, defined in an enclosing module.</span></span>  
  
## <a name="example"></a><span data-ttu-id="de5da-112">例</span><span class="sxs-lookup"><span data-stu-id="de5da-112">Example</span></span>  
 <span data-ttu-id="de5da-113">次の例では、定義、`Print`のメソッド、`String`データ型。</span><span class="sxs-lookup"><span data-stu-id="de5da-113">The following example defines a `Print` method for the `String` data type.</span></span>  
  
```  
Imports StringUtility  
Imports System.Runtime.CompilerServices  
Namespace StringUtility  
    <Extension()>   
    Module StringExtensions  
        <Extension()>   
        Public Sub Print (ByVal str As String)  
            Console.WriteLine(str)  
        End Sub  
    End Module  
End Namespace  
```  
  
## <a name="see-also"></a><span data-ttu-id="de5da-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="de5da-114">See also</span></span>
- [<span data-ttu-id="de5da-115">属性の概要</span><span class="sxs-lookup"><span data-stu-id="de5da-115">Attributes overview</span></span>](../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [<span data-ttu-id="de5da-116">拡張メソッド</span><span class="sxs-lookup"><span data-stu-id="de5da-116">Extension Methods</span></span>](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)
- [<span data-ttu-id="de5da-117">Module ステートメント</span><span class="sxs-lookup"><span data-stu-id="de5da-117">Module Statement</span></span>](../../../visual-basic/language-reference/statements/module-statement.md)
