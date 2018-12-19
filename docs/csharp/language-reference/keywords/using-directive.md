---
title: using ディレクティブ - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- using directive [C#]
ms.assetid: b42b8e61-5e7e-439c-bb71-370094b44ae8
ms.openlocfilehash: b58467953096c26d13f4c837f13548876e645f08
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240321"
---
# <a name="using-directive-c-reference"></a><span data-ttu-id="bfaf9-102">using ディレクティブ (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="bfaf9-102">using Directive (C# Reference)</span></span>
<span data-ttu-id="bfaf9-103">`using` ディレクティブは、次の 3 つの用途で使用します。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-103">The `using` directive has three uses:</span></span>  
  
-   <span data-ttu-id="bfaf9-104">名前空間で型の使用を許可する場合。これにより、その名前空間内では型を修飾せずに使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-104">To allow the use of types in a namespace so that you do not have to qualify the use of a type in that namespace:</span></span>  
  
    ```csharp  
    using System.Text;  
    ```  
  
-   <span data-ttu-id="bfaf9-105">アクセスを型名で修飾することなく、型の静的メンバーおよび入れ子にされた型へのアクセスを許可する場合。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-105">To allow you to access static members and nested types of a type without having to qualify the access with the type name.</span></span> 
  
    ```csharp  
    using static System.Math;  
    ```  
     
    <span data-ttu-id="bfaf9-106">詳細については、「[using static ディレクティブ](using-static.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-106">For more information, see the [using static directive](using-static.md).</span></span>

-   <span data-ttu-id="bfaf9-107">名前空間または型のエイリアスを作成する場合。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-107">To create an alias for a namespace or a type.</span></span> <span data-ttu-id="bfaf9-108">これは "*using エイリアス ディレクティブ*" と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-108">This is called a *using alias directive*.</span></span>  
  
    ```csharp  
    using Project = PC.MyCompany.Project;  
    ```  
  
 <span data-ttu-id="bfaf9-109">`using` キーワードは、*using ステートメント*の作成にも使用します。ファイルやフォントなどの <xref:System.IDisposable> オブジェクトを正しく処理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-109">The `using` keyword is also used to create *using statements*, which help ensure that <xref:System.IDisposable> objects such as files and fonts are handled correctly.</span></span> <span data-ttu-id="bfaf9-110">詳しくは、「[using ステートメント](../../../csharp/language-reference/keywords/using-statement.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-110">See [using Statement](../../../csharp/language-reference/keywords/using-statement.md) for more information.</span></span>  
  
## <a name="using-static-type"></a><span data-ttu-id="bfaf9-111">using static 型</span><span class="sxs-lookup"><span data-stu-id="bfaf9-111">Using Static Type</span></span>  
 <span data-ttu-id="bfaf9-112">アクセスを型名で修飾することなく型の静的メンバーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-112">You can access static members of a type without having to qualify the access with the type name:</span></span>  
  
```csharp  
using static System.Console;   
using static System.Math;  
class Program   
{   
    static void Main()   
    {   
        WriteLine(Sqrt(3*3 + 4*4));   
    }   
}  
```  
  
## <a name="remarks"></a><span data-ttu-id="bfaf9-113">コメント</span><span class="sxs-lookup"><span data-stu-id="bfaf9-113">Remarks</span></span>  
 <span data-ttu-id="bfaf9-114">`using` ディレクティブのスコープは、このディレクティブが存在するファイルに限定されます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-114">The scope of a `using` directive is limited to the file in which it appears.</span></span>
 
 <span data-ttu-id="bfaf9-115">`using` ディレクティブは、次のように記述することができます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-115">The `using` directive can appear:</span></span>
- <span data-ttu-id="bfaf9-116">ソース コード ファイルの先頭、任意の名前空間または型定義の前。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-116">At the beginning of a source code file, before any namespace or type definitions.</span></span>
- <span data-ttu-id="bfaf9-117">任意の名前空間内、ただし、この名前空間内で宣言された任意の名前空間または型の前。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-117">In any namespace, but before any namespace or types declared in this namespace.</span></span>

<span data-ttu-id="bfaf9-118">それ以外の場合は、コンパイラ エラー [CS1529](../../misc/cs1529.md) が生成されます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-118">Otherwise, compiler error [CS1529](../../misc/cs1529.md) is generated.</span></span>
  
 <span data-ttu-id="bfaf9-119">`using` 別名ディレクティブを作成すると、名前空間または型の識別子を修飾しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-119">Create a `using` alias directive to make it easier to qualify an identifier to a namespace or type.</span></span> <span data-ttu-id="bfaf9-120">いずれの `using` ディレクティブにおいても、前に置かれる `using` に関係なく、完全に修飾された名前空間または型を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-120">In any `using` directive, the fully-qualified namespace or type must be used regardless of the `using` directives that come before it.</span></span> <span data-ttu-id="bfaf9-121">`using` ディレクティブの宣言内では、`using` 別名を使用することができません。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-121">No `using` alias can be used in the declaration of a `using` directive.</span></span> <span data-ttu-id="bfaf9-122">たとえば、次の場合はコンパイラ エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-122">For example, the following generates a compiler error:</span></span>
 ```csharp
 using s = System.Text;
 using s.RegularExpressions; 
 ```
  
 <span data-ttu-id="bfaf9-123">`using` ディレクティブを作成すると、名前空間内の型を、名前空間を指定することなく使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-123">Create a `using` directive to use the types in a namespace without having to specify the namespace.</span></span> <span data-ttu-id="bfaf9-124">`using` ディレクティブでは、指定した名前空間に入れ子になった別の名前空間へのアクセスは許可されません。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-124">A `using` directive does not give you access to any namespaces that are nested in the namespace you specify.</span></span>  
  
 <span data-ttu-id="bfaf9-125">名前空間は、ユーザー定義とシステム定義の 2 つのカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-125">Namespaces come in two categories: user-defined and system-defined.</span></span> <span data-ttu-id="bfaf9-126">ユーザー定義の名前空間は、コードで定義された名前空間です。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-126">User-defined namespaces are namespaces defined in your code.</span></span> <span data-ttu-id="bfaf9-127">システム定義の名前空間の一覧については、「[.NET API ブラウザー](https://docs.microsoft.com/dotnet/api/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-127">For a list of the system-defined namespaces, see [.NET API Browser](https://docs.microsoft.com/dotnet/api/).</span></span>  
  
 <span data-ttu-id="bfaf9-128">他のアセンブリのメソッドを参照する方法の例については、[コマンド ラインでアセンブリを作成し、使用する](../../programming-guide/concepts/assemblies-gac/how-to-create-and-use-assemblies-using-the-command-line.md)方法に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-128">For examples on referencing methods in other assemblies, see [Create and Use Assemblies Using the Command Line](../../programming-guide/concepts/assemblies-gac/how-to-create-and-use-assemblies-using-the-command-line.md).</span></span>  
  
## <a name="example-1"></a><span data-ttu-id="bfaf9-129">例 1</span><span class="sxs-lookup"><span data-stu-id="bfaf9-129">Example 1</span></span>  
  
 <span data-ttu-id="bfaf9-130">次の例は、名前空間の `using` エイリアスを定義して使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-130">The following example shows how to define and use a `using` alias for a namespace:</span></span>  
  
 [!code-csharp[csrefKeywordsNamespace#8](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-directive_1.cs)]  
  
 <span data-ttu-id="bfaf9-131">using エイリアス ディレクティブの右側には、オープン ジェネリック型を配置できません。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-131">A using alias directive cannot have an open generic type on the right hand side.</span></span> <span data-ttu-id="bfaf9-132">たとえば、List\<T> の using エイリアスを作成することはできませんが、List\<int> の using エイリアスは作成できます。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-132">For example, you cannot create a using alias for a List\<T>, but you can create one for a List\<int>.</span></span>  
  
## <a name="example-2"></a><span data-ttu-id="bfaf9-133">例 2</span><span class="sxs-lookup"><span data-stu-id="bfaf9-133">Example 2</span></span>  
  
 <span data-ttu-id="bfaf9-134">次の例は、クラスの `using` ディレクティブと `using` エイリアスを定義する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bfaf9-134">The following example shows how to define a `using` directive and a `using` alias for a class:</span></span>  
  
 [!code-csharp[csrefKeywordsNamespace#9](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-directive_2.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="bfaf9-135">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="bfaf9-135">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bfaf9-136">参照</span><span class="sxs-lookup"><span data-stu-id="bfaf9-136">See Also</span></span>

- [<span data-ttu-id="bfaf9-137">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="bfaf9-137">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="bfaf9-138">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="bfaf9-138">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="bfaf9-139">名前空間の使用</span><span class="sxs-lookup"><span data-stu-id="bfaf9-139">Using Namespaces</span></span>](../../../csharp/programming-guide/namespaces/using-namespaces.md)  
- [<span data-ttu-id="bfaf9-140">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="bfaf9-140">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="bfaf9-141">名前空間キーワード</span><span class="sxs-lookup"><span data-stu-id="bfaf9-141">Namespace Keywords</span></span>](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [<span data-ttu-id="bfaf9-142">名前空間</span><span class="sxs-lookup"><span data-stu-id="bfaf9-142">Namespaces</span></span>](../../../csharp/programming-guide/namespaces/index.md)  
- [<span data-ttu-id="bfaf9-143">using ステートメント</span><span class="sxs-lookup"><span data-stu-id="bfaf9-143">using Statement</span></span>](../../../csharp/language-reference/keywords/using-statement.md)
