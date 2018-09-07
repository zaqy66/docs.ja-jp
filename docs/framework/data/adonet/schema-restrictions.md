---
title: スキーマの制限
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 73d2980e-e73c-4987-913a-8ddc93d09144
ms.openlocfilehash: 040ecd8a2ce223f89601de735b77ccc81638c7af
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44079709"
---
# <a name="schema-restrictions"></a><span data-ttu-id="f5dae-102">スキーマの制限</span><span class="sxs-lookup"><span data-stu-id="f5dae-102">Schema Restrictions</span></span>
<span data-ttu-id="f5dae-103">2 番目の省略可能なパラメーター、 **GetSchema**メソッドが返されるスキーマ情報の量を制限するために使用される制限事項、およびに渡される、 **GetSchema**文字列の配列としてメソッド.</span><span class="sxs-lookup"><span data-stu-id="f5dae-103">The second optional parameter of the **GetSchema** method is the restrictions that are used to limit the amount of schema information returned, and it is passed to the **GetSchema** method as an array of strings.</span></span> <span data-ttu-id="f5dae-104">配列での位置により、渡すことができる値が決定します。これは、制限の番号に相当します。</span><span class="sxs-lookup"><span data-stu-id="f5dae-104">The position in the array determines the values that you can pass, and this is equivalent to the restriction number.</span></span>  
  
 <span data-ttu-id="f5dae-105">たとえば、次の表は、.NET Framework Data Provider for SQL Server を使用して、"Tables" スキーマ コレクションによりサポートされる制限を示しています。</span><span class="sxs-lookup"><span data-stu-id="f5dae-105">For example, the following table describes the restrictions supported by the "Tables" schema collection using the .NET Framework Data Provider for SQL Server.</span></span> <span data-ttu-id="f5dae-106">SQL Server スキーマ コレクションの追加の制限をこのトピックの終わりに示します。</span><span class="sxs-lookup"><span data-stu-id="f5dae-106">Additional restrictions for SQL Server schema collections are listed at the end of this topic.</span></span>  
  
|<span data-ttu-id="f5dae-107">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-107">Restriction Name</span></span>|<span data-ttu-id="f5dae-108">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-108">Parameter Name</span></span>|<span data-ttu-id="f5dae-109">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-109">Restriction Default</span></span>|<span data-ttu-id="f5dae-110">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-110">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-111">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-111">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-112">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-112">TABLE_CATALOG</span></span>|<span data-ttu-id="f5dae-113">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-113">1</span></span>|  
|<span data-ttu-id="f5dae-114">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-114">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-115">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-115">TABLE_SCHEMA</span></span>|<span data-ttu-id="f5dae-116">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-116">2</span></span>|  
|<span data-ttu-id="f5dae-117">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-117">Table</span></span>|@Name|<span data-ttu-id="f5dae-118">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-118">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-119">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-119">3</span></span>|  
|<span data-ttu-id="f5dae-120">TableType</span><span class="sxs-lookup"><span data-stu-id="f5dae-120">TableType</span></span>|@TableType|<span data-ttu-id="f5dae-121">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5dae-121">TABLE_TYPE</span></span>|<span data-ttu-id="f5dae-122">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-122">4</span></span>|  
  
## <a name="specifying-restriction-values"></a><span data-ttu-id="f5dae-123">制限値の指定</span><span class="sxs-lookup"><span data-stu-id="f5dae-123">Specifying Restriction Values</span></span>  
 <span data-ttu-id="f5dae-124">"Tables" スキーマ コレクションの制限の 1 つを使用するには、4 つの要素を使って文字列の配列を作成してから、制限の番号と一致する要素内に値を配置します。</span><span class="sxs-lookup"><span data-stu-id="f5dae-124">To use one of the restrictions of the "Tables" schema collection, simply create an array of strings with four elements, then place a value in the element that matches the restriction number.</span></span> <span data-ttu-id="f5dae-125">たとえば、テーブルを制限によって返される、 **GetSchema** 、"Sales"スキーマ内のテーブルのみをメソッドに渡す前に"Sales"配列の 2 番目の要素の設定、 **GetSchema**メソッド。</span><span class="sxs-lookup"><span data-stu-id="f5dae-125">For example, to restrict the tables returned by the **GetSchema** method to only those tables in the "Sales" schema, set the second element of the array to "Sales" before passing it to the **GetSchema** method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f5dae-126">`SqlClient` と `OracleClient` の制限のコレクションには、追加の `ParameterName` 列があります。</span><span class="sxs-lookup"><span data-stu-id="f5dae-126">The restrictions collections for `SqlClient` and `OracleClient` have an additional `ParameterName` column.</span></span> <span data-ttu-id="f5dae-127">制限の既定の列は、下位互換性のために存在してはいますが、現在は無視されています。</span><span class="sxs-lookup"><span data-stu-id="f5dae-127">The restriction default column is still there for backwards compatibility, but is currently ignored.</span></span> <span data-ttu-id="f5dae-128">制限の値を指定する場合、文字列置換ではなく、パラメーター付きのクエリを使って、SQL への注入攻撃のリスクを最小限にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5dae-128">Parameterized queries rather than string replacement should be used to minimize the risk of an SQL injection attack when specifying restriction values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f5dae-129">配列内の要素数は、指定したスキーマ コレクションでサポートされる制限数以下にする必要があります。そうでない場合、<xref:System.ArgumentException> がスローされます。</span><span class="sxs-lookup"><span data-stu-id="f5dae-129">The number of elements in the array must be less than or equal to the number of restrictions supported for the specified schema collection else an <xref:System.ArgumentException> will be thrown.</span></span> <span data-ttu-id="f5dae-130">制限は最大数よりも小さい場合があります。</span><span class="sxs-lookup"><span data-stu-id="f5dae-130">There can be fewer than the maximum number of restrictions.</span></span> <span data-ttu-id="f5dae-131">指定されていない制限は、null (無制限) と見なされます。</span><span class="sxs-lookup"><span data-stu-id="f5dae-131">The missing restrictions are assumed to be null (unrestricted).</span></span>  
  
 <span data-ttu-id="f5dae-132">呼び出すことによってサポートされている制限の一覧を決定する .NET Framework マネージ プロバイダーを照会することができます、 **GetSchema** 「制限」は、制限のスキーマのコレクションの名前を持つメソッド。</span><span class="sxs-lookup"><span data-stu-id="f5dae-132">You can query a .NET Framework managed provider to determine the list of supported restrictions by calling the **GetSchema** method with the name of the restrictions schema collection, which is "Restrictions".</span></span> <span data-ttu-id="f5dae-133">これにより、コレクション名の一覧、制限の名前、既定の制限値、および制限の番号と共に、<xref:System.Data.DataTable> が返されます。</span><span class="sxs-lookup"><span data-stu-id="f5dae-133">This will return a <xref:System.Data.DataTable> with a list of the collection names, the restriction names, the default restriction values, and the restriction numbers.</span></span>  
  
### <a name="example"></a><span data-ttu-id="f5dae-134">例</span><span class="sxs-lookup"><span data-stu-id="f5dae-134">Example</span></span>  
 <span data-ttu-id="f5dae-135">次の例では、使用する方法、 <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> 、.NET Framework Data Provider for SQL Server 方法<xref:System.Data.SqlClient.SqlConnection>に関するすべてのテーブルに含まれるスキーマ情報を取得するクラス、 **AdventureWorks**サンプル データベース、および"Sales"スキーマ内のテーブルのみに返される情報を制限します。</span><span class="sxs-lookup"><span data-stu-id="f5dae-135">The following examples demonstrate how to use the <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> method of the .NET Framework Data Provider for the SQL Server <xref:System.Data.SqlClient.SqlConnection> class to retrieve schema information about all of the tables contained in the **AdventureWorks** sample database, and to restrict the information returned to only those tables in the "Sales" schema:</span></span>  
  
```vb  
Imports System.Data.SqlClient  
  
Module Module1  
Sub Main()  
  Dim connectionString As String = _  
    "Data Source=(local);Database=AdventureWorks;" & _  
       "Integrated Security=true;";  
  
  Dim restrictions(3) As String  
  Using connection As New SqlConnection(connectionString)  
    connection.Open()  
  
    'Specify the restrictions.  
    restrictions(1) = "Sales"  
    Dim table As DataTable = connection.GetSchema("Tables", _  
       restrictions)  
  
    ' Display the contents of the table.  
      For Each row As DataRow In table.Rows  
         For Each col As DataColumn In table.Columns  
            Console.WriteLine("{0} = {1}", col.ColumnName, row(col))  
         Next  
         Console.WriteLine("============================")  
      Next  
    Console.WriteLine("Press any key to continue.")  
    Console.ReadKey()  
  End Using  
End Sub  
End Module  
```  
  
```csharp  
using System;  
using System.Data;  
using System.Data.SqlClient;  
  
class Program  
{  
  static void Main()  
  {  
    string connectionString =   
       "Data Source=(local);Database=AdventureWorks;" +  
       "Integrated Security=true;";  
    using (SqlConnection connection =  
       new SqlConnection(connectionString))  
    {  
        connection.Open();  
  
        // Specify the restrictions.  
        string[] restrictions = new string[4];  
        restrictions[1] = "Sales";  
        System.Data.DataTable table = connection.GetSchema(  
          "Tables", restrictions);  
  
        // Display the contents of the table.  
        foreach (System.Data.DataRow row in table.Rows)  
        {  
            foreach (System.Data.DataColumn col in table.Columns)  
            {  
                Console.WriteLine("{0} = {1}",   
                  col.ColumnName, row[col]);  
            }  
            Console.WriteLine("============================");  
        }  
        Console.WriteLine("Press any key to continue.");  
        Console.ReadKey();  
    }  
  }  
  
  private static string GetConnectionString()  
  {  
     // To avoid storing the connection string in your code,  
     // you can retrieve it from a configuration file.  
     return "Data Source=(local);Database=AdventureWorks;" +  
        "Integrated Security=true;";  
  }  
  
  private static void DisplayData(System.Data.DataTable table)  
  {  
     foreach (System.Data.DataRow row in table.Rows)  
     {  
        foreach (System.Data.DataColumn col in table.Columns)  
        {  
           Console.WriteLine("{0} = {1}", col.ColumnName, row[col]);  
        }  
     Console.WriteLine("============================");  
     }  
  }  
}  
```  
  
## <a name="sql-server-schema-restrictions"></a><span data-ttu-id="f5dae-136">SQL Server スキーマの制限</span><span class="sxs-lookup"><span data-stu-id="f5dae-136">SQL Server Schema Restrictions</span></span>  
 <span data-ttu-id="f5dae-137">次の表に、SQL Server スキーマ コレクションの制限を示します。</span><span class="sxs-lookup"><span data-stu-id="f5dae-137">The following tables list the restrictions for SQL Server schema collections.</span></span>  
  
### <a name="users"></a><span data-ttu-id="f5dae-138">Users</span><span class="sxs-lookup"><span data-stu-id="f5dae-138">Users</span></span>  
  
|<span data-ttu-id="f5dae-139">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-139">Restriction Name</span></span>|<span data-ttu-id="f5dae-140">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-140">Parameter Name</span></span>|<span data-ttu-id="f5dae-141">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-141">Restriction Default</span></span>|<span data-ttu-id="f5dae-142">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-142">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-143">User_Name</span><span class="sxs-lookup"><span data-stu-id="f5dae-143">User_Name</span></span>|@Name|<span data-ttu-id="f5dae-144">name</span><span class="sxs-lookup"><span data-stu-id="f5dae-144">name</span></span>|<span data-ttu-id="f5dae-145">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-145">1</span></span>|  
  
### <a name="databases"></a><span data-ttu-id="f5dae-146">Databases</span><span class="sxs-lookup"><span data-stu-id="f5dae-146">Databases</span></span>  
  
|<span data-ttu-id="f5dae-147">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-147">Restriction Name</span></span>|<span data-ttu-id="f5dae-148">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-148">Parameter Name</span></span>|<span data-ttu-id="f5dae-149">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-149">Restriction Default</span></span>|<span data-ttu-id="f5dae-150">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-150">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-151">名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-151">Name</span></span>|@Name|<span data-ttu-id="f5dae-152">名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-152">Name</span></span>|<span data-ttu-id="f5dae-153">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-153">1</span></span>|  
  
### <a name="tables"></a><span data-ttu-id="f5dae-154">[テーブル]</span><span class="sxs-lookup"><span data-stu-id="f5dae-154">Tables</span></span>  
  
|<span data-ttu-id="f5dae-155">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-155">Restriction Name</span></span>|<span data-ttu-id="f5dae-156">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-156">Parameter Name</span></span>|<span data-ttu-id="f5dae-157">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-157">Restriction Default</span></span>|<span data-ttu-id="f5dae-158">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-158">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-159">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-159">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-160">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-160">TABLE_CATALOG</span></span>|<span data-ttu-id="f5dae-161">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-161">1</span></span>|  
|<span data-ttu-id="f5dae-162">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-162">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-163">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-163">TABLE_SCHEMA</span></span>|<span data-ttu-id="f5dae-164">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-164">2</span></span>|  
|<span data-ttu-id="f5dae-165">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-165">Table</span></span>|@Name|<span data-ttu-id="f5dae-166">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-166">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-167">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-167">3</span></span>|  
|<span data-ttu-id="f5dae-168">TableType</span><span class="sxs-lookup"><span data-stu-id="f5dae-168">TableType</span></span>|@TableType|<span data-ttu-id="f5dae-169">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5dae-169">TABLE_TYPE</span></span>|<span data-ttu-id="f5dae-170">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-170">4</span></span>|  
  
### <a name="columns"></a><span data-ttu-id="f5dae-171">列</span><span class="sxs-lookup"><span data-stu-id="f5dae-171">Columns</span></span>  
  
|<span data-ttu-id="f5dae-172">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-172">Restriction Name</span></span>|<span data-ttu-id="f5dae-173">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-173">Parameter Name</span></span>|<span data-ttu-id="f5dae-174">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-174">Restriction Default</span></span>|<span data-ttu-id="f5dae-175">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-175">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-176">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-176">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-177">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-177">TABLE_CATALOG</span></span>|<span data-ttu-id="f5dae-178">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-178">1</span></span>|  
|<span data-ttu-id="f5dae-179">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-179">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-180">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-180">TABLE_SCHEMA</span></span>|<span data-ttu-id="f5dae-181">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-181">2</span></span>|  
|<span data-ttu-id="f5dae-182">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-182">Table</span></span>|@Table|<span data-ttu-id="f5dae-183">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-183">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-184">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-184">3</span></span>|  
|<span data-ttu-id="f5dae-185">Column</span><span class="sxs-lookup"><span data-stu-id="f5dae-185">Column</span></span>|@Column|<span data-ttu-id="f5dae-186">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-186">COLUMN_NAME</span></span>|<span data-ttu-id="f5dae-187">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-187">4</span></span>|  
  
### <a name="structuredtypemembers"></a><span data-ttu-id="f5dae-188">StructuredTypeMembers</span><span class="sxs-lookup"><span data-stu-id="f5dae-188">StructuredTypeMembers</span></span>  
  
|<span data-ttu-id="f5dae-189">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-189">Restriction Name</span></span>|<span data-ttu-id="f5dae-190">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-190">Parameter Name</span></span>|<span data-ttu-id="f5dae-191">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-191">Restriction Default</span></span>|<span data-ttu-id="f5dae-192">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-192">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-193">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-193">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-194">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-194">TABLE_CATALOG</span></span>|<span data-ttu-id="f5dae-195">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-195">1</span></span>|  
|<span data-ttu-id="f5dae-196">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-196">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-197">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-197">TABLE_SCHEMA</span></span>|<span data-ttu-id="f5dae-198">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-198">2</span></span>|  
|<span data-ttu-id="f5dae-199">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-199">Table</span></span>|@Table|<span data-ttu-id="f5dae-200">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-200">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-201">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-201">3</span></span>|  
|<span data-ttu-id="f5dae-202">Column</span><span class="sxs-lookup"><span data-stu-id="f5dae-202">Column</span></span>|@Column|<span data-ttu-id="f5dae-203">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-203">COLUMN_NAME</span></span>|<span data-ttu-id="f5dae-204">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-204">4</span></span>|  
  
### <a name="views"></a><span data-ttu-id="f5dae-205">ビュー</span><span class="sxs-lookup"><span data-stu-id="f5dae-205">Views</span></span>  
  
|<span data-ttu-id="f5dae-206">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-206">Restriction Name</span></span>|<span data-ttu-id="f5dae-207">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-207">Parameter Name</span></span>|<span data-ttu-id="f5dae-208">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-208">Restriction Default</span></span>|<span data-ttu-id="f5dae-209">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-209">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-210">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-210">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-211">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-211">TABLE_CATALOG</span></span>|<span data-ttu-id="f5dae-212">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-212">1</span></span>|  
|<span data-ttu-id="f5dae-213">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-213">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-214">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-214">TABLE_SCHEMA</span></span>|<span data-ttu-id="f5dae-215">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-215">2</span></span>|  
|<span data-ttu-id="f5dae-216">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-216">Table</span></span>|@Table|<span data-ttu-id="f5dae-217">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-217">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-218">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-218">3</span></span>|  
  
### <a name="viewcolumns"></a><span data-ttu-id="f5dae-219">ViewColumns</span><span class="sxs-lookup"><span data-stu-id="f5dae-219">ViewColumns</span></span>  
  
|<span data-ttu-id="f5dae-220">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-220">Restriction Name</span></span>|<span data-ttu-id="f5dae-221">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-221">Parameter Name</span></span>|<span data-ttu-id="f5dae-222">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-222">Restriction Default</span></span>|<span data-ttu-id="f5dae-223">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-223">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-224">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-224">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-225">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-225">VIEW_CATALOG</span></span>|<span data-ttu-id="f5dae-226">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-226">1</span></span>|  
|<span data-ttu-id="f5dae-227">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-227">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-228">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-228">VIEW_SCHEMA</span></span>|<span data-ttu-id="f5dae-229">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-229">2</span></span>|  
|<span data-ttu-id="f5dae-230">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-230">Table</span></span>|@Table|<span data-ttu-id="f5dae-231">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-231">VIEW_NAME</span></span>|<span data-ttu-id="f5dae-232">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-232">3</span></span>|  
|<span data-ttu-id="f5dae-233">Column</span><span class="sxs-lookup"><span data-stu-id="f5dae-233">Column</span></span>|@Column|<span data-ttu-id="f5dae-234">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-234">COLUMN_NAME</span></span>|<span data-ttu-id="f5dae-235">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-235">4</span></span>|  
  
### <a name="procedureparameters"></a><span data-ttu-id="f5dae-236">ProcedureParameters</span><span class="sxs-lookup"><span data-stu-id="f5dae-236">ProcedureParameters</span></span>  
  
|<span data-ttu-id="f5dae-237">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-237">Restriction Name</span></span>|<span data-ttu-id="f5dae-238">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-238">Parameter Name</span></span>|<span data-ttu-id="f5dae-239">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-239">Restriction Default</span></span>|<span data-ttu-id="f5dae-240">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-240">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-241">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-241">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-242">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-242">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="f5dae-243">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-243">1</span></span>|  
|<span data-ttu-id="f5dae-244">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-244">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-245">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-245">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="f5dae-246">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-246">2</span></span>|  
|<span data-ttu-id="f5dae-247">名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-247">Name</span></span>|@Name|<span data-ttu-id="f5dae-248">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-248">SPECIFIC_NAME</span></span>|<span data-ttu-id="f5dae-249">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-249">3</span></span>|  
|<span data-ttu-id="f5dae-250">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f5dae-250">Parameter</span></span>|@Parameter|<span data-ttu-id="f5dae-251">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-251">PARAMETER_NAME</span></span>|<span data-ttu-id="f5dae-252">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-252">4</span></span>|  
  
### <a name="procedures"></a><span data-ttu-id="f5dae-253">手順</span><span class="sxs-lookup"><span data-stu-id="f5dae-253">Procedures</span></span>  
  
|<span data-ttu-id="f5dae-254">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-254">Restriction Name</span></span>|<span data-ttu-id="f5dae-255">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-255">Parameter Name</span></span>|<span data-ttu-id="f5dae-256">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-256">Restriction Default</span></span>|<span data-ttu-id="f5dae-257">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-257">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-258">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-258">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-259">SPECIFIC_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-259">SPECIFIC_CATALOG</span></span>|<span data-ttu-id="f5dae-260">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-260">1</span></span>|  
|<span data-ttu-id="f5dae-261">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-261">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-262">SPECIFIC_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-262">SPECIFIC_SCHEMA</span></span>|<span data-ttu-id="f5dae-263">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-263">2</span></span>|  
|<span data-ttu-id="f5dae-264">名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-264">Name</span></span>|@Name|<span data-ttu-id="f5dae-265">SPECIFIC_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-265">SPECIFIC_NAME</span></span>|<span data-ttu-id="f5dae-266">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-266">3</span></span>|  
|<span data-ttu-id="f5dae-267">型</span><span class="sxs-lookup"><span data-stu-id="f5dae-267">Type</span></span>|@Type|<span data-ttu-id="f5dae-268">ROUTINE_TYPE</span><span class="sxs-lookup"><span data-stu-id="f5dae-268">ROUTINE_TYPE</span></span>|<span data-ttu-id="f5dae-269">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-269">4</span></span>|  
  
### <a name="indexcolumns"></a><span data-ttu-id="f5dae-270">IndexColumns</span><span class="sxs-lookup"><span data-stu-id="f5dae-270">IndexColumns</span></span>  
  
|<span data-ttu-id="f5dae-271">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-271">Restriction Name</span></span>|<span data-ttu-id="f5dae-272">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-272">Parameter Name</span></span>|<span data-ttu-id="f5dae-273">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-273">Restriction Default</span></span>|<span data-ttu-id="f5dae-274">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-274">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-275">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-275">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-276">db_name()</span><span class="sxs-lookup"><span data-stu-id="f5dae-276">db_name()</span></span>|<span data-ttu-id="f5dae-277">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-277">1</span></span>|  
|<span data-ttu-id="f5dae-278">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-278">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-279">user_name()</span><span class="sxs-lookup"><span data-stu-id="f5dae-279">user_name()</span></span>|<span data-ttu-id="f5dae-280">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-280">2</span></span>|  
|<span data-ttu-id="f5dae-281">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-281">Table</span></span>|@Table|<span data-ttu-id="f5dae-282">o.name</span><span class="sxs-lookup"><span data-stu-id="f5dae-282">o.name</span></span>|<span data-ttu-id="f5dae-283">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-283">3</span></span>|  
|<span data-ttu-id="f5dae-284">ConstraintName</span><span class="sxs-lookup"><span data-stu-id="f5dae-284">ConstraintName</span></span>|@ConstraintName|<span data-ttu-id="f5dae-285">x.name</span><span class="sxs-lookup"><span data-stu-id="f5dae-285">x.name</span></span>|<span data-ttu-id="f5dae-286">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-286">4</span></span>|  
|<span data-ttu-id="f5dae-287">Column</span><span class="sxs-lookup"><span data-stu-id="f5dae-287">Column</span></span>|@Column|<span data-ttu-id="f5dae-288">c.name</span><span class="sxs-lookup"><span data-stu-id="f5dae-288">c.name</span></span>|<span data-ttu-id="f5dae-289">5</span><span class="sxs-lookup"><span data-stu-id="f5dae-289">5</span></span>|  
  
### <a name="indexes"></a><span data-ttu-id="f5dae-290">Indexes</span><span class="sxs-lookup"><span data-stu-id="f5dae-290">Indexes</span></span>  
  
|<span data-ttu-id="f5dae-291">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-291">Restriction Name</span></span>|<span data-ttu-id="f5dae-292">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-292">Parameter Name</span></span>|<span data-ttu-id="f5dae-293">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-293">Restriction Default</span></span>|<span data-ttu-id="f5dae-294">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-294">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-295">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-295">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-296">db_name()</span><span class="sxs-lookup"><span data-stu-id="f5dae-296">db_name()</span></span>|<span data-ttu-id="f5dae-297">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-297">1</span></span>|  
|<span data-ttu-id="f5dae-298">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-298">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-299">user_name()</span><span class="sxs-lookup"><span data-stu-id="f5dae-299">user_name()</span></span>|<span data-ttu-id="f5dae-300">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-300">2</span></span>|  
|<span data-ttu-id="f5dae-301">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-301">Table</span></span>|@Table|<span data-ttu-id="f5dae-302">o.name</span><span class="sxs-lookup"><span data-stu-id="f5dae-302">o.name</span></span>|<span data-ttu-id="f5dae-303">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-303">3</span></span>|  
  
### <a name="userdefinedtypes"></a><span data-ttu-id="f5dae-304">UserDefinedTypes</span><span class="sxs-lookup"><span data-stu-id="f5dae-304">UserDefinedTypes</span></span>  
  
|<span data-ttu-id="f5dae-305">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-305">Restriction Name</span></span>|<span data-ttu-id="f5dae-306">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-306">Parameter Name</span></span>|<span data-ttu-id="f5dae-307">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-307">Restriction Default</span></span>|<span data-ttu-id="f5dae-308">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-308">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-309">assembly_name</span><span class="sxs-lookup"><span data-stu-id="f5dae-309">assembly_name</span></span>|@AssemblyName|<span data-ttu-id="f5dae-310">assemblies.name</span><span class="sxs-lookup"><span data-stu-id="f5dae-310">assemblies.name</span></span>|<span data-ttu-id="f5dae-311">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-311">1</span></span>|  
|<span data-ttu-id="f5dae-312">udt_name</span><span class="sxs-lookup"><span data-stu-id="f5dae-312">udt_name</span></span>|@UDTName|<span data-ttu-id="f5dae-313">types.assembly_class</span><span class="sxs-lookup"><span data-stu-id="f5dae-313">types.assembly_class</span></span>|<span data-ttu-id="f5dae-314">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-314">2</span></span>|  
  
### <a name="foreignkeys"></a><span data-ttu-id="f5dae-315">ForeignKeys</span><span class="sxs-lookup"><span data-stu-id="f5dae-315">ForeignKeys</span></span>  
  
|<span data-ttu-id="f5dae-316">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-316">Restriction Name</span></span>|<span data-ttu-id="f5dae-317">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-317">Parameter Name</span></span>|<span data-ttu-id="f5dae-318">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-318">Restriction Default</span></span>|<span data-ttu-id="f5dae-319">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-319">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-320">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-320">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-321">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-321">CONSTRAINT_CATALOG</span></span>|<span data-ttu-id="f5dae-322">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-322">1</span></span>|  
|<span data-ttu-id="f5dae-323">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-323">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-324">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-324">CONSTRAINT_SCHEMA</span></span>|<span data-ttu-id="f5dae-325">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-325">2</span></span>|  
|<span data-ttu-id="f5dae-326">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-326">Table</span></span>|@Table|<span data-ttu-id="f5dae-327">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-327">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-328">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-328">3</span></span>|  
|<span data-ttu-id="f5dae-329">名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-329">Name</span></span>|@Name|<span data-ttu-id="f5dae-330">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-330">CONSTRAINT_NAME</span></span>|<span data-ttu-id="f5dae-331">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-331">4</span></span>|  
  
## <a name="sql-server-2008-schema-restrictions"></a><span data-ttu-id="f5dae-332">SQL Server 2008 スキーマの制限</span><span class="sxs-lookup"><span data-stu-id="f5dae-332">SQL Server 2008 Schema Restrictions</span></span>  
 <span data-ttu-id="f5dae-333">次の表に、SQL Server 2008 スキーマ コレクションの制限を示します。</span><span class="sxs-lookup"><span data-stu-id="f5dae-333">The following tables list the restrictions for SQL Server 2008 schema collections.</span></span> <span data-ttu-id="f5dae-334">これらの制限は、.NET Framework 3.5 SP1 および SQL Server 2008 以降で有効です。</span><span class="sxs-lookup"><span data-stu-id="f5dae-334">These restrictions are valid beginning with version 3.5 SP1 of the .NET Framework and SQL Server 2008.</span></span> <span data-ttu-id="f5dae-335">これらの制限は、以前のバージョンの .NET Framework および SQL Server ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f5dae-335">They are not supported in earlier versions of the .NET Framework and SQL Server.</span></span>  
  
### <a name="columnsetcolumns"></a><span data-ttu-id="f5dae-336">ColumnSetColumns</span><span class="sxs-lookup"><span data-stu-id="f5dae-336">ColumnSetColumns</span></span>  
  
|<span data-ttu-id="f5dae-337">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-337">Restriction Name</span></span>|<span data-ttu-id="f5dae-338">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-338">Parameter Name</span></span>|<span data-ttu-id="f5dae-339">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-339">Restriction Default</span></span>|<span data-ttu-id="f5dae-340">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-340">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-341">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-341">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-342">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-342">TABLE_CATALOG</span></span>|<span data-ttu-id="f5dae-343">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-343">1</span></span>|  
|<span data-ttu-id="f5dae-344">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-344">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-345">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-345">TABLE_SCHEMA</span></span>|<span data-ttu-id="f5dae-346">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-346">2</span></span>|  
|<span data-ttu-id="f5dae-347">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-347">Table</span></span>|@Table|<span data-ttu-id="f5dae-348">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-348">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-349">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-349">3</span></span>|  
  
### <a name="allcolumns"></a><span data-ttu-id="f5dae-350">AllColumns</span><span class="sxs-lookup"><span data-stu-id="f5dae-350">AllColumns</span></span>  
  
|<span data-ttu-id="f5dae-351">制限の名前</span><span class="sxs-lookup"><span data-stu-id="f5dae-351">Restriction Name</span></span>|<span data-ttu-id="f5dae-352">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f5dae-352">Parameter Name</span></span>|<span data-ttu-id="f5dae-353">制限の既定値</span><span class="sxs-lookup"><span data-stu-id="f5dae-353">Restriction Default</span></span>|<span data-ttu-id="f5dae-354">制限の番号</span><span class="sxs-lookup"><span data-stu-id="f5dae-354">Restriction Number</span></span>|  
|----------------------|--------------------|-------------------------|------------------------|  
|<span data-ttu-id="f5dae-355">Catalog</span><span class="sxs-lookup"><span data-stu-id="f5dae-355">Catalog</span></span>|@Catalog|<span data-ttu-id="f5dae-356">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="f5dae-356">TABLE_CATALOG</span></span>|<span data-ttu-id="f5dae-357">1</span><span class="sxs-lookup"><span data-stu-id="f5dae-357">1</span></span>|  
|<span data-ttu-id="f5dae-358">Owner</span><span class="sxs-lookup"><span data-stu-id="f5dae-358">Owner</span></span>|@Owner|<span data-ttu-id="f5dae-359">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="f5dae-359">TABLE_SCHEMA</span></span>|<span data-ttu-id="f5dae-360">2</span><span class="sxs-lookup"><span data-stu-id="f5dae-360">2</span></span>|  
|<span data-ttu-id="f5dae-361">テーブル</span><span class="sxs-lookup"><span data-stu-id="f5dae-361">Table</span></span>|@Table|<span data-ttu-id="f5dae-362">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-362">TABLE_NAME</span></span>|<span data-ttu-id="f5dae-363">3</span><span class="sxs-lookup"><span data-stu-id="f5dae-363">3</span></span>|  
|<span data-ttu-id="f5dae-364">Column</span><span class="sxs-lookup"><span data-stu-id="f5dae-364">Column</span></span>|@Column|<span data-ttu-id="f5dae-365">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="f5dae-365">COLUMN_NAME</span></span>|<span data-ttu-id="f5dae-366">4</span><span class="sxs-lookup"><span data-stu-id="f5dae-366">4</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f5dae-367">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5dae-367">See Also</span></span>  
 [<span data-ttu-id="f5dae-368">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="f5dae-368">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
