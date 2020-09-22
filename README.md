<div align="center">

## Mysql


</div>

### Description

use mysql
 
### More Info
 
database info; datase query

use mysql database, this code is self explanatory

database query


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[apdanan](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/apdanan.md)
**Level**          |Intermediate
**User Rating**    |4.0 (16 globes from 4 users)
**Compatibility**  |VB\.NET
**Category**       |[Databases](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/databases__10-5.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/apdanan-mysql__10-2565/archive/master.zip)

### API Declarations

www.apdanan.com


### Source Code

```
''you must install odbc mysql 3.51 and odbc .net data provider
''1. create new windows application project
''2. add datagrid
''3. add private declaration after "Windows Form Designer generated code" region
Dim constring As String = "DRIVER={MySQL ODBC 3.51 Driver};SERVER=host;DATABASE=database;UID=username;PASSWORD=password;OPTION=3;"
''4. creat procedure...
Private Sub refreshdb()
    Dim mdata As New DataSet
    Dim mcmd As Odbc.OdbcDataAdapter = New Odbc.OdbcDataAdapter("SELECT * FROM table1", constring)
    mcmd.Fill(mdata, "apdset")
    Me.DataGrid1.DataSource = mdata
End Sub
''5. on form load event add the procedure
 Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load
    refreshdb()
  End Sub
'' hope it helps :)
```

