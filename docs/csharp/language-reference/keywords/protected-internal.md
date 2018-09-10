---
title: protected internal (C# リファレンス)
ms.date: 11/15/2017
author: sputier
ms.openlocfilehash: 1a305cb84989f12350e2e7cc28dd18f9d0c7ae5e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2018
ms.locfileid: "44200211"
---
# <a name="protected-internal-c-reference"></a><span data-ttu-id="42e7c-102">protected internal (C# リファレンス)</span><span class="sxs-lookup"><span data-stu-id="42e7c-102">protected internal (C# Reference)</span></span>

<span data-ttu-id="42e7c-103">キーワード組み合わせ `protected internal` はメンバー アクセス修飾子です。</span><span class="sxs-lookup"><span data-stu-id="42e7c-103">The `protected internal` keyword combination is a member access modifier.</span></span> <span data-ttu-id="42e7c-104">protected internal メンバーには、現在のアセンブリから、または包含クラスから派生した型からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="42e7c-104">A protected internal member is accessible from the current assembly or from types that are derived from the containing class.</span></span> <span data-ttu-id="42e7c-105">`protected internal` と他のアクセス修飾子の比較については、「[アクセシビリティ レベル](accessibility-levels.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42e7c-105">For a comparison of `protected internal` with the other access modifiers, see [Accessibility Levels](accessibility-levels.md).</span></span>

## <a name="example"></a><span data-ttu-id="42e7c-106">例</span><span class="sxs-lookup"><span data-stu-id="42e7c-106">Example</span></span>

<span data-ttu-id="42e7c-107">基底クラスのプロテクト内部メンバーは、包含アセンブリ内の任意の型からアクセスします。</span><span class="sxs-lookup"><span data-stu-id="42e7c-107">A protected internal member of a base class is accessible from any type within its containing assembly.</span></span> <span data-ttu-id="42e7c-108">派生クラス型の変数経由でアクセスする場合にのみ、別のアセンブリにある派生クラスでもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="42e7c-108">It is also accessible in a derived class located in another assembly only if the access occurs through a variable of the derived class type.</span></span> <span data-ttu-id="42e7c-109">たとえば、次のコード セグメントを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="42e7c-109">For example, consider the following code segment:</span></span>

```csharp
// Assembly1.cs
// Compile with: /target:library
public class BaseClass
{
   protected internal int myValue = 0;
}

class TestAccess
{
    void Access()
    {
        BaseClass baseObject = new BaseClass();
        baseObject.myValue = 5;
    }
}
```

```csharp
// Assembly2.cs
// Compile with: /reference:Assembly1.dll
class DerivedClass : BaseClass
{
    static void Main()
    {
        BaseClass baseObject = new BaseClass();
        DerivedClass derivedObject = new DerivedClass();

        // Error CS1540, because myValue can only be accessed by
        // classes derived from BaseClass.
        // baseObject.myValue = 10;

        // OK, because this class derives from BaseClass.
        derivedObject.myValue = 10;
    }
}
```
<span data-ttu-id="42e7c-110">この例には、2 つのファイル (`Assembly1.cs` と `Assembly2.cs`) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="42e7c-110">This example contains two files, `Assembly1.cs` and `Assembly2.cs`.</span></span>
<span data-ttu-id="42e7c-111">最初のファイルには public 基底クラスである `BaseClass` ともう 1 つのクラスである `TestAccess` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="42e7c-111">The first file contains a public base class, `BaseClass`, and another class, `TestAccess`.</span></span> <span data-ttu-id="42e7c-112">`BaseClass` は protected internal メンバーの `myValue` を持っています。これは `TestAccess` 型にアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="42e7c-112">`BaseClass` owns a protected internal member, `myValue`, which is accessed by the `TestAccess` type.</span></span>
<span data-ttu-id="42e7c-113">2 番目のファイルでは、`BaseClass` のインスタンス経由で `myValue` にアクセスしようとするとエラーが発生します。一方で、派生クラス `DerivedClass` のインスタンスからこのメンバーにアクセスすると成功します。</span><span class="sxs-lookup"><span data-stu-id="42e7c-113">In the second file, an attempt to access `myValue` through an instance of `BaseClass` will produce an error, while an access to this member through an instance of a derived class, `DerivedClass` will succeed.</span></span>

<span data-ttu-id="42e7c-114">構造体は継承できないため、構造体メンバーは `protected internal` になりません。</span><span class="sxs-lookup"><span data-stu-id="42e7c-114">Struct members cannot be `protected internal` because the struct cannot be inherited.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="42e7c-115">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="42e7c-115">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="42e7c-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="42e7c-116">See also</span></span>

- [<span data-ttu-id="42e7c-117">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="42e7c-117">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="42e7c-118">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="42e7c-118">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="42e7c-119">C# のキーワード</span><span class="sxs-lookup"><span data-stu-id="42e7c-119">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="42e7c-120">アクセス修飾子</span><span class="sxs-lookup"><span data-stu-id="42e7c-120">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="42e7c-121">アクセシビリティ レベル</span><span class="sxs-lookup"><span data-stu-id="42e7c-121">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="42e7c-122">修飾子</span><span class="sxs-lookup"><span data-stu-id="42e7c-122">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="42e7c-123">public</span><span class="sxs-lookup"><span data-stu-id="42e7c-123">public</span></span>](public.md)
- [<span data-ttu-id="42e7c-124">private</span><span class="sxs-lookup"><span data-stu-id="42e7c-124">private</span></span>](private.md)
- [<span data-ttu-id="42e7c-125">internal</span><span class="sxs-lookup"><span data-stu-id="42e7c-125">internal</span></span>](internal.md)
- <span data-ttu-id="42e7c-126">[Internal Virtual キーワードのセキュリティ関連事項](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/heyd8kky(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="42e7c-126">[Security concerns for internal virtual keywords](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/heyd8kky(v=vs.100))</span></span>