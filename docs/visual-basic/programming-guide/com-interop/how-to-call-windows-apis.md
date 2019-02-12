---
title: '方法: Windows API (Visual Basic) を呼び出す'
ms.date: 07/20/2015
helpviewer_keywords:
- API calls [Visual Basic]
- Windows API, calling
- API calls [Visual Basic], platform invoke
- calls [Visual Basic], stored procedures
ms.assetid: 27d75f0a-54ab-4ee1-b91d-43513a19b12d
ms.openlocfilehash: 9eb667c8492c1e20b82e16ae8d640aee872969e5
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738644"
---
# <a name="how-to-call-windows-apis-visual-basic"></a>方法: Windows API (Visual Basic) を呼び出す
この例を定義し、呼び出し、 `MessageBox` user32.dll 内の関数に文字列を渡します。  
  
## <a name="example"></a>例  
 [!code-vb[VbVbalrInterop#1](../../../visual-basic/programming-guide/com-interop/codesnippet/VisualBasic/how-to-call-windows-apis_1.vb)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   <xref:System> 名前空間への参照  
  
## <a name="robust-programming"></a>信頼性の高いプログラミング  
 次の条件を満たす場合は、例外が発生する可能性があります。  
  
-   メソッドが静的でないするには、抽象クラスでは、または以前に定義します。 親の種類がインターフェイス、またはの長さ*名前*または*dllName*は 0 です。 (<xref:System.ArgumentException>)  
  
-   *名前*または*dllName*は`Nothing`します。 (<xref:System.ArgumentNullException>)  
  
-   含んでいる型が `CreateType` を使用して以前に作成されています。 (<xref:System.InvalidOperationException>)  
  
## <a name="see-also"></a>関連項目

- [プラットフォーム呼び出しの詳細](../../../framework/interop/consuming-unmanaged-dll-functions.md#a-closer-look-at-platform-invoke)
- [プラットフォーム呼び出しの例](../../../framework/interop/platform-invoke-examples.md)
- [アンマネージ DLL 関数の処理](../../../framework/interop/consuming-unmanaged-dll-functions.md)
- [出力のリフレクションを使用してメソッドを定義します。](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/w63y4d4f(v=vs.100))
- [チュートリアル: Windows API の呼び出し](../../../visual-basic/programming-guide/com-interop/walkthrough-calling-windows-apis.md)
- [COM 相互運用](../../../visual-basic/programming-guide/com-interop/index.md)
