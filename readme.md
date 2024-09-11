# Sistema de Gerenciamento de Inventário

## Descrição

O Sistema de Gerenciamento de Inventário é um projeto que visa criar um banco de dados para gerenciar produtos, categorias e fornecedores em um armazém. O sistema permite adicionar, consultar, atualizar e remover informações sobre produtos, categorias e fornecedores.

## Estrutura do Banco de Dados

O banco de dados é composto por três tabelas principais:

- **Categorias**: Armazena as categorias dos produtos.
- **Fornecedores**: Armazena informações sobre os fornecedores.
- **Produtos**: Armazena detalhes dos produtos e inclui uma referência à tabela de Categorias.

### Tabelas

1. **Categorias**

    ```sql
    CREATE TABLE Categorias (
        CategoriaID INT AUTO_INCREMENT PRIMARY KEY,
        Nome VARCHAR(100) NOT NULL
    );
    ```

2. **Fornecedores**

    ```sql
    CREATE TABLE Fornecedores (
        FornecedorID INT AUTO_INCREMENT PRIMARY KEY,
        Nome VARCHAR(100) NOT NULL,
        Contato VARCHAR(100),
        Endereco TEXT
    );
    ```

3. **Produtos**

    ```sql
    CREATE TABLE Produtos (
        ProdutoID INT AUTO_INCREMENT PRIMARY KEY,
        Nome VARCHAR(100) NOT NULL,
        Descricao TEXT,
        Preco DECIMAL(10, 2) NOT NULL,
        QuantidadeEmEstoque INT NOT NULL,
        CategoriaID INT,
        FOREIGN KEY (CategoriaID) REFERENCES Categorias(CategoriaID)
    );
    ```

## Instruções para Uso

1. **Configuração do Banco de Dados**

    - Crie o banco de dados com o nome `InventarioArmazem`.
    - Execute os scripts SQL para criar as tabelas.

2. **Inserção de Dados**

    - Adicione dados às tabelas de Categorias, Fornecedores e Produtos conforme necessário.

3. **Consultas e Manipulação**

    - Consulte e manipule os dados utilizando as instruções SQL fornecidas para listar, atualizar e deletar registros.

## Contribuições

Se desejar contribuir para o projeto, sinta-se à vontade para fazer um fork deste repositório e enviar pull requests com suas melhorias ou correções.

## Licença

Este projeto está licenciado sob a [Licença XYZ](link_para_licenca). Veja o arquivo LICENSE para mais detalhes.

## Contato

Para mais informações, entre em contato com [seu_email@dominio.com](mailto:seu_email@dominio.com).
