# Sistema de Consulta de Endereço pelo CEP

Este sistema permite consultar um endereço a partir de um CEP e armazenar esses endereços em uma lista. O usuário pode ordenar os endereços por cidade, bairro ou estado, de forma crescente ou decrescente. Além disso, o sistema permite a exclusão de endereços individuais da lista por meio de um ícone discreto de lixeira. Abaixo estão as tecnologias utilizadas e o funcionamento do sistema.

---

## Tecnologias Utilizadas

### **Frontend**
- **HTML**: Estrutura da página web, com campos de input, botões e tabela para exibição dos endereços.
- **CSS**: Estilização da página, proporcionando uma interface agradável com cores, margens, tabelas e botões. O layout foi projetado para ser responsivo e interativo.
- **JavaScript**: Responsável pela interação no frontend, captura de dados, manipulação da DOM, realização de requisições para a API ViaCEP e atualização dinâmica da tabela de endereços.
- **Fetch API**: Usada para fazer requisições assíncronas ao backend, que consulta a API ViaCEP e retorna os dados ao frontend.

### **Backend**
- **Node.js**: Plataforma JavaScript no backend, que executa o servidor e gerencia as requisições feitas pelo frontend.
- **Express.js**: Framework para Node.js utilizado para criar rotas e gerenciar as requisições HTTP de forma simples e rápida.
- **Axios**: Biblioteca JavaScript utilizada no backend para consultar a API ViaCEP e obter informações sobre os endereços.
- **API ViaCEP**: API pública que fornece dados de endereço a partir de um CEP, sendo consultada pelo backend.

### **Outras Tecnologias**
- **Tabela HTML**: Usada para exibir os endereços armazenados, permitindo a ordenação e a exclusão dos mesmos.

---

## Funcionamento do Sistema

### **Frontend**
1. O usuário insere um **CEP** no campo de input e clica no botão **Consultar**.
2. O sistema faz uma requisição à API ViaCEP para obter as informações do endereço.
3. O endereço retornado é exibido na tela e armazenado em uma lista interna.
4. A lista de endereços armazenados é exibida em uma tabela HTML. Cada linha da tabela exibe os detalhes do endereço.
5. Ao lado da sigla do **Estado**, um ícone de lixeira é exibido, permitindo que o usuário exclua um endereço individualmente.
6. O usuário pode ordenar a lista por **Cidade**, **Bairro** ou **Estado**, escolhendo a ordem (crescente ou decrescente) por meio de um seletor de opções.

### **Backend**
1. O servidor é executado utilizando **Node.js** e **Express.js**.
2. Quando o usuário consulta um CEP, o backend realiza uma requisição à API **ViaCEP** para obter as informações do endereço.
3. Os dados retornados pela API são enviados de volta ao frontend em formato JSON.

---

## Como Rodar o Sistema

1. Clone este repositório para o seu ambiente local.
2. No terminal, navegue até o diretório do projeto.
3. Instale as dependências executando:
   ```
   npm install
   ```
4. Inicie o servidor com o comando:
   ```
   npm start
   ```
5. Acesse o sistema em `http://localhost:3000` no seu navegador.  

---

## Licença

Este projeto está licenciado sob a MIT License - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
```