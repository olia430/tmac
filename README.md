
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title>计算器</title>
		<meta name="viewport" content="width=device-width, initial-scale=1" charset="utf-8">
		<style >
			*{margin: 0px;}
			#calculator{text-align: center; width: 440px;height: 410px;background-color: aqua;margin: 150px auto;}
		    #show{width: 410px;height: 70px;}
			.button{width: 100px;height: 45px;background-color: bisque;}
			.number{width: 100px;height: 45px;background-color: chartreuse;}
			.fu{width: 100px;height: 45px;background-color: brown;}
			.jieguo{width: 100px;height: 45px;background-color: darkblue;}
		</style>
	</head>
	    <script>
			function add(obj){
				document.getElementById("show").value+= obj.value;
			}
			function results(){
				var obj=document.getElementById("show").value;
					if(obj.indexOf("=")<0){
					document.getElementById("show").value +="="+ eval(obj);
			}
			}
			function clears(){
				document.getElementById("show").value="";
			}
			function backspace(){
				var del = document.getElementById("show");
				del.value= del.value.substring(0,del.value.length-1);
			}
		</script>
	<body>
		<table id="calculator">
			<tr>
				<td colspan="4"><input type="text" readonly="true" id="show"></td>
			</tr>
			<tr>
				<td><input type="button" value="(" class="button" onclick="add(this)"></td>
				<td><input type="button" value=")" class="button" onclick="add(this)"></td>
				<td><input type="button" value="清零" class="button" onclick="clears()"></td>
				<td><input type="button" value="退格" class="button" onclick="backspace()"></td>
			</tr>
			<tr>
				<td><input type="button" value="7" class="number" onclick="add(this)"></td>
				<td><input type="button" value="8" class="number" onclick="add(this)"></td>
				<td><input type="button" value="9" class="number" onclick="add(this)"></td>
				<td><input type="button" value="+" class="fu" onclick="add(this)"></td>
			</tr>
			<tr>
				<td><input type="button" value="4" class="number" onclick="add(this)"></td>
				<td><input type="button" value="5" class="number" onclick="add(this)"></td>
				<td><input type="button" value="6" class="number" onclick="add(this)"></td>
				<td><input type="button" value="-" class="fu" onclick="add(this)"></td>
			</tr>
			<tr>
				<td><input type="button" value="1" class="number" onclick="add(this)"></td>
				<td><input type="button" value="2" class="number" onclick="add(this)"></td>
				<td><input type="button" value="3" class="number" onclick="add(this)"></td>
				<td><input type="button" value="*" class="fu" onclick="add(this)"></td>
			</tr>
			<tr>
				<td><input type="button" value="0" class="number" onclick="add(this)"></td>
				<td><input type="button" value="." class="button" onclick="add(this)"></td>
				<td><input type="button" value="=" class="jieguo" onclick="results()"></td>
				<td><input type="button" value="/" class="fu" onclick="add(this)"></td>
			</tr>
			
			
		</table>
		
	</body>
</html>
