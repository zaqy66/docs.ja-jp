---
title: '&lt;オフ&gt;schemeSettings (Uri 設定) の要素'
ms.date: 03/30/2017
ms.assetid: 65098332-ce61-4542-ab8d-e7dc0257d31f
author: mcleblanc
ms.author: markl
ms.openlocfilehash: f0daa689ba09fa39ffe0f38d769112f0f095592a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47070644"
---
# <a name="ltcleargt-element-for-schemesettings-uri-settings"></a><span data-ttu-id="1ed30-102">&lt;オフ&gt;schemeSettings (Uri 設定) の要素</span><span class="sxs-lookup"><span data-stu-id="1ed30-102">&lt;clear&gt; Element for schemeSettings (Uri Settings)</span></span>
<span data-ttu-id="1ed30-103">既存のすべての構成設定をクリアします。</span><span class="sxs-lookup"><span data-stu-id="1ed30-103">Clears all existing scheme settings.</span></span>  
  
 <span data-ttu-id="1ed30-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="1ed30-104">\<configuration></span></span>  
<span data-ttu-id="1ed30-105">\<uri ></span><span class="sxs-lookup"><span data-stu-id="1ed30-105">\<uri></span></span>  
<span data-ttu-id="1ed30-106">\<schemeSettings ></span><span class="sxs-lookup"><span data-stu-id="1ed30-106">\<schemeSettings></span></span>  
<span data-ttu-id="1ed30-107">\<クリア ></span><span class="sxs-lookup"><span data-stu-id="1ed30-107">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ed30-108">構文</span><span class="sxs-lookup"><span data-stu-id="1ed30-108">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1ed30-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="1ed30-109">Attributes and Elements</span></span>  
 <span data-ttu-id="1ed30-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="1ed30-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1ed30-111">属性</span><span class="sxs-lookup"><span data-stu-id="1ed30-111">Attributes</span></span>  
 <span data-ttu-id="1ed30-112">なし。</span><span class="sxs-lookup"><span data-stu-id="1ed30-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1ed30-113">子要素</span><span class="sxs-lookup"><span data-stu-id="1ed30-113">Child Elements</span></span>  
 <span data-ttu-id="1ed30-114">なし。</span><span class="sxs-lookup"><span data-stu-id="1ed30-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1ed30-115">親要素</span><span class="sxs-lookup"><span data-stu-id="1ed30-115">Parent Elements</span></span>  
  
|<span data-ttu-id="1ed30-116">要素</span><span class="sxs-lookup"><span data-stu-id="1ed30-116">Element</span></span>|<span data-ttu-id="1ed30-117">説明</span><span class="sxs-lookup"><span data-stu-id="1ed30-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1ed30-118">\<schemeSettings> 要素 (Uri 設定)</span><span class="sxs-lookup"><span data-stu-id="1ed30-118">\<schemeSettings> Element (Uri Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|<span data-ttu-id="1ed30-119"><xref:System.Uri> が特定のスキームに解析される方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ed30-119">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1ed30-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="1ed30-120">Remarks</span></span>  
 <span data-ttu-id="1ed30-121">既定で、<xref:System.Uri?displayProperty=nameWithType>クラスのエスケープを解除パーセントは、パスの圧縮を実行する前にパスの区切り文字をエンコードします。</span><span class="sxs-lookup"><span data-stu-id="1ed30-121">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="1ed30-122">これは、次のような攻撃に対するセキュリティ メカニズムとして実装されていました。</span><span class="sxs-lookup"><span data-stu-id="1ed30-122">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="1ed30-123">この URI が渡される場合は、モジュール % を処理しないエンコードした文字を正しく、サーバーで実行されている次のコマンドになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1ed30-123">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="1ed30-124">このため、<xref:System.Uri?displayProperty=nameWithType>クラスの最初のエスケープを解除パス区切り記号とし、パスの圧縮を適用します。</span><span class="sxs-lookup"><span data-stu-id="1ed30-124">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="1ed30-125">上への悪意のある URL を渡すことの結果<xref:System.Uri?displayProperty=nameWithType>クラスに次の URI のコンス トラクターの結果。</span><span class="sxs-lookup"><span data-stu-id="1ed30-125">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="1ed30-126">SchemeSettings の構成オプションを使用して、特定のスキームのないのエスケープを解除のパーセントでエンコードされたパス区切りには、この既定の動作を変更できます。</span><span class="sxs-lookup"><span data-stu-id="1ed30-126">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="1ed30-127">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="1ed30-127">Configuration Files</span></span>  
 <span data-ttu-id="1ed30-128">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="1ed30-128">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1ed30-129">例</span><span class="sxs-lookup"><span data-stu-id="1ed30-129">Example</span></span>  
 <span data-ttu-id="1ed30-130">次の例で使用する構成を示しています、<xref:System.Uri>スキームの設定をすべて消去し、http スキームのパスをパーセントでエンコードされた区切り記号をエスケープしないサポートを追加するクラス。</span><span class="sxs-lookup"><span data-stu-id="1ed30-130">The following example shows a configuration used by the <xref:System.Uri> class that clears all scheme settings and then adds support for not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <clear/>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1ed30-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ed30-131">See Also</span></span>  
 <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>  
 <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>  
 <xref:System.GenericUriParserOptions?displayProperty=nameWithType>  
 <xref:System.Uri?displayProperty=nameWithType>  
 [<span data-ttu-id="1ed30-132">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="1ed30-132">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
