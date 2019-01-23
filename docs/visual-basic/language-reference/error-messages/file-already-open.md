---
title: ファイルは既に開かれています。
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: cda72e03eb5c2469b8106957a0c50fbfa5314549
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54567036"
---
# <a name="file-already-open"></a><span data-ttu-id="5ba05-102">ファイルは既に開かれています。</span><span class="sxs-lookup"><span data-stu-id="5ba05-102">File already open</span></span>
<span data-ttu-id="5ba05-103">前に、別のファイルを閉じる必要が場合があります`FileOpen`または他の操作が発生することができます。</span><span class="sxs-lookup"><span data-stu-id="5ba05-103">Sometimes a file must be closed before another `FileOpen` or other operation can occur.</span></span> <span data-ttu-id="5ba05-104">このエラーでは以下の原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="5ba05-104">Among the possible causes of this error are:</span></span>  
  
-   <span data-ttu-id="5ba05-105">シーケンシャル出力モード`FileOpen`操作が既に開いているファイルに対して実行されました。</span><span class="sxs-lookup"><span data-stu-id="5ba05-105">A sequential output mode `FileOpen` operation was executed for a file that is already open</span></span>  
  
-   <span data-ttu-id="5ba05-106">ステートメントは、開くファイルを指します。</span><span class="sxs-lookup"><span data-stu-id="5ba05-106">A statement refers to an open file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="5ba05-107">このエラーを解決するには</span><span class="sxs-lookup"><span data-stu-id="5ba05-107">To correct this error</span></span>  
  
1.  <span data-ttu-id="5ba05-108">ステートメントを実行する前に、ファイルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ba05-108">Close the file before executing the statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ba05-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ba05-109">See also</span></span>
- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
