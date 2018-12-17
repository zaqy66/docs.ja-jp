---
title: dotnet nuget push コマンド - .NET Core CLI
description: dotnet nuget push コマンドでは、パッケージをサーバーにプッシュして発行します。
author: karann-msft
ms.date: 12/04/2018
ms.openlocfilehash: 090dbfbe3db83b2bb234867aed295ac416b27865
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143062"
---
# <a name="dotnet-nuget-push"></a><span data-ttu-id="05822-103">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="05822-103">dotnet nuget push</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="05822-104">name</span><span class="sxs-lookup"><span data-stu-id="05822-104">Name</span></span>

<span data-ttu-id="05822-105">`dotnet nuget push` - パッケージをサーバーにプッシュして発行します。</span><span class="sxs-lookup"><span data-stu-id="05822-105">`dotnet nuget push` - Pushes a package to the server and publishes it.</span></span>

## <a name="synopsis"></a><span data-ttu-id="05822-106">構文</span><span class="sxs-lookup"><span data-stu-id="05822-106">Synopsis</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="05822-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="05822-107">.NET Core 2.x</span></span>](#tab/netcore2x)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [--interactive] [-k|--api-key] [-n|--no-symbols]
    [--no-service-endpoint] [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="05822-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="05822-108">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="05822-109">説明</span><span class="sxs-lookup"><span data-stu-id="05822-109">Description</span></span>

<span data-ttu-id="05822-110">`dotnet nuget push` コマンドは、パッケージをサーバーにプッシュして発行します。</span><span class="sxs-lookup"><span data-stu-id="05822-110">The `dotnet nuget push` command pushes a package to the server and publishes it.</span></span> <span data-ttu-id="05822-111">プッシュ コマンドでは、システムの NuGet 構成ファイル、または構成ファイルのチェーンで検出されたサーバーと資格情報の詳細を使用します。</span><span class="sxs-lookup"><span data-stu-id="05822-111">The push command uses server and credential details found in the system's NuGet config file or chain of config files.</span></span> <span data-ttu-id="05822-112">構成ファイルの詳細については、「[Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior)」 (NuGet 動作を構成する) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="05822-112">For more information on config files, see [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior).</span></span> <span data-ttu-id="05822-113">NuGet の既定の構成は、*%AppData%\NuGet\NuGet.config* (Windows) または *$HOME/.local/share* (Linux/macOS) を読み込み、次にドライブのルートから開始され、現在のディレクトリで終わる、任意の *nuget.config* または *.nuget\nuget.config* を読み込むことによって取得されます。</span><span class="sxs-lookup"><span data-stu-id="05822-113">NuGet's default configuration is obtained by loading *%AppData%\NuGet\NuGet.config* (Windows) or *$HOME/.local/share* (Linux/macOS), then loading any *nuget.config* or *.nuget\nuget.config* starting from the root of drive and ending in the current directory.</span></span>

## <a name="arguments"></a><span data-ttu-id="05822-114">引数</span><span class="sxs-lookup"><span data-stu-id="05822-114">Arguments</span></span>

* **`ROOT`**

  <span data-ttu-id="05822-115">プッシュされるパッケージのファイル パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="05822-115">Specifies the file path to the package to be pushed.</span></span>

## <a name="options"></a><span data-ttu-id="05822-116">オプション</span><span class="sxs-lookup"><span data-stu-id="05822-116">Options</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="05822-117">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="05822-117">.NET Core 2.x</span></span>](#tab/netcore2x)

* **`-d|--disable-buffering`**

  <span data-ttu-id="05822-118">メモリ使用量を削減するために、HTTP(S) サーバーにプッシュするときのバッファリングを無効にします。</span><span class="sxs-lookup"><span data-stu-id="05822-118">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

* **`--force-english-output`**

  <span data-ttu-id="05822-119">インバリアントの英語ベースのカルチャを使用して、アプリケーションの実行を強制します。</span><span class="sxs-lookup"><span data-stu-id="05822-119">Forces the application to run using an invariant, English-based culture.</span></span>

* **`-h|--help`**

<span data-ttu-id="05822-120">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="05822-120">Prints out a short help for the command.</span></span>

* **`--interactive`**

  <span data-ttu-id="05822-121">コマンドが認証などの操作をブロックして、手動アクションを要求することを許可します。</span><span class="sxs-lookup"><span data-stu-id="05822-121">Allows the command to block and requires manual action for operations like authentication.</span></span> <span data-ttu-id="05822-122">.NET Core 2.2 SDK 以降、使用できるオプションです。</span><span class="sxs-lookup"><span data-stu-id="05822-122">Option available since .NET Core 2.2 SDK.</span></span>

* **`-k|--api-key <API_KEY>`**

  <span data-ttu-id="05822-123">サーバーの API キーです。</span><span class="sxs-lookup"><span data-stu-id="05822-123">The API key for the server.</span></span>

* **`-n|--no-symbols`**

  <span data-ttu-id="05822-124">シンボルをプッシュしません (存在する場合でも)。</span><span class="sxs-lookup"><span data-stu-id="05822-124">Doesn't push symbols (even if present).</span></span>

* **`--no-service-endpoint`**

  <span data-ttu-id="05822-125">ソース URL に "api/v2/package" を追加しません。</span><span class="sxs-lookup"><span data-stu-id="05822-125">Doesn't append "api/v2/package" to the source URL.</span></span> <span data-ttu-id="05822-126">.NET Core 2.1 SDK 以降、使用できるオプションです。</span><span class="sxs-lookup"><span data-stu-id="05822-126">Option available since .NET Core 2.1 SDK.</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="05822-127">サーバー URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="05822-127">Specifies the server URL.</span></span> <span data-ttu-id="05822-128">`DefaultPushSource` 構成値が NuGet 構成ファイルに設定されない限り、このオプションは必須です。</span><span class="sxs-lookup"><span data-stu-id="05822-128">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

* **`-sk|--symbol-api-key <API_KEY>`**

  <span data-ttu-id="05822-129">シンボル サーバーの API キーです。</span><span class="sxs-lookup"><span data-stu-id="05822-129">The API key for the symbol server.</span></span>

* **`-ss|--symbol-source <SOURCE>`**

  <span data-ttu-id="05822-130">シンボル サーバーの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="05822-130">Specifies the symbol server URL.</span></span>

* **`-t|--timeout <TIMEOUT>`**

  <span data-ttu-id="05822-131">秒単位でサーバーにプッシュする場合のタイムアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="05822-131">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="05822-132">既定値は 300 秒 (5 分) です。</span><span class="sxs-lookup"><span data-stu-id="05822-132">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="05822-133">0 (0 秒) を指定すると、既定値が適用されます。</span><span class="sxs-lookup"><span data-stu-id="05822-133">Specifying 0 (zero seconds) applies the default value.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="05822-134">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="05822-134">.NET Core 1.x</span></span>](#tab/netcore1x)

* **`-d|--disable-buffering`**

  <span data-ttu-id="05822-135">メモリ使用量を削減するために、HTTP(S) サーバーにプッシュするときのバッファリングを無効にします。</span><span class="sxs-lookup"><span data-stu-id="05822-135">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

* **`--force-english-output`**

  <span data-ttu-id="05822-136">インバリアントの英語ベースのカルチャを使用して、アプリケーションの実行を強制します。</span><span class="sxs-lookup"><span data-stu-id="05822-136">Forces the application to run using an invariant, English-based culture.</span></span>

* **`-h|--help`**

  <span data-ttu-id="05822-137">コマンドの短いヘルプを印刷します。</span><span class="sxs-lookup"><span data-stu-id="05822-137">Prints out a short help for the command.</span></span>

* **`-k|--api-key <API_KEY>`**

  <span data-ttu-id="05822-138">サーバーの API キーです。</span><span class="sxs-lookup"><span data-stu-id="05822-138">The API key for the server.</span></span>

* **`-n|--no-symbols`**

  <span data-ttu-id="05822-139">シンボルをプッシュしません (存在する場合でも)。</span><span class="sxs-lookup"><span data-stu-id="05822-139">Doesn't push symbols (even if present).</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="05822-140">サーバー URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="05822-140">Specifies the server URL.</span></span> <span data-ttu-id="05822-141">`DefaultPushSource` 構成値が NuGet 構成ファイルに設定されない限り、このオプションは必須です。</span><span class="sxs-lookup"><span data-stu-id="05822-141">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

* **`-sk|--symbol-api-key <API_KEY>`**

  <span data-ttu-id="05822-142">シンボル サーバーの API キーです。</span><span class="sxs-lookup"><span data-stu-id="05822-142">The API key for the symbol server.</span></span>

* **`-ss|--symbol-source <SOURCE>`**

  <span data-ttu-id="05822-143">シンボル サーバーの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="05822-143">Specifies the symbol server URL.</span></span>

* **`-t|--timeout <TIMEOUT>`**

  <span data-ttu-id="05822-144">秒単位でサーバーにプッシュする場合のタイムアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="05822-144">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="05822-145">既定値は 300 秒 (5 分) です。</span><span class="sxs-lookup"><span data-stu-id="05822-145">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="05822-146">0 (0 秒) を指定すると、既定値が適用されます。</span><span class="sxs-lookup"><span data-stu-id="05822-146">Specifying 0 (zero seconds) applies the default value.</span></span>

---

## <a name="examples"></a><span data-ttu-id="05822-147">使用例</span><span class="sxs-lookup"><span data-stu-id="05822-147">Examples</span></span>

* <span data-ttu-id="05822-148">API キーを指定して、既定のプッシュ ソースに *foo.nupkg* をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="05822-148">Pushes *foo.nupkg* to the default push source, specifying an API key:</span></span>

  ```console
  dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a
  ```

* <span data-ttu-id="05822-149">API キーを指定して、カスタム プッシュ ソース `https://customsource` に *foo.nupkg* をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="05822-149">Push *foo.nupkg* to the custom push source `https://customsource`, specifying an API key:</span></span>

  ```console
  dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s https://customsource/
  ```

* <span data-ttu-id="05822-150">既定のプッシュ ソースに *foo.nupkg* をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="05822-150">Pushes *foo.nupkg* to the default push source:</span></span>

  ```console
  dotnet nuget push foo.nupkg
  ```

* <span data-ttu-id="05822-151">既定のシンボル ソースに *foo.symbols.nupkg* をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="05822-151">Pushes *foo.symbols.nupkg* to the default symbols source:</span></span>

  ```console
  dotnet nuget push foo.symbols.nupkg
  ```

* <span data-ttu-id="05822-152">360 秒のタイムアウトを指定して、既定のプッシュ ソースに *foo.nupkg* をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="05822-152">Pushes *foo.nupkg* to the default push source, specifying a 360-second timeout:</span></span>

  ```console
  dotnet nuget push foo.nupkg --timeout 360
  ```

* <span data-ttu-id="05822-153">既定のプッシュ ソースに現在のディレクトリ内のすべての *.nupkg* ファイルをプッシュします。</span><span class="sxs-lookup"><span data-stu-id="05822-153">Pushes all *.nupkg* files in the current directory to the default push source:</span></span>

  ```console
  dotnet nuget push *.nupkg
  ```