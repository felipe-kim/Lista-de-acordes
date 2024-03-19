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

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lista de Arquivos do Repositório</title>
</head>
<body>

<h1>Lista de Arquivos do Repositório</h1>

<ul id="fileList">
  <!-- Lista de arquivos será inserida aqui -->
</ul>

<script>
// Configurações
const username = 'felipe-kim';
const repository = 'Lista-de-acordes';

// URL da API do GitHub para obter a lista de arquivos
const apiUrl = `https://api.github.com/repos/${username}/${repository}/contents`;

// Função para buscar a lista de arquivos
async function fetchFiles() {
  try {
    const response = await fetch(apiUrl);
    const data = await response.json();
    
    // Limpar a lista de arquivos
    const fileList = document.getElementById('fileList');
    fileList.innerHTML = '';
    
    // Adicionar cada arquivo à lista
    data.forEach(file => {
      const listItem = document.createElement('li');
      const link = document.createElement('a');
      link.textContent = file.name;
      link.href = file.html_url;
      listItem.appendChild(link);
      fileList.appendChild(listItem);
    });
  } catch (error) {
    console.error('Erro ao buscar a lista de arquivos:', error);
  }
}

// Chamar a função para buscar a lista de arquivos quando a página carregar
fetchFiles();
</script>

</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lista de Arquivos do Repositório</title>
</head>
<body>

<h1>Lista de Arquivos do Repositório</h1>

<ul id="fileList">
  <!-- Lista de arquivos será inserida aqui -->
</ul>

<script>
// Configurações
const username = 'seu_nome_de_usuário';
const repository = 'seu_repositório';

// URL base do GitHub para visualização do arquivo
const githubUrl = `https://github.com/${username}/${repository}/blob/main/`;

// Função para buscar a lista de arquivos
async function fetchFiles() {
  try {
    const response = await fetch(`https://api.github.com/repos/${username}/${repository}/contents`);
    const data = await response.json();
    
    // Limpar a lista de arquivos
    const fileList = document.getElementById('fileList');
    fileList.innerHTML = '';
    
    // Adicionar cada arquivo à lista
    data.forEach(file => {
      const listItem = document.createElement('li');
      const link = document.createElement('a');
      link.textContent = file.name;
      link.href = githubUrl + file.path; // URL completa do arquivo
      listItem.appendChild(link);
      fileList.appendChild(listItem);
    });
  } catch (error) {
    console.error('Erro ao buscar a lista de arquivos:', error);
  }
}

// Chamar a função para buscar a lista de arquivos quando a página carregar
fetchFiles();
</script>

</body>
</html>
