# htmlcss
Calculator

<html>
	<head>
		<title>Simple Calculator</title>
		<style>
				#calc-contain{
				position: relative;
				width: 300px;
				border: 2px solid black;
				border-radius: 4px;
				background: #FFFFFF;
				margin-top: 10px;
			}
				input[type=button]{
			background: #FFFFFF;
			width: 20%;
			font-size: 20px;
			font-weight: 900;
			margin: 2%;
			border-radius: 4px;
		}
				input[type=text]{
			position: relative;
			display: block;
			border-radius: 4px;
			width: 95%;
			height: 80px;
			margin: 15px auto;
			font-size: 30px;
			background: #FFFFFF;
			color: #000000;
			margin-right: auto;
		}
			</style>
				<script text='text/javascript'>
					var i = 0;
					function brackets(){
							if(i == 0){
								calculator.display.value += '(';
								i = 1;	
							}
							else if(i == 1){
								calculator.display.value += ')';
								i = 0;
							}
					}
					function backspace(){
						var x = calculator.display.value; 
						if(x.length > 0){
							x = x.substring(0, x.length-1); 
							calculator.display.value = x;
						}
					}
				</script>
	</head>
	<body>
		<center>
			<div id="calc-contain">
				<form name="calculator">
					<input type="text" name="display"/>
					<br/>
					<input type="button" value=" C " onclick="calculator.display.value =''"/>
					<input type="button" value=" +/- " onclick="calculator.display.value +='-' + (calculator.display.value)" style = "background: #CCCCCC"/>
					<input type="button" value=" % " onclick="calculator.display.value +='%'" style = "background: #CCCCCC"/>
					<input type="button" value=" / " onclick="calculator.display.value +='/'" style = "background: #333333; color: #FFFFFF;"/>
					
					<br/>
					<input type="button" value=" 7 " onclick="calculator.display.value +='7'"/>
					<input type="button" value=" 8 " onclick="calculator.display.value +='8'"/>
					<input type="button" value=" 9 " onclick="calculator.display.value +='9'"/>
					<input type="button" value=" X" onclick="calculator.display.value +='*'" style = "background: #333333; color: #FFFFFF;"/>
					<br/>
					<input type="button" value=" 4 " onclick="calculator.display.value +='4'"/>
					<input type="button" value=" 5 " onclick="calculator.display.value +='5'"/>
					<input type="button" value=" 6 " onclick="calculator.display.value +='6'"/>
					<input type="button" value=" - " onclick="calculator.display.value +='-'" style = "background: #333333; color: #FFFFFF;"/>
					<br/>
					<input type="button" value=" 1 " onclick="calculator.display.value +='1'"/>
					<input type="button" value=" 2 " onclick="calculator.display.value +='2'"/>
					<input type="button" value=" 3 " onclick="calculator.display.value +='3'"/>
					<input type="button" value=" + " onclick="calculator.display.value +='+'" style = "background: #333333; color: #FFFFFF;"/>
					
					<br/>
					
					<input type="button" value=" 0 " onclick="calculator.display.value +='0'"/>
					<input type="button" value=" &#8592 " onclick="backspace()"/>
					<input type="button" value=" . " onclick="calculator.display.value +='.'" style = "background: #FFFFFF"/><input type="button" value=" = " onclick="calculator.display.value = eval(calculator.display.value)" style = "background: #FFA500; width: 22%;"/>	
					
					<br/>
				</form>
			</div>
		</center>	
		<p>&nbsp;</p>
	</body>	
</html>
