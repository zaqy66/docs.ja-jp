---
title: '方法: EdmGen.exe を使用してオブジェクトレイヤー コードを生成する'
ms.date: 03/30/2017
ms.assetid: c44d2ebe-f66f-42cb-9741-4a3f0c2dcffb
ms.openlocfilehash: c15ceec66ad5b1c9ef414c3e57e3b6e49c372e7a
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2018
ms.locfileid: "44276620"
---
# <a name="how-to-use-edmgenexe-to-generate-object-layer-code"></a><span data-ttu-id="74d5a-102">方法: EdmGen.exe を使用してオブジェクトレイヤー コードを生成する</span><span class="sxs-lookup"><span data-stu-id="74d5a-102">How to: Use EdmGen.exe to Generate Object-Layer Code</span></span>
<span data-ttu-id="74d5a-103">このトピックでは、使用する方法を示します、 [EDM ジェネレーター (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) .csdl ファイルに基づいてオブジェクト レイヤー コードを生成するためのツール。</span><span class="sxs-lookup"><span data-stu-id="74d5a-103">This topic shows how to use the [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) tool to generate object-layer code  based on the .csdl file.</span></span>  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-visual-basic-project-using-edmgenexe"></a><span data-ttu-id="74d5a-104">EdmGen.exe を使用して Visual Basic プロジェクト用の School モデルのオブジェクトレイヤー コードを生成するには</span><span class="sxs-lookup"><span data-stu-id="74d5a-104">To generate object-layer code for the School model for a Visual Basic project using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="74d5a-105">School データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-105">Create the School database.</span></span> <span data-ttu-id="74d5a-106">詳細については、次を参照してください。 [School サンプル データベースを作成する](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0)します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-106">For more information, see [Creating the School Sample Database](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span></span>  
  
2.  <span data-ttu-id="74d5a-107">School モデルを生成するか、School.csdl ファイルを取得します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-107">Generate the School model or obtain the School.csdl file.</span></span> <span data-ttu-id="74d5a-108">詳細については、次を参照してください。[方法: モデル ファイルとマッピング ファイルを生成する使用 EdmGen.exe](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-108">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="74d5a-109">コマンド プロンプトで、次のコマンド (改行なし) を実行します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-109">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.vb /language:VB  
    ```  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-c-project-using-edmgenexe"></a><span data-ttu-id="74d5a-110">EdmGen.exe を使用して C# プロジェクト用の School モデルのオブジェクトレイヤー コードを生成するには</span><span class="sxs-lookup"><span data-stu-id="74d5a-110">To generate object-layer code for the School model for a C# project using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="74d5a-111">School データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-111">Create the School database.</span></span> <span data-ttu-id="74d5a-112">詳細については、次を参照してください。 [School サンプル データベースを作成する](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0)します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-112">For more information, see [Creating the School Sample Database](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span></span>  
  
2.  <span data-ttu-id="74d5a-113">School モデルを生成するか、School.csdl ファイルを取得します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-113">Generate the School model or obtain the School.csdl file.</span></span> <span data-ttu-id="74d5a-114">詳細については、次を参照してください。[方法: モデル ファイルとマッピング ファイルを生成する使用 EdmGen.exe](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-114">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="74d5a-115">コマンド プロンプトで、次のコマンド (改行なし) を実行します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-115">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.cs /language:CSharp  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="74d5a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="74d5a-116">See Also</span></span>  
 [<span data-ttu-id="74d5a-117">モデリングとマッピング</span><span class="sxs-lookup"><span data-stu-id="74d5a-117">Modeling and Mapping</span></span>](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)  
 [<span data-ttu-id="74d5a-118">方法: Entity Framework プロジェクトを手動で構成します。</span><span class="sxs-lookup"><span data-stu-id="74d5a-118">How to: Manually Configure an Entity Framework Project</span></span>](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)  
 [<span data-ttu-id="74d5a-119">ADO.NET Entity Data Model ツール</span><span class="sxs-lookup"><span data-stu-id="74d5a-119">ADO.NET Entity Data Model  Tools</span></span>](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)  
 [<span data-ttu-id="74d5a-120">方法: クエリのパフォーマンスを向上させるためにビューを事前に生成</span><span class="sxs-lookup"><span data-stu-id="74d5a-120">How to: Pre-Generate Views to Improve Query Performance</span></span>](https://msdn.microsoft.com/library/b18a9d16-e10b-4043-ba91-b632f85a2579)  
 [<span data-ttu-id="74d5a-121">方法: EdmGen.exe を使用してモデル ファイルとマッピング ファイルを生成する</span><span class="sxs-lookup"><span data-stu-id="74d5a-121">How to: Use EdmGen.exe to Generate the Model and Mapping Files</span></span>](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)
