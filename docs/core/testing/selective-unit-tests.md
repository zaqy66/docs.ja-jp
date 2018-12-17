---
title: 選択的単体テストの実行 - .NET Core
description: .NET Core において dotnet test コマンドでフィルター式を使用して、選択的単体テストを実行する方法。
author: smadala
ms.author: mairaw
ms.date: 03/22/2017
ms.custom: seodec18
ms.openlocfilehash: 3c24fb8cc5024399ae523801373b0fd8eff85f45
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53151747"
---
# <a name="running-selective-unit-tests"></a><span data-ttu-id="12a8d-103">選択的単体テストの実行</span><span class="sxs-lookup"><span data-stu-id="12a8d-103">Running selective unit tests</span></span>

<span data-ttu-id="12a8d-104">次の例では、`dotnet test` を使用します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-104">The following examples use `dotnet test`.</span></span> <span data-ttu-id="12a8d-105">`vstest.console.exe` を使用している場合は、`--filter ` を `--testcasefilter:` に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="12a8d-105">If you're using `vstest.console.exe`, replace `--filter ` with `--testcasefilter:`.</span></span>

## <a name="mstest"></a><span data-ttu-id="12a8d-106">MSTest</span><span class="sxs-lookup"><span data-stu-id="12a8d-106">MSTest</span></span>

```csharp
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace MSTestNamespace
{
    [TestClass]
    public class UnitTest1
    {
        [TestCategory("CategoryA")]
        [Priority(1)]
        [TestMethod]
        public void TestMethod1()
        {
        }

        [Priority(2)]
        [TestMethod]
        public void TestMethod2()
        {
        }
    }
}
```

| <span data-ttu-id="12a8d-107">正規表現</span><span class="sxs-lookup"><span data-stu-id="12a8d-107">Expression</span></span> | <span data-ttu-id="12a8d-108">結果</span><span class="sxs-lookup"><span data-stu-id="12a8d-108">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="12a8d-109">`FullyQualifiedName` に `Method` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-109">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="12a8d-110">`vstest 15.1+` で使用できます。</span><span class="sxs-lookup"><span data-stu-id="12a8d-110">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="12a8d-111">名前に `TestMethod1` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-111">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | <span data-ttu-id="12a8d-112">クラス `MSTestNamespace.UnitTest1` 内にあるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-112">Runs tests which are in class `MSTestNamespace.UnitTest1`.</span></span><br><span data-ttu-id="12a8d-113">**注:** `ClassName` 値には名前空間があるため、`ClassName=UnitTest1` は機能しません。</span><span class="sxs-lookup"><span data-stu-id="12a8d-113">**Note:** The `ClassName` value should have a namespace, so `ClassName=UnitTest1` won't work.</span></span> |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="12a8d-114">`MSTestNamespace.UnitTest1.TestMethod1` 以外のテストをすべて実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-114">Runs all tests except `MSTestNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="12a8d-115">`[TestCategory("CategoryA")]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-115">Runs tests which are annotated with `[TestCategory("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="12a8d-116">`[Priority(2)]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-116">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="12a8d-117">**条件演算子| と &amp; の使用**</span><span class="sxs-lookup"><span data-stu-id="12a8d-117">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="12a8d-118">正規表現</span><span class="sxs-lookup"><span data-stu-id="12a8d-118">Expression</span></span> | <span data-ttu-id="12a8d-119">結果</span><span class="sxs-lookup"><span data-stu-id="12a8d-119">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="12a8d-120">`FullyQualifiedName` に `UnitTest1` がある、**または** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-120">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="12a8d-121">`FullyQualifiedName` に `UnitTest1` がある、**および** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-121">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="12a8d-122">`UnitTest1` を含む `FullyQualifiedName` **および** `TestCategory` が `CategoryA`、**または** `Priority` が 1 かのいずれかのテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-122">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="xunit"></a><span data-ttu-id="12a8d-123">xUnit</span><span class="sxs-lookup"><span data-stu-id="12a8d-123">xUnit</span></span>

```csharp
using Xunit;

namespace XUnitNamespace
{
    public class TestClass1
    {
        [Trait("Category", "CategoryA")]
        [Trait("Priority", "1")]
        [Fact]
        public void Test1()
        {
        }

        [Trait("Priority", "2")]
        [Fact]
        public void Test2()
        {
        }
    }
}
```

| <span data-ttu-id="12a8d-124">正規表現</span><span class="sxs-lookup"><span data-stu-id="12a8d-124">Expression</span></span> | <span data-ttu-id="12a8d-125">結果</span><span class="sxs-lookup"><span data-stu-id="12a8d-125">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="12a8d-126">`XUnitNamespace.TestClass1.Test1` という 1 つのテストのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-126">Runs only one test, `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="12a8d-127">`XUnitNamespace.TestClass1.Test1` 以外のテストをすべて実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-127">Runs all tests except `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter DisplayName~TestClass1` | <span data-ttu-id="12a8d-128">表示名に `TestClass1` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-128">Runs tests whose display name contains `TestClass1`.</span></span> |

<span data-ttu-id="12a8d-129">コード例では、特性をキー `Category` や `Priority` で定義すると、フィルター処理に使用できます。</span><span class="sxs-lookup"><span data-stu-id="12a8d-129">In the code example, the defined traits with keys `Category` and `Priority` can be used for filtering.</span></span>

| <span data-ttu-id="12a8d-130">正規表現</span><span class="sxs-lookup"><span data-stu-id="12a8d-130">Expression</span></span> | <span data-ttu-id="12a8d-131">結果</span><span class="sxs-lookup"><span data-stu-id="12a8d-131">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter XUnit` | <span data-ttu-id="12a8d-132">`FullyQualifiedName` に `XUnit` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-132">Runs tests whose `FullyQualifiedName` contains `XUnit`.</span></span>  <span data-ttu-id="12a8d-133">`vstest 15.1+` で使用できます。</span><span class="sxs-lookup"><span data-stu-id="12a8d-133">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Category=CategoryA` | <span data-ttu-id="12a8d-134">`[Trait("Category", "CategoryA")]` があるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-134">Runs tests which have `[Trait("Category", "CategoryA")]`.</span></span> |

<span data-ttu-id="12a8d-135">**条件演算子| と &amp; の使用**</span><span class="sxs-lookup"><span data-stu-id="12a8d-135">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="12a8d-136">正規表現</span><span class="sxs-lookup"><span data-stu-id="12a8d-136">Expression</span></span> | <span data-ttu-id="12a8d-137">結果</span><span class="sxs-lookup"><span data-stu-id="12a8d-137">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | <span data-ttu-id="12a8d-138">`FullyQualifiedName` に `TestClass1` がある、**または** `Category` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-138">Runs tests which has `TestClass1` in `FullyQualifiedName` **or** `Category` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | <span data-ttu-id="12a8d-139">`FullyQualifiedName` に `TestClass1` がある、**および** `Category` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-139">Runs tests which has `TestClass1` in `FullyQualifiedName` **and** `Category` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="12a8d-140">`TestClass1` を含む `FullyQualifiedName` **および** `Category` が `CategoryA`、**または** `Priority` が 1 かのいずれかのテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-140">Runs tests which have either `FullyQualifiedName` containing `TestClass1` **and** `Category` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="nunit"></a><span data-ttu-id="12a8d-141">NUnit</span><span class="sxs-lookup"><span data-stu-id="12a8d-141">NUnit</span></span>

```csharp
using NUnit.Framework;

namespace NUnitNamespace
{
    public class UnitTest1
    {
        [Category("CategoryA")]
        [Property("Priority", 1)]
        [Test]
        public void TestMethod1()
        {
        }

        [Property("Priority", 2)]
        [Test]
        public void TestMethod2()
        {
        }
    }
}
```

| <span data-ttu-id="12a8d-142">正規表現</span><span class="sxs-lookup"><span data-stu-id="12a8d-142">Expression</span></span> | <span data-ttu-id="12a8d-143">結果</span><span class="sxs-lookup"><span data-stu-id="12a8d-143">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="12a8d-144">`FullyQualifiedName` に `Method` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-144">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="12a8d-145">`vstest 15.1+` で使用できます。</span><span class="sxs-lookup"><span data-stu-id="12a8d-145">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="12a8d-146">名前に `TestMethod1` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-146">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | <span data-ttu-id="12a8d-147">クラス `NUnitNamespace.UnitTest1` 内にあるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-147">Runs tests which are in class `NUnitNamespace.UnitTest1`.</span></span><br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="12a8d-148">`NUnitNamespace.UnitTest1.TestMethod1` 以外のテストをすべて実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-148">Runs all tests except `NUnitNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="12a8d-149">`[Category("CategoryA")]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-149">Runs tests which are annotated with `[Category("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="12a8d-150">`[Priority(2)]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-150">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="12a8d-151">**条件演算子| と &amp; の使用**</span><span class="sxs-lookup"><span data-stu-id="12a8d-151">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="12a8d-152">正規表現</span><span class="sxs-lookup"><span data-stu-id="12a8d-152">Expression</span></span> | <span data-ttu-id="12a8d-153">結果</span><span class="sxs-lookup"><span data-stu-id="12a8d-153">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="12a8d-154">`FullyQualifiedName` に `UnitTest1` がある、**または** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-154">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="12a8d-155">`FullyQualifiedName` に `UnitTest1` がある、**および** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-155">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="12a8d-156">`UnitTest1` を含む `FullyQualifiedName` **および** `TestCategory` が `CategoryA`、**または** `Priority` が 1 かのいずれかのテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="12a8d-156">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |
