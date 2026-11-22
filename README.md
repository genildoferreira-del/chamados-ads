# API de Chamados de Suporte

**Estudante:** Genildo da Silva Ferreira

## 1. Objetivo do Projeto
Este projeto consiste na estrutura inicial de uma API REST para gerenciamento de chamados de suporte técnico, desenvolvida em Python com o framework **Flask** e gerenciada com a ferramenta **uv**, como parte da Atividade #1 da disciplina. Nesta etapa inicial, a aplicação disponibiliza a rota de verificação de status (`GET /`) para validar o funcionamento do servidor.

## 2. Organização do Repositório
A estrutura do projeto está organizada da seguinte forma:

- **`app.py`**: código-fonte principal da aplicação Flask e definição da rota inicial.
- **`pyproject.toml`**: configurações do projeto e declaração das dependências.
- **`uv.lock`**: registro das versões exatas das dependências instaladas.
- **`.gitignore`**: arquivos e diretórios ignorados pelo controle de versão (incluindo `.venv/` e `__pycache__/`).
- **`README.md`**: documentação do projeto, identificação do estudante e instruções de uso.

## 3. Instalação das Dependências
Certifique-se de ter o **uv** instalado em seu ambiente. Na raiz do projeto, execute o comando abaixo para criar o ambiente virtual e instalar as dependências exatamente nas versões definidas no `uv.lock`:

```bash
uv sync --locked
```

## 4. Como Executar a Aplicação
Com as dependências instaladas, inicie o servidor web do Flask na porta `5000` executando o comando abaixo na raiz do projeto:

```bash
uv run flask --app app run --host=0.0.0.0 --port=5000
```

Após executar o comando, o servidor iniciará e ficará disponível em `http://localhost:5000/`. Para encerrar a execução, pressione `Ctrl + C` no terminal.

## 5. Como Acessar a Rota Inicial e Resposta Esperada
Com a aplicação em execução, faça uma requisição `GET` para a rota `/` abrindo `http://localhost:5000/` no navegador ou executando no terminal:

```bash
curl -i http://localhost:5000/
```

### Resposta Esperada
- **Código HTTP:** `200 OK`
- **Cabeçalho:** `Content-Type: application/json`
- **Corpo (JSON):**
```json
{
  "mensagem": "API de chamados em funcionamento"
}
```
