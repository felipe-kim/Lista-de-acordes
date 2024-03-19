# Lista-de-acordes

Digite o título da música seguido pela letra:

- **Título da Música 1:**
  Letra da música 1.

- **Título da Música 2:**
  Letra da música 2.

<!-- Adicione mais músicas conforme necessário -->

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Caixa de Texto GitHub Pages</title>
</head>
<body>
    <h1>Caixa de Texto GitHub Pages</h1>
    
    <form id="songForm">
        <label for="songName">Digite o nome da música:</label><br>
        <input type="text" id="songName" name="songName"><br><br>
        <button type="submit">Adicionar Música</button>
    </form>

    <div id="musicList">
        <!-- Aqui será exibida a lista de músicas adicionadas -->
    </div>

    <script>
        document.getElementById("songForm").addEventListener("submit", function(event) {
            event.preventDefault(); // Impede o envio do formulário padrão
            
            // Obtém o valor do campo de texto
            var songName = document.getElementById("songName").value;
            
            // Limpa o campo de texto
            document.getElementById("songName").value = "";
            
            // Adiciona o nome da música à lista
            var musicList = document.getElementById("musicList");
            musicList.innerHTML += "<p>" + songName + "</p>";
        });
    </script>
</body>
</html>

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
