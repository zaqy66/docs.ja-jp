---
title: 機械学習の処理のために複数ファイルのデータを読み込む - ML.NET
description: ML.NET で機械学習モデルの構築、トレーニング、スコア付けに使用するデータを、複数のファイルから読み込む方法について説明します
ms.date: 02/06/2019
ms.custom: mvc,how-to
ms.openlocfilehash: f5108aaed80769f2bc7ed2f974f9a729abe8455e
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2019
ms.locfileid: "56092047"
---
# <a name="load-data-from-multiple-files-for-machine-learning-processing---mlnet"></a><span data-ttu-id="1202f-103">機械学習の処理のために複数ファイルのデータを読み込む - ML.NET</span><span class="sxs-lookup"><span data-stu-id="1202f-103">Load data from multiple files for machine learning processing - ML.NET</span></span>

<span data-ttu-id="1202f-104">`TextLoader` を使用して、ファイルの配列を `Read` メソッドに指定します。</span><span class="sxs-lookup"><span data-stu-id="1202f-104">Use the `TextLoader`, and specify an array of files to the `Read` method.</span></span> <span data-ttu-id="1202f-105">ファイルに含まれているスキーマは同じである必要があります (列の数と種類が同じ)。</span><span class="sxs-lookup"><span data-stu-id="1202f-105">The files must have the same schema (same number and type of columns):</span></span>

* [<span data-ttu-id="1202f-106">ファイルの例 1</span><span class="sxs-lookup"><span data-stu-id="1202f-106">Example file1</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.train)
* [<span data-ttu-id="1202f-107">ファイルの例 2</span><span class="sxs-lookup"><span data-stu-id="1202f-107">Example file2</span></span>](https://github.com/dotnet/machinelearning/blob/e3a34ae6ae1b25ac96faa0317308703ce943ff95/test/data/adult.test)

```csharp
// Create a new context for ML.NET operations. It can be used for exception tracking and logging, 
// as a catalog of available operations and as the source of randomness.
var mlContext = new MLContext();

// Create the reader: define the data columns and where to find them in the text file.
var reader = mlContext.Data.CreateTextLoader(
    columns: new TextLoader.Column[]
    {
        // A boolean column depicting the 'target label'.
        new TextLoader.Column("IsOver50k",DataKind.BL,0),
        // Three text columns.
        new TextLoader.Column("WorkClass",DataKind.TX,1),
        new TextLoader.Column("Education",DataKind.TX,2),
        new TextLoader.Column("MaritalStatus",DataKind.TX,3)
    },
    hasHeader: true
);

// Now read the files (remember though, readers are lazy, so the actual reading will happen when the data is accessed).
var data = reader.Read(exampleFile1, exampleFile2);
```