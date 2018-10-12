---
title: 1 秒あたりのキューに置かれた有害メッセージ
ms.date: 03/30/2017
ms.assetid: d193fdd1-02f1-44a0-906e-f632a8f574c3
ms.openlocfilehash: d4c921b105dfd1c1a364d2c86f54ab920078dd4a
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43509340"
---
# <a name="queued-poison-messages-per-second"></a>1 秒あたりのキューに置かれた有害メッセージ
カウンター名 : 1 秒あたりのキューに置かれた有害メッセージ  
  
## <a name="description"></a>説明  
 このサービスでキューに置かれたトランスポートによって 1 秒あたりに有害とマークされたメッセージの数です。  
  
 このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
