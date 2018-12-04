---
title: 機械学習の処理のために複数ファイルのデータを読み込む - ML.NET
description: ML.NET で機械学習モデルの構築、トレーニング、スコア付けに使用するデータを、複数のファイルから読み込む方法について説明します
ms.date: 11/07/2018
ms.custom: mvc,how-to
ms.openlocfilehash: c9b34bd6bcbac62e9f9c33226f5d0feb41168392
ms.sourcegitcommit: 7f7664837d35320a0bad3f7e4ecd68d6624633b2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/30/2018
ms.locfileid: "52672406"
---
# <a name="load-data-from-multiple-files-for-machine-learning-processing---mlnet"></a><span data-ttu-id="5fe94-103">機械学習の処理のために複数ファイルのデータを読み込む - ML.NET</span><span class="sxs-lookup"><span data-stu-id="5fe94-103">Load data from multiple files for machine learning processing - ML.NET</span></span>

<span data-ttu-id="5fe94-104">`TextLoader` を使用して、ファイルの配列を `Read` メソッドに指定します。</span><span class="sxs-lookup"><span data-stu-id="5fe94-104">Use the `TextLoader`, and specify an array of files to the `Read` method.</span></span> <span data-ttu-id="5fe94-105">ファイルに含まれているスキーマは同じである必要があります (列の数と種類が同じ)。</span><span class="sxs-lookup"><span data-stu-id="5fe94-105">The files must have the same schema (same number and type of columns):</span></span>

* [<span data-ttu-id="5fe94-106">ファイルの例 1</span><span class="sxs-lookup"><span data-stu-id="5fe94-106">Example file1</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.train)
* [<span data-ttu-id="5fe94-107">ファイルの例 2</span><span class="sxs-lookup"><span data-stu-id="5fe94-107">Example file2</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.test)

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.TextReader(new TextLoader.Arguments
{
    Column = new[] {
        // A boolean column depicting the 'label'.
        new TextLoader.Column("IsOver50k", DataKind.BL, 0),
        // Three text columns.
        new TextLoader.Column("Workclass", DataKind.TX, 1),
        new TextLoader.Column("Education", DataKind.TX, 2),
        new TextLoader.Column("MaritalStatus", DataKind.TX, 3)
    },
    // First line of the file is a header, not a data row.
    HasHeader = true
});

var data = reader.Read(exampleFile1, exampleFile2);
```