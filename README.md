<!DOCTYPE html>
<html>
<style>
.header {
  background-color: #f54336;
  padding: 30px 40px;
  color: white;
  text-align: center;
}
input {
  margin: 0;
  border: none;
  border-radius: 0;
  width: 75%;
  padding: 10px;
  float: left;
  font-size: 16px;
}
buttom{
  padding: 10px;
  width: 25%;
  background: #d9d9d9;
  color: #555;
  float: left;
  text-align: center;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
  border-radius: 0;
}
buttom:hover {
  background-color: #bbb;
}
ul li:nth-child(odd) {
  background: #f9f9f9;
}
ul li:hover {
  background: #ddd;
}
</style>
<script>


var array = [];


function printList() {
	var string = '';
	
	for(element of array) {
		string += '<li>' + element.date + '  ' + element.message + '</li>';
	}
	
	console.log('LIST RESULT= ', string);
	document.querySelector('ul').innerHTML = string;
}

function saveMessage() {
	var value = document.querySelector('#mi-input').value;
	var date = new Date();
	
	
	var obj = {
		message: value,
		date: date
	};
	
	
	array.push(obj);
	
	
	
	console.log('*****', value);
	console.log('*****', array);
	
	printList();
}
</script>
<body>


<div id="myDIV" class="header">
  <h2 style="margin:5px">My To Do List</h2>
<input id="mi-input" type="text" placeholder="introduce un mensaje">
<button onclick="saveMessage()">
	Guardar
</button>
</div>

<ul>
</ul>

</body>
</html>
