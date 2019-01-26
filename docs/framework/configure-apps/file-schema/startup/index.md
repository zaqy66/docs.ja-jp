---
title: スタートアップ設定スキーマ
ms.date: 03/30/2017
helpviewer_keywords:
- startup settings schema
- schema startup settings
- configuration schema [.NET Framework], startup settings
ms.assetid: 03de6972-442a-4648-9f3e-efa654e3b949
ms.openlocfilehash: e5f9c9af64ff38e7c0f1f26ccab039261b052e30
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083419"
---
# <a name="startup-settings-schema"></a><span data-ttu-id="0300c-102">スタートアップ設定スキーマ</span><span class="sxs-lookup"><span data-stu-id="0300c-102">Startup settings schema</span></span>

<span data-ttu-id="0300c-103">スタートアップ設定は、アプリケーションを実行する必要のある共通言語ランタイムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="0300c-103">Startup settings specify the version of the common language runtime that should run the application.</span></span>  
  
|<span data-ttu-id="0300c-104">要素</span><span class="sxs-lookup"><span data-stu-id="0300c-104">Element</span></span>|<span data-ttu-id="0300c-105">説明</span><span class="sxs-lookup"><span data-stu-id="0300c-105">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0300c-106">\<requiredRuntime></span><span class="sxs-lookup"><span data-stu-id="0300c-106">\<requiredRuntime></span></span>](requiredruntime-element.md)|<span data-ttu-id="0300c-107">バージョン 1.0 の共通言語ランタイムのみがアプリケーションでサポートされることを指定します。</span><span class="sxs-lookup"><span data-stu-id="0300c-107">Specifies that the application supports only version 1.0 of the common language runtime.</span></span> <span data-ttu-id="0300c-108">ランタイムのバージョン 1.1 でビルドされたアプリケーションは、**\<supportedRuntime >** 要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="0300c-108">Applications built with runtime version 1.1 should use the **\<supportedRuntime>** element.</span></span>|  
|[<span data-ttu-id="0300c-109">\<supportedRuntime></span><span class="sxs-lookup"><span data-stu-id="0300c-109">\<supportedRuntime></span></span>](supportedruntime-element.md)|<span data-ttu-id="0300c-110">アプリケーションでサポートされる共通言語ランタイムのバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="0300c-110">Specifies which versions of the common language runtime the application supports.</span></span>|  
|[<span data-ttu-id="0300c-111">\<startup></span><span class="sxs-lookup"><span data-stu-id="0300c-111">\<startup></span></span>](startup-element.md)|<span data-ttu-id="0300c-112">**\<requiredRuntime>** 要素と **\<supportedRuntime>** 要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="0300c-112">Contains the **\<requiredRuntime>** and **\<supportedRuntime>** elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0300c-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="0300c-113">See also</span></span>

- [<span data-ttu-id="0300c-114">構成ファイル スキーマ</span><span class="sxs-lookup"><span data-stu-id="0300c-114">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="0300c-115">方法: .NET Framework 4 以降のバージョンをサポートするアプリを構成する</span><span class="sxs-lookup"><span data-stu-id="0300c-115">How to: Configure an app to support .NET Framework 4 or later versions</span></span>](../../../migration-guide/how-to-configure-an-app-to-support-net-framework-4-or-4-5.md)
