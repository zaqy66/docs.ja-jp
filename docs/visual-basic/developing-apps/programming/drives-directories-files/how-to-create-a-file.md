---
title: '方法: Visual Basic でファイルを作成する'
ms.date: 07/20/2015
helpviewer_keywords:
- text files [Visual Basic], creating
- files [Visual Basic], creating
ms.assetid: 0253bb6d-5519-4a50-b882-b93ef5cca0d9
ms.openlocfilehash: e9eedb6dafdd181b254610331899b5df7ac0823f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54661374"
---
# <a name="how-to-create-a-file-in-visual-basic"></a><span data-ttu-id="24fad-102">方法: Visual Basic でファイルを作成する</span><span class="sxs-lookup"><span data-stu-id="24fad-102">How to: Create a File in Visual Basic</span></span>
<span data-ttu-id="24fad-103">この例では、<xref:System.IO.File> クラスで <xref:System.IO.File.Create%2A> メソッドを使用して、指定したパスに空のテキスト ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="24fad-103">This example creates an empty text file at the specified path using the <xref:System.IO.File.Create%2A> method in the <xref:System.IO.File> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="24fad-104">例</span><span class="sxs-lookup"><span data-stu-id="24fad-104">Example</span></span>  
 [!code-vb[VbFileIOMisc#1](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-create-a-file_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="24fad-105">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="24fad-105">Compiling the Code</span></span>  
 <span data-ttu-id="24fad-106">ファイルに書き込むには、`file` 変数を使用します。</span><span class="sxs-lookup"><span data-stu-id="24fad-106">Use the `file` variable to write to the file.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="24fad-107">信頼性の高いプログラミング</span><span class="sxs-lookup"><span data-stu-id="24fad-107">Robust Programming</span></span>  
 <span data-ttu-id="24fad-108">ファイルが既に存在する場合、それは置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="24fad-108">If the file already exists, it is replaced.</span></span>  
  
 <span data-ttu-id="24fad-109">次の条件を満たす場合は、例外が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="24fad-109">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="24fad-110">パス名が不適切である場合。</span><span class="sxs-lookup"><span data-stu-id="24fad-110">The path name is malformed.</span></span> <span data-ttu-id="24fad-111">たとえば、不正な文字が含まれている場合や、空白だけの場合などです (<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="24fad-111">For example, it contains illegal characters or is only white space (<xref:System.ArgumentException>).</span></span>  
  
-   <span data-ttu-id="24fad-112">パスが読み取り専用の場合 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="24fad-112">The path is read-only (<xref:System.IO.IOException>).</span></span>  
  
-   <span data-ttu-id="24fad-113">パス名が `Nothing` の場合 (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="24fad-113">The path name is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
-   <span data-ttu-id="24fad-114">パス名が長すぎる場合 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="24fad-114">The path name is too long (<xref:System.IO.PathTooLongException>).</span></span>  
  
-   <span data-ttu-id="24fad-115">パスが無効な場合 (<xref:System.IO.DirectoryNotFoundException>)。</span><span class="sxs-lookup"><span data-stu-id="24fad-115">The path is invalid (<xref:System.IO.DirectoryNotFoundException>).</span></span>  
  
-   <span data-ttu-id="24fad-116">パスがコロン ":" のみである場合 (<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="24fad-116">The path is only a colon ":" (<xref:System.NotSupportedException>).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="24fad-117">.NET Framework セキュリティ</span><span class="sxs-lookup"><span data-stu-id="24fad-117">.NET Framework Security</span></span>  
 <span data-ttu-id="24fad-118">部分信頼環境では、<xref:System.Security.SecurityException> がスローされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="24fad-118">A <xref:System.Security.SecurityException> may be thrown in partial-trust environments.</span></span>  
  
 <span data-ttu-id="24fad-119"><xref:System.IO.File.Create%2A> メソッドへの呼び出しでは、<xref:System.Security.Permissions.FileIOPermission> が必要です。</span><span class="sxs-lookup"><span data-stu-id="24fad-119">The call to the <xref:System.IO.File.Create%2A> method requires <xref:System.Security.Permissions.FileIOPermission>.</span></span>  
  
 <span data-ttu-id="24fad-120">ユーザーがファイルを作成するアクセス許可を持っていない場合、<xref:System.UnauthorizedAccessException> がスローされます。</span><span class="sxs-lookup"><span data-stu-id="24fad-120">An <xref:System.UnauthorizedAccessException> is thrown if the user does not have permission to create the file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24fad-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="24fad-121">See also</span></span>
- <xref:System.IO>
- <xref:System.IO.File.Create%2A>
- [<span data-ttu-id="24fad-122">部分信頼コードからのライブラリの使用</span><span class="sxs-lookup"><span data-stu-id="24fad-122">Using Libraries from Partially Trusted Code</span></span>](../../../../framework/misc/using-libraries-from-partially-trusted-code.md)
- [<span data-ttu-id="24fad-123">コード アクセス セキュリティの基礎</span><span class="sxs-lookup"><span data-stu-id="24fad-123">Code Access Security Basics</span></span>](../../../../framework/misc/code-access-security-basics.md)
