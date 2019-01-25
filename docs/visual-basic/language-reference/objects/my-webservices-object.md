---
title: My.WebServices オブジェクト (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.WebServices
- My.MyProject.WebServices
helpviewer_keywords:
- My.WebServices object
ms.assetid: f188dc05-2c75-41b6-bb68-122d1c3110a2
ms.openlocfilehash: b3a486cb886e8f39081f30a2849e2d14573cf5e0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676342"
---
# <a name="mywebservices-object"></a><span data-ttu-id="08e8b-102">My.WebServices オブジェクト</span><span class="sxs-lookup"><span data-stu-id="08e8b-102">My.WebServices Object</span></span>
<span data-ttu-id="08e8b-103">プロパティは、作成して、現在のプロジェクトによって参照される各 XML Web サービスの 1 つのインスタンスへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-103">Provides properties for creating and accessing a single instance of each XML Web service referenced by the current project.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="08e8b-104">Remarks</span><span class="sxs-lookup"><span data-stu-id="08e8b-104">Remarks</span></span>  
 <span data-ttu-id="08e8b-105">`My.WebServices` オブジェクトは、現在のプロジェクトにより参照されている各 Web サービスのインスタンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-105">The `My.WebServices` object provides an instance of each Web service referenced by the current project.</span></span> <span data-ttu-id="08e8b-106">各インスタンスは要求に応じてインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="08e8b-106">Each instance is instantiated on demand.</span></span> <span data-ttu-id="08e8b-107">これらの Web サービスには `My.WebServices` オブジェクトのプロパティを介してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="08e8b-107">You can access these Web services through the properties of the `My.WebServices` object.</span></span> <span data-ttu-id="08e8b-108">プロパティの名前は、プロパティがアクセスする Web サービスの名前と同じになります。</span><span class="sxs-lookup"><span data-stu-id="08e8b-108">The name of the property is the same as the name of the Web service that the property accesses.</span></span> <span data-ttu-id="08e8b-109"><xref:System.Web.Services.Protocols.SoapHttpClientProtocol> から継承されたクラスはすべて Web サービスです。</span><span class="sxs-lookup"><span data-stu-id="08e8b-109">Any class that inherits from <xref:System.Web.Services.Protocols.SoapHttpClientProtocol> is a Web service.</span></span> <span data-ttu-id="08e8b-110">Web サービスをプロジェクトに追加する方法の詳細については、次を参照してください。[にアクセスするアプリケーションの Web サービス](../../../visual-basic/developing-apps/programming/accessing-application-web-services.md)します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-110">For information about adding Web services to a project, see [Accessing Application Web Services](../../../visual-basic/developing-apps/programming/accessing-application-web-services.md).</span></span>  
  
 <span data-ttu-id="08e8b-111">`My.WebServices`オブジェクトは、現在のプロジェクトに関連付けられている Web サービスのみを公開します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-111">The `My.WebServices` object exposes only the Web services associated with the current project.</span></span> <span data-ttu-id="08e8b-112">参照される Dll で宣言されている Web サービスへのアクセスは行いません。</span><span class="sxs-lookup"><span data-stu-id="08e8b-112">It does not provide access to Web services declared in referenced DLLs.</span></span> <span data-ttu-id="08e8b-113">DLL を提供する Web サービスにアクセスするには、フォームで、Web サービスの修飾名を使用する必要があります*DllName*.*WebServiceName*します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-113">To access a Web service that a DLL provides, you must use the qualified name of the Web service, in the form *DllName*.*WebServiceName*.</span></span> <span data-ttu-id="08e8b-114">詳細については、次を参照してください。[にアクセスするアプリケーションの Web サービス](../../../visual-basic/developing-apps/programming/accessing-application-web-services.md)します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-114">For more information, see [Accessing Application Web Services](../../../visual-basic/developing-apps/programming/accessing-application-web-services.md).</span></span>  
  
 <span data-ttu-id="08e8b-115">オブジェクトとそのプロパティでは、Web アプリケーションを使用できません。</span><span class="sxs-lookup"><span data-stu-id="08e8b-115">The object and its properties are not available for Web applications.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="08e8b-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="08e8b-116">Properties</span></span>  
 <span data-ttu-id="08e8b-117">各プロパティ、`My.WebServices`オブジェクトは、現在のプロジェクトによって参照される Web サービスのインスタンスへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-117">Each property of the `My.WebServices` object provides access to an instance of a Web service referenced by the current project.</span></span> <span data-ttu-id="08e8b-118">プロパティの名前が同じプロパティがアクセスする Web サービスの名前とプロパティの型が、Web サービスの型と同じです。</span><span class="sxs-lookup"><span data-stu-id="08e8b-118">The name of the property is the same as the name of the Web service that the property accesses, and the property type is the same as the Web service's type.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="08e8b-119">Web サービスにアクセスするためのプロパティ名は、名前の競合がある場合*RootNamespace*_*Namespace*\_*ServiceName*します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-119">If there is a name collision, the property name for accessing a Web service is *RootNamespace*_*Namespace*\_*ServiceName*.</span></span> <span data-ttu-id="08e8b-120">たとえば、という名前の 2 つの Web サービス`Service1`します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-120">For example, consider two Web services named `Service1`.</span></span> <span data-ttu-id="08e8b-121">ルート名前空間ではこれらのサービスのいずれかのかどうかは`WindowsApplication1`と名前空間に`Namespace1`を使用して、そのサービスにアクセス`My.WebServices.WindowsApplication1_Namespace1_Service1`します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-121">If one of these services is in the root namespace `WindowsApplication1` and in the namespace `Namespace1`, you would access that service by using `My.WebServices.WindowsApplication1_Namespace1_Service1`.</span></span>  
  
 <span data-ttu-id="08e8b-122">初めてアクセスしたときの 1 つ、`My.WebServices`オブジェクトのプロパティでは、Web サービスの新しいインスタンスを作成し、格納します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-122">When you first access one of the `My.WebServices` object's properties, it creates a new instance of the Web service and stores it.</span></span> <span data-ttu-id="08e8b-123">そのプロパティの後続のアクセスは、Web サービスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-123">Subsequent accesses of that property return that instance of the Web service.</span></span>  
  
 <span data-ttu-id="08e8b-124">Web サービスを処分するには、割り当てることで`Nothing`をその Web サービスのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="08e8b-124">You can dispose of a Web service by assigning `Nothing` to the property for that Web service.</span></span> <span data-ttu-id="08e8b-125">プロパティ set アクセス操作子を割り当てます`Nothing`に格納されている値。</span><span class="sxs-lookup"><span data-stu-id="08e8b-125">The property setter assigns `Nothing` to the stored value.</span></span> <span data-ttu-id="08e8b-126">以外の任意の値を割り当てた場合`Nothing`プロパティの setter がスローされます、<xref:System.ArgumentException>例外。</span><span class="sxs-lookup"><span data-stu-id="08e8b-126">If you assign any value other than `Nothing` to the property, the setter throws an <xref:System.ArgumentException> exception.</span></span>  
  
 <span data-ttu-id="08e8b-127">プロパティかどうかをテストすることができます、`My.WebServices`オブジェクトを使用して、Web サービスのインスタンスを格納する、`Is`または`IsNot`演算子。</span><span class="sxs-lookup"><span data-stu-id="08e8b-127">You can test whether a property of the `My.WebServices` object stores an instance of the Web service by using the `Is` or `IsNot` operator.</span></span> <span data-ttu-id="08e8b-128">これらの演算子を使用するには、プロパティの値をチェックする`Nothing`します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-128">You can use those operators to check if the value of the property is `Nothing`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="08e8b-129">通常、`Is`または`IsNot`オペレーターは、比較を実行するプロパティの値を読み取ることがあります。</span><span class="sxs-lookup"><span data-stu-id="08e8b-129">Typically, the `Is` or `IsNot` operator has to read the value of the property to perform the comparison.</span></span> <span data-ttu-id="08e8b-130">ただし、プロパティが現在格納されている場合`Nothing`プロパティ、Web サービスの新しいインスタンスを作成し、し、そのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-130">However, if the property currently stores `Nothing`, the property creates a new instance of the Web service and then returns that instance.</span></span> <span data-ttu-id="08e8b-131">ただし、Visual Basic コンパイラがのプロパティを処理、`My.WebServices`でき、特別に、オブジェクト、`Is`または`IsNot`演算子をその値を変更することがなく、プロパティの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-131">However, the Visual Basic compiler treats the properties of the `My.WebServices` object specially, and allows the `Is` or `IsNot` operator to check the status of the property without altering its value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="08e8b-132">例</span><span class="sxs-lookup"><span data-stu-id="08e8b-132">Example</span></span>  
 <span data-ttu-id="08e8b-133">この例では、`FahrenheitToCelsius`のメソッド、 `TemperatureConverter` XML Web サービスでは、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-133">This example calls the `FahrenheitToCelsius` method of the `TemperatureConverter` XML Web service, and returns the result.</span></span>  
  
 [!code-vb[VbVbalrMyWebService#1](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-webservices-object_1.vb)]  
  
 <span data-ttu-id="08e8b-134">この例を動作させるには、プロジェクトがという名前の Web サービスを参照する必要があります`Converter`、し、その Web サービスを公開する必要があります、`ConvertTemperature`メソッド。</span><span class="sxs-lookup"><span data-stu-id="08e8b-134">For this example to work, your project must reference a Web service named `Converter`, and that Web service must expose the `ConvertTemperature` method.</span></span> <span data-ttu-id="08e8b-135">詳細については、次を参照してください。[にアクセスするアプリケーションの Web サービス](../../../visual-basic/developing-apps/programming/accessing-application-web-services.md)します。</span><span class="sxs-lookup"><span data-stu-id="08e8b-135">For more information, see [Accessing Application Web Services](../../../visual-basic/developing-apps/programming/accessing-application-web-services.md).</span></span>  
  
 <span data-ttu-id="08e8b-136">このコードは、Web アプリケーション プロジェクトでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="08e8b-136">This code does not work in a Web application project.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08e8b-137">必要条件</span><span class="sxs-lookup"><span data-stu-id="08e8b-137">Requirements</span></span>  
  
### <a name="availability-by-project-type"></a><span data-ttu-id="08e8b-138">プロジェクトの種類ごとの可用性</span><span class="sxs-lookup"><span data-stu-id="08e8b-138">Availability by Project Type</span></span>  
  
|<span data-ttu-id="08e8b-139">プロジェクトの種類</span><span class="sxs-lookup"><span data-stu-id="08e8b-139">Project type</span></span>|<span data-ttu-id="08e8b-140">使用可能</span><span class="sxs-lookup"><span data-stu-id="08e8b-140">Available</span></span>|  
|---|---|  
|<span data-ttu-id="08e8b-141">Windows アプリケーション</span><span class="sxs-lookup"><span data-stu-id="08e8b-141">Windows Application</span></span>|<span data-ttu-id="08e8b-142">**はい**</span><span class="sxs-lookup"><span data-stu-id="08e8b-142">**Yes**</span></span>|  
|<span data-ttu-id="08e8b-143">クラス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="08e8b-143">Class Library</span></span>|<span data-ttu-id="08e8b-144">**はい**</span><span class="sxs-lookup"><span data-stu-id="08e8b-144">**Yes**</span></span>|  
|<span data-ttu-id="08e8b-145">コンソール アプリケーション</span><span class="sxs-lookup"><span data-stu-id="08e8b-145">Console Application</span></span>|<span data-ttu-id="08e8b-146">**はい**</span><span class="sxs-lookup"><span data-stu-id="08e8b-146">**Yes**</span></span>|  
|<span data-ttu-id="08e8b-147">Windows コントロール ライブラリ</span><span class="sxs-lookup"><span data-stu-id="08e8b-147">Windows Control Library</span></span>|<span data-ttu-id="08e8b-148">**はい**</span><span class="sxs-lookup"><span data-stu-id="08e8b-148">**Yes**</span></span>|  
|<span data-ttu-id="08e8b-149">Web コントロール ライブラリ</span><span class="sxs-lookup"><span data-stu-id="08e8b-149">Web Control Library</span></span>|<span data-ttu-id="08e8b-150">**はい**</span><span class="sxs-lookup"><span data-stu-id="08e8b-150">**Yes**</span></span>|  
|<span data-ttu-id="08e8b-151">Windows サービス</span><span class="sxs-lookup"><span data-stu-id="08e8b-151">Windows Service</span></span>|<span data-ttu-id="08e8b-152">**はい**</span><span class="sxs-lookup"><span data-stu-id="08e8b-152">**Yes**</span></span>|  
|<span data-ttu-id="08e8b-153">Web サイト</span><span class="sxs-lookup"><span data-stu-id="08e8b-153">Web Site</span></span>|<span data-ttu-id="08e8b-154">いいえ</span><span class="sxs-lookup"><span data-stu-id="08e8b-154">No</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="08e8b-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="08e8b-155">See also</span></span>
- <xref:System.Web.Services.Protocols.SoapHttpClientProtocol>
- <xref:System.ArgumentException>
- [<span data-ttu-id="08e8b-156">アプリケーションの Web サービスへのアクセス</span><span class="sxs-lookup"><span data-stu-id="08e8b-156">Accessing Application Web Services</span></span>](../../../visual-basic/developing-apps/programming/accessing-application-web-services.md)
