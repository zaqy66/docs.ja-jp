---
title: My.Forms および My.WebServices が提供する既定のオブジェクト インスタンス (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My.WebServices object [Visual Basic], developing applications
- My.Forms object [Visual Basic], developing applications
- rapid application development (RAD), My.Forms
- rapid application development (RAD), My.WebServices
ms.assetid: de930027-9108-4f0c-b97c-5e7db4d6ef79
ms.openlocfilehash: 9285e88e3dc9fd8b3731416b1c40811188d6a33d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563601"
---
# <a name="default-object-instances-provided-by-myforms-and-mywebservices-visual-basic"></a>My.Forms および My.WebServices が提供する既定のオブジェクト インスタンス (Visual Basic)
[My.Forms](../../../visual-basic/language-reference/objects/my-forms-object.md)と[My.WebServices](../../../visual-basic/language-reference/objects/my-webservices-object.md)オブジェクトは、フォーム、データ ソース、およびアプリケーションによって使用される XML Web サービスへのアクセスを提供します。 コレクションを提供することによってこれを実現*既定インスタンス*のこれらの各オブジェクト。  
  
## <a name="default-instances"></a>既定のインスタンス  
 既定のインスタンスがインスタンスには、ランタイムによって提供されする必要はありませんが、クラスの宣言およびインスタンスを使用して、`Dim`と`New`ステートメント。 次の例は、どのようにする可能性がありますが宣言およびインスタンスのインスタンスを<xref:System.Windows.Forms.Form>と呼ばれるクラス`Form1`、どのようにこの既定のインスタンスを取得することができました<xref:System.Windows.Forms.Form>クラスを通じて`My.Forms`します。  
  
 [!code-vb[VbVbcnMy#5](../../../visual-basic/developing-apps/development-with-my/codesnippet/VisualBasic/default-object-instances-provided-by-my-forms-and-my-webservices_1.vb)]  
  
 [!code-vb[VbVbcnMy#6](../../../visual-basic/developing-apps/development-with-my/codesnippet/VisualBasic/default-object-instances-provided-by-my-forms-and-my-webservices_2.vb)]  
  
 `My.Forms`オブジェクトの既定のインスタンスのコレクションを返すすべて`Form`プロジェクト内に存在するクラス。 同様に、`My.WebServices`アプリケーションへの参照を作成したすべての Web サービスのプロキシ クラスの既定のインスタンスを提供します。  
  
## <a name="see-also"></a>関連項目
- [My.Forms オブジェクト](../../../visual-basic/language-reference/objects/my-forms-object.md)
- [My.WebServices オブジェクト](../../../visual-basic/language-reference/objects/my-webservices-object.md)
- [プロジェクトの種類に応じた My の機能](../../../visual-basic/developing-apps/development-with-my/how-my-depends-on-project-type.md)
