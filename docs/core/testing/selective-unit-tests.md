---
title: 選択的単体テストの実行
description: dotnet test コマンドでフィルター式を使用して、選択的単体テストを実行する方法を紹介します。
author: smadala
ms.author: mairaw
ms.date: 03/22/2017
ms.openlocfilehash: 428e31014f5d8d487deb7c4b4317ebcef13c294d
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935181"
---
# <a name="running-selective-unit-tests"></a><span data-ttu-id="3b0c7-103">選択的単体テストの実行</span><span class="sxs-lookup"><span data-stu-id="3b0c7-103">Running selective unit tests</span></span>

<span data-ttu-id="3b0c7-104">次の例では、`dotnet test` を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-104">The following examples use `dotnet test`.</span></span> <span data-ttu-id="3b0c7-105">`vstest.console.exe` を使用している場合は、`--filter ` を `--testcasefilter:` に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-105">If you're using `vstest.console.exe`, replace `--filter ` with `--testcasefilter:`.</span></span>

## <a name="mstest"></a><span data-ttu-id="3b0c7-106">MSTest</span><span class="sxs-lookup"><span data-stu-id="3b0c7-106">MSTest</span></span>

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

| <span data-ttu-id="3b0c7-107">正規表現</span><span class="sxs-lookup"><span data-stu-id="3b0c7-107">Expression</span></span> | <span data-ttu-id="3b0c7-108">結果</span><span class="sxs-lookup"><span data-stu-id="3b0c7-108">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="3b0c7-109">`FullyQualifiedName` に `Method` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-109">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="3b0c7-110">`vstest 15.1+` で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-110">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="3b0c7-111">名前に `TestMethod1` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-111">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | <span data-ttu-id="3b0c7-112">クラス `MSTestNamespace.UnitTest1` 内にあるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-112">Runs tests which are in class `MSTestNamespace.UnitTest1`.</span></span><br><span data-ttu-id="3b0c7-113">**注:** `ClassName` 値には名前空間があるため、`ClassName=UnitTest1` は機能しません。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-113">**Note:** The `ClassName` value should have a namespace, so `ClassName=UnitTest1` won't work.</span></span> |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="3b0c7-114">`MSTestNamespace.UnitTest1.TestMethod1` 以外のテストをすべて実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-114">Runs all tests except `MSTestNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="3b0c7-115">`[TestCategory("CategoryA")]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-115">Runs tests which are annotated with `[TestCategory("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="3b0c7-116">`[Priority(2)]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-116">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="3b0c7-117">**条件演算子| と &amp; の使用**</span><span class="sxs-lookup"><span data-stu-id="3b0c7-117">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="3b0c7-118">正規表現</span><span class="sxs-lookup"><span data-stu-id="3b0c7-118">Expression</span></span> | <span data-ttu-id="3b0c7-119">結果</span><span class="sxs-lookup"><span data-stu-id="3b0c7-119">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="3b0c7-120">`FullyQualifiedName` に `UnitTest1` がある、**または** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-120">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="3b0c7-121">`FullyQualifiedName` に `UnitTest1` がある、**および** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-121">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="3b0c7-122">`UnitTest1` を含む `FullyQualifiedName` **および** `TestCategory` が `CategoryA`、**または** `Priority` が 1 かのいずれかのテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-122">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="xunit"></a><span data-ttu-id="3b0c7-123">xUnit</span><span class="sxs-lookup"><span data-stu-id="3b0c7-123">xUnit</span></span>

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

| <span data-ttu-id="3b0c7-124">正規表現</span><span class="sxs-lookup"><span data-stu-id="3b0c7-124">Expression</span></span> | <span data-ttu-id="3b0c7-125">結果</span><span class="sxs-lookup"><span data-stu-id="3b0c7-125">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="3b0c7-126">`XUnitNamespace.TestClass1.Test1` という 1 つのテストのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-126">Runs only one test, `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="3b0c7-127">`XUnitNamespace.TestClass1.Test1` 以外のテストをすべて実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-127">Runs all tests except `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter DisplayName~TestClass1` | <span data-ttu-id="3b0c7-128">表示名に `TestClass1` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-128">Runs tests whose display name contains `TestClass1`.</span></span> |

<span data-ttu-id="3b0c7-129">コード例では、特性をキー `Category` や `Priority` で定義すると、フィルター処理に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-129">In the code example, the defined traits with keys `Category` and `Priority` can be used for filtering.</span></span>

| <span data-ttu-id="3b0c7-130">正規表現</span><span class="sxs-lookup"><span data-stu-id="3b0c7-130">Expression</span></span> | <span data-ttu-id="3b0c7-131">結果</span><span class="sxs-lookup"><span data-stu-id="3b0c7-131">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter XUnit` | <span data-ttu-id="3b0c7-132">`FullyQualifiedName` に `XUnit` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-132">Runs tests whose `FullyQualifiedName` contains `XUnit`.</span></span>  <span data-ttu-id="3b0c7-133">`vstest 15.1+` で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-133">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Category=CategoryA` | <span data-ttu-id="3b0c7-134">`[Trait("Category", "CategoryA")]` があるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-134">Runs tests which have `[Trait("Category", "CategoryA")]`.</span></span> |

<span data-ttu-id="3b0c7-135">**条件演算子| と &amp; の使用**</span><span class="sxs-lookup"><span data-stu-id="3b0c7-135">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="3b0c7-136">正規表現</span><span class="sxs-lookup"><span data-stu-id="3b0c7-136">Expression</span></span> | <span data-ttu-id="3b0c7-137">結果</span><span class="sxs-lookup"><span data-stu-id="3b0c7-137">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | <span data-ttu-id="3b0c7-138">`FullyQualifiedName` に `TestClass1` がある、**または** `Category` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-138">Runs tests which has `TestClass1` in `FullyQualifiedName` **or** `Category` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | <span data-ttu-id="3b0c7-139">`FullyQualifiedName` に `TestClass1` がある、**および** `Category` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-139">Runs tests which has `TestClass1` in `FullyQualifiedName` **and** `Category` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="3b0c7-140">`TestClass1` を含む `FullyQualifiedName` **および** `Category` が `CategoryA`、**または** `Priority` が 1 かのいずれかのテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-140">Runs tests which have either `FullyQualifiedName` containing `TestClass1` **and** `Category` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="nunit"></a><span data-ttu-id="3b0c7-141">NUnit</span><span class="sxs-lookup"><span data-stu-id="3b0c7-141">NUnit</span></span>

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

| <span data-ttu-id="3b0c7-142">正規表現</span><span class="sxs-lookup"><span data-stu-id="3b0c7-142">Expression</span></span> | <span data-ttu-id="3b0c7-143">結果</span><span class="sxs-lookup"><span data-stu-id="3b0c7-143">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="3b0c7-144">`FullyQualifiedName` に `Method` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-144">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="3b0c7-145">`vstest 15.1+` で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-145">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="3b0c7-146">名前に `TestMethod1` が含まれるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-146">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | <span data-ttu-id="3b0c7-147">クラス `NUnitNamespace.UnitTest1` 内にあるテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-147">Runs tests which are in class `NUnitNamespace.UnitTest1`.</span></span><br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="3b0c7-148">`NUnitNamespace.UnitTest1.TestMethod1` 以外のテストをすべて実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-148">Runs all tests except `NUnitNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="3b0c7-149">`[Category("CategoryA")]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-149">Runs tests which are annotated with `[Category("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="3b0c7-150">`[Priority(2)]` の注釈が付けられているテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-150">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="3b0c7-151">**条件演算子| と &amp; の使用**</span><span class="sxs-lookup"><span data-stu-id="3b0c7-151">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="3b0c7-152">正規表現</span><span class="sxs-lookup"><span data-stu-id="3b0c7-152">Expression</span></span> | <span data-ttu-id="3b0c7-153">結果</span><span class="sxs-lookup"><span data-stu-id="3b0c7-153">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="3b0c7-154">`FullyQualifiedName` に `UnitTest1` がある、**または** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-154">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="3b0c7-155">`FullyQualifiedName` に `UnitTest1` がある、**および** `TestCategory` が `CategoryA` のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-155">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="3b0c7-156">`UnitTest1` を含む `FullyQualifiedName` **および** `TestCategory` が `CategoryA`、**または** `Priority` が 1 かのいずれかのテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b0c7-156">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |
