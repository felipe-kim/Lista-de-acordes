# Lista-de-acordes

Digite o título da música seguido pela letra:

- **Título da Música 1:**
  Letra da música 1.

- **Título da Música 2:**
  Letra da música 2.

<!-- Adicione mais músicas conforme necessário -->

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Open File on GitHub Pages</title>
</head>
<body>

<label for="fileInput">Digite o nome do arquivo:</label>
<input type="text" id="fileInput">
<button onclick="openFile()">Abrir Arquivo</button>

<script>
function openFile() {
  var fileName = document.getElementById("fileInput").value;
  // Redirecionar para o arquivo especificado
  window.location.href = fileName;
}
</script>

</body>
</html>
