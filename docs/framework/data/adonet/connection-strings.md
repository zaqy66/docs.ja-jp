---
title: ADO.NET での接続文字列
ms.date: 03/30/2017
ms.assetid: 745c5f95-2f02-4674-b378-6d51a7ec2490
ms.openlocfilehash: 1e6e2b6870195c99279639e1f4576a30b7126d4d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583696"
---
# <a name="connection-strings-in-adonet"></a><span data-ttu-id="5fafe-102">ADO.NET での接続文字列</span><span class="sxs-lookup"><span data-stu-id="5fafe-102">Connection Strings in ADO.NET</span></span>
<span data-ttu-id="5fafe-103">.NET Framework 2.0 では、接続文字列を扱う新しい機能が導入されました。接続文字列ビルダー クラスに追加された新しいキーワードもその 1 つであり、有効な接続文字列を実行時に簡単に作成できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="5fafe-103">The .NET Framework 2.0 introduced new capabilities for working with connection strings, including the introduction of new keywords to the connection string builder classes, which facilitate creating valid connection strings at run time.</span></span>  
  
<span data-ttu-id="5fafe-104">接続文字列には、データ プロバイダーからデータ ソースにパラメーターとして渡す初期化情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5fafe-104">A connection string contains initialization information that is passed as a parameter from a data provider to a data source.</span></span> <span data-ttu-id="5fafe-105">接続文字列は接続を開くときに解析され、その構文はデータ プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="5fafe-105">The syntax depends on the data provider, and the connection string is parsed during the attempt to open a connection.</span></span> <span data-ttu-id="5fafe-106">構文エラーの場合はランタイム例外が生成されますが、その他のエラーは、データ ソースが接続情報を受け取った後でのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-106">Syntax errors generate a run-time exception, but other errors occur only after the data source receives connection information.</span></span> <span data-ttu-id="5fafe-107">いったん接続文字列が検証されると、接続文字列に指定されたオプションがデータ ソースによって適用されて接続が開かれます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-107">Once validated, the data source applies the options specified in the connection string and opens the connection.</span></span>
  
<span data-ttu-id="5fafe-108">接続文字列の形式は、キーと値パラメーターのペアをセミコロンで区切ったリストです。</span><span class="sxs-lookup"><span data-stu-id="5fafe-108">The format of a connection string is a semicolon-delimited list of key/value parameter pairs:</span></span>
  
    keyword1=value; keyword2=value;
  
<span data-ttu-id="5fafe-109">キーワードは区別されません。</span><span class="sxs-lookup"><span data-stu-id="5fafe-109">Keywords are not case-sensitive.</span></span> <span data-ttu-id="5fafe-110">値、ただし、可能性があります、データ ソースによって、大文字小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-110">Values, however, may be case-sensitive, depending on the data source.</span></span> <span data-ttu-id="5fafe-111">キーワードと値の両方を含めることができます[空白文字](https://en.wikipedia.org/wiki/Whitespace_character#Unicode)先頭および末尾の空白はキーワードで無視され、引用符は、値。</span><span class="sxs-lookup"><span data-stu-id="5fafe-111">Both keywords and values may contain [whitespace characters](https://en.wikipedia.org/wiki/Whitespace_character#Unicode), although leading and trailing whitespace is ignored in keywords and unquoted values.</span></span>

<span data-ttu-id="5fafe-112">値には、セミコロンが含まれている場合[Unicode コントロール文字](https://en.wikipedia.org/wiki/Unicode_control_characters)、先頭または末尾の空白を囲む必要があります単一引用符または二重引用符でなど。</span><span class="sxs-lookup"><span data-stu-id="5fafe-112">If a value contains the semicolon, [Unicode control characters](https://en.wikipedia.org/wiki/Unicode_control_characters), leading or trailing whitespace it must be enclosed in single or double quotation marks, e.g.:</span></span>

    Keyword=" whitespace  ";
    Keyword='special;character';

<span data-ttu-id="5fafe-113">それを囲む文字を囲む値内で発生しません。</span><span class="sxs-lookup"><span data-stu-id="5fafe-113">The enclosing character may not occur within the value it encloses.</span></span> <span data-ttu-id="5fafe-114">そのため、単一引用符を含む値を囲む二重引用符でのみ、またはその逆ことができます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-114">Therefore, a value containing single quotation marks can be enclosed only in double quotation marks and vice versa:</span></span>

    Keyword='double"quotation;mark';
    Keyword="single'quotation;mark";

<span data-ttu-id="5fafe-115">、等号と同様に、引用符は不要、エスケープため、次の接続文字列が無効です。</span><span class="sxs-lookup"><span data-stu-id="5fafe-115">The quotation marks themselves, as well as the equals sign, do not require escaping, so the following connection strings are valid:</span></span>

    Keyword=no "escaping" 'required';
    Keyword=a=b=c

<span data-ttu-id="5fafe-116">後者の例の値は、各値は、[次へ] のセミコロンまたは文字列の末尾まで読み取ることが、ため`a=b=c`、最後のセミコロンは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="5fafe-116">Since each value is read till the next semicolon or the end of string, the value in the latter example is `a=b=c`, and the final semicolon is optional.</span></span>

<span data-ttu-id="5fafe-117">有効な接続文字列の構文はプロバイダーによって異なり、ODBC のような初期の API から長年にわたって進化しています。</span><span class="sxs-lookup"><span data-stu-id="5fafe-117">Valid connection string syntax depends on the provider, and has evolved over the years from earlier APIs like ODBC.</span></span> <span data-ttu-id="5fafe-118">.NET Framework Data Provider for SQL Server (SqlClient) には、古い構文の要素が多数組み込まれており、一般的に、共通の接続文字列の構文に対しては柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="5fafe-118">The .NET Framework Data Provider for SQL Server (SqlClient) incorporates many elements from older syntax and is generally more flexible with common connection string syntax.</span></span> <span data-ttu-id="5fafe-119">多くの場合、接続文字列の構文要素には同等として扱われる有効なシノニムが存在しますが、構文やスペルの誤りによって問題が生じる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="5fafe-119">There are frequently equally valid synonyms for connection string syntax elements, but some syntax and spelling errors can cause problems.</span></span> <span data-ttu-id="5fafe-120">たとえば、"`Integrated Security=true`" は有効ですが、"`IntegratedSecurity=true`" ではエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-120">For example, "`Integrated Security=true`" is valid, whereas "`IntegratedSecurity=true`" causes an error.</span></span> <span data-ttu-id="5fafe-121">また、ユーザー入力を基にして接続文字列を実行時に構築する場合、入力された文字列を検証しないと、文字列のインジェクション攻撃を招き、データ ソースのセキュリティが脅かされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5fafe-121">In addition, connection strings constructed at run time from unvalidated user input can lead to string injection attacks, jeopardizing security at the data source.</span></span>
  
<span data-ttu-id="5fafe-122">こうした問題に対処するため、ADO.NET 2.0 では、各 .NET Framework データ プロバイダー用の新しい接続文字列ビルダーが導入されました。</span><span class="sxs-lookup"><span data-stu-id="5fafe-122">To address these problems, ADO.NET 2.0 introduced new connection string builders for each .NET Framework data provider.</span></span> <span data-ttu-id="5fafe-123">キーワードがプロパティとして公開され、接続文字列をデータ ソースに送信する前に、その構文を検証できます。</span><span class="sxs-lookup"><span data-stu-id="5fafe-123">Keywords are exposed as properties, enabling connection string syntax to be validated before submission to the data source.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5fafe-124">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="5fafe-124">In This Section</span></span>  
 [<span data-ttu-id="5fafe-125">接続文字列ビルダー</span><span class="sxs-lookup"><span data-stu-id="5fafe-125">Connection String Builders</span></span>](../../../../docs/framework/data/adonet/connection-string-builders.md)  
 <span data-ttu-id="5fafe-126">`ConnectionStringBuilder` クラスを使用して、有効な接続文字列を実行時に作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-126">Demonstrates how to use the `ConnectionStringBuilder` classes to construct valid connection strings at run time.</span></span>
  
 [<span data-ttu-id="5fafe-127">接続文字列と構成ファイル</span><span class="sxs-lookup"><span data-stu-id="5fafe-127">Connection Strings and Configuration Files</span></span>](../../../../docs/framework/data/adonet/connection-strings-and-configuration-files.md)  
 <span data-ttu-id="5fafe-128">構成ファイルを使用した接続文字列の格納と取得の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-128">Demonstrates how to store and retrieve connection strings in configuration files.</span></span>
  
 [<span data-ttu-id="5fafe-129">接続文字列の構文</span><span class="sxs-lookup"><span data-stu-id="5fafe-129">Connection String Syntax</span></span>](../../../../docs/framework/data/adonet/connection-string-syntax.md)  
 <span data-ttu-id="5fafe-130">`SqlClient`、`OracleClient`、`OleDb`、`Odbc` の各プロバイダーに固有の接続文字列を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-130">Describes how to configure provider-specific connection strings for `SqlClient`, `OracleClient`, `OleDb`, and `Odbc`.</span></span>
  
 [<span data-ttu-id="5fafe-131">接続情報の保護</span><span class="sxs-lookup"><span data-stu-id="5fafe-131">Protecting Connection Information</span></span>](../../../../docs/framework/data/adonet/protecting-connection-information.md)  
 <span data-ttu-id="5fafe-132">データ ソースへの接続に使用する情報を保護する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5fafe-132">Demonstrates techniques for protecting information used to connect to a data source.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5fafe-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fafe-133">See Also</span></span>  
 [<span data-ttu-id="5fafe-134">データ ソースへの接続</span><span class="sxs-lookup"><span data-stu-id="5fafe-134">Connecting to a Data Source</span></span>](/cpp/data/odbc/connecting-to-a-data-source)  
 [<span data-ttu-id="5fafe-135">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="5fafe-135">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
