$$$$$$$$\ $$$$$$$\   $$$$$$\  $$\   $$\ $$$$$$$$\      $$$$$$$$\ $$\   $$\ $$$$$$$\  
$$  _____|$$  __$$\ $$  __$$\ $$$\  $$ |\__$$  __|     $$  _____|$$$\  $$ |$$  __$$\ 
$$ |      $$ |  $$ |$$ /  $$ |$$$$\ $$ |   $$ |        $$ |      $$$$\ $$ |$$ |  $$ |
$$$$$\    $$$$$$$  |$$ |  $$ |$$ $$\$$ |   $$ |$$$$$$\ $$$$$\    $$ $$\$$ |$$ |  $$ |
$$  __|   $$  __$$< $$ |  $$ |$$ \$$$$ |   $$ |\______|$$  __|   $$ \$$$$ |$$ |  $$ |
$$ |      $$ |  $$ |$$ |  $$ |$$ |\$$$ |   $$ |        $$ |      $$ |\$$$ |$$ |  $$ |
$$ |      $$ |  $$ | $$$$$$  |$$ | \$$ |   $$ |        $$$$$$$$\ $$ | \$$ |$$$$$$$  |
\__|      \__|  \__| \______/ \__|  \__|   \__|        \________|\__|  \__|\_______/ 
                                                                                     
                                                                                                                                                                   

# Front-End de Loja Virtual (Consumindo API PHP)

Este é um projeto front-end simples de e-commerce, construído com HTML, CSS e JavaScript puros. Ele foi projetado para consumir uma API de backend (feita em PHP) para listar produtos, filtrar por categorias e exibir detalhes de produtos individuais.

## ✨ Funcionalidades Principais

* **Listagem Completa (`index.html`):** A página principal exibe todos os produtos disponíveis na API.
* **Menu de Categorias:** Navegação simples que permite ao usuário filtrar produtos por categoria.
* **Página de Categoria (`categoria.html`):** Exibe produtos filtrados com base na categoria passada pela URL (ex: `?categoria=Celulares`).
* **Página de Detalhes (`produto.html`):** Exibe a imagem, nome, preço e descrição completa de um produto específico, selecionado pelo ID na URL (ex: `?id=1`).
* **Layout Moderno:** Apresenta os produtos em um layout de *cards* com badges "NEW" para itens recentes.
* **Imagens Padrão:** Utiliza uma imagem local (`img/no-image.jpg`) caso o produto não possua uma imagem cadastrada na API.

## 💻 Tecnologias Utilizadas

* **HTML5** (Estrutura semântica das páginas)
* **CSS3** (Estilização dos cards e layout, embutida na tag `<style>`)
* **JavaScript (ES6+)** (Vanilla JS)
    * `fetch` e `async/await` para o consumo de dados da API.
    * Manipulação do DOM para renderizar os produtos dinamicamente.
    * `URLSearchParams` para ler parâmetros das URLs (ID do produto e nome da categoria).

## 🚀 Como Executar o Projeto

Este projeto é **apenas o front-end** e não funcionará sozinho. Ele é 100% dependente do seu backend (API-Loja) estar em execução.

### Pré-requisitos

1.  **Servidor da API (Backend):** Você precisa ter o seu projeto de API PHP (`API-Loja`) rodando em um servidor local.
2.  **Porta do Servidor:** O front-end está configurado para fazer requisições para `http://localhost:8080`. Certifique-se de que sua API PHP esteja respondendo nesta porta.
3.  **Estrutura de Pastas:** O projeto front-end deve seguir a estrutura de pastas abaixo para que as imagens sejam carregadas corretamente.

### Estrutura de Pastas Esperada

/seu-projeto-frontend/ │ ├── index.html (Página principal) ├── categoria.html (Página de categorias) ├── produto.html (Página de detalhes do produto) │ └── img/ └── no-image.jpg (Imagem padrão para produtos sem foto)

### Passos para Execução

1.  **Inicie sua API PHP** (Ex: usando o servidor embutido do PHP, XAMPP, WAMP, etc.) e garanta que ela esteja acessível em `http://localhost:8080`.
2.  **Clone este repositório** para sua máquina local.
3.  **Abra o arquivo `index.html`** diretamente no seu navegador de preferência (Google Chrome, Firefox, etc.).

Não é necessário um servidor web para o front-end, pois ele é composto apenas de arquivos estáticos.

## 🔗 Endpoints da API (Esperados)

Este front-end foi construído para consumir os seguintes endpoints do seu backend:

* **Listar todos os produtos:**
    * `GET http://localhost:8080/API-Loja/api.php/produtos/`

* **Buscar um produto por ID:**
    * `GET http://localhost:8080/API-Loja/api.php/produtos/{id}`

* **Filtrar produtos por Categoria:**
    * `GET http://localhost:8080/API-Loja/api.php/produtos/categoria/{nome_da_categoria}`

