# exceltocoverttable
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Table export excel</title>
        <!-- CSS only -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi" crossorigin="anonymous">
<!-- JavaScript Bundle with Popper -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-OERcA2EqjJCMA+/3y+gxIOqMEjwtxJY7qPCqsdltbNJuaOe923+mo//f6V8Qbsw3" crossorigin="anonymous"></script>
<script type="text/javascript" src="https://unpkg.com/xlsx@0.15.1/dist/xlsx.full.min.js"></script>
</head>
<style>
.table1{
    box-sizing: 200px;
    margin-left: 100px;
    margin-right: 500px;
    margin-top: 50px;
    border: 1px solid black;
}
h2{
    margin-left: 20px;
    margin-top: 50px;
}
#demo-ex{
    margin-left: 100px;
    margin-top: 50px;

}
button{
    margin-top: 10px;
    margin-left: 100px;
}

</style>

<body>
    <h2> Emp-detail</h2>
<div class="table1">
    
    <table class="table" id="example-table">
        <thead>
          <tr>
            <th scope="col">#</th>
            <th scope="col">First</th>
            <th scope="col">Last</th>
            <th scope="col">Address</th>
            <th scope="col">Email</th>
          </tr>
        </thead>
        <tbody class="table-group-divider">
          <tr>
            <th scope="row">1</th>
            <td>sathish</td>
            <td>M</td>
            <td>5/425,rayakotai</td>
            <td>srssathish555@gmail.com</td>
          </tr>
          <tr>
            <th scope="row">2</th>
            <td>Main</td>
            <td>v</td>
            <td>5/6754,selam</td>
            <td> mani555@gmail.com</td>
          </tr>
          <tr>
            <th scope="row">3</th>
            <td >kalai</td>
            <td>B</td>
            <td>7/587,selam</td>
            <td> kalai87976745454@gmail.com</td>
          </tr>
          <tr>
            <th scope="row">4</th>
            <td >goutham</td>
            <td>B</td>
            <td>1/875,selam-0007</td>
            <td> gowtham5502@gmail.com</td>
          </tr>
        </tbody>
      </table>

</div>
<button onclick="ExportToExcel('xlsx')">Export table to excel</button>

    
<script>
 
    function ExportToExcel(type, fn, dl) {
        var elt = document.getElementById('example-table');
        var wb = XLSX.utils.table_to_book(elt, { sheet: "sheet1" });
        return dl ?
            XLSX.write(wb, { bookType: type, bookSST: true, type: 'base64' }) :
            XLSX.writeFile(wb, fn || ('MySheetName.' + (type || 'xlsx')));
    }
   
   
</script>
</body>
</html>



