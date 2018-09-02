---
title: コレクション アクティビティの使用
ms.date: 03/30/2017
ms.assetid: e1977cf8-1695-4071-b946-7046fe39601e
ms.openlocfilehash: a92208583ddf1c0d5d85b5af6a250a15ac8851b9
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2018
ms.locfileid: "43422628"
---
# <a name="using-collection-activities"></a><span data-ttu-id="cd83a-102">コレクション アクティビティの使用</span><span class="sxs-lookup"><span data-stu-id="cd83a-102">Using Collection Activities</span></span>
<span data-ttu-id="cd83a-103">このサンプルでは、<xref:System.Activities.Statements.AddToCollection%601> インターフェイスを実装するクラスでコレクション アクティビティ (<xref:System.Activities.Statements.ClearCollection%601>、<xref:System.Activities.Statements.ExistsInCollection%601>、<xref:System.Activities.Statements.RemoveFromCollection%601>、および <xref:System.Collections.ICollection>) を使用する方法と、コレクションを反復処理してコレクション内の各要素の内容を出力するカスタム アクティビティを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-103">This sample demonstrates how to use the collection activities (<xref:System.Activities.Statements.AddToCollection%601>, <xref:System.Activities.Statements.ClearCollection%601>, <xref:System.Activities.Statements.ExistsInCollection%601>, and <xref:System.Activities.Statements.RemoveFromCollection%601>) with a class that implements the <xref:System.Collections.ICollection> interface and how to create a custom activity that iterates over a collection to print out the contents of each element in the collection.</span></span> <span data-ttu-id="cd83a-104">`PrintCollection` という名前のカスタム アクティビティは、`Numbers` という名前のコレクションの項目メンバーをコンソールに出力します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-104">The custom activity, which is named `PrintCollection`, prints to the console the item members of a collection named `Numbers`.</span></span>  
  
 <span data-ttu-id="cd83a-105">次の表で、ワークフローにコレクション操作を提供する 4 つのアクティビティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-105">The following table describes the four activities that provide collection manipulation for workflows.</span></span>  
  
|<span data-ttu-id="cd83a-106">アクティビティ名</span><span class="sxs-lookup"><span data-stu-id="cd83a-106">Activity name</span></span>|<span data-ttu-id="cd83a-107">説明</span><span class="sxs-lookup"><span data-stu-id="cd83a-107">Description</span></span>|  
|-------------------|-----------------|  
|<xref:System.Activities.Statements.AddToCollection%601>|<span data-ttu-id="cd83a-108">項目をコレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-108">Adds an item to a collection.</span></span>|  
|<xref:System.Activities.Statements.ClearCollection%601>|<span data-ttu-id="cd83a-109">コレクションの項目をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-109">Clears all items in a collection</span></span>|  
|<xref:System.Activities.Statements.ExistsInCollection%601>|<span data-ttu-id="cd83a-110">指定された項目がコレクション内に存在する場合、`true` を返します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-110">Returns `true` if specified item exists in collection.</span></span>|  
|<xref:System.Activities.Statements.RemoveFromCollection%601>|<span data-ttu-id="cd83a-111">コレクションから項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-111">Removes an item from a collection.</span></span>|  
  
 <span data-ttu-id="cd83a-112">このサンプルは 2 つのソリューションで構成されます。1 つは CodedWorkflow ディレクトリにあり、もう 1 つは DesignerWorkflow ディレクトリにあります。</span><span class="sxs-lookup"><span data-stu-id="cd83a-112">The sample consists of two solutions, one under the CodedWorkflow directory and the other under the DesignerWorkflow directory.</span></span> <span data-ttu-id="cd83a-113">これらのソリューションでは、アクティビティを使用して同じ目的を達成するための 2 つの異なる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-113">They demonstrate two different ways of using the activities for the same purposes.</span></span>  
  
|<span data-ttu-id="cd83a-114">ソリューション</span><span class="sxs-lookup"><span data-stu-id="cd83a-114">Solution</span></span>|<span data-ttu-id="cd83a-115">説明</span><span class="sxs-lookup"><span data-stu-id="cd83a-115">Description</span></span>|<span data-ttu-id="cd83a-116">メイン ファイル</span><span class="sxs-lookup"><span data-stu-id="cd83a-116">Main Files</span></span>|  
|-|-|-|  
|<span data-ttu-id="cd83a-117">CodedWorkflow</span><span class="sxs-lookup"><span data-stu-id="cd83a-117">CodedWorkflow</span></span>|<span data-ttu-id="cd83a-118">プログラムでコレクション アクティビティを呼び出す方法を示すサンプル クライアント アプリケーション。</span><span class="sxs-lookup"><span data-stu-id="cd83a-118">Sample client application that demonstrates how to invoke the collection activities programmatically.</span></span>|<span data-ttu-id="cd83a-119">**PrintCollection.cs**: コレクション内のすべての項目をコンソールに出力するヘルパー アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="cd83a-119">**PrintCollection.cs**: helper activity to print out to the console every item in a collection.</span></span><br /><br /> <span data-ttu-id="cd83a-120">**Program.cs**: プログラムによって、一連のコレクション アクティビティを実行するシーケンス アクティビティをビルドします。</span><span class="sxs-lookup"><span data-stu-id="cd83a-120">**Program.cs**: programmatically builds a sequence activity that contains a series of collection activities, and executes it.</span></span>|  
|<span data-ttu-id="cd83a-121">DesignerWorkflow</span><span class="sxs-lookup"><span data-stu-id="cd83a-121">DesignerWorkflow</span></span>|<span data-ttu-id="cd83a-122">ワークフロー デザイナーでコレクション アクティビティを宣言的に使用する方法を示すサンプル クライアント アプリケーション。</span><span class="sxs-lookup"><span data-stu-id="cd83a-122">Sample client application that demonstrates how to use the collection activities declaratively in the workflow designer.</span></span>|<span data-ttu-id="cd83a-123">**CollectionWorkflow.xaml**: コレクション アクティビティを使用するデザイナーで宣言によって作成されたワークフローです。</span><span class="sxs-lookup"><span data-stu-id="cd83a-123">**CollectionWorkflow.xaml**: a workflow created declaratively with the designer that uses the collection activities.</span></span><br /><br /> <span data-ttu-id="cd83a-124">**PrintCollection.cs**: コレクション内のすべての項目をコンソールに出力するヘルパー アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="cd83a-124">**PrintCollection.cs**: helper activity to print out to the console every item in a collection.</span></span><br /><br /> <span data-ttu-id="cd83a-125">**Program.cs**: CollectionWorkflow.xaml に記述されたワークフローを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-125">**Program.cs**: invokes the workflow described in CollectionWorkflow.xaml.</span></span>|  
  
 <span data-ttu-id="cd83a-126">デモでは、`Numbers` という名前のカスタム定義アクティビティを使用して、コレクション `PrintCollection` の項目メンバーをコンソールに出力します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-126">In the demonstration, the item members of collection `Numbers` are printed on the console using a custom-defined activity called `PrintCollection`.</span></span>  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="cd83a-127">このサンプルを使用するには</span><span class="sxs-lookup"><span data-stu-id="cd83a-127">To use this sample</span></span>  
  
1.  <span data-ttu-id="cd83a-128">[!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] を使用して、Collection.sln ソリューション ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="cd83a-128">Using [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], open the Collection.sln solution file.</span></span>  
  
2.  <span data-ttu-id="cd83a-129">ソリューションをビルドするには、Ctrl キーと Shift キーを押しながら B キーを押します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-129">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="cd83a-130">ソリューションを実行するには、Ctrl キーを押しながら F5 キーを押します。</span><span class="sxs-lookup"><span data-stu-id="cd83a-130">To run the solution, press CTRL+F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="cd83a-131">サンプルは、既にコンピューターにインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd83a-131">The samples may already be installed on your machine.</span></span> <span data-ttu-id="cd83a-132">続行する前に、次の (既定の) ディレクトリを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cd83a-132">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="cd83a-133">このディレクトリが存在しない場合に移動[Windows Communication Foundation (WCF) と .NET Framework 4 向けの Windows Workflow Foundation (WF) サンプル](https://go.microsoft.com/fwlink/?LinkId=150780)すべて Windows Communication Foundation (WCF) をダウンロードして[!INCLUDE[wf1](../../../../includes/wf1-md.md)]サンプル。</span><span class="sxs-lookup"><span data-stu-id="cd83a-133">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="cd83a-134">このサンプルは、次のディレクトリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="cd83a-134">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\Collection`