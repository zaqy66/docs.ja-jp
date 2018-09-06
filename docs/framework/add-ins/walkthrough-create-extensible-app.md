---
title: 'チュートリアル : 拡張性のあるアプリケーションの作成'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [.NET Framework], add-in pipeline
- host-side adapters for add-ins [.NET Framework]
- add-in pipeline [.NET Framework], creating
- add-in-side adapter [.NET Framework]
- contracts for add-in pipelines [.NET Framework]
ms.assetid: 694a33c5-a040-450d-aed5-ac49fc88ce61
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d2aaeaffaf3abbe1e8efcdb57d40e6ae60f89b5
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43875097"
---
# <a name="walkthrough-creating-an-extensible-application"></a><span data-ttu-id="2571c-102">チュートリアル : 拡張性のあるアプリケーションの作成</span><span class="sxs-lookup"><span data-stu-id="2571c-102">Walkthrough: Creating an Extensible Application</span></span>
<span data-ttu-id="2571c-103">このチュートリアルでは、簡単な計算機機能を実行するアドインのパイプラインを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2571c-103">This walkthrough describes how to create a pipeline for an add-in that performs simple calculator functions.</span></span> <span data-ttu-id="2571c-104">実際のシナリオは含まれていません代わりに、パイプラインとアドインを追加できるようにするホストのサービスの基本的な機能を示します。</span><span class="sxs-lookup"><span data-stu-id="2571c-104">It does not demonstrate a real-world scenario; rather, it demonstrates the basic functionality of a pipeline and how an add-in can provide services for a host.</span></span>  
  
 <span data-ttu-id="2571c-105">このチュートリアルでは、次のタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2571c-105">This walkthrough describes the following tasks:</span></span>  
  
-   <span data-ttu-id="2571c-106">Visual Studio ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-106">Creating a Visual Studio solution.</span></span>  
  
-   <span data-ttu-id="2571c-107">パイプライン ディレクトリ構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-107">Creating the pipeline directory structure.</span></span>  
  
-   <span data-ttu-id="2571c-108">ビューのコントラクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-108">Creating the contract and views.</span></span>  
  
-   <span data-ttu-id="2571c-109">追加アドイン側アダプターを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-109">Creating the add-in-side adapter.</span></span>  
  
-   <span data-ttu-id="2571c-110">ホスト側アダプターを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-110">Creating the host-side adapter.</span></span>  
  
-   <span data-ttu-id="2571c-111">ホストを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-111">Creating the host.</span></span>  
  
-   <span data-ttu-id="2571c-112">アドインを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-112">Creating the add-in.</span></span>  
  
-   <span data-ttu-id="2571c-113">パイプラインをデプロイします。</span><span class="sxs-lookup"><span data-stu-id="2571c-113">Deploying the pipeline.</span></span>  
  
-   <span data-ttu-id="2571c-114">ホスト アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="2571c-114">Running the host application.</span></span>  
  
 <span data-ttu-id="2571c-115">このパイプラインは、シリアル化可能な型のみを渡します (<xref:System.Double>と<xref:System.String>)、ホストとアドイン間。</span><span class="sxs-lookup"><span data-stu-id="2571c-115">This pipeline passes only serializable types (<xref:System.Double> and <xref:System.String>), between the host and the add-in.</span></span> <span data-ttu-id="2571c-116">複雑なデータ型のコレクションを渡す方法を示す例を参照してください[チュートリアル: ホスト間でコレクションを渡すと、アドイン](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-116">For an example that shows how to pass collections of complex data types, see [Walkthrough: Passing Collections Between Hosts and Add-Ins](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5).</span></span>  
  
 <span data-ttu-id="2571c-117">このパイプラインのコントラクトは、算術演算の 4 つのオブジェクト モデルを定義します。 追加、減算、乗算、および除算します。</span><span class="sxs-lookup"><span data-stu-id="2571c-117">The contract for this pipeline defines an object model of four arithmetic operations: add, subtract, multiply, and divide.</span></span> <span data-ttu-id="2571c-118">ホストからアドインなど、2 + 2 を計算する数式れ、アドインのホストに結果を返します。</span><span class="sxs-lookup"><span data-stu-id="2571c-118">The host provides the add-in with an equation to calculate, such as 2 + 2, and the add-in returns the result to the host.</span></span>  
  
 <span data-ttu-id="2571c-119">計算ツール アドインのバージョン 2 より高度を示し、バージョン管理を示します。</span><span class="sxs-lookup"><span data-stu-id="2571c-119">Version 2 of the calculator add-in provides more calculating possibilities and demonstrates versioning.</span></span> <span data-ttu-id="2571c-120">説明されている、[チュートリアル: 変更のホストとしての旧バージョンとの互換性を有効にする](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-120">It is described in [Walkthrough: Enabling Backward Compatibility as Your Host Changes](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="2571c-121">必須コンポーネント</span><span class="sxs-lookup"><span data-stu-id="2571c-121">Prerequisites</span></span>  
 <span data-ttu-id="2571c-122">このチュートリアルを完了するための要件は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2571c-122">You need the following to complete this walkthrough:</span></span>  
  
-   <span data-ttu-id="2571c-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2571c-123">Visual Studio.</span></span>  
  
## <a name="creating-a-visual-studio-solution"></a><span data-ttu-id="2571c-124">Visual Studio ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-124">Creating a Visual Studio Solution</span></span>  
 <span data-ttu-id="2571c-125">Visual Studio でソリューションを使用して、パイプライン セグメントのプロジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2571c-125">Use a solution in Visual Studio to contain the projects of your pipeline segments.</span></span>  
  
#### <a name="to-create-the-pipeline-solution"></a><span data-ttu-id="2571c-126">パイプラインのソリューションを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-126">To create the pipeline solution</span></span>  
  
1.  <span data-ttu-id="2571c-127">Visual Studio で、という名前の新しいプロジェクトを作成`Calc1Contract`です。</span><span class="sxs-lookup"><span data-stu-id="2571c-127">In Visual Studio, create a new project named `Calc1Contract`.</span></span> <span data-ttu-id="2571c-128">基に、**クラス ライブラリ**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-128">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="2571c-129">ソリューションの名前を`CalculatorV1`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-129">Name the solution `CalculatorV1`.</span></span>  
  
## <a name="creating-the-pipeline-directory-structure"></a><span data-ttu-id="2571c-130">パイプライン ディレクトリ構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-130">Creating the Pipeline Directory Structure</span></span>  
 <span data-ttu-id="2571c-131">アドイン モデルでは、指定したディレクトリ構造に配置するパイプライン セグメントのアセンブリが必要です。</span><span class="sxs-lookup"><span data-stu-id="2571c-131">The add-in model requires the pipeline segment assemblies to be placed in a specified directory structure.</span></span> <span data-ttu-id="2571c-132">パイプラインの構造の詳細については、次を参照してください。[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-132">For more information about the pipeline structure, see [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
#### <a name="to-create-the-pipeline-directory-structure"></a><span data-ttu-id="2571c-133">パイプライン ディレクトリ構造を作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-133">To create the pipeline directory structure</span></span>  
  
1.  <span data-ttu-id="2571c-134">コンピューターに任意の場所、アプリケーション フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-134">Create an application folder anywhere on your computer.</span></span>  
  
2.  <span data-ttu-id="2571c-135">、そのフォルダー内には、次の構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-135">In that folder, create the following structure:</span></span>  
  
    ```  
    Pipeline  
      AddIns  
        CalcV1  
        CalcV2  
      AddInSideAdapters  
      AddInViews  
      Contracts  
      HostSideAdapters  
    ```  
  
     <span data-ttu-id="2571c-136">アプリケーション フォルダー内のパイプラインのフォルダー構造を配置する必要はありません。それは利便性のためにはここで行われます。</span><span class="sxs-lookup"><span data-stu-id="2571c-136">It is not necessary to put the pipeline folder structure in your application folder; it is done here only for convenience.</span></span> <span data-ttu-id="2571c-137">適切な手順、チュートリアルのパイプライン フォルダー構造が別の場所にある場合は、コードを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2571c-137">At the appropriate step, the walkthrough explains how to change the code if the pipeline folder structure is in a different location.</span></span> <span data-ttu-id="2571c-138">パイプライン ディレクトリ要件の説明を参照[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-138">See the discussion of pipeline directory requirements in [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="2571c-139">`CalcV2`フォルダーは、このチュートリアルでは使用されません。 のプレース ホルダーは[チュートリアル: 変更のホストとしての旧バージョンとの互換性を有効にする](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-139">The `CalcV2` folder is not used in this walkthrough; it is a placeholder for [Walkthrough: Enabling Backward Compatibility as Your Host Changes](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848).</span></span>  
  
## <a name="creating-the-contract-and-views"></a><span data-ttu-id="2571c-140">コントラクトとビューの作成</span><span class="sxs-lookup"><span data-stu-id="2571c-140">Creating the Contract and Views</span></span>  
 <span data-ttu-id="2571c-141">このパイプラインのコントラクト セグメントの定義、`ICalc1Contract`を 4 つのメソッドを定義するインターフェイス: `add`、 `subtract`、 `multiply`、および`divide`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-141">The contract segment for this pipeline defines the `ICalc1Contract` interface, which defines four methods: `add`, `subtract`, `multiply`, and `divide`.</span></span>  
  
#### <a name="to-create-the-contract"></a><span data-ttu-id="2571c-142">コントラクトを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-142">To create the contract</span></span>  
  
1.  <span data-ttu-id="2571c-143">という名前の Visual Studio ソリューションで`CalculatorV1`、オープン、`Calc1Contract`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-143">In the Visual Studio solution named `CalculatorV1`, open the `Calc1Contract` project.</span></span>  
  
2.  <span data-ttu-id="2571c-144">**ソリューション エクスプ ローラー**には、次のアセンブリへの参照を追加、`Calc1Contract`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-144">In **Solution Explorer**, add references to the following assemblies to the `Calc1Contract` project:</span></span>  
  
     <span data-ttu-id="2571c-145">System.AddIn.Contract.dll</span><span class="sxs-lookup"><span data-stu-id="2571c-145">System.AddIn.Contract.dll</span></span>  
  
     <span data-ttu-id="2571c-146">System.AddIn.dll</span><span class="sxs-lookup"><span data-stu-id="2571c-146">System.AddIn.dll</span></span>  
  
3.  <span data-ttu-id="2571c-147">**ソリューション エクスプ ローラー**、新規に追加される既定のクラスを除外する**クラス ライブラリ**プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-147">In **Solution Explorer**, exclude the default class that is added to new **Class Library** projects.</span></span>  
  
4.  <span data-ttu-id="2571c-148">**ソリューション エクスプ ローラー**、プロジェクトに新しい項目の追加を使用して、**インターフェイス**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-148">In **Solution Explorer**, add a new item to the project, using the **Interface** template.</span></span> <span data-ttu-id="2571c-149">**新しい項目の追加**ダイアログ ボックスで、インターフェイスの名前`ICalc1Contract`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-149">In the **Add New Item** dialog box, name the interface `ICalc1Contract`.</span></span>  
  
5.  <span data-ttu-id="2571c-150">インターフェイスのファイルの名前空間参照を追加<xref:System.AddIn.Contract>と<xref:System.AddIn.Pipeline>します。</span><span class="sxs-lookup"><span data-stu-id="2571c-150">In the interface file, add namespace references to <xref:System.AddIn.Contract> and <xref:System.AddIn.Pipeline>.</span></span>  
  
6.  <span data-ttu-id="2571c-151">このコントラクト セグメントを完了するのにには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2571c-151">Use the following code to complete this contract segment.</span></span> <span data-ttu-id="2571c-152">このインターフェイスがありますに注意してください、<xref:System.AddIn.Pipeline.AddInContractAttribute>属性。</span><span class="sxs-lookup"><span data-stu-id="2571c-152">Note that this interface must have the <xref:System.AddIn.Pipeline.AddInContractAttribute> attribute.</span></span>  
  
     [!code-csharp[AddInP1Contract#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Contract/cs/ICalc1Contract.cs#1)]
     [!code-vb[AddInP1Contract#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Contract/vb/ICalc1Contract.vb#1)]  
  
7.  <span data-ttu-id="2571c-153">必要に応じて、Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-153">Optionally, build the Visual Studio solution.</span></span> <span data-ttu-id="2571c-154">最後の手順が、各手順は、各プロジェクトがあることを確認した後にビルドが修正されるまでは、ソリューションを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="2571c-154">The solution cannot be run until the final procedure, but building it after each procedure ensures that each project is correct.</span></span>  
  
 <span data-ttu-id="2571c-155">アドイン ビューとホストの表示のため、アドインをアドインでの最初のバージョンで特に通常同じコードを持つ、同時に、ビューを簡単に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2571c-155">Because the add-in view and the host view of the add-in usually have the same code, especially in the first version of an add-in, you can easily create the views at the same time.</span></span> <span data-ttu-id="2571c-156">1 要素のみが異なる: アドイン ビューが必要です、<xref:System.AddIn.Pipeline.AddInBaseAttribute>属性は、アドインのホスト ビューですべての属性が必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2571c-156">They differ by only one factor: the add-in view requires the <xref:System.AddIn.Pipeline.AddInBaseAttribute> attribute, while the host view of the add-in does not require any attributes.</span></span>  
  
#### <a name="to-create-the-add-in-view"></a><span data-ttu-id="2571c-157">アドイン ビューを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-157">To create the add-in view</span></span>  
  
1.  <span data-ttu-id="2571c-158">という名前の新しいプロジェクトを追加`Calc1AddInView`を`CalculatorV1`ソリューション。</span><span class="sxs-lookup"><span data-stu-id="2571c-158">Add a new project named `Calc1AddInView` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="2571c-159">基に、**クラス ライブラリ**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-159">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="2571c-160">**ソリューション エクスプ ローラー**に System.AddIn.dll への参照を追加、`Calc1AddInView`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-160">In **Solution Explorer**, add a reference to System.AddIn.dll to the `Calc1AddInView` project.</span></span>  
  
3.  <span data-ttu-id="2571c-161">**ソリューション エクスプ ローラー**、新規に追加される既定のクラスを除外する**クラス ライブラリ**プロジェクト、およびプロジェクトに新しい項目の追加を使用して、**インターフェイス**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-161">In **Solution Explorer**, exclude the default class that is added to new **Class Library** projects, and add a new item to the project, using the **Interface** template.</span></span> <span data-ttu-id="2571c-162">**新しい項目の追加**ダイアログ ボックスで、インターフェイスの名前`ICalculator`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-162">In the **Add New Item** dialog box, name the interface `ICalculator`.</span></span>  
  
4.  <span data-ttu-id="2571c-163">インターフェイスのファイルへの参照を名前空間を追加します。<xref:System.AddIn.Pipeline>します。</span><span class="sxs-lookup"><span data-stu-id="2571c-163">In the interface file, add a namespace reference to <xref:System.AddIn.Pipeline>.</span></span>  
  
5.  <span data-ttu-id="2571c-164">このアドインのビューを完了するのにには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2571c-164">Use the following code to complete this add-in view.</span></span> <span data-ttu-id="2571c-165">このインターフェイスがありますに注意してください、<xref:System.AddIn.Pipeline.AddInBaseAttribute>属性。</span><span class="sxs-lookup"><span data-stu-id="2571c-165">Note that this interface must have the <xref:System.AddIn.Pipeline.AddInBaseAttribute> attribute.</span></span>  
  
     [!code-csharp[AddInP1AddInViews#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInViews/cs/Calc1AddInView.cs#1)]
     [!code-vb[AddInP1AddInViews#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInViews/vb/Calc1AddInView.vb#1)]  
  
6.  <span data-ttu-id="2571c-166">必要に応じて、Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-166">Optionally, build the Visual Studio solution.</span></span>  
  
#### <a name="to-create-the-host-view-of-the-add-in"></a><span data-ttu-id="2571c-167">アドインのホスト ビューを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-167">To create the host view of the add-in</span></span>  
  
1.  <span data-ttu-id="2571c-168">という名前の新しいプロジェクトを追加`Calc1HVA`を`CalculatorV1`ソリューション。</span><span class="sxs-lookup"><span data-stu-id="2571c-168">Add a new project named `Calc1HVA` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="2571c-169">基に、**クラス ライブラリ**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-169">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="2571c-170">**ソリューション エクスプ ローラー**、新規に追加される既定のクラスを除外する**クラス ライブラリ**プロジェクト、およびプロジェクトに新しい項目の追加を使用して、**インターフェイス**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-170">In **Solution Explorer**, exclude the default class that is added to new **Class Library** projects, and add a new item to the project, using the **Interface** template.</span></span> <span data-ttu-id="2571c-171">**新しい項目の追加**ダイアログ ボックスで、インターフェイスの名前`ICalculator`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-171">In the **Add New Item** dialog box, name the interface `ICalculator`.</span></span>  
  
3.  <span data-ttu-id="2571c-172">インターフェイス ファイルに次のコードを使用して、アドインのホスト ビューを完了します。</span><span class="sxs-lookup"><span data-stu-id="2571c-172">In the interface file, use the following code to complete the host view of the add-in.</span></span>  
  
     [!code-csharp[AddInP1HVA#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HVA/cs/calc1hva.cs#1)]
     [!code-vb[AddInP1HVA#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HVA/vb/Calc1HVA.vb#1)]  
  
4.  <span data-ttu-id="2571c-173">必要に応じて、Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-173">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-add-in-side-adapter"></a><span data-ttu-id="2571c-174">アドイン側アダプターを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-174">Creating the Add-in-side Adapter</span></span>  
 <span data-ttu-id="2571c-175">このアドイン側アダプターは、1 つのビューからコントラクトへのアダプターで構成されます。</span><span class="sxs-lookup"><span data-stu-id="2571c-175">This add-in-side adapter consists of one view-to-contract adapter.</span></span> <span data-ttu-id="2571c-176">このパイプライン セグメントは、型をアドイン ビューからコントラクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="2571c-176">This pipeline segment converts the types from the add-in view to the contract.</span></span>  
  
 <span data-ttu-id="2571c-177">このパイプラインで、アドイン、ホストにサービスを提供します。 と種類が、アドインからホストにフローします。</span><span class="sxs-lookup"><span data-stu-id="2571c-177">In this pipeline, the add-in provides a service to the host, and the types flow from the add-in to the host.</span></span> <span data-ttu-id="2571c-178">ホストからアドインへの種類がフローしないために、このパイプラインのアドイン側のコントラクトからビューへのアダプターを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2571c-178">Because no types flow from the host to the add-in, you do not have to include a contract-to-view adapter on the add-in side of this pipeline.</span></span>  
  
#### <a name="to-create-the-add-in-side-adapter"></a><span data-ttu-id="2571c-179">追加アドイン側アダプターを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-179">To create the add-in-side adapter</span></span>  
  
1.  <span data-ttu-id="2571c-180">という名前の新しいプロジェクトを追加`Calc1AddInSideAdapter`を`CalculatorV1`ソリューション。</span><span class="sxs-lookup"><span data-stu-id="2571c-180">Add a new project named `Calc1AddInSideAdapter` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="2571c-181">基に、**クラス ライブラリ**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-181">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="2571c-182">**ソリューション エクスプ ローラー**には、次のアセンブリへの参照を追加、`Calc1AddInSideAdapter`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-182">In **Solution Explorer**, add references to the following assemblies to the `Calc1AddInSideAdapter` project:</span></span>  
  
     <span data-ttu-id="2571c-183">System.AddIn.dll</span><span class="sxs-lookup"><span data-stu-id="2571c-183">System.AddIn.dll</span></span>  
  
     <span data-ttu-id="2571c-184">System.AddIn.Contract.dll</span><span class="sxs-lookup"><span data-stu-id="2571c-184">System.AddIn.Contract.dll</span></span>  
  
3.  <span data-ttu-id="2571c-185">隣接するパイプライン セグメントのプロジェクトへのプロジェクト参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="2571c-185">Add project references to the projects for the adjacent pipeline segments:</span></span>  
  
     `Calc1AddInView`  
  
     `Calc1Contract`  
  
4.  <span data-ttu-id="2571c-186">各プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。</span><span class="sxs-lookup"><span data-stu-id="2571c-186">Select each project reference, and in **Properties** set **Copy Local** to **False**.</span></span> <span data-ttu-id="2571c-187">Visual Basic で使用して、**参照** タブの**プロジェクトのプロパティ**を設定する**ローカル コピー**に**False**の 2 つのプロジェクト参照。</span><span class="sxs-lookup"><span data-stu-id="2571c-187">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False** for the two project references.</span></span>  
  
5.  <span data-ttu-id="2571c-188">プロジェクトの既定のクラスの名前を変更`CalculatorViewToContractAddInSideAdapter`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-188">Rename the project's default class `CalculatorViewToContractAddInSideAdapter`.</span></span>  
  
6.  <span data-ttu-id="2571c-189">クラス ファイルで名前空間参照を追加<xref:System.AddIn.Pipeline>します。</span><span class="sxs-lookup"><span data-stu-id="2571c-189">In the class file, add namespace references to <xref:System.AddIn.Pipeline>.</span></span>  
  
7.  <span data-ttu-id="2571c-190">クラス ファイルで、隣接するセグメントの名前空間の参照を追加します:`CalcAddInViews`と`CalculatorContracts`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-190">In the class file, add namespace references for the adjacent segments: `CalcAddInViews` and `CalculatorContracts`.</span></span> <span data-ttu-id="2571c-191">(この名前空間の参照は、Visual basic で`Calc1AddInView.CalcAddInViews`と`Calc1Contract.CalculatorContracts`Visual Basic プロジェクトで既定の名前空間をオフにしている場合を除き、します)。</span><span class="sxs-lookup"><span data-stu-id="2571c-191">(In Visual Basic, these namespace references are `Calc1AddInView.CalcAddInViews` and `Calc1Contract.CalculatorContracts`, unless you have turned off the default namespaces in your Visual Basic projects.)</span></span>  
  
8.  <span data-ttu-id="2571c-192">適用、<xref:System.AddIn.Pipeline.AddInAdapterAttribute>属性を`CalculatorViewToContractAddInSideAdapter`クラスに追加アドイン側アダプターとして識別します。</span><span class="sxs-lookup"><span data-stu-id="2571c-192">Apply the <xref:System.AddIn.Pipeline.AddInAdapterAttribute> attribute to the `CalculatorViewToContractAddInSideAdapter` class, to identify it as the add-in-side adapter.</span></span>  
  
9. <span data-ttu-id="2571c-193">ように、`CalculatorViewToContractAddInSideAdapter`クラスを継承<xref:System.AddIn.Pipeline.ContractBase>の既定の実装を提供する、<xref:System.AddIn.Contract.IContract>インターフェイス、およびパイプラインのコントラクト インターフェイスを実装して`ICalc1Contract`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-193">Make the `CalculatorViewToContractAddInSideAdapter` class inherit <xref:System.AddIn.Pipeline.ContractBase>, which provides a default implementation of the <xref:System.AddIn.Contract.IContract> interface, and implement the contract interface for the pipeline, `ICalc1Contract`.</span></span>  
  
10. <span data-ttu-id="2571c-194">受け取るパブリック コンス トラクターを追加、`ICalculator`というプライベート フィールドにキャッシュ、および、基底クラスのコンス トラクターを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2571c-194">Add a public constructor that accepts an `ICalculator`, caches it in a private field, and calls the base class constructor.</span></span>  
  
11. <span data-ttu-id="2571c-195">メンバーを実装する`ICalc1Contract`の対応するメンバーを呼び出すだけです、`ICalculator`インスタンスをコンス トラクターに渡され、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="2571c-195">To implement the members of `ICalc1Contract`, simply call the corresponding members of the `ICalculator` instance that is passed to the constructor, and return the results.</span></span> <span data-ttu-id="2571c-196">これは、ビューを適応 (`ICalculator`)、コントラクト (`ICalc1Contract`)。</span><span class="sxs-lookup"><span data-stu-id="2571c-196">This adapts the view (`ICalculator`) to the contract (`ICalc1Contract`).</span></span>  
  
     <span data-ttu-id="2571c-197">次のコードでは、完成した追加アドイン側アダプターを示します。</span><span class="sxs-lookup"><span data-stu-id="2571c-197">The following code shows the completed add-in-side adapter.</span></span>  
  
     [!code-csharp[AddInP1AddInSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInSideAdapters/cs/Calc1ViewToContractAddInSideAdapter.cs#1)]
     [!code-vb[AddInP1AddInSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInSideAdapters/vb/Calc1ViewToContractAddInSideAdapter.vb#1)]  
  
12. <span data-ttu-id="2571c-198">必要に応じて、Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-198">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-host-side-adapter"></a><span data-ttu-id="2571c-199">ホスト側アダプターを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-199">Creating the Host-side Adapter</span></span>  
 <span data-ttu-id="2571c-200">このホスト側アダプターは、1 つのコントラクトからビューへのアダプターで構成されます。</span><span class="sxs-lookup"><span data-stu-id="2571c-200">This host-side adapter consists of one contract-to-view adapter.</span></span> <span data-ttu-id="2571c-201">このセグメントでは、コントラクトのアドインのホスト ビューを適合させます。</span><span class="sxs-lookup"><span data-stu-id="2571c-201">This segment adapts the contract to the host view of the add-in.</span></span>  
  
 <span data-ttu-id="2571c-202">このパイプラインでは、アドインのホストと型フローにサービスをホストにアドインから提供します。</span><span class="sxs-lookup"><span data-stu-id="2571c-202">In this pipeline, the add-in provides a service to the host and the types flow from the add-in to the host.</span></span> <span data-ttu-id="2571c-203">ホストからアドインへの種類がフローしないために、ビューからコントラクトへのアダプターを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2571c-203">Because no types flow from the host to the add-in, you do not have to include a view-to-contract adapter.</span></span>  
  
 <span data-ttu-id="2571c-204">有効期間管理を実装するには、使用、<xref:System.AddIn.Pipeline.ContractHandle>コントラクトに有効期間トークンをアタッチするオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-204">To implement lifetime management, use a <xref:System.AddIn.Pipeline.ContractHandle> object to attach a lifetime token to the contract.</span></span> <span data-ttu-id="2571c-205">有効期間管理を機能させるために、このハンドルへの参照を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2571c-205">You must keep a reference to this handle in order for lifetime management to work.</span></span> <span data-ttu-id="2571c-206">トークンが適用されると、追加のプログラミングは必要ありませんのでは使用しなくなったとガベージ コレクションで利用できるように、アドイン システムがオブジェクトの破棄できます。</span><span class="sxs-lookup"><span data-stu-id="2571c-206">After the token is applied, no additional programming is required because the add-in system can dispose of objects when they are no longer being used and make them available for garbage collection.</span></span> <span data-ttu-id="2571c-207">詳細については、次を参照してください。[有効期間管理](https://msdn.microsoft.com/library/57a9c87e-394c-4fef-89f2-aa4223a2aeb5)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-207">For more information, see [Lifetime Management](https://msdn.microsoft.com/library/57a9c87e-394c-4fef-89f2-aa4223a2aeb5).</span></span>  
  
#### <a name="to-create-the-host-side-adapter"></a><span data-ttu-id="2571c-208">ホスト側アダプターを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-208">To create the host-side adapter</span></span>  
  
1.  <span data-ttu-id="2571c-209">という名前の新しいプロジェクトを追加`Calc1HostSideAdapter`を`CalculatorV1`ソリューション。</span><span class="sxs-lookup"><span data-stu-id="2571c-209">Add a new project named `Calc1HostSideAdapter` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="2571c-210">基に、**クラス ライブラリ**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-210">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="2571c-211">**ソリューション エクスプ ローラー**には、次のアセンブリへの参照を追加、`Calc1HostSideAdapter`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-211">In **Solution Explorer**, add references to the following assemblies to the `Calc1HostSideAdapter` project:</span></span>  
  
     <span data-ttu-id="2571c-212">System.AddIn.dll</span><span class="sxs-lookup"><span data-stu-id="2571c-212">System.AddIn.dll</span></span>  
  
     <span data-ttu-id="2571c-213">System.AddIn.Contract.dll</span><span class="sxs-lookup"><span data-stu-id="2571c-213">System.AddIn.Contract.dll</span></span>  
  
3.  <span data-ttu-id="2571c-214">隣接するセグメントのプロジェクトへのプロジェクト参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="2571c-214">Add project references to the projects for the adjacent segments:</span></span>  
  
     `Calc1Contract`  
  
     `Calc1HVA`  
  
4.  <span data-ttu-id="2571c-215">各プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。</span><span class="sxs-lookup"><span data-stu-id="2571c-215">Select each project reference, and in **Properties** set **Copy Local** to **False**.</span></span> <span data-ttu-id="2571c-216">Visual Basic で使用して、**参照** タブの**プロジェクトのプロパティ**を設定する**ローカル コピー**に**False**の 2 つのプロジェクト参照。</span><span class="sxs-lookup"><span data-stu-id="2571c-216">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False** for the two project references.</span></span>  
  
5.  <span data-ttu-id="2571c-217">プロジェクトの既定のクラスの名前を変更`CalculatorContractToViewHostSideAdapter`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-217">Rename the project's default class `CalculatorContractToViewHostSideAdapter`.</span></span>  
  
6.  <span data-ttu-id="2571c-218">クラス ファイルで名前空間参照を追加<xref:System.AddIn.Pipeline>します。</span><span class="sxs-lookup"><span data-stu-id="2571c-218">In the class file, add namespace references to <xref:System.AddIn.Pipeline>.</span></span>  
  
7.  <span data-ttu-id="2571c-219">クラス ファイルで、隣接するセグメントの名前空間の参照を追加します:`CalcHVAs`と`CalculatorContracts`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-219">In the class file, add namespace references for the adjacent segments: `CalcHVAs` and `CalculatorContracts`.</span></span> <span data-ttu-id="2571c-220">(この名前空間の参照は、Visual basic で`Calc1HVA.CalcHVAs`と`Calc1Contract.CalculatorContracts`Visual Basic プロジェクトで既定の名前空間をオフにしている場合を除き、します)。</span><span class="sxs-lookup"><span data-stu-id="2571c-220">(In Visual Basic, these namespace references are `Calc1HVA.CalcHVAs` and `Calc1Contract.CalculatorContracts`, unless you have turned off the default namespaces in your Visual Basic projects.)</span></span>  
  
8.  <span data-ttu-id="2571c-221">適用、<xref:System.AddIn.Pipeline.HostAdapterAttribute>属性を`CalculatorContractToViewHostSideAdapter`クラス、ホスト側アダプター セグメントとして識別します。</span><span class="sxs-lookup"><span data-stu-id="2571c-221">Apply the <xref:System.AddIn.Pipeline.HostAdapterAttribute> attribute to the `CalculatorContractToViewHostSideAdapter` class, to identify it as the host-side adapter segment.</span></span>  
  
9. <span data-ttu-id="2571c-222">ように、`CalculatorContractToViewHostSideAdapter`クラスで、追加のホスト ビューを表すインターフェイスを実装: `Calc1HVAs.ICalculator` (`Calc1HVA.CalcHVAs.ICalculator` Visual Basic で)。</span><span class="sxs-lookup"><span data-stu-id="2571c-222">Make the `CalculatorContractToViewHostSideAdapter` class implement the interface that represents the host view of the add-in: `Calc1HVAs.ICalculator` (`Calc1HVA.CalcHVAs.ICalculator` in Visual Basic).</span></span>  
  
10. <span data-ttu-id="2571c-223">パイプラインのコントラクトの型を受け取るパブリック コンス トラクターを追加`ICalc1Contract`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-223">Add a public constructor that accepts the pipeline contract type, `ICalc1Contract`.</span></span> <span data-ttu-id="2571c-224">コンス トラクターは、コントラクトへの参照をキャッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2571c-224">The constructor must cache the reference to the contract.</span></span> <span data-ttu-id="2571c-225">作成し、新しいキャッシュも<xref:System.AddIn.Pipeline.ContractHandle>、コントラクトのアドインの有効期間を管理します。</span><span class="sxs-lookup"><span data-stu-id="2571c-225">It must also create and cache a new <xref:System.AddIn.Pipeline.ContractHandle> for the contract, to manage the lifetime of the add-in.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="2571c-226"><xref:System.AddIn.Pipeline.ContractHandle>有効期間管理に不可欠です。</span><span class="sxs-lookup"><span data-stu-id="2571c-226">The <xref:System.AddIn.Pipeline.ContractHandle> is critical to lifetime management.</span></span> <span data-ttu-id="2571c-227">参照の保持に失敗した場合、<xref:System.AddIn.Pipeline.ContractHandle>オブジェクトのガベージ コレクションによって回収され、プログラムで想定されていないときに、パイプラインはシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="2571c-227">If you fail to keep a reference to the <xref:System.AddIn.Pipeline.ContractHandle> object, garbage collection will reclaim it, and the pipeline will shut down when your program does not expect it.</span></span> <span data-ttu-id="2571c-228">など、診断が困難なエラーが生じる<xref:System.AppDomainUnloadedException>します。</span><span class="sxs-lookup"><span data-stu-id="2571c-228">This can lead to errors that are difficult to diagnose, such as <xref:System.AppDomainUnloadedException>.</span></span> <span data-ttu-id="2571c-229">シャット ダウンは、パイプラインの有効期間のステージは通常この条件は、エラーを検出するために、有効期間管理コードの方法はありません。</span><span class="sxs-lookup"><span data-stu-id="2571c-229">Shutdown is a normal stage in the life of a pipeline, so there is no way for the lifetime management code to detect that this condition is an error.</span></span>  
  
11. <span data-ttu-id="2571c-230">メンバーを実装する`ICalculator`の対応するメンバーを呼び出すだけです、`ICalc1Contract`インスタンスをコンス トラクターに渡され、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="2571c-230">To implement the members of `ICalculator`, simply call the corresponding members of the `ICalc1Contract` instance that is passed to the constructor, and return the results.</span></span> <span data-ttu-id="2571c-231">これは、コントラクトを適応 (`ICalc1Contract`) ビューに (`ICalculator`)。</span><span class="sxs-lookup"><span data-stu-id="2571c-231">This adapts the contract (`ICalc1Contract`) to the view (`ICalculator`).</span></span>  
  
     <span data-ttu-id="2571c-232">次のコードでは、完成したホスト側アダプターを示します。</span><span class="sxs-lookup"><span data-stu-id="2571c-232">The following code shows the completed host-side adapter.</span></span>  
  
     [!code-csharp[AddInP1HostSideAdapters#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1HostSideAdapters/cs/Calc1ContractToViewHostSideAdapter.cs#1)]
     [!code-vb[AddInP1HostSideAdapters#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1HostSideAdapters/vb/Calc1ContractToViewHostSideAdapter.vb#1)]  
  
12. <span data-ttu-id="2571c-233">必要に応じて、Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-233">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-host"></a><span data-ttu-id="2571c-234">ホストの作成</span><span class="sxs-lookup"><span data-stu-id="2571c-234">Creating the Host</span></span>  
 <span data-ttu-id="2571c-235">ホスト アプリケーションは、アドインのホスト ビュー アドインと対話します。</span><span class="sxs-lookup"><span data-stu-id="2571c-235">A host application interacts with the add-in through the host view of the add-in.</span></span> <span data-ttu-id="2571c-236">アドインの検出とアクティブ化によって提供されるメソッドを使用して、<xref:System.AddIn.Hosting.AddInStore>と<xref:System.AddIn.Hosting.AddInToken>クラスは、次の操作します。</span><span class="sxs-lookup"><span data-stu-id="2571c-236">It uses add-in discovery and activation methods provided by the <xref:System.AddIn.Hosting.AddInStore> and <xref:System.AddIn.Hosting.AddInToken> classes to do the following:</span></span>  
  
-   <span data-ttu-id="2571c-237">パイプラインとアドインの情報のキャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="2571c-237">Update the cache of pipeline and add-in information.</span></span>  
  
-   <span data-ttu-id="2571c-238">ホスト ビューの種類のアドインの検索`ICalculator`、指定したパイプラインのルート ディレクトリの下。</span><span class="sxs-lookup"><span data-stu-id="2571c-238">Find add-ins of the host view type, `ICalculator`, under the specified pipeline root directory.</span></span>  
  
-   <span data-ttu-id="2571c-239">アドインを使用する指定を求めるボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2571c-239">Prompt the user to specify which add-in to use.</span></span>  
  
-   <span data-ttu-id="2571c-240">指定したセキュリティ信頼レベルで新しいアプリケーション ドメインでの選択のアドインをアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="2571c-240">Activate the selected add-in in a new application domain with a specified security trust level.</span></span>  
  
-   <span data-ttu-id="2571c-241">カスタム実行`RunCalculator`メソッドで、アドインのホスト ビューで指定されたアドインのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2571c-241">Run the custom `RunCalculator` method, which calls the add-in's methods as specified by the host view of the add-in.</span></span>  
  
#### <a name="to-create-the-host"></a><span data-ttu-id="2571c-242">ホストを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-242">To create the host</span></span>  
  
1.  <span data-ttu-id="2571c-243">という名前の新しいプロジェクトを追加`Calc1Host`を`CalculatorV1`ソリューション。</span><span class="sxs-lookup"><span data-stu-id="2571c-243">Add a new project named `Calc1Host` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="2571c-244">基に、**コンソール アプリケーション**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-244">Base it on the **Console Application** template.</span></span>  
  
2.  <span data-ttu-id="2571c-245">**ソリューション エクスプ ローラー**、System.AddIn.dll アセンブリへの参照を追加、`Calc1Host`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-245">In **Solution Explorer**, add a reference to the System.AddIn.dll assembly to the `Calc1Host` project.</span></span>  
  
3.  <span data-ttu-id="2571c-246">プロジェクト参照を追加、`Calc1HVA`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-246">Add a project reference to the `Calc1HVA` project.</span></span> <span data-ttu-id="2571c-247">プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。</span><span class="sxs-lookup"><span data-stu-id="2571c-247">Select the project reference, and in **Properties** set **Copy Local** to **False**.</span></span> <span data-ttu-id="2571c-248">Visual Basic で使用して、**参照**のタブ**プロジェクトのプロパティ**を設定する**ローカル コピー**に**False**します。</span><span class="sxs-lookup"><span data-stu-id="2571c-248">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False**.</span></span>  
  
4.  <span data-ttu-id="2571c-249">クラス ファイル (Visual Basic でのモジュール) の名前を変更`MathHost1`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-249">Rename the class file (module in Visual Basic) `MathHost1`.</span></span>  
  
5.  <span data-ttu-id="2571c-250">Visual Basic で使用して、**アプリケーション**のタブ、**プロジェクト プロパティ**ダイアログ ボックスを設定**スタートアップ オブジェクト**に**Sub Main**します。</span><span class="sxs-lookup"><span data-stu-id="2571c-250">In Visual Basic, use the **Application** tab of the **Project Properties** dialog box to set **Startup object** to **Sub Main**.</span></span>  
  
6.  <span data-ttu-id="2571c-251">そのクラスまたはモジュール ファイルに名前空間参照を追加<xref:System.AddIn.Hosting>します。</span><span class="sxs-lookup"><span data-stu-id="2571c-251">In the class or module file, add a namespace reference to <xref:System.AddIn.Hosting>.</span></span>  
  
7.  <span data-ttu-id="2571c-252">クラスまたはモジュール ファイルで、アドインのホスト ビューの名前空間参照を追加:`CalcHVAs`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-252">In the class or module file, add a namespace reference for the host view of the add-in: `CalcHVAs`.</span></span> <span data-ttu-id="2571c-253">(Visual Basic の場合は、この名前空間のリファレンスは`Calc1HVA.CalcHVAs`Visual Basic プロジェクトで既定の名前空間をオフにしている場合を除き、します)。</span><span class="sxs-lookup"><span data-stu-id="2571c-253">(In Visual Basic, this namespace reference is `Calc1HVA.CalcHVAs`, unless you have turned off the default namespaces in your Visual Basic projects.)</span></span>  
  
8.  <span data-ttu-id="2571c-254">**ソリューション エクスプ ローラー**、ソリューションの選択との間、**プロジェクト**メニュー**プロパティ**。</span><span class="sxs-lookup"><span data-stu-id="2571c-254">In **Solution Explorer**, select the solution and from the **Project** menu choose **Properties**.</span></span> <span data-ttu-id="2571c-255">**ソリューション プロパティ ページ**ダイアログ ボックスで、セット、**シングル スタートアップ プロジェクト**をこのホスト アプリケーション プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-255">In the **Solution Property Pages** dialog box, set the **Single Startup Project** to be this host application project.</span></span>  
  
9. <span data-ttu-id="2571c-256">クラスまたはモジュール ファイルを使用、<xref:System.AddIn.Hosting.AddInStore.Update%2A?displayProperty=nameWithType>メソッド キャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="2571c-256">In the class or module file, use the <xref:System.AddIn.Hosting.AddInStore.Update%2A?displayProperty=nameWithType> method to update the cache.</span></span> <span data-ttu-id="2571c-257">使用して、<xref:System.AddIn.Hosting.AddInStore.FindAddIn%2A?displayProperty=nameWithType>メソッドを使用して、トークンのコレクションを取得、<xref:System.AddIn.Hosting.AddInToken.Activate%2A?displayProperty=nameWithType>アドインをアクティブ化するメソッド。</span><span class="sxs-lookup"><span data-stu-id="2571c-257">Use the <xref:System.AddIn.Hosting.AddInStore.FindAddIn%2A?displayProperty=nameWithType> method to get a collection of tokens, and use the <xref:System.AddIn.Hosting.AddInToken.Activate%2A?displayProperty=nameWithType> method to activate an add-in.</span></span>  
  
     <span data-ttu-id="2571c-258">次のコードでは、完全なホスト アプリケーションを示します。</span><span class="sxs-lookup"><span data-stu-id="2571c-258">The following code shows the completed host application.</span></span>  
  
     [!code-csharp[AddInP1Host#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1Host/cs/MathHost1.cs#1)]
     [!code-vb[AddInP1Host#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1Host/vb/MathHost1.vb#1)]  
  
    > [!NOTE]
    >  <span data-ttu-id="2571c-259">このコードでは、パイプラインのフォルダー構造がアプリケーション フォルダー内にあることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="2571c-259">This code assumes that the pipeline folder structure is located in the application folder.</span></span> <span data-ttu-id="2571c-260">他の場所で配置する場合は、設定するコードの行を変更、`addInRoot`変数、変数が、パイプライン ディレクトリ構造へのパスが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="2571c-260">If you located it elsewhere, change the line of code that sets the `addInRoot` variable, so that the variable contains the path to your pipeline directory structure.</span></span>  
  
     <span data-ttu-id="2571c-261">コードを使用して、`ChooseCalculator`メソッドをトークンを一覧表示し、アドインを選択するユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="2571c-261">The code uses a `ChooseCalculator` method to list the tokens and to prompt the user to choose an add-in.</span></span> <span data-ttu-id="2571c-262">`RunCalculator`メソッドは、単純な算術式のユーザーに求めますを使用して式を解析し、`Parser`クラス、さらに、アドインによって返される結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2571c-262">The `RunCalculator` method prompts the user for simple math expressions, parses the expressions using the `Parser` class, and displays the results returned by the add-in.</span></span>  
  
10. <span data-ttu-id="2571c-263">必要に応じて、Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-263">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="creating-the-add-in"></a><span data-ttu-id="2571c-264">アドインを作成します。</span><span class="sxs-lookup"><span data-stu-id="2571c-264">Creating the Add-In</span></span>  
 <span data-ttu-id="2571c-265">アドインをアドイン ビューによって指定されたメソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="2571c-265">An add-in implements the methods specified by the add-in view.</span></span> <span data-ttu-id="2571c-266">このアドインでは、実装、 `Add`、 `Subtract`、 `Multiply`、および`Divide`操作し、ホストに、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="2571c-266">This add-in implements the `Add`, `Subtract`, `Multiply`, and `Divide` operations and returns the results to the host.</span></span>  
  
#### <a name="to-create-the-add-in"></a><span data-ttu-id="2571c-267">アドインを作成するには</span><span class="sxs-lookup"><span data-stu-id="2571c-267">To create the add-in</span></span>  
  
1.  <span data-ttu-id="2571c-268">という名前の新しいプロジェクトを追加`AddInCalcV1`を`CalculatorV1`ソリューション。</span><span class="sxs-lookup"><span data-stu-id="2571c-268">Add a new project named `AddInCalcV1` to the `CalculatorV1` solution.</span></span> <span data-ttu-id="2571c-269">基に、**クラス ライブラリ**テンプレート。</span><span class="sxs-lookup"><span data-stu-id="2571c-269">Base it on the **Class Library** template.</span></span>  
  
2.  <span data-ttu-id="2571c-270">**ソリューション エクスプ ローラー**、System.AddIn.dll アセンブリへの参照をプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="2571c-270">In **Solution Explorer**, add a reference to the System.AddIn.dll assembly to the project.</span></span>  
  
3.  <span data-ttu-id="2571c-271">プロジェクト参照を追加、`Calc1AddInView`プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="2571c-271">Add a project reference to the `Calc1AddInView` project.</span></span> <span data-ttu-id="2571c-272">プロジェクト参照を選択し、**プロパティ**設定**ローカル コピー**に**False**します。</span><span class="sxs-lookup"><span data-stu-id="2571c-272">Select the project reference, and in **Properties**, set **Copy Local** to **False**.</span></span> <span data-ttu-id="2571c-273">Visual Basic で使用して、**参照**のタブ**プロジェクトのプロパティ**を設定する**ローカルにコピー**に**False**プロジェクト参照。</span><span class="sxs-lookup"><span data-stu-id="2571c-273">In Visual Basic, use the **References** tab of **Project Properties** to set **Copy Local** to **False** for the project reference.</span></span>  
  
4.  <span data-ttu-id="2571c-274">クラスの名前変更`AddInCalcV1`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-274">Rename the class `AddInCalcV1`.</span></span>  
  
5.  <span data-ttu-id="2571c-275">クラス ファイルで名前空間への参照を追加<xref:System.AddIn>およびアドイン ビュー セグメント: `CalcAddInViews` (`Calc1AddInView.CalcAddInViews` Visual Basic で)。</span><span class="sxs-lookup"><span data-stu-id="2571c-275">In the class file, add a namespace reference to <xref:System.AddIn> and the add-in view segment: `CalcAddInViews` (`Calc1AddInView.CalcAddInViews` in Visual Basic).</span></span>  
  
6.  <span data-ttu-id="2571c-276">適用、<xref:System.AddIn.AddInAttribute>属性を`AddInCalcV1`アドインとしてクラスを識別するために、クラス。</span><span class="sxs-lookup"><span data-stu-id="2571c-276">Apply the <xref:System.AddIn.AddInAttribute> attribute to the `AddInCalcV1` class, to identify the class as an add-in.</span></span>  
  
7.  <span data-ttu-id="2571c-277">ように、`AddInCalcV1`アドイン ビューを表すインターフェイスを実装するクラス。 `CalcAddInViews.ICalculator` (`Calc1AddInView.CalcAddInViews.ICalculator` Visual Basic で)。</span><span class="sxs-lookup"><span data-stu-id="2571c-277">Make the `AddInCalcV1` class implement the interface that represents the add-in view: `CalcAddInViews.ICalculator` (`Calc1AddInView.CalcAddInViews.ICalculator` in Visual Basic).</span></span>  
  
8.  <span data-ttu-id="2571c-278">メンバーを実装する`ICalculator`適切な計算の結果を返すことによって。</span><span class="sxs-lookup"><span data-stu-id="2571c-278">Implement the members of `ICalculator` by returning the results of the appropriate calculations.</span></span>  
  
     <span data-ttu-id="2571c-279">完了したアドインの次のコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="2571c-279">The following code shows the completed add-in.</span></span>  
  
     [!code-csharp[AddInP1AddInCalcV1#1](../../../samples/snippets/csharp/VS_Snippets_CLR/AddInP1AddInCalcV1/cs/AddInCalcV1.cs#1)]
     [!code-vb[AddInP1AddInCalcV1#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AddInP1AddInCalcV1/vb/AddInCalcV1.vb#1)]  
  
9. <span data-ttu-id="2571c-280">必要に応じて、Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-280">Optionally, build the Visual Studio solution.</span></span>  
  
## <a name="deploying-the-pipeline"></a><span data-ttu-id="2571c-281">パイプラインを展開します。</span><span class="sxs-lookup"><span data-stu-id="2571c-281">Deploying the Pipeline</span></span>  
 <span data-ttu-id="2571c-282">ビルドし、必要なパイプライン ディレクトリ構造に追加のセグメントをデプロイする準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="2571c-282">You are now ready to build and deploy the add-in segments to the required pipeline directory structure.</span></span>  
  
#### <a name="to-deploy-the-segments-to-the-pipeline"></a><span data-ttu-id="2571c-283">パイプライン セグメントをデプロイするには</span><span class="sxs-lookup"><span data-stu-id="2571c-283">To deploy the segments to the pipeline</span></span>  
  
1.  <span data-ttu-id="2571c-284">ソリューション内の各プロジェクトを使用して、**ビルド**タブ**プロジェクトのプロパティ**(、**コンパイル**Visual Basic でのタブ) の値を設定する、**出力パス** (、**ビルド出力パス**Visual Basic で)。</span><span class="sxs-lookup"><span data-stu-id="2571c-284">For each project in the solution, use the **Build** tab of **Project Properties** (the **Compile** tab in Visual Basic) to set the value of the **Output path** (the **Build output path** in Visual Basic).</span></span> <span data-ttu-id="2571c-285">アプリケーションのフォルダーの名前を付けた場合`MyApp`、次のフォルダーに、プロジェクトのビルドはたとえば。</span><span class="sxs-lookup"><span data-stu-id="2571c-285">If you named your application folder `MyApp`, for example, your projects would build into the following folders:</span></span>  
  
    |<span data-ttu-id="2571c-286">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="2571c-286">Project</span></span>|<span data-ttu-id="2571c-287">パス</span><span class="sxs-lookup"><span data-stu-id="2571c-287">Path</span></span>|  
    |-------------|----------|  
    |<span data-ttu-id="2571c-288">AddInCalcV1</span><span class="sxs-lookup"><span data-stu-id="2571c-288">AddInCalcV1</span></span>|<span data-ttu-id="2571c-289">MyApp\Pipeline\AddIns\CalcV1</span><span class="sxs-lookup"><span data-stu-id="2571c-289">MyApp\Pipeline\AddIns\CalcV1</span></span>|  
    |<span data-ttu-id="2571c-290">Calc1AddInSideAdapter</span><span class="sxs-lookup"><span data-stu-id="2571c-290">Calc1AddInSideAdapter</span></span>|<span data-ttu-id="2571c-291">MyApp\Pipeline\AddInSideAdapters</span><span class="sxs-lookup"><span data-stu-id="2571c-291">MyApp\Pipeline\AddInSideAdapters</span></span>|  
    |<span data-ttu-id="2571c-292">Calc1AddInView</span><span class="sxs-lookup"><span data-stu-id="2571c-292">Calc1AddInView</span></span>|<span data-ttu-id="2571c-293">MyApp\Pipeline\AddInViews</span><span class="sxs-lookup"><span data-stu-id="2571c-293">MyApp\Pipeline\AddInViews</span></span>|  
    |<span data-ttu-id="2571c-294">Calc1Contract</span><span class="sxs-lookup"><span data-stu-id="2571c-294">Calc1Contract</span></span>|<span data-ttu-id="2571c-295">MyApp\Pipeline\Contracts</span><span class="sxs-lookup"><span data-stu-id="2571c-295">MyApp\Pipeline\Contracts</span></span>|  
    |<span data-ttu-id="2571c-296">Calc1Host</span><span class="sxs-lookup"><span data-stu-id="2571c-296">Calc1Host</span></span>|<span data-ttu-id="2571c-297">MyApp</span><span class="sxs-lookup"><span data-stu-id="2571c-297">MyApp</span></span>|  
    |<span data-ttu-id="2571c-298">Calc1HostSideAdapter</span><span class="sxs-lookup"><span data-stu-id="2571c-298">Calc1HostSideAdapter</span></span>|<span data-ttu-id="2571c-299">MyApp\Pipeline\HostSideAdapters</span><span class="sxs-lookup"><span data-stu-id="2571c-299">MyApp\Pipeline\HostSideAdapters</span></span>|  
    |<span data-ttu-id="2571c-300">Calc1HVA</span><span class="sxs-lookup"><span data-stu-id="2571c-300">Calc1HVA</span></span>|<span data-ttu-id="2571c-301">MyApp</span><span class="sxs-lookup"><span data-stu-id="2571c-301">MyApp</span></span>|  
  
    > [!NOTE]
    >  <span data-ttu-id="2571c-302">パイプライン フォルダー構造をアプリケーション フォルダー以外の場所に配置した場合は、それに応じて、テーブルのパスを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2571c-302">If you decided to put your pipeline folder structure in a location other than your application folder, you must modify the paths shown in the table accordingly.</span></span> <span data-ttu-id="2571c-303">パイプライン ディレクトリ要件の説明を参照[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-303">See the discussion of pipeline directory requirements in [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
2.  <span data-ttu-id="2571c-304">Visual Studio ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="2571c-304">Build the Visual Studio solution.</span></span>  
  
3.  <span data-ttu-id="2571c-305">アセンブリが適切なディレクトリにコピーされたことと、アセンブリの余分なコピーが正しくないフォルダーにインストールされていないことを確認するアプリケーションとパイプラインのディレクトリを確認します。</span><span class="sxs-lookup"><span data-stu-id="2571c-305">Check the application and pipeline directories to ensure that the assemblies were copied to the correct directories and that no extra copies of assemblies were installed in the wrong folders.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="2571c-306">変更していない場合**ローカル コピー**に**False**の`Calc1AddInView`プロジェクトで参照、`AddInCalcV1`プロジェクト、ローダー コンテキストの問題により、アドインに配置されているからです。</span><span class="sxs-lookup"><span data-stu-id="2571c-306">If you did not change **Copy Local** to **False** for the `Calc1AddInView` project reference in the `AddInCalcV1` project, loader context problems will prevent the add-in from being located.</span></span>  
  
     <span data-ttu-id="2571c-307">パイプラインを展開する方法の詳細については、次を参照してください。[パイプライン開発の必要条件](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)します。</span><span class="sxs-lookup"><span data-stu-id="2571c-307">For information about deploying to the pipeline, see [Pipeline Development Requirements](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5).</span></span>  
  
## <a name="running-the-host-application"></a><span data-ttu-id="2571c-308">ホスト アプリケーションの実行</span><span class="sxs-lookup"><span data-stu-id="2571c-308">Running the Host Application</span></span>  
 <span data-ttu-id="2571c-309">ホストを実行し、アドインを操作する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="2571c-309">You are now ready to run the host and interact with the add-in.</span></span>  
  
#### <a name="to-run-the-host-application"></a><span data-ttu-id="2571c-310">ホスト アプリケーションを実行するには</span><span class="sxs-lookup"><span data-stu-id="2571c-310">To run the host application</span></span>  
  
1.  <span data-ttu-id="2571c-311">コマンド プロンプトで、アプリケーション ディレクトリに移動し、ホスト アプリケーションを実行`Calc1Host.exe`します。</span><span class="sxs-lookup"><span data-stu-id="2571c-311">At the command prompt, go to the application directory and run the host application, `Calc1Host.exe`.</span></span>  
  
2.  <span data-ttu-id="2571c-312">ホストは、すべて使用可能なアドインの型を検索し、アドインを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="2571c-312">The host finds all available add-ins of its type and prompts you to select an add-in.</span></span> <span data-ttu-id="2571c-313">入力**1** for のみ使用可能なアドイン。</span><span class="sxs-lookup"><span data-stu-id="2571c-313">Enter **1** for the only available add-in.</span></span>  
  
3.  <span data-ttu-id="2571c-314">計算の数式を入力**2 + 2**します。</span><span class="sxs-lookup"><span data-stu-id="2571c-314">Enter an equation for the calculator, such as **2 + 2**.</span></span> <span data-ttu-id="2571c-315">数字と演算子の間にスペースが必要があります。</span><span class="sxs-lookup"><span data-stu-id="2571c-315">There must be spaces between the numbers and the operator.</span></span>  
  
4.  <span data-ttu-id="2571c-316">型**終了**キーを押すと、 **」と入力**キー アプリケーションを終了します。</span><span class="sxs-lookup"><span data-stu-id="2571c-316">Type **exit** and press the **Enter** key to close the application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2571c-317">関連項目</span><span class="sxs-lookup"><span data-stu-id="2571c-317">See Also</span></span>  
 [<span data-ttu-id="2571c-318">チュートリアル: ホスト変更時の下位互換性を有効にします。</span><span class="sxs-lookup"><span data-stu-id="2571c-318">Walkthrough: Enabling Backward Compatibility as Your Host Changes</span></span>](https://msdn.microsoft.com/library/6fa15bb5-8f04-407d-bd7d-675dc043c848)  
 [<span data-ttu-id="2571c-319">チュートリアル: アドインとホスト間でコレクションの引き渡し</span><span class="sxs-lookup"><span data-stu-id="2571c-319">Walkthrough: Passing Collections Between Hosts and Add-Ins</span></span>](https://msdn.microsoft.com/library/b532c604-548e-4fab-b11c-377257dd0ee5)  
 [<span data-ttu-id="2571c-320">パイプライン開発の必要条件</span><span class="sxs-lookup"><span data-stu-id="2571c-320">Pipeline Development Requirements</span></span>](https://msdn.microsoft.com/library/ef9fa986-e80b-43e1-868b-247f4c1d9da5)  
 [<span data-ttu-id="2571c-321">コントラクト、ビュー、およびアダプター</span><span class="sxs-lookup"><span data-stu-id="2571c-321">Contracts, Views, and Adapters</span></span>](https://msdn.microsoft.com/library/a6460173-9507-4b87-8c07-d4ee245d715c)  
 [<span data-ttu-id="2571c-322">パイプライン開発</span><span class="sxs-lookup"><span data-stu-id="2571c-322">Pipeline Development</span></span>](../../../docs/framework/add-ins/pipeline-development.md)
