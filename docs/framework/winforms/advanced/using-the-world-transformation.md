---
title: ワールド変換の使用
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], world transformation
- world transformation [Windows Forms], examples
ms.assetid: 1e717711-1361-448e-aa49-0f3ec43110c9
ms.openlocfilehash: ec232c92d32b91a7b334b237c869db8eb428eccc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647609"
---
# <a name="using-the-world-transformation"></a>ワールド変換の使用
ワールド変換のプロパティである、<xref:System.Drawing.Graphics>クラス。 ワールド変換を指定する数値が格納されている、<xref:System.Drawing.Drawing2D.Matrix>オブジェクトで、3 × 3 行列を表します。 <xref:System.Drawing.Drawing2D.Matrix>と<xref:System.Drawing.Graphics>クラス ワールド変換行列の数値を設定するためのいくつかの方法があります。  
  
## <a name="different-types-of-transformations"></a>異なる種類の変換  
 次の例では、コードは、最初 50 × 50 四角形を作成し、その原点 (0, 0)。 原点は、クライアント領域の左上隅にあること。  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#11)]  
  
 次のコードでは、x 方向に 1.75 倍、四角形を拡大し、y 方向に 0.5 倍で、四角形を縮小するためのスケーリング変換を適用します。  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#12)]  
  
 X 方向に時間が長く、y 方向の元よりも短いとなる四角形になります。  
  
 スケールではなく四角形を回転するには、次のコードを使用します。  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#13)]  
  
 四角形を変換するには、次のコードを使用します。  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#14)]
 [!code-vb[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#14)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Drawing.Drawing2D.Matrix>
- [座標系と変換](../../../../docs/framework/winforms/advanced/coordinate-systems-and-transformations.md)
- [マネージド GDI+ での変換の使用](../../../../docs/framework/winforms/advanced/using-transformations-in-managed-gdi.md)
