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
# <a name="operationalize-a-trained-machine-learning-model-in-apps---mlnet"></a>トレーニング済みの機械学習モデルをアプリで運用化する - ML.NET

モデルのメトリックに満足したら、次はモデルを "運用化" します。 構築した `model` オブジェクトは、トレーニング中に "学習" したものと同じ手順を適用して、さまざまな環境で使用、永続化、および再利用することができます。

モデルをファイルに保存し、(場合によっては別のコンテキストで) 再度読み込むには、次の例を使用します。

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
