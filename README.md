# Emissão Automática de Notas Fiscais de Serviço

Automação em Python para preenchimento de **Notas Fiscais de Serviço (NFS-e)**. O robô lê uma base de dados em Excel e utiliza **Selenium** para inserir os dados em um sistema web, reduzindo erros humanos e economizando tempo.

---

## 🚀 Funcionalidades

- **Integração com Excel**: Leitura automatizada de dados usando **Pandas**.
- **Navegação Web**: Automação de login e preenchimento de formulários complexos (Endereço, CNPJ, Itens, Valores).
- **Gestão de Drivers**: Uso do **webdriver-manager** para compatibilidade automática com o ChromeDriver.
- **Loop de Processamento**: Emite múltiplas notas em sequência, com atualização automática de página.

---

## 📦 Pré-requisitos

Certifique-se de ter instalado o Python 3 e as bibliotecas abaixo:

```bash
pip install selenium pandas openpyxl webdriver-manager
🛠️ Configuração e Uso

Planilha de Dados
Certifique-se de que o arquivo NotasEmitir.xlsx esteja na raiz do projeto com as colunas mapeadas corretamente, por exemplo:
Cliente, CPF/CNPJ, Valor Total, ...

Configuração de Diretórios
O script utiliza caminhos absolutos para o diretório de downloads. Caso necessário, altere a variável prefs no bloco de configuração do Chrome.

Execução

Abra o arquivo EmissaoNF.ipynb no Jupyter Notebook ou VS Code.

Execute as células na ordem apresentada.

📝 Estrutura do Código

Bloco 1: Configurações do WebDriver e diretórios de download.

Blocos 2 e 3: Rotina de login no sistema.

Bloco 4: Carregamento da base de dados via Pandas.

Bloco 5: Loop principal que percorre a planilha e preenche os campos do formulário via seletores (Name / XPath).

⚠️ Observações

O script foi desenvolvido usando seletores específicos para um arquivo login.html local. Para uso em portais oficiais, atualize os XPaths e Nomes de elementos.

Mantenha o Google Chrome atualizado para garantir compatibilidade com o driver.

