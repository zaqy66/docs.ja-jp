---
title: <cryptographySettings> 要素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptographySettings
helpviewer_keywords:
- cryptographySettings element
- <cryptographySettings> element
ms.assetid: 6201b7da-bcb7-49f7-b9f5-ba1fe05573b9
ms.openlocfilehash: 11f07bbf5de04edc98a5a5bc0ba07f1629763a9f
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55258709"
---
# <a name="cryptographysettings-element"></a><span data-ttu-id="0f695-102">\<cryptographySettings > 要素</span><span class="sxs-lookup"><span data-stu-id="0f695-102">\<cryptographySettings> Element</span></span>
<span data-ttu-id="0f695-103">暗号設定を含みます。</span><span class="sxs-lookup"><span data-stu-id="0f695-103">Contains cryptography settings.</span></span>  
  
 <span data-ttu-id="0f695-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="0f695-104">\<configuration></span></span>  
<span data-ttu-id="0f695-105">\<mscorlib></span><span class="sxs-lookup"><span data-stu-id="0f695-105">\<mscorlib></span></span>  
<span data-ttu-id="0f695-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="0f695-106">\<cryptographySettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f695-107">構文</span><span class="sxs-lookup"><span data-stu-id="0f695-107">Syntax</span></span>  
  
```xml  
      <cryptographySettings>   
</cryptographySettings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0f695-108">属性および要素</span><span class="sxs-lookup"><span data-stu-id="0f695-108">Attributes and Elements</span></span>  
 <span data-ttu-id="0f695-109">以降のセクションでは、属性、子要素、および親要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f695-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0f695-110">属性</span><span class="sxs-lookup"><span data-stu-id="0f695-110">Attributes</span></span>  
 <span data-ttu-id="0f695-111">なし。</span><span class="sxs-lookup"><span data-stu-id="0f695-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0f695-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0f695-112">Child Elements</span></span>  
  
|<span data-ttu-id="0f695-113">要素</span><span class="sxs-lookup"><span data-stu-id="0f695-113">Element</span></span>|<span data-ttu-id="0f695-114">説明</span><span class="sxs-lookup"><span data-stu-id="0f695-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0f695-115">\<cryptoNameMapping></span><span class="sxs-lookup"><span data-stu-id="0f695-115">\<cryptoNameMapping></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)|<span data-ttu-id="0f695-116">表示名へのクラスのマッピングを含みます。</span><span class="sxs-lookup"><span data-stu-id="0f695-116">Contains mappings of classes to friendly names.</span></span>|  
|[<span data-ttu-id="0f695-117">\<oidMap></span><span class="sxs-lookup"><span data-stu-id="0f695-117">\<oidMap></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)|<span data-ttu-id="0f695-118">クラスへの ASN.1 オブジェクト識別子 (OID) のマッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f695-118">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0f695-119">親要素</span><span class="sxs-lookup"><span data-stu-id="0f695-119">Parent Elements</span></span>  
  
|<span data-ttu-id="0f695-120">要素</span><span class="sxs-lookup"><span data-stu-id="0f695-120">Element</span></span>|<span data-ttu-id="0f695-121">説明</span><span class="sxs-lookup"><span data-stu-id="0f695-121">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="0f695-122">共通言語ランタイムおよび .NET Framework アプリケーションで使用されるすべての構成ファイルのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="0f695-122">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`mscorlib`|<span data-ttu-id="0f695-123">`cryptographySettings`要素を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="0f695-123">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0f695-124">例</span><span class="sxs-lookup"><span data-stu-id="0f695-124">Example</span></span>  
 <span data-ttu-id="0f695-125">次の例では、  **\<cryptographySettings >** 暗号名のマッピングおよび OID マッピングを格納する要素。</span><span class="sxs-lookup"><span data-stu-id="0f695-125">The following example shows how use the **\<cryptographySettings>** element to contain cryptography name mappings and OID mappings.</span></span> <span data-ttu-id="0f695-126">この例では、ランタイムように<xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType>を返します、`MyHashClass`オブジェクトと`MyCryptoClass`クラスのオブジェクト識別子 1.3.36.2.1 にマップされます。</span><span class="sxs-lookup"><span data-stu-id="0f695-126">This example configures the runtime so that <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> returns a `MyHashClass` object and the `MyCryptoClass` class maps to the object identifier 1.3.36.2.1.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyHash="MyHashClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="System.Security.Cryptography.HashAlgorithm"  
                       class="MyHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0f695-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f695-127">See also</span></span>
- [<span data-ttu-id="0f695-128">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="0f695-128">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="0f695-129">暗号化設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="0f695-129">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)
- [<span data-ttu-id="0f695-130">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="0f695-130">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
