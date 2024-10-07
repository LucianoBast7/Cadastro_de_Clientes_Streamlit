# 🍕 Projeto: Cadastro de Clientes

Este é um projeto simples em Python utilizando **Streamlit** para criar uma interface web de cadastro de clientes. Os dados são gravados em um arquivo CSV com o nome, data de nascimento e tipo de cliente (Pessoa Física ou Pessoa Jurídica). A aplicação exibe mensagens de sucesso ou erro após a tentativa de cadastro.

## 🚀 Funcionalidades

- Interface web para entrada de dados de clientes.
- Validação da data de nascimento (a data deve ser anterior ou igual ao dia atual).
- Gravação dos dados em um arquivo CSV (`clientes.csv`).
- Feedback visual com mensagens de **sucesso** ou **erro** após o cadastro.

## 🛠 Tecnologias Utilizadas

- **Python**: Linguagem de programação utilizada.
- **Streamlit**: Framework para criação de aplicações web de forma rápida e simples.
- **Pandas**: Biblioteca utilizada para manipulação de dados.
- **Datetime**: Biblioteca para trabalhar com datas.

## 📂 Estrutura do Projeto

- `app.py`: Arquivo principal que contém o código da aplicação.
- `clientes.csv`: Arquivo onde os dados dos clientes são armazenados (criado automaticamente após o primeiro cadastro).

## ⚙️ Como Executar

### Pré-requisitos

- Ter o Python instalado (>= 3.7).
- Instalar as bibliotecas necessárias (**Streamlit**, **Pandas**).

### Passos para Execução

1. **Clone este repositório**:

   ```bash
   git clone https://github.com/LucianoBast7/Cadastro_de_Clientes_Streamlit.git

2. **Acesseo Repositório do Projeto**:

   ```bash
   cd cadastro-clientes

3. **Instale as Dependências**:

   ```bash
   pip install -r requirements.txt

4. **Execute a aplicação com o Streamlit**:

   ```bash
   streamlit run app.py

5. **Acesse o navegador no endereço sugerido pelo terminal (geralmente http://localhost:8501).**

## 📋 Campos do Formulário

A aplicação possui um formulário simples com os seguintes campos:

- **Nome**: Campo de texto onde o nome do cliente deve ser informado.
- **Data de Nascimento**: Um campo de data que só permite datas até o dia atual.
- **Tipo de Cliente**: Um campo de seleção com duas opções:
  - **Pessoa Física**
  - **Pessoa Jurídica**

### Como Funciona

1. O usuário preenche os campos **Nome**, **Data de Nascimento** e seleciona o **Tipo de Cliente**.
2. Ao clicar no botão **Cadastrar**, os dados são validados:
   - O nome não pode estar vazio.
   - A data de nascimento deve ser anterior ou igual à data atual.
3. Se os dados forem válidos:
   - ✅ Uma mensagem de **sucesso** será exibida e os dados serão gravados no arquivo `clientes.csv`.
4. Caso contrário:
   - ❌ Uma mensagem de **erro** será exibida informando o problema.

---

## 🔄 Funcionamento

- Após o preenchimento dos dados, o botão **Cadastrar** será ativado.
- O arquivo `clientes.csv` será atualizado com as informações de nome, data de nascimento e tipo de cliente.
- O arquivo CSV tem o seguinte formato:

   ```csv
   Nome, Data de Nascimento, Tipo de Cliente
   Exemplo Cliente, 1990-01-01, Pessoa Física

### Mensagens de Feedback

- **Cadastro bem-sucedido**: Caso todos os dados estejam corretos, você verá uma mensagem de sucesso como esta:

   ```markdown
   🟢 Cliente cadastrado com sucesso! ✅

- **Erro no Cadastro**: Caso ocorra algum problema, como data inválida ou nome não preenchido, será exibida uma mensagem de erro:

   ```markdown
   🔴 Houve um erro no cadastro. Verifique os dados inseridos e tente novamente. ❌
