---
title: My.Request オブジェクト (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Request
- My.Request
helpviewer_keywords:
- My.Request object
ms.assetid: 93d5f0e2-6b60-4a2c-8652-d90216f6ad10
ms.openlocfilehash: a9af211df358b8c87cc9735f05d18c191b49500e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716196"
---
# <a name="myrequest-object"></a>My.Request オブジェクト
要求されたページの <xref:System.Web.HttpRequest> オブジェクトを取得します。  
  
## <a name="remarks"></a>Remarks  
 `My.Request` オブジェクトには、現在の HTTP 要求に関する情報が含まれています。  
  
 `My.Request` オブジェクトは、ASP.NET アプリケーションでのみ使うことができます。  
  
## <a name="example"></a>例  
 次の例からヘッダーのコレクションを取得、`My.Request`オブジェクトと使用、 `My.Response` ASP.NET ページに書き込むオブジェクト。  
  
 [!code-vb[VbVbalrMyWeb#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-request-object_1.aspx)]  
  
## <a name="see-also"></a>関連項目
- <xref:System.Web.HttpRequest>
- [My.Response オブジェクト](../../../visual-basic/language-reference/objects/my-response-object.md)
