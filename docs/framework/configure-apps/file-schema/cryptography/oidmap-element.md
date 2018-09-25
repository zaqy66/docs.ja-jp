---
title: '&lt;oidMap&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#oidMap
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/oidMap
helpviewer_keywords:
- <oidMap> element
- oidMap element
ms.assetid: 7f0c2246-c070-4748-b96a-2f66a296c539
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 4ec2ba884f0f60182dd59bb6a4491e223f43ce1a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47073542"
---
# <a name="ltoidmapgt-element"></a><span data-ttu-id="1328a-102">&lt;oidMap&gt;要素</span><span class="sxs-lookup"><span data-stu-id="1328a-102">&lt;oidMap&gt; Element</span></span>
<span data-ttu-id="1328a-103">クラスへの ASN.1 オブジェクト識別子 (OID) のマッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1328a-103">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>  
  
 <span data-ttu-id="1328a-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="1328a-104">\<configuration></span></span>  
<span data-ttu-id="1328a-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="1328a-105">\<mscorlib></span></span>  
<span data-ttu-id="1328a-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="1328a-106">\<cryptographySettings></span></span>  
<span data-ttu-id="1328a-107">\<oidMap ></span><span class="sxs-lookup"><span data-stu-id="1328a-107">\<oidMap></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1328a-108">構文</span><span class="sxs-lookup"><span data-stu-id="1328a-108">Syntax</span></span>  
  
```xml  
<oidMap>   
</oidMap>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1328a-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="1328a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="1328a-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="1328a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1328a-111">属性</span><span class="sxs-lookup"><span data-stu-id="1328a-111">Attributes</span></span>  
 <span data-ttu-id="1328a-112">なし。</span><span class="sxs-lookup"><span data-stu-id="1328a-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="1328a-113">子要素</span><span class="sxs-lookup"><span data-stu-id="1328a-113">Child Elements</span></span>  
  
|<span data-ttu-id="1328a-114">要素</span><span class="sxs-lookup"><span data-stu-id="1328a-114">Element</span></span>|<span data-ttu-id="1328a-115">説明</span><span class="sxs-lookup"><span data-stu-id="1328a-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1328a-116">\<oidEntry ></span><span class="sxs-lookup"><span data-stu-id="1328a-116">\<oidEntry></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md)|<span data-ttu-id="1328a-117">ASN.1 OID をフレンドリ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1328a-117">Maps an ASN.1 OID to a friendly name.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1328a-118">親要素</span><span class="sxs-lookup"><span data-stu-id="1328a-118">Parent Elements</span></span>  
  
|<span data-ttu-id="1328a-119">要素</span><span class="sxs-lookup"><span data-stu-id="1328a-119">Element</span></span>|<span data-ttu-id="1328a-120">説明</span><span class="sxs-lookup"><span data-stu-id="1328a-120">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="1328a-121">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="1328a-121">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="1328a-122">暗号設定を含みます。</span><span class="sxs-lookup"><span data-stu-id="1328a-122">Contains cryptography settings.</span></span>|  
|`mscorlib`|<span data-ttu-id="1328a-123">`cryptographySettings`要素を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="1328a-123">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="1328a-124">例</span><span class="sxs-lookup"><span data-stu-id="1328a-124">Example</span></span>  
 <span data-ttu-id="1328a-125">次の例は、使用する方法を示します、  **\<oidMap >** 要素にそのハッシュ アルゴリズムの実装に ripemd-160 のハッシュ アルゴリズムの OID のマッピングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1328a-125">The following example shows how to use the **\<oidMap>** element to contain a mapping of an OID for the RIPEMD-160 hash algorithm to an implementation of that hash algorithm.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RIPEMD-160" class="MyCrypto"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"  name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1328a-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="1328a-126">See Also</span></span>  
 [<span data-ttu-id="1328a-127">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="1328a-127">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="1328a-128">暗号化設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="1328a-128">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [<span data-ttu-id="1328a-129">暗号サービス</span><span class="sxs-lookup"><span data-stu-id="1328a-129">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)  
 [<span data-ttu-id="1328a-130">暗号化クラスの設定</span><span class="sxs-lookup"><span data-stu-id="1328a-130">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)  
 [<span data-ttu-id="1328a-131">暗号化アルゴリズムへのオブジェクト ID の割り当て</span><span class="sxs-lookup"><span data-stu-id="1328a-131">Mapping Object Identifiers to Cryptography Algorithms</span></span>](../../../../../docs/framework/configure-apps/map-object-identifiers-to-cryptography-algorithms.md)
