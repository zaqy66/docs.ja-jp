---
title: 型 'Object' の引数を使用する場合は、'FileGet' ではなく 'FileGetObject' を使用してください。
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: ddbe187ed1210d238448a5ff3feaee18beea1def
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/22/2018
ms.locfileid: "53768012"
---
# <a name="use-filegetobject-instead-of-fileget-when-using-argument-of-type-object"></a>型 'Object' の引数を使用する場合は、'FileGet' ではなく 'FileGetObject' を使用してください。
`FileGet` メソッドには、型 `Object` の引数が含まれています。 あいまいさを避けるため、`FileGetObject` の代わりに `FileGet` を使用する必要があります。  
  
 `My.Computer.Filesystem` によって提供される機能は、`FileGet` または `FileGetObject` よりも使いやすく、パフォーマンスが優れています。  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  `FileGet` を `FileGetObject`に置き換えます。  
  
2.  `Object` 引数をより具体的な種類にキャストします。  
  
## <a name="see-also"></a>関連項目  
   
 [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)
