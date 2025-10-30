# LivrosApi: API de Gerenciamento de Livros

### Camila do Prado Padalino - RM98316
### Gabriel Teixeira Machado - RM551570

## 📚 Tema Escolhido e Funcionalidade

O tema escolhido para esta aplicação Web API é **Gerenciamento de Livros** (Book Management).

Esta API implementa as quatro operações básicas de um CRUD (Create, Read, Update, Delete) para a entidade `Livro`. A lista de livros é mantida em memória, atendendo ao requisito de **não ser necessário realizar conexão com DB**.

## 🛠️ Tecnologias Utilizadas

*   **Linguagem:** C#
*   **Framework:** ASP.NET Core 8.0 Web API
*   **Documentação:** Swagger/OpenAPI

## 📂 Estrutura do Projeto

O projeto segue uma estrutura simples e organizada, focada na clareza e legibilidade do código:

| Diretório/Arquivo | Função |
| :--- | :--- |
| `Controllers/LivrosController.cs` | Contém a lógica dos endpoints HTTP (GET, POST, PUT, DELETE). |
| `Models/Livro.cs` | Define a estrutura da entidade `Livro`. |
| `Program.cs` | Arquivo de inicialização e configuração do serviço, incluindo o Swagger. |
| `LivrosApi.csproj` | Arquivo de projeto C# (referências e configurações). |

## ⚙️ Endpoints da API

A API expõe os seguintes endpoints sob a rota base `/api/Livros`.

| Método HTTP | Rota | Descrição |
| :--- | :--- | :--- |
| **GET** | `/api/Livros` | Retorna a lista completa de todos os livros. |
| **GET** | `/api/Livros/{id}` | Retorna um livro específico pelo seu `Id`. |
| **POST** | `/api/Livros` | Adiciona um novo livro à coleção. |
| **PUT** | `/api/Livros/{id}` | Atualiza completamente os dados de um livro existente. |
| **DELETE** | `/api/Livros/{id}` | Remove um livro da coleção pelo seu `Id`. |

### Exemplo de Uso (POST)

Para adicionar um novo livro, envie um `POST` para `/api/Livros` com o seguinte corpo (Body) em formato JSON:

```json
{
  "titulo": "A Arte da Guerra",
  "autor": "Sun Tzu",
  "anoPublicacao": 500
}
```

## 🚀 Como Executar o Projeto

1.  **Pré-requisitos:** Certifique-se de ter o [.NET SDK 8.0](https://dotnet.microsoft.com/download/dotnet/8.0) instalado em sua máquina.
2.  **Navegue até o diretório do projeto:**
    ```bash
    cd LivrosApi
    ```
3.  **Execute a API:**
    ```bash
    dotnet run
    ```
    A API será iniciada, geralmente nas portas `5000` (HTTP) e `5001` (HTTPS).

## 📄 Documentação (Swagger/OpenAPI)

Após a execução, a documentação interativa da API, gerada automaticamente pelo Swagger, estará disponível no seguinte endereço:

`https://localhost:5001/swagger` (ou a porta HTTPS que o console indicar)

Você pode usar esta interface para visualizar a estrutura da API e testar todos os endpoints (GET, POST, PUT, DELETE) diretamente no seu navegador.
