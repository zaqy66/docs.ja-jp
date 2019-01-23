---
title: '方法: シーケンシャル ワークフローの作成'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5280e816-ae17-48c4-8de0-a1e6895dd8f0
ms.openlocfilehash: 33a4d6f7db140023bc33839fec7d5e28b7f5fe51
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547307"
---
# <a name="how-to-create-a-sequential-workflow"></a><span data-ttu-id="5e22c-102">方法: シーケンシャル ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="5e22c-102">How to: Create a Sequential Workflow</span></span>
<span data-ttu-id="5e22c-103">ワークフローは、ビルトイン アクティビティおよびカスタム アクティビティから構築できます。</span><span class="sxs-lookup"><span data-stu-id="5e22c-103">Workflows can be constructed from built-in activities as well as from custom activities.</span></span> <span data-ttu-id="5e22c-104">このトピックでなど両方の組み込みのアクティビティを使用するワークフローを作成する手順、<xref:System.Activities.Statements.Sequence>アクティビティ、およびカスタム アクティビティ、前の[方法。アクティビティ作成](../../../docs/framework/windows-workflow-foundation/how-to-create-an-activity.md)トピック。</span><span class="sxs-lookup"><span data-stu-id="5e22c-104">This topic steps through creating a workflow that uses both built-in activities such as the <xref:System.Activities.Statements.Sequence> activity, and the custom activities from the previous [How to: Create an Activity](../../../docs/framework/windows-workflow-foundation/how-to-create-an-activity.md) topic.</span></span> <span data-ttu-id="5e22c-105">このワークフローは、数値推測ゲームをモデル化しています。</span><span class="sxs-lookup"><span data-stu-id="5e22c-105">The workflow models a number guessing game.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5e22c-106">チュートリアル入門の各トピックは、前のトピックに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="5e22c-106">Each topic in the Getting Started tutorial depends on the previous topics.</span></span> <span data-ttu-id="5e22c-107">このトピックを完了する必要がありますを完了して[方法。アクティビティ作成](../../../docs/framework/windows-workflow-foundation/how-to-create-an-activity.md)です。</span><span class="sxs-lookup"><span data-stu-id="5e22c-107">To complete this topic, you must first complete [How to: Create an Activity](../../../docs/framework/windows-workflow-foundation/how-to-create-an-activity.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5e22c-108">チュートリアルの完成版をダウンロードするには、「 [Windows Workflow Foundation (WF45) - Getting Started Tutorial (Windows Workflow Foundation (WF45) - チュートリアル入門)](https://go.microsoft.com/fwlink/?LinkID=248976)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e22c-108">To download a completed version of the tutorial, see [Windows Workflow Foundation (WF45) - Getting Started Tutorial](https://go.microsoft.com/fwlink/?LinkID=248976).</span></span>  
  
### <a name="to-create-the-workflow"></a><span data-ttu-id="5e22c-109">ワークフローを作成するには</span><span class="sxs-lookup"><span data-stu-id="5e22c-109">To create the workflow</span></span>  
  
1.  <span data-ttu-id="5e22c-110">右クリック**NumberGuessWorkflowActivities**で**ソリューション エクスプ ローラー**選択**追加**、**新しい項目の**します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-110">Right-click **NumberGuessWorkflowActivities** in **Solution Explorer** and select **Add**, **New Item**.</span></span>  
  
2.  <span data-ttu-id="5e22c-111">**インストール済み**、**一般的な項目**ノードの **ワークフロー**します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-111">In the **Installed**, **Common Items** node, select **Workflow**.</span></span> <span data-ttu-id="5e22c-112">選択**アクティビティ**から、**ワークフロー**一覧。</span><span class="sxs-lookup"><span data-stu-id="5e22c-112">Select **Activity** from the **Workflow** list.</span></span>  
  
3.  <span data-ttu-id="5e22c-113">型`SequentialNumberGuessWorkflow`に、**名前**ボックスし、をクリックして**追加**します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-113">Type `SequentialNumberGuessWorkflow` into the **Name** box and click **Add**.</span></span>  
  
4.  <span data-ttu-id="5e22c-114">ドラッグ、**シーケンス**からのアクティビティ、**制御フロー**のセクション、**ツールボックス**にドロップし、**ここにアクティビティをドロップ**のラベルをワークフロー デザイン サーフェイス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-114">Drag a **Sequence** activity from the **Control Flow** section of the **Toolbox** and drop it onto the **Drop activity here** label on the workflow design surface.</span></span>  
  
### <a name="to-create-the-workflow-variables-and-arguments"></a><span data-ttu-id="5e22c-115">ワークフロー変数および引数を作成するには</span><span class="sxs-lookup"><span data-stu-id="5e22c-115">To create the workflow variables and arguments</span></span>  
  
1.  <span data-ttu-id="5e22c-116">ダブルクリック**SequentialNumberGuessWorkflow.xaml**で**ソリューション エクスプ ローラー**まだ表示されていない場合に、デザイナーでワークフローを表示します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-116">Double-click **SequentialNumberGuessWorkflow.xaml** in **Solution Explorer** to display the workflow in the designer, if it is not already displayed.</span></span>  
  
2.  <span data-ttu-id="5e22c-117">クリックして**引数**を表示するワークフロー デザイナーの左下で、**引数**ウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-117">Click **Arguments** in the lower-left side of the workflow designer to display the **Arguments** pane.</span></span>  
  
3.  <span data-ttu-id="5e22c-118">クリックして**引数の作成**です。</span><span class="sxs-lookup"><span data-stu-id="5e22c-118">Click **Create Argument**.</span></span>  
  
4.  <span data-ttu-id="5e22c-119">型`MaxNumber`に、**名前**ボックスで、**で**から、**方向**ドロップダウン リストで、 **Int32** から**引数の型**ドロップダウン リスト、および引数を保存するには ENTER キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-119">Type `MaxNumber` into the **Name** box, select **In** from the **Direction** drop-down list, select **Int32** from the **Argument type** drop-down list, and then press ENTER to save the argument.</span></span>  
  
5.  <span data-ttu-id="5e22c-120">クリックして**引数の作成**です。</span><span class="sxs-lookup"><span data-stu-id="5e22c-120">Click **Create Argument**.</span></span>  
  
6.  <span data-ttu-id="5e22c-121">型`Turns`に、**名前**新しく追加された下にあるボックス`MaxNumber`引数で、**アウト**から、**方向**選択ドロップダウンリスト**Int32**から、**引数の型**ドロップダウン リスト、および ENTER キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-121">Type `Turns` into the **Name** box that is below the newly added `MaxNumber` argument, select **Out** from the **Direction** drop-down list, select **Int32** from the **Argument type** drop-down list, and then press ENTER.</span></span>  
  
7.  <span data-ttu-id="5e22c-122">クリックして**引数**を閉じるアクティビティ デザイナーの左下で、**引数**ウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-122">Click **Arguments** in the lower-left side of the activity designer to close the **Arguments** pane.</span></span>  
  
8.  <span data-ttu-id="5e22c-123">クリックして**変数**を表示するワークフロー デザイナーの左下で、**変数**ウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-123">Click **Variables** in the lower-left side of the workflow designer to display the **Variables** pane.</span></span>  
  
9. <span data-ttu-id="5e22c-124">クリックして**変数作成**です。</span><span class="sxs-lookup"><span data-stu-id="5e22c-124">Click **Create Variable**.</span></span>  
  
    > [!TIP]
    >  <span data-ttu-id="5e22c-125">ない場合は**変数の作成**ボックスが表示されたら、をクリックして、**シーケンス**ことを選択するには、ワークフロー デザイナー画面上のアクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-125">If no **Create Variable** box is displayed, click the **Sequence** activity on the workflow designer surface to select it.</span></span>  
  
10. <span data-ttu-id="5e22c-126">型`Guess`に、**名前**ボックスで、 **Int32**から、**変数の型**ドロップダウン リスト、および、変数に保存するには ENTER キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-126">Type `Guess` into the **Name** box, select **Int32** from the **Variable type** drop-down list, and then press ENTER to save the variable.</span></span>  
  
11. <span data-ttu-id="5e22c-127">クリックして**変数作成**です。</span><span class="sxs-lookup"><span data-stu-id="5e22c-127">Click **Create Variable**.</span></span>  
  
12. <span data-ttu-id="5e22c-128">型`Target`に、**名前**ボックスで、 **Int32**から、**変数の型**ドロップダウン リスト、および、変数に保存するには ENTER キーを押します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-128">Type `Target` into the **Name** box, select **Int32** from the **Variable type** drop-down list, and then press ENTER to save the variable.</span></span>  
  
13. <span data-ttu-id="5e22c-129">クリックして**変数**を閉じるアクティビティ デザイナーの左下で、**変数**ウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-129">Click **Variables** in the lower-left side of the activity designer to close the **Variables** pane.</span></span>  
  
### <a name="to-add-the-workflow-activities"></a><span data-ttu-id="5e22c-130">ワークフロー アクティビティを追加するには</span><span class="sxs-lookup"><span data-stu-id="5e22c-130">To add the workflow activities</span></span>  
  
1.  <span data-ttu-id="5e22c-131">ドラッグ、**割り当てる**からのアクティビティ、**プリミティブ**のセクション、**ツールボックス**にドロップし、**シーケンス**アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-131">Drag an **Assign** activity from the **Primitives** section of the **Toolbox** and drop it onto the **Sequence** activity.</span></span> <span data-ttu-id="5e22c-132">型`Target`に、**に**ボックスし、次の式を**c# 式を入力します**または**VB の式を入力します。** ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-132">Type `Target` into the **To** box and the following expression into the **Enter a C# expression** or **Enter a VB expression** box.</span></span>  
  
    ```vb  
    New System.Random().Next(1, MaxNumber + 1)  
    ```  
  
    ```csharp  
    new System.Random().Next(1, MaxNumber + 1)  
    ```  
  
    > [!TIP]
    >  <span data-ttu-id="5e22c-133">場合、**ツールボックス**ウィンドウが表示されない場合、選択**ツールボックス**から、**ビュー**メニュー。</span><span class="sxs-lookup"><span data-stu-id="5e22c-133">If the **Toolbox** window is not displayed, select **Toolbox** from the **View** menu.</span></span>  
  
2.  <span data-ttu-id="5e22c-134">ドラッグ、 **DoWhile**からのアクティビティ、**制御フロー**のセクション、**ツールボックス**下に、ワークフローにドロップし、**割り当てる**アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-134">Drag a **DoWhile** activity from the **Control Flow** section of the **Toolbox** and drop it on the workflow so that it is below the **Assign** activity.</span></span>  
  
3.  <span data-ttu-id="5e22c-135">次の式を入力、 **DoWhile**アクティビティの**条件**プロパティ値ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-135">Type the following expression into the **DoWhile** activity’s **Condition** property value box.</span></span>  
  
    ```vb  
    Guess <> Target  
    ```  
  
    ```csharp  
    Guess != Target  
    ```  
  
     <span data-ttu-id="5e22c-136"><xref:System.Activities.Statements.DoWhile> アクティビティはその子アクティビティを実行し、その <xref:System.Activities.Statements.DoWhile.Condition%2A> を評価します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-136">A <xref:System.Activities.Statements.DoWhile> activity executes its child activities and then evaluates its <xref:System.Activities.Statements.DoWhile.Condition%2A>.</span></span> <span data-ttu-id="5e22c-137"><xref:System.Activities.Statements.DoWhile.Condition%2A> が `True` と評価される場合、<xref:System.Activities.Statements.DoWhile> 内のアクティビティが再度実行されます。</span><span class="sxs-lookup"><span data-stu-id="5e22c-137">If the <xref:System.Activities.Statements.DoWhile.Condition%2A> evaluates to `True`, then the activities in the <xref:System.Activities.Statements.DoWhile> execute again.</span></span> <span data-ttu-id="5e22c-138">この例では、ユーザーの推定値が評価され、推定値が正しいと判断されるまで <xref:System.Activities.Statements.DoWhile> が続行されます。</span><span class="sxs-lookup"><span data-stu-id="5e22c-138">In this example, the user’s guess is evaluated and the <xref:System.Activities.Statements.DoWhile> continues until the guess is correct.</span></span>  
  
4.  <span data-ttu-id="5e22c-139">ドラッグ、**プロンプト**からのアクティビティ、 **NumberGuessWorkflowActivities**のセクション、**ツールボックス**にドロップし、 **DoWhile**アクティビティ前の手順。</span><span class="sxs-lookup"><span data-stu-id="5e22c-139">Drag a **Prompt** activity from the **NumberGuessWorkflowActivities** section of the **Toolbox** and drop it in the **DoWhile** activity from the previous step.</span></span>  
  
5.  <span data-ttu-id="5e22c-140">**プロパティ ウィンドウ**、型`"EnterGuess"`に引用符を含む、 **BookmarkName**のプロパティ値ボックスに、**プロンプト**アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-140">In the **Properties Window**, type `"EnterGuess"` including the quotes into the **BookmarkName** property value box for the **Prompt** activity.</span></span> <span data-ttu-id="5e22c-141">型`Guess`に、**結果**プロパティの値のボックスとには、次の式を入力、**テキスト**プロパティ ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-141">Type `Guess` into the **Result** property value box, and type the following expression into the **Text** property box.</span></span>  
  
    ```vb  
    "Please enter a number between 1 and " & MaxNumber  
    ```  
  
    ```csharp  
    "Please enter a number between 1 and " + MaxNumber  
    ```  
  
    > [!TIP]
    >  <span data-ttu-id="5e22c-142">場合、**プロパティ ウィンドウ**が表示されている、選択**プロパティ ウィンドウ**から、**ビュー**メニュー。</span><span class="sxs-lookup"><span data-stu-id="5e22c-142">If the **Properties Window** is not displayed, select **Properties Window** from the **View** menu.</span></span>  
  
6.  <span data-ttu-id="5e22c-143">ドラッグ、**割り当てる**からのアクティビティ、**プリミティブ**のセクション、**ツールボックス**にドロップし、 **DoWhile**アクティビティの後になるように、**プロンプト**アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-143">Drag an **Assign** activity from the **Primitives** section of the **Toolbox** and drop it in the **DoWhile** activity so that it follows the **Prompt** activity.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="5e22c-144">ドロップすると、**割り当てる**アクティビティをワークフロー デザイナーが自動的に追加する方法を確認、**シーケンス**両方を含むアクティビティ、**プロンプト**アクティビティと新しく追加されました。**割り当てる**アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-144">When you drop the **Assign** activity, note how the workflow designer automatically adds a **Sequence** activity to contain both the **Prompt** activity and the newly added **Assign** activity.</span></span>  
  
7.  <span data-ttu-id="5e22c-145">型`Turns`に、**に**ボックスと`Turns + 1`に、 **c# 式を入力します**または**VB の式を入力します。** ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-145">Type `Turns` into the **To** box and `Turns + 1` into the **Enter a C# expression** or **Enter a VB expression** box.</span></span>  
  
8.  <span data-ttu-id="5e22c-146">ドラッグ、**場合**からのアクティビティ、**制御フロー**のセクション、**ツールボックス**にドロップし、**シーケンス**アクティビティの後になるように、新しく追加された**割り当てる**アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-146">Drag an **If** activity from the **Control Flow** section of the **Toolbox** and drop it in the **Sequence** activity so that it follows the newly added **Assign** activity.</span></span>  
  
9. <span data-ttu-id="5e22c-147">次の式を入力、**場合**アクティビティの**条件**プロパティ値ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-147">Type the following expression into the **If** activity’s **Condition** property value box.</span></span>  
  
    ```vb  
    Guess <> Target  
    ```  
  
    ```csharp  
    Guess != Target  
    ```  
  
10. <span data-ttu-id="5e22c-148">もう 1 つドラッグ**場合**からのアクティビティ、**制御フロー**のセクション、**ツールボックス**にドロップし、**し**最初のセクション**場合**アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="5e22c-148">Drag another **If** activity from the **Control Flow** section of the **Toolbox** and drop it in the **Then** section of the first **If** activity.</span></span>  
  
11. <span data-ttu-id="5e22c-149">新しく追加された次の式を入力**場合**アクティビティの**条件**プロパティ値ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-149">Type the following expression into the newly added **If** activity’s **Condition** property value box.</span></span>  
  
    ```
    Guess < Target  
    ```  
  
12. <span data-ttu-id="5e22c-150">2 つをドラッグして**WriteLine**アクティビティから、**プリミティブ**のセクション、**ツールボックス**で 1 つがされるようにドロップし、**し**のセクション新しく追加された**場合**、もう 1 つは、 **Else**セクション。</span><span class="sxs-lookup"><span data-stu-id="5e22c-150">Drag two **WriteLine** activities from the **Primitives** section of the **Toolbox** and drop them so that one is in the **Then** section of the newly added **If** activity, and one is in the **Else** section.</span></span>  
  
13. <span data-ttu-id="5e22c-151">をクリックして、 **WriteLine**内のアクティビティ、**し**セクションを選択しとには、次の式を入力、**テキスト**プロパティ値ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-151">Click the **WriteLine** activity in the **Then** section to select it, and type the following expression into the **Text** property value box.</span></span>  
  
    ```vb  
    "Your guess is too low."  
    ```  
  
14. <span data-ttu-id="5e22c-152">をクリックして、 **WriteLine**内のアクティビティ、 **Else**セクションを選択しとには、次の式を入力、**テキスト**プロパティ値ボックス。</span><span class="sxs-lookup"><span data-stu-id="5e22c-152">Click the **WriteLine** activity in the **Else** section to select it, and type the following expression into the **Text** property value box.</span></span>  
  
    ```vb  
    "Your guess is too high."  
    ```  
  
     <span data-ttu-id="5e22c-153">次の例は完成したワークフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="5e22c-153">The following example illustrates the completed workflow.</span></span>  
  
     <span data-ttu-id="5e22c-154">![完成したシーケンシャル ワークフロー](../../../docs/framework/windows-workflow-foundation/media/wfsequentialgettingstartedtutorialcomplete.JPG "WFSequentialGettingStartedTutorialComplete")</span><span class="sxs-lookup"><span data-stu-id="5e22c-154">![Completed Sequential Workflow](../../../docs/framework/windows-workflow-foundation/media/wfsequentialgettingstartedtutorialcomplete.JPG "WFSequentialGettingStartedTutorialComplete")</span></span>  
  
### <a name="to-build-the-workflow"></a><span data-ttu-id="5e22c-155">ワークフローをビルドするには</span><span class="sxs-lookup"><span data-stu-id="5e22c-155">To build the workflow</span></span>  
  
1.  <span data-ttu-id="5e22c-156">Ctrl キーと Shift キーを押しながら B キーを押して、ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="5e22c-156">Press CTRL+SHIFT+B to build the solution.</span></span>  
  
     <span data-ttu-id="5e22c-157">ワークフローを実行する方法について、次のトピックをご覧ください[方法。ワークフローを実行する](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md)します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-157">For instructions on how to run the workflow, please see the next topic, [How to: Run a Workflow](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md).</span></span> <span data-ttu-id="5e22c-158">既に完了している場合、[方法。ワークフローを実行する](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md)さまざまなスタイルのワークフローにステップ イン、シーケンシャル ワークフローこの手順を使用してを実行してに進んで、 [、アプリケーションをビルドして実行](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md#BKMK_ToRunTheApplication)のセクション[方法。ワークフローを実行する](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md)します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-158">If you have already completed the [How to: Run a Workflow](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md) step with a different style of workflow and wish to run it using the sequential workflow from this step, skip ahead to the [To build and run the application](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md#BKMK_ToRunTheApplication) section of [How to: Run a Workflow](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e22c-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e22c-159">See also</span></span>
- <xref:System.Activities.Statements.Flowchart>
- <xref:System.Activities.Statements.FlowDecision>
- [<span data-ttu-id="5e22c-160">Windows Workflow Foundation プログラミング</span><span class="sxs-lookup"><span data-stu-id="5e22c-160">Windows Workflow Foundation Programming</span></span>](../../../docs/framework/windows-workflow-foundation/programming.md)
- [<span data-ttu-id="5e22c-161">ワークフローの設計</span><span class="sxs-lookup"><span data-stu-id="5e22c-161">Designing Workflows</span></span>](../../../docs/framework/windows-workflow-foundation/designing-workflows.md)
- [<span data-ttu-id="5e22c-162">チュートリアル入門</span><span class="sxs-lookup"><span data-stu-id="5e22c-162">Getting Started Tutorial</span></span>](../../../docs/framework/windows-workflow-foundation/getting-started-tutorial.md)
- [<span data-ttu-id="5e22c-163">方法: アクティビティを作成します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-163">How to: Create an Activity</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-create-an-activity.md)
- [<span data-ttu-id="5e22c-164">方法: ワークフローを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e22c-164">How to: Run a Workflow</span></span>](../../../docs/framework/windows-workflow-foundation/how-to-run-a-workflow.md)
