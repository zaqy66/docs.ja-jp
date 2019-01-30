---
title: <oidMap> 要素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#oidMap
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/oidMap
helpviewer_keywords:
- <oidMap> element
- oidMap element
ms.assetid: 7f0c2246-c070-4748-b96a-2f66a296c539
ms.openlocfilehash: d726965a921a11be1ff9c11d4fb348068b2ec0a3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262518"
---
# <a name="oidmap-element"></a><span data-ttu-id="2b8b3-102">\<oidMap > 要素</span><span class="sxs-lookup"><span data-stu-id="2b8b3-102">\<oidMap> Element</span></span>
<span data-ttu-id="2b8b3-103">クラスへの ASN.1 オブジェクト識別子 (OID) のマッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-103">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>  
  
 <span data-ttu-id="2b8b3-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="2b8b3-104">\<configuration></span></span>  
<span data-ttu-id="2b8b3-105">\<mscorlib></span><span class="sxs-lookup"><span data-stu-id="2b8b3-105">\<mscorlib></span></span>  
<span data-ttu-id="2b8b3-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="2b8b3-106">\<cryptographySettings></span></span>  
<span data-ttu-id="2b8b3-107">\<oidMap></span><span class="sxs-lookup"><span data-stu-id="2b8b3-107">\<oidMap></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b8b3-108">構文</span><span class="sxs-lookup"><span data-stu-id="2b8b3-108">Syntax</span></span>  
  
```xml  
<oidMap>   
</oidMap>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2b8b3-109">属性および要素</span><span class="sxs-lookup"><span data-stu-id="2b8b3-109">Attributes and Elements</span></span>  
 <span data-ttu-id="2b8b3-110">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2b8b3-111">属性</span><span class="sxs-lookup"><span data-stu-id="2b8b3-111">Attributes</span></span>  
 <span data-ttu-id="2b8b3-112">なし。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2b8b3-113">子要素</span><span class="sxs-lookup"><span data-stu-id="2b8b3-113">Child Elements</span></span>  
  
|<span data-ttu-id="2b8b3-114">要素</span><span class="sxs-lookup"><span data-stu-id="2b8b3-114">Element</span></span>|<span data-ttu-id="2b8b3-115">説明</span><span class="sxs-lookup"><span data-stu-id="2b8b3-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2b8b3-116">\<oidEntry></span><span class="sxs-lookup"><span data-stu-id="2b8b3-116">\<oidEntry></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md)|<span data-ttu-id="2b8b3-117">ASN.1 OID をフレンドリ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-117">Maps an ASN.1 OID to a friendly name.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2b8b3-118">親要素</span><span class="sxs-lookup"><span data-stu-id="2b8b3-118">Parent Elements</span></span>  
  
|<span data-ttu-id="2b8b3-119">要素</span><span class="sxs-lookup"><span data-stu-id="2b8b3-119">Element</span></span>|<span data-ttu-id="2b8b3-120">説明</span><span class="sxs-lookup"><span data-stu-id="2b8b3-120">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="2b8b3-121">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-121">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="2b8b3-122">暗号設定を含みます。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-122">Contains cryptography settings.</span></span>|  
|`mscorlib`|<span data-ttu-id="2b8b3-123">`cryptographySettings`要素を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-123">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="2b8b3-124">例</span><span class="sxs-lookup"><span data-stu-id="2b8b3-124">Example</span></span>  
 <span data-ttu-id="2b8b3-125">次の例は、使用する方法を示します、  **\<oidMap >** 要素にそのハッシュ アルゴリズムの実装に ripemd-160 のハッシュ アルゴリズムの OID のマッピングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2b8b3-125">The following example shows how to use the **\<oidMap>** element to contain a mapping of an OID for the RIPEMD-160 hash algorithm to an implementation of that hash algorithm.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="2b8b3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b8b3-126">See also</span></span>
- [<span data-ttu-id="2b8b3-127">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="2b8b3-127">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="2b8b3-128">暗号化設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="2b8b3-128">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)
- [<span data-ttu-id="2b8b3-129">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="2b8b3-129">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
- [<span data-ttu-id="2b8b3-130">暗号化クラスの設定</span><span class="sxs-lookup"><span data-stu-id="2b8b3-130">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
- [<span data-ttu-id="2b8b3-131">暗号化アルゴリズムへのオブジェクト ID の割り当て</span><span class="sxs-lookup"><span data-stu-id="2b8b3-131">Mapping Object Identifiers to Cryptography Algorithms</span></span>](../../../../../docs/framework/configure-apps/map-object-identifiers-to-cryptography-algorithms.md)
