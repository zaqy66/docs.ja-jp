---
title: Load メソッド
ms.date: 03/30/2017
dev_langs:
- vb
ms.assetid: e22e5812-89c6-41f0-9302-bb899a46dbff
ms.openlocfilehash: 06666e069f20bc06f303c4e829d1c69c185a8a84
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602482"
---
# <a name="the-load-method"></a><span data-ttu-id="925d5-102">Load メソッド</span><span class="sxs-lookup"><span data-stu-id="925d5-102">The Load Method</span></span>
<span data-ttu-id="925d5-103"><xref:System.Data.DataTable.Load%2A> メソッドを使用して、データ ソースの行を <xref:System.Data.DataTable> に読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="925d5-103">You can use the <xref:System.Data.DataTable.Load%2A> method to load a <xref:System.Data.DataTable> with rows from a data source.</span></span> <span data-ttu-id="925d5-104">これは最も単純な形式では、1 つのパラメーターを受け取っているオーバー ロードされたメソッド、 **DataReader**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-104">This is an overloaded method which, in its simplest form, accepts a single parameter, a **DataReader**.</span></span> <span data-ttu-id="925d5-105">このフォームで、単に読み込む、 **DataTable**行。</span><span class="sxs-lookup"><span data-stu-id="925d5-105">In this form, it simply loads the **DataTable** with rows.</span></span> <span data-ttu-id="925d5-106">必要に応じて、指定、 **LoadOption**にデータを追加する方法を制御するパラメーター、 **DataTable**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-106">Optionally, you can specify the **LoadOption** parameter to control how data is added to the **DataTable**.</span></span>  
  
 <span data-ttu-id="925d5-107">**LoadOption**パラメーターの場合に特に便利ですが、 **DataTable**既にデータの行を含む、データと組み合わせて、データ ソースからデータを受信する方法を記述できるため、テーブルの既存の。</span><span class="sxs-lookup"><span data-stu-id="925d5-107">The **LoadOption** parameter is particularly useful in cases where the **DataTable** already contains rows of data, because it describes how incoming data from the data source will be combined with the data already in the table.</span></span> <span data-ttu-id="925d5-108">たとえば、 **PreserveCurrentValues** (既定値) を指定する場合は、行がマークが**Added**で、 **DataTable**、**元**値列または列の各データ ソースから一致する行の内容に設定されています。</span><span class="sxs-lookup"><span data-stu-id="925d5-108">For example, **PreserveCurrentValues** (the default) specifies that in cases where a row is marked as **Added** in the **DataTable**, the **Original** value or each column is set to the contents of the matching row from the data source.</span></span> <span data-ttu-id="925d5-109">**現在**値は、行が追加されたときに割り当てられた値を保持し、 **RowState**の行に設定されます**Changed**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-109">The **Current** value will retain the values assigned when the row was added, and the **RowState** of the row will be set to **Changed**.</span></span>  
  
 <span data-ttu-id="925d5-110"><xref:System.Data.LoadOption> 列挙値の簡単な説明を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="925d5-110">The following table gives a short description of the <xref:System.Data.LoadOption> enumeration values.</span></span>  
  
|<span data-ttu-id="925d5-111">LoadOption の値</span><span class="sxs-lookup"><span data-stu-id="925d5-111">LoadOption value</span></span>|<span data-ttu-id="925d5-112">説明</span><span class="sxs-lookup"><span data-stu-id="925d5-112">Description</span></span>|  
|----------------------|-----------------|  
|<span data-ttu-id="925d5-113">**OverwriteRow**</span><span class="sxs-lookup"><span data-stu-id="925d5-113">**OverwriteRow**</span></span>|<span data-ttu-id="925d5-114">受信した行が同じである場合**PrimaryKey**として既に存在する行の値、 **DataTable**、**元**と**現在**それぞれの値列は、受信した行の値に置き換え、 **RowState**プロパティに設定されて**Unchanged**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-114">If incoming rows have the same **PrimaryKey** value as a row already in the **DataTable**, the **Original** and **Current** values of each column are replaced with the values in the incoming row, and the **RowState** property is set to **Unchanged**.</span></span><br /><br /> <span data-ttu-id="925d5-115">行に既に存在しないデータ ソースから、 **DataTable**を使用して追加、 **RowState** @property **Unchanged**。</span><span class="sxs-lookup"><span data-stu-id="925d5-115">Rows from the data source that do not already exist in the **DataTable** are added with a **RowState** value of **Unchanged**.</span></span><br /><br /> <span data-ttu-id="925d5-116">このオプションが有効の内容を更新、 **DataTable**データ ソースの内容と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="925d5-116">This option in effect refreshes the contents of the **DataTable** so that it matches the contents of the data source.</span></span>|  
|<span data-ttu-id="925d5-117">**PreserveCurrentValues (既定値)**</span><span class="sxs-lookup"><span data-stu-id="925d5-117">**PreserveCurrentValues (default)**</span></span>|<span data-ttu-id="925d5-118">受信した行が同じである場合**PrimaryKey**として既に存在する行の値、 **DataTable**、**元**値は、受信した行、および、の内容に設定されて**現在**値は変更されません。</span><span class="sxs-lookup"><span data-stu-id="925d5-118">If incoming rows have the same **PrimaryKey** value as a row already in the **DataTable**, the **Original** value is set to the contents of the incoming row, and the **Current** value is not changed.</span></span><br /><br /> <span data-ttu-id="925d5-119">場合、 **RowState**は**Added**または**Modified**に設定されている**Modified**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-119">If the **RowState** is **Added** or **Modified**, it is set to **Modified**.</span></span><br /><br /> <span data-ttu-id="925d5-120">場合、 **RowState**が**Deleted**、まま**Deleted**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-120">If the **RowState** was **Deleted**, it remains **Deleted**.</span></span><br /><br /> <span data-ttu-id="925d5-121">行に既に存在しないデータ ソースから、 **DataTable**が追加されると、 **RowState**に設定されている**Unchanged**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-121">Rows from the data source that do not already exist in the **DataTable** are added, and the **RowState** is set to **Unchanged**.</span></span>|  
|<span data-ttu-id="925d5-122">**UpdateCurrentValues**</span><span class="sxs-lookup"><span data-stu-id="925d5-122">**UpdateCurrentValues**</span></span>|<span data-ttu-id="925d5-123">受信した行が同じである場合**PrimaryKey**として既に存在する行の値、 **DataTable**、**現在**値をコピー、**元**値、および**現在**値は、受信した行の内容に設定されます。</span><span class="sxs-lookup"><span data-stu-id="925d5-123">If incoming rows have the same **PrimaryKey** value as the row already in the **DataTable**, the **Current** value is copied to the **Original** value, and the **Current** value is then set to the contents of the incoming row.</span></span><br /><br /> <span data-ttu-id="925d5-124">場合、 **RowState**で、 **DataTable**が**Added**、 **RowState**まま**Added**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-124">If the **RowState** in the **DataTable** was **Added**, the **RowState** remains **Added**.</span></span> <span data-ttu-id="925d5-125">としてマークされた行**Modified**または**Deleted**、 **RowState**は**Modified**します。</span><span class="sxs-lookup"><span data-stu-id="925d5-125">For rows marked as **Modified** or **Deleted**, the **RowState** is **Modified**.</span></span><br /><br /> <span data-ttu-id="925d5-126">行に既に存在しないデータ ソースから、 **DataTable**が追加されると、 **RowState**に設定されている**Added**。</span><span class="sxs-lookup"><span data-stu-id="925d5-126">Rows from the data source that do not already exist in the **DataTable** are added, and the **RowState** is set to **Added**.</span></span>|  
  
 <span data-ttu-id="925d5-127">次のサンプルは、**ロード**に従業員の誕生日の一覧を表示するメソッド、 **Northwind**データベース。</span><span class="sxs-lookup"><span data-stu-id="925d5-127">The following sample uses the **Load** method to display a list of birthdays for the employees in the **Northwind** database.</span></span>  
  
```vb  
Private Sub LoadBirthdays(ByVal connectionString As String)  
    ' Assumes that connectionString is a valid connection string  
    ' to the Northwind database on SQL Server.  
    Dim queryString As String = _  
    "SELECT LastName, FirstName, BirthDate " & _  
      " FROM dbo.Employees " & _  
      "ORDER BY BirthDate, LastName, FirstName"  
  
    ' Open and fill a DataSet.   
    Dim adapter As SqlDataAdapter = New SqlDataAdapter( _  
        queryString, connectionString)  
    Dim employees As New DataSet  
    adapter.Fill(employees, "Employees")  
  
    ' Create a SqlDataReader for use with the Load Method.  
    Dim reader As DataTableReader = employees.GetDataReader()  
  
    ' Create an instance of DataTable and assign the first  
    ' DataTable in the DataSet.Tables collection to it.  
    Dim dataTableEmp As DataTable = employees.Tables(0)  
  
    ' Fill the DataTable with data by calling Load and  
    ' passing the SqlDataReader.  
    dataTableEmp.Load(reader, LoadOption.OverwriteRow)  
  
    ' Loop through the rows collection and display the values  
    ' in the console window.  
    Dim employeeRow As DataRow  
    For Each employeeRow In dataTableEmp.Rows  
        Console.WriteLine("{0:MM\\dd\\yyyy}" & ControlChars.Tab & _  
          "{1}, {2}", _  
          employeeRow("BirthDate"), _  
          employeeRow("LastName"), _  
          employeeRow("FirstName"))  
    Next employeeRow  
  
    ' Keep the window opened to view the contents.  
    Console.ReadLine()  
End Sub  
```  
  
## <a name="see-also"></a><span data-ttu-id="925d5-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="925d5-128">See also</span></span>
- [<span data-ttu-id="925d5-129">DataTable 内のデータの操作</span><span class="sxs-lookup"><span data-stu-id="925d5-129">Manipulating Data in a DataTable</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)
- [<span data-ttu-id="925d5-130">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="925d5-130">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
