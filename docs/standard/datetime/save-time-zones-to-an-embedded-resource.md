---
title: '方法: 埋め込みリソースにタイム ゾーンを保存'
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET Framework], saving
- time zone objects [.NET Framework], serializing
- time zone objects [.NET Framework], saving
ms.assetid: 3c96d83a-a057-4496-abb0-8f4b12712558
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 921874e774d18751c29db495dac1bc53d10cc8ad
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2018
ms.locfileid: "44211854"
---
# <a name="how-to-save-time-zones-to-an-embedded-resource"></a><span data-ttu-id="ab217-102">方法: 埋め込みリソースにタイム ゾーンを保存</span><span class="sxs-lookup"><span data-stu-id="ab217-102">How to: Save time zones to an embedded resource</span></span>

<span data-ttu-id="ab217-103">多くの場合、タイム ゾーンに対応するアプリケーションでは、特定のタイム ゾーンの存在が必要です。</span><span class="sxs-lookup"><span data-stu-id="ab217-103">A time zone-aware application often requires the presence of a particular time zone.</span></span> <span data-ttu-id="ab217-104">ただし、ため、個々 の可用性<xref:System.TimeZoneInfo>オブジェクトは、システムのローカル レジストリに格納されている情報によって異なります、慣例的でも使用可能なタイム ゾーンが存在しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ab217-104">However, because the availability of individual <xref:System.TimeZoneInfo> objects depends on information stored in the local system's registry, even customarily available time zones may be absent.</span></span> <span data-ttu-id="ab217-105">使用してさらに、カスタム タイム ゾーンに関する情報がインスタンス化、<xref:System.TimeZoneInfo.CreateCustomTimeZone%2A>メソッドは、レジストリ内の他のタイム ゾーン情報には格納されません。</span><span class="sxs-lookup"><span data-stu-id="ab217-105">In addition, information about custom time zones instantiated by using the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method is not stored with other time zone information in the registry.</span></span> <span data-ttu-id="ab217-106">必要なときにこれらのタイム ゾーンが使用できることを確認するには、シリアル化して保存し、それらを逆シリアル化して復元することができます。</span><span class="sxs-lookup"><span data-stu-id="ab217-106">To ensure that these time zones are available when they are needed, you can save them by serializing them, and later restore them by deserializing them.</span></span>

<span data-ttu-id="ab217-107">通常、シリアル化、<xref:System.TimeZoneInfo>オブジェクトは、タイム ゾーン対応アプリケーションとは別に発生します。</span><span class="sxs-lookup"><span data-stu-id="ab217-107">Typically, serializing a <xref:System.TimeZoneInfo> object occurs apart from the time zone-aware application.</span></span> <span data-ttu-id="ab217-108">シリアル化された保持するために使用されるデータ ストアによって<xref:System.TimeZoneInfo>オブジェクト、または (たとえば、レジストリのアプリケーション キーでデータが格納されている場合)、セットアップやインストール ルーチンの一部として実行しているユーティリティ ルーチンの一部としては、タイム ゾーンのデータをシリアル化される可能性があります前に、(たとえば、シリアル化されたデータは .NET XML リソース (.resx) ファイルに格納されている) 場合、最終的なアプリケーションがコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="ab217-108">Depending on the data store used to hold serialized <xref:System.TimeZoneInfo> objects, time zone data may be serialized as part of a setup or installation routine (for example, when the data is stored in an application key of the registry), or as part of a utility routine that runs before the final application is compiled (for example, when the serialized data is stored in a .NET XML resource (.resx) file).</span></span>

<span data-ttu-id="ab217-109">だけでなく、アプリケーションでコンパイルされるリソース ファイル、その他のいくつかのデータ ストアは、タイム ゾーン情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab217-109">In addition to a resource file that is compiled with the application, several other data stores can be used for time zone information.</span></span> <span data-ttu-id="ab217-110">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="ab217-110">These include the following:</span></span>

* <span data-ttu-id="ab217-111">レジストリ。</span><span class="sxs-lookup"><span data-stu-id="ab217-111">The registry.</span></span> <span data-ttu-id="ab217-112">アプリケーションで、hkey_local_machine \software\microsoft\windows nt \currentversion\time Zones のサブキーを使用するのではなく、カスタムのタイム ゾーンのデータを格納する独自のアプリケーション キーのサブキーを使用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ab217-112">Note that an application should use the subkeys of its own application key to store custom time zone data rather than using the subkeys of HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Time Zones.</span></span>

* <span data-ttu-id="ab217-113">構成ファイル。</span><span class="sxs-lookup"><span data-stu-id="ab217-113">Configuration files.</span></span>

* <span data-ttu-id="ab217-114">その他のシステム ファイル。</span><span class="sxs-lookup"><span data-stu-id="ab217-114">Other system files.</span></span>

### <a name="to-save-a-time-zone-by-serializing-it-to-a-resx-file"></a><span data-ttu-id="ab217-115">.Resx ファイルにシリアル化され、タイム ゾーンを保存するには</span><span class="sxs-lookup"><span data-stu-id="ab217-115">To save a time zone by serializing it to a .resx file</span></span>

1. <span data-ttu-id="ab217-116">既存のタイム ゾーンを取得するか、新しいタイム ゾーンを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab217-116">Retrieve an existing time zone or create a new time zone.</span></span>

   <span data-ttu-id="ab217-117">既存のタイム ゾーンを取得するには、次を参照してください。[方法: 定義済みの UTC とローカル タイム ゾーン オブジェクトにアクセス](../../../docs/standard/datetime/access-utc-and-local.md)と[方法: TimeZoneInfo オブジェクトをインスタンス化](../../../docs/standard/datetime/instantiate-time-zone-info.md)します。</span><span class="sxs-lookup"><span data-stu-id="ab217-117">To retrieve an existing time zone, see [How to: Access the predefined UTC and local time zone objects](../../../docs/standard/datetime/access-utc-and-local.md) and [How to: Instantiate a TimeZoneInfo object](../../../docs/standard/datetime/instantiate-time-zone-info.md).</span></span>

   <span data-ttu-id="ab217-118">新しいタイム ゾーンを作成するには、いずれかのオーバー ロードを呼び出す、<xref:System.TimeZoneInfo.CreateCustomTimeZone%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="ab217-118">To create a new time zone, call one of the overloads of the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method.</span></span> <span data-ttu-id="ab217-119">詳細については、次を参照してください。[方法: 調整規則のないタイム ゾーンを作成](../../../docs/standard/datetime/create-time-zones-without-adjustment-rules.md)と[方法: 調整規則のあるタイム ゾーンを作成](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md)です。</span><span class="sxs-lookup"><span data-stu-id="ab217-119">For more information, see [How to: Create time zones without adjustment rules](../../../docs/standard/datetime/create-time-zones-without-adjustment-rules.md) and [How to: Create time zones with adjustment rules](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md).</span></span>

2. <span data-ttu-id="ab217-120">呼び出す、<xref:System.TimeZoneInfo.ToSerializedString%2A>タイム ゾーンのデータを格納する文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="ab217-120">Call the <xref:System.TimeZoneInfo.ToSerializedString%2A> method to create a string that contains the time zone's data.</span></span>

3. <span data-ttu-id="ab217-121">インスタンスを作成、<xref:System.IO.StreamWriter>オブジェクト、名前と必要に応じて、.resx ファイルのパスを提供することで、<xref:System.IO.StreamWriter>クラスのコンス トラクター。</span><span class="sxs-lookup"><span data-stu-id="ab217-121">Instantiate a <xref:System.IO.StreamWriter> object by providing the name and optionally the path of the .resx file to the <xref:System.IO.StreamWriter> class constructor.</span></span>

4. <span data-ttu-id="ab217-122">インスタンスを作成、<xref:System.Resources.ResXResourceWriter>オブジェクトを渡すことによって、<xref:System.IO.StreamWriter>オブジェクトを<xref:System.Resources.ResXResourceWriter>クラスのコンス トラクター。</span><span class="sxs-lookup"><span data-stu-id="ab217-122">Instantiate a <xref:System.Resources.ResXResourceWriter> object by passing the <xref:System.IO.StreamWriter> object to the <xref:System.Resources.ResXResourceWriter> class constructor.</span></span>

5. <span data-ttu-id="ab217-123">タイム ゾーンをパスに文字列をシリアル化、<xref:System.Resources.ResXResourceWriter.AddResource%2A?displayProperty=nameWithType>メソッド。</span><span class="sxs-lookup"><span data-stu-id="ab217-123">Pass the time zone's serialized string to the <xref:System.Resources.ResXResourceWriter.AddResource%2A?displayProperty=nameWithType> method.</span></span>

6. <span data-ttu-id="ab217-124"><xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType> メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ab217-124">Call the <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType> method.</span></span>

7. <span data-ttu-id="ab217-125"><xref:System.Resources.ResXResourceWriter.Close%2A?displayProperty=nameWithType> メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ab217-125">Call the <xref:System.Resources.ResXResourceWriter.Close%2A?displayProperty=nameWithType> method.</span></span>

8. <span data-ttu-id="ab217-126">閉じる、<xref:System.IO.StreamWriter>オブジェクトを呼び出すことによってその<xref:System.IO.StreamWriter.Close%2A>メソッド。</span><span class="sxs-lookup"><span data-stu-id="ab217-126">Close the <xref:System.IO.StreamWriter> object by calling its <xref:System.IO.StreamWriter.Close%2A> method.</span></span>

9. <span data-ttu-id="ab217-127">アプリケーションの Visual Studio プロジェクトに生成された .resx ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="ab217-127">Add the generated .resx file to the application's Visual Studio project.</span></span>

10. <span data-ttu-id="ab217-128">使用して、**プロパティ**Visual Studio で、ウィンドウを確認する、.resx ファイルの**ビルド アクション**プロパティに設定されて**埋め込まれたリソース**します。</span><span class="sxs-lookup"><span data-stu-id="ab217-128">Using the **Properties** window in Visual Studio, make sure that the .resx file's **Build Action** property is set to **Embedded Resource**.</span></span>

## <a name="example"></a><span data-ttu-id="ab217-129">例</span><span class="sxs-lookup"><span data-stu-id="ab217-129">Example</span></span>

<span data-ttu-id="ab217-130">次の例では、シリアル化、<xref:System.TimeZoneInfo>中部標準時を表すオブジェクトを<xref:System.TimeZoneInfo>SerializedTimeZones.resx という .NET XML リソース ファイルにパーマー基地、南極時間を表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ab217-130">The following example serializes a <xref:System.TimeZoneInfo> object that represents Central Standard Time and a <xref:System.TimeZoneInfo> object that represents the Palmer Station, Antarctica time to a .NET XML resource file that is named SerializedTimeZones.resx.</span></span> <span data-ttu-id="ab217-131">中部標準時は通常、レジストリで定義されています。Palmer ステーション、南極カスタム タイム ゾーンです。</span><span class="sxs-lookup"><span data-stu-id="ab217-131">Central Standard Time is typically defined in the registry; Palmer Station, Antarctica is a custom time zone.</span></span>

[!code-csharp[TimeZone2.Serialization#1](../../../samples/snippets/csharp/VS_Snippets_CLR/TimeZone2.Serialization/cs/SerializeTimeZoneData.cs#1)]
[!code-vb[TimeZone2.Serialization#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/TimeZone2.Serialization/vb/SerializeTimeZoneData.vb#1)]

<span data-ttu-id="ab217-132">この例のシリアル化<xref:System.TimeZoneInfo>されるので使用可能なリソース ファイルのコンパイル時のオブジェクトします。</span><span class="sxs-lookup"><span data-stu-id="ab217-132">This example serializes <xref:System.TimeZoneInfo> objects so that they are available in a resource file at compile time.</span></span>

<span data-ttu-id="ab217-133"><xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType>メソッドは、.NET XML リソース ファイルに完全なヘッダー情報を追加、既存のファイルにリソースを追加するために使用できません。</span><span class="sxs-lookup"><span data-stu-id="ab217-133">Because the <xref:System.Resources.ResXResourceWriter.Generate%2A?displayProperty=nameWithType> method adds complete header information to a .NET XML resource file, it cannot be used to add resources to an existing file.</span></span> <span data-ttu-id="ab217-134">例では、これを処理 SerializedTimeZones.resx ファイルをチェックして、存在する場合以外のすべてのリソースを格納する、2 つシリアル化をジェネリックのタイム ゾーン<xref:System.Collections.Generic.Dictionary%602>オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ab217-134">The example handles this by checking for the SerializedTimeZones.resx file and, if it exists, storing all of its resources other than the two serialized time zones to a generic <xref:System.Collections.Generic.Dictionary%602> object.</span></span> <span data-ttu-id="ab217-135">既存のファイルが削除され、既存のリソースが SerializedTimeZones.resx の新しいファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ab217-135">The existing file is then deleted and the existing resources are added to a new SerializedTimeZones.resx file.</span></span> <span data-ttu-id="ab217-136">タイム ゾーンのシリアル化されたデータは、このファイルにも追加されます。</span><span class="sxs-lookup"><span data-stu-id="ab217-136">The serialized time zone data is also added to this file.</span></span>

<span data-ttu-id="ab217-137">キー (または**名前**) リソースのフィールドは空白を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ab217-137">The key (or **Name**) fields of resources should not contain embedded spaces.</span></span> <span data-ttu-id="ab217-138"><xref:System.String.Replace%28System.String%2CSystem.String%29>リソース ファイルに割り当てられている、前に、タイム ゾーン識別子のすべての埋め込みスペースを削除するメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ab217-138">The <xref:System.String.Replace%28System.String%2CSystem.String%29> method is called to remove all embedded spaces in the time zone identifiers before they are assigned to the resource file.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="ab217-139">コードのコンパイル</span><span class="sxs-lookup"><span data-stu-id="ab217-139">Compiling the code</span></span>

<span data-ttu-id="ab217-140">この例で必要な要素は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ab217-140">This example requires:</span></span>

* <span data-ttu-id="ab217-141">System.Windows.Forms.dll、System.Core.dll への参照をプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="ab217-141">That a reference to System.Windows.Forms.dll and System.Core.dll be added to the project.</span></span>

* <span data-ttu-id="ab217-142">次の名前空間は、インポートします。</span><span class="sxs-lookup"><span data-stu-id="ab217-142">That the following namespaces be imported:</span></span>

  [!code-csharp[TimeZone2.Serialization#2](../../../samples/snippets/csharp/VS_Snippets_CLR/TimeZone2.Serialization/cs/SerializeTimeZoneData.cs#2)]
  [!code-vb[TimeZone2.Serialization#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/TimeZone2.Serialization/vb/SerializeTimeZoneData.vb#2)]

## <a name="see-also"></a><span data-ttu-id="ab217-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab217-143">See also</span></span>

* [<span data-ttu-id="ab217-144">日付、時刻、およびタイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="ab217-144">Dates, times, and time zones</span></span>](../../../docs/standard/datetime/index.md)
* [<span data-ttu-id="ab217-145">タイム ゾーンの概要</span><span class="sxs-lookup"><span data-stu-id="ab217-145">Time zone overview</span></span>](../../../docs/standard/datetime/time-zone-overview.md)
* [<span data-ttu-id="ab217-146">方法: 埋め込みリソースからタイム ゾーンを復元する</span><span class="sxs-lookup"><span data-stu-id="ab217-146">How to: Restore time zones from an embedded resource</span></span>](../../../docs/standard/datetime/restore-time-zones-from-an-embedded-resource.md)
