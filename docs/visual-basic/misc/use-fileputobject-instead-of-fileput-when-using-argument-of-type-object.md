---
title: 型 'Object' の引数を使う場合は、'FilePut' ではなく 'FilePutObject' を使用してください。
ms.date: 07/20/2015
f1_keywords:
- vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
ms.openlocfilehash: df7d7c54992984bcb1684e41f60ae8361a3aed03
ms.sourcegitcommit: 0888d7b24f475c346a3f444de8d83ec1ca7cd234
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/22/2018
ms.locfileid: "53774226"
---
# <a name="use-fileputobject-instead-of-fileput-when-using-argument-of-type-object"></a>型 'Object' の引数を使う場合は、'FilePut' ではなく 'FilePutObject' を使用してください。
`FilePut` メソッドには、型 `Object`の引数が含まれています。 あいまいさを避けるため、`FilePutObject` の代わりに `FilePut` を使用する必要があります。  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   `FilePut` を `FilePutObject`に置き換えます。  
  
-   `Object` 引数をより具体的な種類にキャストします。  
  
-   `My.Computer.FileSystem` オブジェクトで利用できる機能を使用します。  
  
## <a name="see-also"></a>関連項目  
   
 [My.Computer.FileSystem](xref:Microsoft.VisualBasic.FileIO.FileSystem)  
 [My.Computer.FileSystem.WriteAllBytes](xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.WriteAllBytes%2A)
