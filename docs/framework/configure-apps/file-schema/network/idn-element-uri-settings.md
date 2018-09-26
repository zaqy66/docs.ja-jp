---
title: '&lt;idn&gt;要素 (Uri 設定)'
ms.date: 03/30/2017
ms.assetid: 16c8e869-1791-4cf5-9244-3d3c738f60ec
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 1537c17cb3c16beeb41cfaa4103e0664e93facc7
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47170601"
---
# <a name="ltidngt-element-uri-settings"></a><span data-ttu-id="e3c8a-102">&lt;idn&gt;要素 (Uri 設定)</span><span class="sxs-lookup"><span data-stu-id="e3c8a-102">&lt;idn&gt; Element (Uri Settings)</span></span>
<span data-ttu-id="e3c8a-103">ドメイン名に国際化ドメイン名 (IDN) 解析が適用されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-103">Specifies if Internationalized Domain Name (IDN) parsing is applied to a domain name.</span></span>  
  
## <a name="schema-hierarchy"></a><span data-ttu-id="e3c8a-104">スキーマの階層</span><span class="sxs-lookup"><span data-stu-id="e3c8a-104">Schema Hierarchy</span></span>  
 [<span data-ttu-id="e3c8a-105">\<configuration> 要素</span><span class="sxs-lookup"><span data-stu-id="e3c8a-105">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [<span data-ttu-id="e3c8a-106">\<Uri > 要素 (Uri 設定)</span><span class="sxs-lookup"><span data-stu-id="e3c8a-106">\<Uri> Element (Uri Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)  
  
 [<span data-ttu-id="e3c8a-107">\<idn ></span><span class="sxs-lookup"><span data-stu-id="e3c8a-107">\<idn></span></span>](../../../../../docs/framework/configure-apps/file-schema/network/idn-element-uri-settings.md)  
  
## <a name="syntax"></a><span data-ttu-id="e3c8a-108">構文</span><span class="sxs-lookup"><span data-stu-id="e3c8a-108">Syntax</span></span>  
  
```xml  
<idn  
  enabled="All|AllExceptIntranet|None"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e3c8a-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="e3c8a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e3c8a-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e3c8a-111">属性</span><span class="sxs-lookup"><span data-stu-id="e3c8a-111">Attributes</span></span>  
  
|<span data-ttu-id="e3c8a-112">**要素**</span><span class="sxs-lookup"><span data-stu-id="e3c8a-112">**Element**</span></span>|<span data-ttu-id="e3c8a-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3c8a-113">**Description**</span></span>|  
|-----------------|---------------------|  
|`enabled`|<span data-ttu-id="e3c8a-114">国際化ドメイン名 (IDN) 解析がドメイン名に適用される場合、既定値は none を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-114">Specifies if Internationalized Domain Name (IDN) parsing is applied to a domain name The default value is none.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e3c8a-115">子要素</span><span class="sxs-lookup"><span data-stu-id="e3c8a-115">Child Elements</span></span>  
 <span data-ttu-id="e3c8a-116">なし</span><span class="sxs-lookup"><span data-stu-id="e3c8a-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e3c8a-117">親要素</span><span class="sxs-lookup"><span data-stu-id="e3c8a-117">Parent Elements</span></span>  
  
|<span data-ttu-id="e3c8a-118">**要素**</span><span class="sxs-lookup"><span data-stu-id="e3c8a-118">**Element**</span></span>|<span data-ttu-id="e3c8a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3c8a-119">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="e3c8a-120">Uri</span><span class="sxs-lookup"><span data-stu-id="e3c8a-120">uri</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)|<span data-ttu-id="e3c8a-121">.NET Framework での uniform resource identifier (Uri) を使用して表現された web アドレスの処理方法を指定する設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-121">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e3c8a-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="e3c8a-122">Remarks</span></span>  
 <span data-ttu-id="e3c8a-123">既存の<xref:System.Uri>クラスは、.NET Framework 3.5 で拡張されています。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-123">The existing <xref:System.Uri> class has been extended in .NET Framework 3.5.</span></span> <span data-ttu-id="e3c8a-124">3.0 SP1、および 2.0 SP1 国際リソース識別子 (IRI) および国際化ドメイン名 (IDN) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-124">3.0 SP1, and 2.0 SP1 with support for International Resource Identifiers (IRI) and Internationalized Domain Names (IDN).</span></span> <span data-ttu-id="e3c8a-125">IRI と IDN 明確には、現在のユーザーに、.NET Framework 2.0 の動作から変更は表示されないをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-125">Current users will not see any change from the .NET Framework 2.0 behavior unless they specifically enable IRI and IDN support.</span></span> <span data-ttu-id="e3c8a-126">これにより、.NET Framework の以前のバージョンとのアプリケーションの互換性を保証します。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-126">This ensures application compatibility with prior versions of the .NET Framework.</span></span>  
  
 <span data-ttu-id="e3c8a-127">IRI のサポートを有効にするのには、次の 2 つの変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-127">To enable support for IRI, the following two changes are required:</span></span>  
  
1.  <span data-ttu-id="e3c8a-128">.NET Framework 2.0 のディレクトリの machine.config ファイルに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-128">Add the following line to the machine.config file under the .NET Framework 2.0 directory</span></span>  
  
    ```xml  
    <section name="uri" type="System.Configuration.UriSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    ```  
  
2.  <span data-ttu-id="e3c8a-129">国際化ドメイン名 (IDN) 解析のドメイン名に適用するかどうか、および IRI 解析規則を適用する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-129">Specify whether you want Internationalized Domain Name (IDN) parsing applied to the domain name and whether IRI parsing rules should be applied.</span></span> <span data-ttu-id="e3c8a-130">これは、machine.config ファイルまたは app.config ファイルで指定できます。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-130">This can be done in the machine.config or in the app.config file.</span></span>  
  
 <span data-ttu-id="e3c8a-131">IDN を使用する DNS サーバーによって可能な値は 3 つです。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-131">There are three possible values for IDN depending on the DNS servers that are used:</span></span>  
  
-   <span data-ttu-id="e3c8a-132">idn を有効になっている = All</span><span class="sxs-lookup"><span data-stu-id="e3c8a-132">idn enabled = All</span></span>  
  
     <span data-ttu-id="e3c8a-133">この値は、任意の Unicode ドメイン名を等価の Punycode (IDN 名) に変換されます。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-133">This value will convert any Unicode domain names to their Punycode equivalents (IDN names).</span></span>  
  
-   <span data-ttu-id="e3c8a-134">idn を有効になっている AllExceptIntranet を =</span><span class="sxs-lookup"><span data-stu-id="e3c8a-134">idn enabled = AllExceptIntranet</span></span>  
  
     <span data-ttu-id="e3c8a-135">この値は、等価の Punycode (IDN 名) を使用するローカルのイントラネットではなく、すべての Unicode ドメイン名に変換されます。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-135">This value will convert all Unicode domain names not on the local Intranet to use the Punycode equivalents (IDN names).</span></span> <span data-ttu-id="e3c8a-136">ここでローカルのイントラネットで国際名を処理するために、イントラネットに使用される DNS サーバーは、Unicode の名前解決をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-136">In this case to handle international names on the local Intranet, the DNS servers that are used for the Intranet should support Unicode name resolution.</span></span>  
  
-   <span data-ttu-id="e3c8a-137">idn を有効になっている = なし</span><span class="sxs-lookup"><span data-stu-id="e3c8a-137">idn enabled = None</span></span>  
  
     <span data-ttu-id="e3c8a-138">この値は Punycode を使用する Unicode ドメイン名を変換できません。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-138">This value will not convert any Unicode domain names to use Punycode.</span></span> <span data-ttu-id="e3c8a-139">これは、.NET Framework 2.0 の動作と一貫した既定値です。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-139">This is the default value which is consistent with the .NET Framework 2.0 behaviour.</span></span>  
  
 <span data-ttu-id="e3c8a-140">IDN を有効にすると、ドメイン名に含まれるすべての Unicode のラベルが Punycode のラベルに変換されます。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-140">Enabling IDN will convert all Unicode labels in a domain name to their Punycode equivalents.</span></span> <span data-ttu-id="e3c8a-141">Punycode 名には ASCII 文字のみが含まれ、常に xn-- プレフィックスで始まります。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-141">Punycode names contain only ASCII characters and always start with the xn-- prefix.</span></span> <span data-ttu-id="e3c8a-142">この理由は、ほとんどの DNS サーバーは ASCII 文字しかサポートしていないため、インターネットで既存の DNS サーバーをサポートするためです (RFC 3940 を参照)。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-142">The reason for this is to support existing DNS servers on the Internet, since most DNS servers only support ASCII characters (see RFC 3940).</span></span>  
  
### <a name="configuration-files"></a><span data-ttu-id="e3c8a-143">構成ファイル</span><span class="sxs-lookup"><span data-stu-id="e3c8a-143">Configuration Files</span></span>  
 <span data-ttu-id="e3c8a-144">この要素は、アプリケーション構成ファイルまたはマシン構成ファイル (Machine.config) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-144">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e3c8a-145">例</span><span class="sxs-lookup"><span data-stu-id="e3c8a-145">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="e3c8a-146">説明</span><span class="sxs-lookup"><span data-stu-id="e3c8a-146">Description</span></span>  
 <span data-ttu-id="e3c8a-147">次の例で使用する構成を示しています、<xref:System.Uri>解析する IRI と IDN 名をサポートするクラス。</span><span class="sxs-lookup"><span data-stu-id="e3c8a-147">The following example shows a configuration used by the <xref:System.Uri> class to support IRI parsing and IDN names.</span></span>  
  
### <a name="code"></a><span data-ttu-id="e3c8a-148">コード</span><span class="sxs-lookup"><span data-stu-id="e3c8a-148">Code</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e3c8a-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3c8a-149">See Also</span></span>  
 <xref:System.Configuration.IdnElement?displayProperty=nameWithType>  
 <xref:System.Configuration.UriSection?displayProperty=nameWithType>  
 [<span data-ttu-id="e3c8a-150">ネットワーク設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="e3c8a-150">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
