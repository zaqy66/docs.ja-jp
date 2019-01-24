---
title: '方法: オーバー ロードされたプロシージャ (Visual Basic) を呼び出す'
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], overloading
- procedures [Visual Basic], calling
- procedures [Visual Basic], multiple versions
- procedure calls [Visual Basic], overloaded
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
ms.openlocfilehash: 8320bc550c818fd2bea53f75107709eab8456096
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706418"
---
# <a name="how-to-call-an-overloaded-procedure-visual-basic"></a>方法: オーバー ロードされたプロシージャ (Visual Basic) を呼び出す
プロシージャのオーバー ロードの利点は、呼び出しの柔軟性です。 呼び出し元のコードでは、プロシージャに渡すし、どの引数が渡される、1 つのプロシージャの名前を呼び出して必要な情報を取得できます。  
  
### <a name="to-call-a-procedure-that-has-more-than-one-version-defined"></a>定義されている 1 つ以上のバージョンを含むプロシージャを呼び出す  
  
1.  呼び出し元のコードで、プロシージャに渡すデータを決定します。  
  
2.  引数リスト内のデータの表示、通常の方法で、プロシージャの呼び出しを記述します。 引数がパラメーター リストで、プロシージャに対して定義されたバージョンのいずれかと一致してください。  
  
3.  呼び出すプロシージャのバージョンを決定する必要はありません。 Visual Basic では、引数リストに一致するバージョンに制御を渡します。  
  
     次の例では、`post`プロシージャ内で宣言[方法。プロシージャの複数のバージョンを定義](./how-to-define-multiple-versions-of-a-procedure.md)します。 顧客 id を取得、かどうかを決定しますが、`String`または`Integer`、し、いずれの場合も同じ手順を呼び出します。  
  
     [!code-vb[VbVbcnProcedures#56](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_1.vb)]  
  
     [!code-vb[VbVbcnProcedures#57](./codesnippet/VisualBasic/how-to-call-an-overloaded-procedure_2.vb)]  
  
## <a name="see-also"></a>関連項目
- [プロシージャ](./index.md)
- [プロシージャのパラメーターと引数](./procedure-parameters-and-arguments.md)
- [プロシージャのオーバーロード](./procedure-overloading.md)
- [プロシージャのトラブルシューティング](./troubleshooting-procedures.md)
- [方法: 複数のバージョンのプロシージャを定義します。](./how-to-define-multiple-versions-of-a-procedure.md)
- [方法: 省略可能なパラメーターを受け取るプロシージャをオーバー ロードします。](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [方法: 不特定数のパラメーターを受け取るプロシージャをオーバー ロードします。](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)
- [プロシージャのオーバーロードに関する注意事項](./considerations-in-overloading-procedures.md)
- [オーバーロードの解決](./overload-resolution.md)
- [オーバーロード](../../../../visual-basic/language-reference/modifiers/overloads.md)
