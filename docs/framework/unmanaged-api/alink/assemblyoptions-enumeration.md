---
title: AssemblyOptions 列挙体
ms.date: 03/30/2017
api_name:
- AssemblyOptions
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 939e815f4d3adc5f6e1c8b8fc85c9f4b89372501
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571484"
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="ca4ee-102">AssemblyOptions 列挙体</span><span class="sxs-lookup"><span data-stu-id="ca4ee-102">AssemblyOptions Enumeration</span></span>
<span data-ttu-id="ca4ee-103">アセンブリ オプションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-103">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca4ee-104">構文</span><span class="sxs-lookup"><span data-stu-id="ca4ee-104">Syntax</span></span>  
  
```  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a><span data-ttu-id="ca4ee-105">フィールド</span><span class="sxs-lookup"><span data-stu-id="ca4ee-105">Fields</span></span>  
  
|<span data-ttu-id="ca4ee-106">フィールド</span><span class="sxs-lookup"><span data-stu-id="ca4ee-106">Field</span></span>|<span data-ttu-id="ca4ee-107">説明</span><span class="sxs-lookup"><span data-stu-id="ca4ee-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="ca4ee-108">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="ca4ee-108">optAssemTitle</span></span>|<span data-ttu-id="ca4ee-109">文字列 - アセンブリのタイトルを表します。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-109">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="ca4ee-110">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="ca4ee-110">optAssemDescription</span></span>|<span data-ttu-id="ca4ee-111">文字列 - アセンブリの説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-111">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="ca4ee-112">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="ca4ee-112">optAssemConfig</span></span>|<span data-ttu-id="ca4ee-113">文字列 - アセンブリの構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-113">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="ca4ee-114">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="ca4ee-114">optAssemOS</span></span>|<span data-ttu-id="ca4ee-115">-エンコードされた文字列:"dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion"。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-115">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="ca4ee-116">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="ca4ee-116">optAssemProcessor</span></span>|<span data-ttu-id="ca4ee-117">ULONG</span><span class="sxs-lookup"><span data-stu-id="ca4ee-117">ULONG</span></span>|  
|<span data-ttu-id="ca4ee-118">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="ca4ee-118">optAssemLocale</span></span>|<span data-ttu-id="ca4ee-119">文字列 - アセンブリのロケールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-119">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="ca4ee-120">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="ca4ee-120">optAssemVersion</span></span>|<span data-ttu-id="ca4ee-121">文字列 - としてエンコードされます。"Major.Minor.Build.Revision"。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-121">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="ca4ee-122">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="ca4ee-122">optAssemCompany</span></span>|<span data-ttu-id="ca4ee-123">文字列 - 会社が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-123">String - Contains the company.</span></span>|  
|<span data-ttu-id="ca4ee-124">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="ca4ee-124">optAssemProduct</span></span>|<span data-ttu-id="ca4ee-125">文字列 - 製品名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-125">String - Contains the product name.</span></span>|  
|<span data-ttu-id="ca4ee-126">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="ca4ee-126">optAssemProductVersion</span></span>|<span data-ttu-id="ca4ee-127">文字列 (InformationalVersion とも呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-127">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="ca4ee-128">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="ca4ee-128">optAssemCopyright</span></span>|<span data-ttu-id="ca4ee-129">文字列 - 著作権情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-129">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="ca4ee-130">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="ca4ee-130">optAssemTrademark</span></span>|<span data-ttu-id="ca4ee-131">文字列 - 商標に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-131">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="ca4ee-132">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="ca4ee-132">optAssemKeyFile</span></span>|<span data-ttu-id="ca4ee-133">String (ファイル名)。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-133">String (file name).</span></span>|  
|<span data-ttu-id="ca4ee-134">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="ca4ee-134">optAssemKeyName</span></span>|<span data-ttu-id="ca4ee-135">文字列 (キー名)。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-135">String (The key name).</span></span>|  
|<span data-ttu-id="ca4ee-136">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="ca4ee-136">optAssemAlgID</span></span>|<span data-ttu-id="ca4ee-137">ULONG</span><span class="sxs-lookup"><span data-stu-id="ca4ee-137">ULONG</span></span>|  
|<span data-ttu-id="ca4ee-138">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="ca4ee-138">optAssemFlags</span></span>|<span data-ttu-id="ca4ee-139">ULONG</span><span class="sxs-lookup"><span data-stu-id="ca4ee-139">ULONG</span></span>|  
|<span data-ttu-id="ca4ee-140">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="ca4ee-140">optAssemHalfSign</span></span>|<span data-ttu-id="ca4ee-141">Bool (DelaySign とも呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-141">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="ca4ee-142">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="ca4ee-142">optAssemFileVersion</span></span>|<span data-ttu-id="ca4ee-143">文字列 -"Major.Minor.Build.Revision"--ProductVersion と同じようにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="ca4ee-144">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="ca4ee-144">optAssemSatelliteVer</span></span>|<span data-ttu-id="ca4ee-145">文字列の"Major.Minor.Build.Revision"としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-145">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="ca4ee-146">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="ca4ee-146">optLastAssemOption</span></span>|<span data-ttu-id="ca4ee-147">要素の数のカウンター。</span><span class="sxs-lookup"><span data-stu-id="ca4ee-147">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ca4ee-148">必要条件</span><span class="sxs-lookup"><span data-stu-id="ca4ee-148">Requirements</span></span>  
 <span data-ttu-id="ca4ee-149">**ヘッダー:** alink.h</span><span class="sxs-lookup"><span data-stu-id="ca4ee-149">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="ca4ee-150">**ライブラリ**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="ca4ee-150">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca4ee-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca4ee-151">See also</span></span>
- [<span data-ttu-id="ca4ee-152">Al.exe (アセンブリ リンカー)</span><span class="sxs-lookup"><span data-stu-id="ca4ee-152">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
