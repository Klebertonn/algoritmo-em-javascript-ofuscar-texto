# algoritmo-em-javascript-ofuscar-texto
Protejo em html css e javascript com a função replace, faz o ofuscamento das mensagens substituindo as strings, e com o campo de retornar o valor original.
<!DOCTYPE html>
<head>
	<title> Front-end</title>
	<meta charset="utf-8">
	<!-- inicio do css-->
	<style>
		body{
			background-color:#151515;
		}
		h1{
			color:white;
		}
	    textarea{
	    	text-decoration-line:blue;
		}
		button{
			color:white;
			background-color:black;
		}

	</style>
	<!--termino do css-->
</head>
<html>
<body>
	<!--inicio da sessão de html e botões-->
   <h1>Texto Ofuscado</h1>
   <textarea id="texto"></textarea>
   <textarea id="texto2"></textarea>
   <button id="btn1" onclick=" Ofuscar()">Ofuscar</button>
   <button id="btn2" onclick="Desofuscar()">Desofuscar</button>
   <!-- termino dos campos html-->
   <!--inicio dos comandos script com o metodo replace-->
<script>
function Ofuscar() {
  var str = document.getElementById("texto").value; 
   str = str.replace(/i/gi, "inis");
   str = str.replace(/e/gi, "enter");
   str = str.replace(/o/gi, "omber");
   str = str.replace(/u/gi, "ufter");
   str = str.replace(/a/gi, "ais");
  document.getElementById("texto2").value = str;
}
//sessão para desofuscar os textos//
function Desofuscar(){
	var str = document.getElementById("texto").value; 
   str = str.replace(/ais/gi, "a");
   str = str.replace(/enter/gi, "e");
   str = str.replace(/inis/gi, "i");
   str = str.replace(/omber/gi, "o");
   str = str.replace(/ufter/gi, "u");
  document.getElementById("texto2").value = str;
}
</script>
<!--fim do algoritmo script-->
</body>
</html>
