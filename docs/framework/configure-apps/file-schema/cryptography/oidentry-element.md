---
title: '&lt;oidEntry&gt;要素'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/oidMap/oidEntry
- http://schemas.microsoft.com/.NetConfiguration/v2.0#oidEntry
helpviewer_keywords:
- <oidEntry> element
- oidEntry element
ms.assetid: 22fb88b0-bf27-489c-9ca0-e65950ac136c
author: mcleblanc
ms.author: markl
ms.openlocfilehash: c5be6ef95693f274e5cb2002e5642d5e58a7661a
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2018
ms.locfileid: "48033130"
---
# <a name="ltoidentrygt-element"></a><span data-ttu-id="97511-102">&lt;oidEntry&gt;要素</span><span class="sxs-lookup"><span data-stu-id="97511-102">&lt;oidEntry&gt; Element</span></span>
<span data-ttu-id="97511-103">ASN.1 オブジェクト識別子 (OID) を表示名にマップします。</span><span class="sxs-lookup"><span data-stu-id="97511-103">Maps an ASN.1 object identifier (OID) to a friendly name.</span></span>  
  
 <span data-ttu-id="97511-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="97511-104">\<configuration></span></span>  
<span data-ttu-id="97511-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="97511-105">\<mscorlib></span></span>  
<span data-ttu-id="97511-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="97511-106">\<cryptographySettings></span></span>  
<span data-ttu-id="97511-107">\<oidMap ></span><span class="sxs-lookup"><span data-stu-id="97511-107">\<oidMap></span></span>  
<span data-ttu-id="97511-108">\<oidEntry ></span><span class="sxs-lookup"><span data-stu-id="97511-108">\<oidEntry></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97511-109">構文</span><span class="sxs-lookup"><span data-stu-id="97511-109">Syntax</span></span>  
  
```xml  
<oidEntry OID="object identifier number" name="friendly name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="97511-110">属性および要素</span><span class="sxs-lookup"><span data-stu-id="97511-110">Attributes and Elements</span></span>  
 <span data-ttu-id="97511-111">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="97511-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="97511-112">属性</span><span class="sxs-lookup"><span data-stu-id="97511-112">Attributes</span></span>  
  
|<span data-ttu-id="97511-113">属性</span><span class="sxs-lookup"><span data-stu-id="97511-113">Attribute</span></span>|<span data-ttu-id="97511-114">説明</span><span class="sxs-lookup"><span data-stu-id="97511-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="97511-115">**OID**</span><span class="sxs-lookup"><span data-stu-id="97511-115">**OID**</span></span>|<span data-ttu-id="97511-116">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="97511-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="97511-117">クラスで実装されているアルゴリズムに対応する ASN.1 OID を指定します。</span><span class="sxs-lookup"><span data-stu-id="97511-117">Specifies the ASN.1 OID corresponding to the algorithm implemented by your class.</span></span>|  
|<span data-ttu-id="97511-118">**name**</span><span class="sxs-lookup"><span data-stu-id="97511-118">**name**</span></span>|<span data-ttu-id="97511-119">必須の属性です。</span><span class="sxs-lookup"><span data-stu-id="97511-119">Required attribute.</span></span><br /><br /> <span data-ttu-id="97511-120">値を指定します、**名前**属性、 [ \<nameEntry >](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md)タグ。</span><span class="sxs-lookup"><span data-stu-id="97511-120">Specifies the value for the **name** attribute in the [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) tag.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="97511-121">子要素</span><span class="sxs-lookup"><span data-stu-id="97511-121">Child Elements</span></span>  
 <span data-ttu-id="97511-122">なし。</span><span class="sxs-lookup"><span data-stu-id="97511-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="97511-123">親要素</span><span class="sxs-lookup"><span data-stu-id="97511-123">Parent Elements</span></span>  
  
|<span data-ttu-id="97511-124">要素</span><span class="sxs-lookup"><span data-stu-id="97511-124">Element</span></span>|<span data-ttu-id="97511-125">説明</span><span class="sxs-lookup"><span data-stu-id="97511-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="97511-126">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="97511-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="97511-127">暗号設定を含みます。</span><span class="sxs-lookup"><span data-stu-id="97511-127">Contains cryptography settings.</span></span>|  
|`mscorlib`|<span data-ttu-id="97511-128">`cryptographySettings`要素を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="97511-128">Contains the `cryptographySettings` element.</span></span>|  
|`oidMap`|<span data-ttu-id="97511-129">クラスへの ASN.1 オブジェクト識別子 (OID) のマッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="97511-129">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="97511-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="97511-130">Remarks</span></span>  
 <span data-ttu-id="97511-131">ASN.1 オブジェクト識別子では、いくつかの暗号化形式でアルゴリズムを識別します。</span><span class="sxs-lookup"><span data-stu-id="97511-131">ASN.1 object identifiers identify algorithms in some cryptographic formats.</span></span> <span data-ttu-id="97511-132">オブジェクト識別子を特定するアルゴリズムの表示名にマップします。</span><span class="sxs-lookup"><span data-stu-id="97511-132">Map object identifiers to friendly names for the algorithms you want to identify.</span></span>  
  
## <a name="example"></a><span data-ttu-id="97511-133">例</span><span class="sxs-lookup"><span data-stu-id="97511-133">Example</span></span>  
 <span data-ttu-id="97511-134">次の例は、使用する方法を示します、  **\<oidEntry >** ripemd-160 のハッシュ アルゴリズムのオブジェクト識別子をそのハッシュ アルゴリズムの実装にマップする要素。</span><span class="sxs-lookup"><span data-stu-id="97511-134">The following example shows how to use the **\<oidEntry>** element to map an object identifier for the RIPEMD-160 hash algorithm to an implementation of that hash algorithm.</span></span>  
  
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
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="97511-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="97511-135">See Also</span></span>  
 [<span data-ttu-id="97511-136">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="97511-136">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="97511-137">暗号化設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="97511-137">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [<span data-ttu-id="97511-138">暗号サービス</span><span class="sxs-lookup"><span data-stu-id="97511-138">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)  
 [<span data-ttu-id="97511-139">暗号化クラスの設定</span><span class="sxs-lookup"><span data-stu-id="97511-139">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)  
 [<span data-ttu-id="97511-140">暗号化アルゴリズムへのオブジェクト ID の割り当て</span><span class="sxs-lookup"><span data-stu-id="97511-140">Mapping Object Identifiers to Cryptography Algorithms</span></span>](../../../../../docs/framework/configure-apps/map-object-identifiers-to-cryptography-algorithms.md)
