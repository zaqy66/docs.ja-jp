---
title: 'エンドポイント: 1 秒あたりの失敗した呼び出し'
ms.date: 03/30/2017
ms.assetid: bcbe9da4-c8dd-4e27-b630-11611adc7580
ms.openlocfilehash: fa4fc1d8a875557f1da9e54e7a05eb012e7c221c
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43856349"
---
# <a name="endpoint-calls-failed-per-second"></a>エンドポイント: 1 秒あたりの失敗した呼び出し
カウンター名 : 1 秒あたりの失敗した呼び出し。  
  
## <a name="description"></a>説明  
 未処理の例外を伴ってこのエンドポイントに到達した、1 秒あたりの呼び出しの回数。  
  
 このカウンターは、パフォーマンス カウンター型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)、次の数式を使用して、その値が計算されます。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)  
  
 このカウンターは、このエンドポイントで未処理の例外が発生すると常にインクリメントされます。  
  
## <a name="see-also"></a>関連項目  
 [コントラクトおよびサービスのエラーの指定と処理](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
