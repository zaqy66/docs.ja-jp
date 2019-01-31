---
title: ML.NET と Machine Learning の基本を理解する方法について
description: 無料、オープンソース、クロスプラットフォームの機械学習フレームワークである ML.NET について説明します。AI のカスタム ソリューションを構築し、これを .NET アプリケーションに統合できるようになります。
author: cjgronlund
ms.custom: seodec18
ms.topic: overview
ms.date: 11/06/2018
ms.openlocfilehash: fb0ece94d77c76fddc667070a8aaef154fd2053a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55252421"
---
# <a name="what-is-mlnet-and-how-do-i-understand-machine-learning-basics"></a><span data-ttu-id="56485-103">ML.NET と Machine Learning の基本を理解する方法について</span><span class="sxs-lookup"><span data-stu-id="56485-103">What is ML.NET and how do I understand Machine Learning basics?</span></span>

<span data-ttu-id="56485-104">ML.NET は無料、オープンソース、クロスプラットフォームの機械学習フレームワークです。機械学習のカスタム ソリューションを構築し、これを .NET アプリケーションに統合できるようになります。</span><span class="sxs-lookup"><span data-stu-id="56485-104">ML.NET is a free, open-source, and cross-platform machine learning framework that enables you to build custom machine learning solutions and integrate them into your .NET applications.</span></span> <span data-ttu-id="56485-105">ML.NET API により、.NET を離れることなく、お持ちの .NET スキルを使用してアプリに AI を組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="56485-105">With the ML.NET APIs you can incorporate AI into your apps using the .NET skills you already have and without leaving .NET.</span></span>

## <a name="what-is-machine-learning"></a><span data-ttu-id="56485-106">機械学習とは</span><span class="sxs-lookup"><span data-stu-id="56485-106">What is machine learning?</span></span>

<span data-ttu-id="56485-107">機械学習とは、コンピューターが既存のデータを使用し、将来の動作、結果および傾向を予測するデータ サイエンス テクニックです。</span><span class="sxs-lookup"><span data-stu-id="56485-107">Machine learning is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes, and trends.</span></span> <span data-ttu-id="56485-108">機械学習を使用すると、明示的にプログラミングをしなくても、コンピューターに学習させることが可能です。</span><span class="sxs-lookup"><span data-stu-id="56485-108">Using machine learning, computers learn without being explicitly programmed.</span></span>

<span data-ttu-id="56485-109">機械学習の予測でアプリおよびデバイスはより賢くなります。</span><span class="sxs-lookup"><span data-stu-id="56485-109">Forecasts or predictions from machine learning can make apps and devices smarter.</span></span> <span data-ttu-id="56485-110">オンライン ショッピングのとき、機械学習は購入履歴に基づいて他の製品も勧めます。</span><span class="sxs-lookup"><span data-stu-id="56485-110">When you shop online, machine learning helps recommend other products you might like based on what you've purchased.</span></span> <span data-ttu-id="56485-111">クレジット カードを読み取るとき、不正行為を検出するために、機械学習はそのトランザクションをデータベースのトランザクションと比較します。</span><span class="sxs-lookup"><span data-stu-id="56485-111">When your credit card is swiped, machine learning compares the transaction to a database of transactions and helps detect fraud.</span></span> <span data-ttu-id="56485-112">ロボット掃除機で部屋を掃除するとき、機械学習は作業が完了したかを判断します。</span><span class="sxs-lookup"><span data-stu-id="56485-112">When your robot vacuum cleaner vacuums a room, machine learning helps it decide whether the job is done.</span></span>


## <a name="short-videos-on-data-science"></a><span data-ttu-id="56485-113">データ サイエンスに関する短いビデオ</span><span class="sxs-lookup"><span data-stu-id="56485-113">Short videos on data science</span></span> 

<span data-ttu-id="56485-114">5 つの短い*初心者向けデータ サイエンス* ビデオで、一流のデータ サイエンティストが機械学習とデータ サイエンスの概要を簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="56485-114">Get a quick introduction to the basics of machine learning and data science from *Data Science for Beginners* in five short videos from a top data scientist.</span></span> <span data-ttu-id="56485-115">これらは基本的な内容を扱っているビデオですが、データ サイエンスの実行に関心を持っている場合や、データ サイエンティストと共に作業する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="56485-115">These videos are basic but useful, whether you're interested in doing data science or you work with data scientists.</span></span>

* <span data-ttu-id="56485-116">ビデオ 1: [データ サイエンスが回答する 5 つの質問](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-the-5-questions-data-science-answers) *(5 分 14 秒)*</span><span class="sxs-lookup"><span data-stu-id="56485-116">Video 1: [The 5 questions data science answers](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-the-5-questions-data-science-answers) *(5 min 14 sec)*.</span></span>

* <span data-ttu-id="56485-117">ビデオ 2: [データ サイエンス用のデータの準備はお済みですか?](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-is-your-data-ready-for-data-science)</span><span class="sxs-lookup"><span data-stu-id="56485-117">Video 2: [Is your data ready for data science?](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-is-your-data-ready-for-data-science)</span></span> <span data-ttu-id="56485-118">*(4 分 56 秒)*</span><span class="sxs-lookup"><span data-stu-id="56485-118">*(4 min 56 sec)*</span></span>

* <span data-ttu-id="56485-119">ビデオ 3: [データで回答できる質問をする](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-ask-a-question-you-can-answer-with-data) *(4 分 17 秒)*</span><span class="sxs-lookup"><span data-stu-id="56485-119">Video 3: [Ask a question you can answer with data](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-ask-a-question-you-can-answer-with-data) *(4 min 17 sec)*</span></span>

* <span data-ttu-id="56485-120">ビデオ 4: [単純なモデルで回答を予測する](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-predict-an-answer-with-a-simple-model) *(7 分 42 秒)*</span><span class="sxs-lookup"><span data-stu-id="56485-120">Video 4: [Predict an answer with a simple model](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-predict-an-answer-with-a-simple-model) *(7 min 42 sec)*</span></span>

* <span data-ttu-id="56485-121">ビデオ 5: [他のユーザーの成果物をコピーしてデータ サイエンスを実行する](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-copy-other-peoples-work-to-do-data-science) *(3 分 18 秒)*</span><span class="sxs-lookup"><span data-stu-id="56485-121">Video 5: [Copy other people's work to do data science](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-copy-other-peoples-work-to-do-data-science) *(3 min 18 sec)*</span></span>
