Emissão Automática de NF
Script em Python para automação de preenchimento de notas fiscais de serviço. O robô lê uma base de dados em Excel e utiliza Selenium para inserir os dados em um sistema web, reduzindo o erro humano e o tempo de operação.

🚀 Funcionalidades
Integração com Excel: Leitura automatizada de dados via biblioteca Pandas.

Navegação Web: Automação de login e preenchimento de formulários complexos (Endereço, CNPJ, Itens, Valores).

Gestão de Drivers: Uso do webdriver-manager para evitar problemas de versão do ChromeDriver.

Loop de Processamento: Emite múltiplas notas em sequência com atualização automática de página (refresh).

📦 Pré-requisitos
Antes de executar, você precisará instalar as dependências necessárias:

Bash

pip install selenium pandas openpyxl webdriver-manager
🛠️ Configuração e Uso
Planilha de Dados: Certifique-se de que o arquivo NotasEmitir.xlsx esteja na raiz do projeto com as colunas mapeadas (Cliente, CPF/CNPJ, Valor Total, etc.).

Caminhos de Arquivo: O script utiliza caminhos absolutos para o diretório de downloads. Caso necessário, altere a variável prefs no bloco de configuração do Chrome.

Execução:

Abra o arquivo EmissaoNF.ipynb no Jupyter ou VS Code.

Execute as células em ordem.

📝 Estrutura do Código
Bloco 1: Configurações do Webdriver e diretórios de download.

Bloco 2 e 3: Rotina de login no sistema.

Bloco 4: Carregamento da base de dados via Pandas.

Bloco 5: Loop principal que percorre a planilha e preenche os campos do formulário via seletores (Name/XPath).

⚠️ Notas
O script foi desenvolvido utilizando seletores específicos para um arquivo login.html local. Se for utilizar em um portal oficial, os XPaths e Nomes de elementos devem ser atualizados.

Mantenha o seu Google Chrome atualizado para garantir a compatibilidade com o driver.
