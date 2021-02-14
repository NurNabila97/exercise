<!DOCTYPE html> 
<htmI lang = “en”>
<head> 
<meta charset="UTF-8"> 
<title> Flight Detail </title>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.css"> 
<style type="text/css"> 
. wrapper{ 
width: 500px; 
margin: auto;} 
body, html { 
height : 100%; 
font-family: Arial, Helvetica, sans-serif; 
background-image: 
min-height : 700px; 
background-position: center; 
background - repeat : no- repeat; 
background -size : cover; 
position : relative; 
table tr td{ 
border: solid 1px #eee; 
padding: 10px; }
</style> 
< body>
<div class = "wrapper" > 
<div class =" container-fluid" > 
<div class = " row" > 
<div class = "col-md-12"> 
<div class "page-header"> 
<h2> Flight Detail </h2>
</div> 
<form role= “form” onsubmit= "signup (event);" > 
<div class =“form-group" > 
< label for =“id”> Flight ID: </label>
<input type= "number" class=“form-control” name=“id” id=“id”>
</div> 
<div class =“form-group" > 
< label for = "name" > Flight Name: </label>
<select name="name" input type= "text" class=“form-control" name=“name” id=“name”>

<div class =“form-group" > 
< label for = "pri" > Price: </label>
<input type= "double" class=“form-control" name=“pri” id=“pri”> </div>

<div class =“form-group" > 
< label for = "ddate" > Date: </label>
<input type= "date" class=“form-control" name=“ddate” id=“ddate”> </div>

<div class =“form-group" > 
< label for = "dura" > Duration: </label>
<input type= "time" class=“form-control" name=“dura” id=“dura”></div>

<div class =“input-group" > 
< button type=“submit”> Submit </button>
</div><br>

<h2> my info </h2>
<div id=“output”>
</div> </div>

<script type="text/javascript"> 
const signUp = e => { 
let formData={ 
id : document. getElementById ( ‘id’) . value, 
name : document. getElementById ( ‘name ' ) . value, 
pri : document. getElementById ( ' pri ' ) value, 
ddate : document. getElementById( ‘ddate ' ) . value, 
dura : document. getElementById( ‘dura ' ) . value }
localStorage.setltem( formData , JSON. stringify(formData) ) ; 

dispData() ; 
e. preventDefault( ) ; 

function dispData(){ 

let{id, name, pri, ddate, dura} = 
JSON.parse(localStorage.getItem('formData')); 
var output = document.getElementById( 'output' ) ; 
output. innerHTML = ‘
<table> 
<tbody>
<tr> 
<td>F1ight ID</td> 
<td>${id}</td> 
</tr> 
<tr> 
<td>F1ight Name</td> 
<td>${name}</td> 
</tr> 
<tr>
<td>Price 
<td>${pri}</td> 
</tr>
<tr>
<td>Date</td> 
<td>${ddate)</td> 
</tr>
<tr> 
<td>Duration</td> 
<td>${dura)</td> 
</tr> 
</tbody> 
</table>’;}
</script> 
<br><a href="flight. html" class="btn btn-default"> Logout </a> 
</form> 
</div> 
</div> 
</div>
</div>
</body>
</html>
