---
title: 空間関数
ms.date: 03/30/2017
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
ms.openlocfilehash: ad6b722e84aae40354e30434b107752d02352645
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44202090"
---
# <a name="spatial-functions"></a>空間関数
空間型のリテラル形式はありません。 ただし、Well-Known Text 形式の文字列を使用して呼び出す正規の Entity Framework 関数を使用できます。 たとえば、次の関数呼び出しでは、ジオメトリ ポイントが作成されます。  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 [SpatialEdmFunctions メソッド](https://msdn.microsoft.com/library/hh749531.aspx)ページは、空間に関する正規 Entity Framework メソッドすべてを一覧表示されます。 目的のメソッドをクリックすると、関数に渡す必要のあるパラメーターを確認できます。
