---
title: '方法 : 独自のスレッドで各 Windows フォームを表示して COM 相互運用機能をサポートする'
ms.date: 03/30/2017
dev_langs:
- vb
helpviewer_keywords:
- COM interop [Windows Forms], Windows Forms
- COM [Windows Forms]
- Windows Forms, unmanaged
- ActiveX controls [Windows Forms], COM interop
- Windows Forms, interop
ms.assetid: a9e04765-d2de-4389-a494-a9a6d07aa6ee
ms.openlocfilehash: d0d8dfd4a19b31be790d2643847396d136098278
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44085609"
---
# <a name="how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread"></a><span data-ttu-id="62d66-102">方法 : 独自のスレッドで各 Windows フォームを表示して COM 相互運用機能をサポートする</span><span class="sxs-lookup"><span data-stu-id="62d66-102">How to: Support COM Interop by Displaying Each Windows Form on Its Own Thread</span></span>
<span data-ttu-id="62d66-103">[!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] メッセージ ループでフォームを表示して、COM 相互運用性の問題を解決できます。これは、<xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> メソッドを使用して作成することができます。</span><span class="sxs-lookup"><span data-stu-id="62d66-103">You can resolve COM interoperability problems by displaying your form on a [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] message loop, which you can create by using the <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="62d66-104">Windows フォームが COM クライアント アプリケーションから正しく動作するには、Windows フォームのメッセージ ループ上でフォームを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62d66-104">To make a Windows Form work correctly from a COM client application, you must run the form on a Windows Forms message loop.</span></span> <span data-ttu-id="62d66-105">そのためには、次の方法のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="62d66-105">To do this, use one of the following approaches:</span></span>  
  
-   <span data-ttu-id="62d66-106"><xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> メソッドを使用して、Windows フォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="62d66-106">Use the <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> method to display the Windows Form.</span></span> <span data-ttu-id="62d66-107">詳細については、「 [方法 : ShowDialog メソッドで Windows フォームを表示して COM 相互運用機能をサポートする](../../../../docs/framework/winforms/advanced/com-interop-by-displaying-a-windows-form-shadow.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62d66-107">For more information, see [How to: Support COM Interop by Displaying a Windows Form with the ShowDialog Method](../../../../docs/framework/winforms/advanced/com-interop-by-displaying-a-windows-form-shadow.md).</span></span>  
  
-   <span data-ttu-id="62d66-108">各 Windows フォームを別のスレッドで表示します。</span><span class="sxs-lookup"><span data-stu-id="62d66-108">Display each Windows Form on a separate thread.</span></span>  
  
 <span data-ttu-id="62d66-109">Visual Studio でこの機能の広範なサポートがあります。</span><span class="sxs-lookup"><span data-stu-id="62d66-109">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="62d66-110">参照してください[チュートリアル: on Its Own Thread 各 Windows フォームを表示して COM 相互運用をサポート](https://msdn.microsoft.com/library/ms233639\(v=vs.110\))します。</span><span class="sxs-lookup"><span data-stu-id="62d66-110">Also see [Walkthrough: Supporting COM Interop by Displaying Each Windows Form on Its Own Thread](https://msdn.microsoft.com/library/ms233639\(v=vs.110\)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="62d66-111">例</span><span class="sxs-lookup"><span data-stu-id="62d66-111">Example</span></span>  
 <span data-ttu-id="62d66-112">次のコード例は、個別のスレッドでフォームを表示し、<xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> メソッドを呼び出して、スレッドで Windows フォーム メッセージ ポンプを開始する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="62d66-112">The following code example demonstrates how to display the form on a separate thread and call the <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> method to start a Windows Forms message pump on that thread.</span></span> <span data-ttu-id="62d66-113">この方法を使用するには、 <xref:System.Windows.Forms.Control.Invoke%2A> メソッドを使用して、アンマネージ アプリケーションからのフォームの呼び出しをマーシャリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62d66-113">To use this approach, you must marshal any calls to the form from the unmanaged application by using the <xref:System.Windows.Forms.Control.Invoke%2A> method.</span></span>  
  
 <span data-ttu-id="62d66-114">この方法は、独自のメッセージ ループを使用して、独自のスレッドで、フォームの各インスタンスが実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62d66-114">This approach requires that each instance of a form runs on its own thread by using its own message loop.</span></span> <span data-ttu-id="62d66-115">1 つのスレッドに対して複数のメッセージ ループを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="62d66-115">You cannot have more than one message loop running per thread.</span></span> <span data-ttu-id="62d66-116">そのため、クライアント アプリケーションのメッセージ ループを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="62d66-116">Therefore, you cannot change the client application's message loop.</span></span> <span data-ttu-id="62d66-117">ただし、 [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] コンポーネントを変更して、独自のメッセージ ループを使用する新しいスレッドを開始することができます。</span><span class="sxs-lookup"><span data-stu-id="62d66-117">However, you can modify the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] component to start a new thread that uses its own message loop.</span></span>  
  
 [!code-vb[System.Windows.Forms.ComInterop#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ComInterop/VB/COMForm.vb#1)]  
  
 [!code-vb[System.Windows.Forms.ComInterop#10](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ComInterop/VB/FormManager.vb#10)]  
  
 [!code-vb[System.Windows.Forms.ComInterop#100](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ComInterop/VB/Form1.vb#100)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="62d66-118">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="62d66-118">Compiling the Code</span></span>  
  
-   <span data-ttu-id="62d66-119">`COMForm`、 `Form1`、および `FormManager` の型を、 `COMWinform.dll`と呼ばれるアセンブリにコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="62d66-119">Compile the `COMForm`, `Form1`, and `FormManager` types into an assembly called `COMWinform.dll`.</span></span> <span data-ttu-id="62d66-120">「 [Packaging an Assembly for COM](../../../../docs/framework/interop/packaging-an-assembly-for-com.md)」で説明するメソッドのいずれかを使用して COM にアセンブリを登録します。</span><span class="sxs-lookup"><span data-stu-id="62d66-120">Register the assembly for COM interop by using one of the methods described in [Packaging an Assembly for COM](../../../../docs/framework/interop/packaging-an-assembly-for-com.md).</span></span> <span data-ttu-id="62d66-121">これで、アンマネージ アプリケーションのアセンブリと対応する型のライブラリ (.tlb) ファイルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="62d66-121">You can now use the assembly and its corresponding type library (.tlb) file in unmanaged applications.</span></span> <span data-ttu-id="62d66-122">たとえば、Visual Basic 6.0 の実行可能なプロジェクトで参照として型ライブラリを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="62d66-122">For example, you can use the type library as a reference in a Visual Basic 6.0 executable project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62d66-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="62d66-123">See Also</span></span>  
 [<span data-ttu-id="62d66-124">COM への .NET Framework コンポーネントの公開</span><span class="sxs-lookup"><span data-stu-id="62d66-124">Exposing .NET Framework Components to COM</span></span>](../../../../docs/framework/interop/exposing-dotnet-components-to-com.md)  
 [<span data-ttu-id="62d66-125">COM 用のアセンブリのパッケージ化</span><span class="sxs-lookup"><span data-stu-id="62d66-125">Packaging an Assembly for COM</span></span>](../../../../docs/framework/interop/packaging-an-assembly-for-com.md)  
 [<span data-ttu-id="62d66-126">COM へのアセンブリの登録</span><span class="sxs-lookup"><span data-stu-id="62d66-126">Registering Assemblies with COM</span></span>](../../../../docs/framework/interop/registering-assemblies-with-com.md)  
 [<span data-ttu-id="62d66-127">方法: ShowDialog メソッドで Windows フォームを表示して COM 相互運用機能をサポートする</span><span class="sxs-lookup"><span data-stu-id="62d66-127">How to: Support COM Interop by Displaying a Windows Form with the ShowDialog Method</span></span>](../../../../docs/framework/winforms/advanced/com-interop-by-displaying-a-windows-form-shadow.md)  
 [<span data-ttu-id="62d66-128">Windows フォームおよびアンマネージ アプリケーションの概要</span><span class="sxs-lookup"><span data-stu-id="62d66-128">Windows Forms and Unmanaged Applications Overview</span></span>](../../../../docs/framework/winforms/advanced/windows-forms-and-unmanaged-applications-overview.md)
