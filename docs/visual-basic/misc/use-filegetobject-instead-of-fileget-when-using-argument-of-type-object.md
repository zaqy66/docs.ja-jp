---
title: 型 'Object' の引数を使用する場合は、'FileGet' ではなく 'FileGetObject' を使用してください。
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: 60eaabc686070aced908116728f06d4e82b5cecb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723395"
---
# <a name="use-filegetobject-instead-of-fileget-when-using-argument-of-type-object"></a><span data-ttu-id="6ecad-102">型 'Object' の引数を使用する場合は、'FileGet' ではなく 'FileGetObject' を使用してください。</span><span class="sxs-lookup"><span data-stu-id="6ecad-102">Use 'FileGetObject' instead of 'FileGet' when using argument of type 'Object'</span></span>
<span data-ttu-id="6ecad-103">`FileGet` メソッドには、型 `Object`の引数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ecad-103">The `FileGet` method includes an argument of type `Object`.</span></span> <span data-ttu-id="6ecad-104">あいまいさを避けるため、`FileGetObject` の代わりに `FileGet` を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ecad-104">`FileGetObject` should be used in place of `FileGet` to avoid ambiguities.</span></span>  
  
 <span data-ttu-id="6ecad-105">`My.Computer.Filesystem` によって提供される機能は、`FileGet` または `FileGetObject` よりも使いやすく、パフォーマンスが優れています。</span><span class="sxs-lookup"><span data-stu-id="6ecad-105">Notice that the functionality offered by `My.Computer.Filesystem` offers greater ease of use and performance than either `FileGet` or `FileGetObject`.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="6ecad-106">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="6ecad-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="6ecad-107">`FileGet` を `FileGetObject`に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6ecad-107">Replace `FileGet` with `FileGetObject`.</span></span>  
  
2.  <span data-ttu-id="6ecad-108">`Object` 引数をより具体的な種類にキャストします。</span><span class="sxs-lookup"><span data-stu-id="6ecad-108">Cast the `Object` argument to a more specific type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ecad-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ecad-109">See also</span></span>

- [<span data-ttu-id="6ecad-110">My.Computer.FileSystem</span><span class="sxs-lookup"><span data-stu-id="6ecad-110">My.Computer.FileSystem</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem)
