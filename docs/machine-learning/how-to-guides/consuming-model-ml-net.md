---
title: トレーニング済みの機械学習モデルをアプリで運用化する - ML.NET
description: ML.NET を使用して、アプリケーションでトレーニングおよび評価された機械学習モデルを使用する方法について説明します
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: ff3f0a8856382d020129693bcf722f572fd87606
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131646"
---
# <a name="operationalize-a-trained-machine-learning-model-in-apps---mlnet"></a><span data-ttu-id="eaa59-103">トレーニング済みの機械学習モデルをアプリで運用化する - ML.NET</span><span class="sxs-lookup"><span data-stu-id="eaa59-103">Operationalize a trained machine learning model in apps - ML.NET</span></span>

<span data-ttu-id="eaa59-104">モデルのメトリックに満足したら、次はモデルを "運用化" します。</span><span class="sxs-lookup"><span data-stu-id="eaa59-104">When the model metrics look good to you, it's time to 'operationalize' the model.</span></span> <span data-ttu-id="eaa59-105">構築した `model` オブジェクトは、トレーニング中に "学習" したものと同じ手順を適用して、さまざまな環境で使用、永続化、および再利用することができます。</span><span class="sxs-lookup"><span data-stu-id="eaa59-105">The `model` object you built can be consumed, persisted, and reused in different environments, applying the same steps that it 'learned' during training.</span></span>

<span data-ttu-id="eaa59-106">モデルをファイルに保存し、(場合によっては別のコンテキストで) 再度読み込むには、次の例を使用します。</span><span class="sxs-lookup"><span data-stu-id="eaa59-106">To save the model to a file, and reload it (potentially in a different context), use the following example:</span></span>

```csharp
using (var stream = File.Create(modelPath))
{
    // Saving and loading happens to 'dynamic' models.
    mlContext.Model.Save(model, stream);
}

// Potentially, the lines below can be in a different process altogether.

// When you load the model, it's a transformer.
ITransformer loadedModel;
using (var stream = File.OpenRead(modelPath))
    loadedModel = mlContext.Model.Load(stream);
```
