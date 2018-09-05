---
title: OracleDataReader の REF CURSOR パラメーター
ms.date: 03/30/2017
dev_langs:
- vb
ms.assetid: 801dff0f-2508-45aa-9416-f45d6887740c
ms.openlocfilehash: 3a2c8949537c749ba30b116a0dc8131336de6092
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2018
ms.locfileid: "43671583"
---
# <a name="ref-cursor-parameters-in-an-oracledatareader"></a><span data-ttu-id="03e27-102">OracleDataReader の REF CURSOR パラメーター</span><span class="sxs-lookup"><span data-stu-id="03e27-102">REF CURSOR Parameters in an OracleDataReader</span></span>
<span data-ttu-id="03e27-103">この Microsoft Visual Basic の例では、REF CURSOR パラメーターを返し、<xref:System.Data.OracleClient.OracleDataReader> を使用して値を読み取る、PL/SQL ストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="03e27-103">This Microsoft Visual Basic example executes a PL/SQL stored procedure that returns a REF CURSOR parameter, and reads the value as an <xref:System.Data.OracleClient.OracleDataReader>.</span></span>  
  
```vb  
Private Sub Button1_Click(ByVal sender As Object, _  
  ByVal e As System.EventArgs) Handles Button1.Click  
  
  Dim connString As New String(_  
      "Data Source=Oracle9i;User ID=scott;Password=tiger;")  
  Using conn As New OracleConnection(connString)  
    Dim cmd As New OracleCommand()  
    Dim rdr As OracleDataReader  
  
    conn.Open()  
    cmd.Connection = conn  
    cmd.CommandText = "CURSPKG.OPEN_ONE_CURSOR"  
    cmd.CommandType = CommandType.StoredProcedure  
    cmd.Parameters.Add(New OracleParameter(  
      "N_EMPNO", OracleType.Number)).Value = 7369  
    cmd.Parameters.Add(New OracleParameter(  
      "IO_CURSOR", OracleType.Cursor)).Direction = ParameterDirection.Output  
  
    rdr = cmd.ExecuteReader()  
    While (rdr.Read())  
        REM do something with the values  
    End While  
  
    rdr.Close()  
  End Using  
End Sub  
```  
  
## <a name="see-also"></a><span data-ttu-id="03e27-104">関連項目</span><span class="sxs-lookup"><span data-stu-id="03e27-104">See Also</span></span>  
 [<span data-ttu-id="03e27-105">Oracle REF CURSOR</span><span class="sxs-lookup"><span data-stu-id="03e27-105">Oracle REF CURSORs</span></span>](../../../../docs/framework/data/adonet/oracle-ref-cursors.md)  
 [<span data-ttu-id="03e27-106">ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="03e27-106">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
