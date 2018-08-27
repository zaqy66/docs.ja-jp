---
title: partial (型) (C# リファレンス)
ms.date: 07/20/2015
f1_keywords:
- partialtype
- partialtype_CSharpKeyword
helpviewer_keywords:
- partial types [C#]
ms.assetid: 27320743-a22e-4c7b-b0b3-53afe3607334
ms.openlocfilehash: 362a02815cb249d57c0bd19706714df1d71644f4
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42929664"
---
# <a name="partial-type-c-reference"></a><span data-ttu-id="4446f-102">partial (型) (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="4446f-102">partial (Type) (C# Reference)</span></span>
<span data-ttu-id="4446f-103">部分型定義では、クラス、構造体、またはインターフェイスの定義を複数のファイルに分割することができます。</span><span class="sxs-lookup"><span data-stu-id="4446f-103">Partial type definitions allow for the definition of a class, struct, or interface to be split into multiple files.</span></span>  
  
 <span data-ttu-id="4446f-104">次に File1.cs の部分型定義を示します。</span><span class="sxs-lookup"><span data-stu-id="4446f-104">In File1.cs:</span></span>  
  
 [!code-csharp[csrefKeywordsContextual#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_1.cs)]  
  
 <span data-ttu-id="4446f-105">次に File2.cs での宣言を示します。</span><span class="sxs-lookup"><span data-stu-id="4446f-105">In File2.cs the declaration:</span></span>  
  
 [!code-csharp[csrefKeywordsContextual#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/partial-type_2.cs)]  
  
## <a name="remarks"></a><span data-ttu-id="4446f-106">コメント</span><span class="sxs-lookup"><span data-stu-id="4446f-106">Remarks</span></span>  
 <span data-ttu-id="4446f-107">クラス型、構造体型、またはインターフェイス型を複数のファイルに分割する操作は、大規模なプロジェクトや、[Windows フォーム デザイナー](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)で自動生成されるコードを処理する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4446f-107">Splitting a class, struct or interface type over several files can be useful when you are working with large projects, or with automatically generated code such as that provided by the [Windows Forms Designer](../../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md).</span></span> <span data-ttu-id="4446f-108">部分型には、[部分メソッド](../../../csharp/language-reference/keywords/partial-method.md)が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4446f-108">A partial type may contain a [partial method](../../../csharp/language-reference/keywords/partial-method.md).</span></span> <span data-ttu-id="4446f-109">詳細については、「[部分クラスと部分メソッド](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4446f-109">For more information, see [Partial Classes and Methods](../../../csharp/programming-guide/classes-and-structs/partial-classes-and-methods.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="4446f-110">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="4446f-110">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4446f-111">参照</span><span class="sxs-lookup"><span data-stu-id="4446f-111">See Also</span></span>

- [<span data-ttu-id="4446f-112">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="4446f-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="4446f-113">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="4446f-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="4446f-114">修飾子</span><span class="sxs-lookup"><span data-stu-id="4446f-114">Modifiers</span></span>](../../../csharp/language-reference/keywords/modifiers.md)  
- [<span data-ttu-id="4446f-115">ジェネリックの概要</span><span class="sxs-lookup"><span data-stu-id="4446f-115">Introduction to Generics</span></span>](../../../csharp/programming-guide/generics/introduction-to-generics.md)
