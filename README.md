## Automação de Emissão de Notas Fiscais (RPA)
Este script foi desenvolvido para automatizar o preenchimento e a emissão de notas fiscais de serviço a partir de uma base de dados em Excel. A solução utiliza Selenium para interagir com o navegador, eliminando o trabalho manual de redigitação de dados.

Como o script funciona
O fluxo de execução segue estes passos:

Configuração do Browser: Define o diretório padrão de downloads e ignora prompts de confirmação para agilizar o processo.

Autenticação: O robô acede ao ficheiro de login local (ou URL do sistema) e insere as credenciais predefinidas.

Processamento de Dados: Utiliza a biblioteca Pandas para ler a folha de cálculo NotasEmitir.xlsx.

Loop de Preenchimento: Para cada linha da tabela, o script localiza os campos de input pelo atributo NAME ou XPATH e insere as informações do cliente e do serviço.

Finalização: Após clicar no botão de emissão, a página é atualizada para limpar o formulário e passar para o próximo registo.

Requisitos de Sistema
É necessário ter o Python instalado, juntamente com as seguintes bibliotecas:

selenium: Para controlo do navegador.

pandas: Para manipulação da base de dados.

openpyxl: Para suporte à leitura de ficheiros .xlsx.

webdriver-manager: Para gestão automática do driver do Chrome.

Estrutura da Planilha (NotasEmitir.xlsx)
O script espera que o ficheiro Excel contenha exatamente estas colunas (conforme mapeado no código):

Identificação: Cliente, CPF/CNPJ, Inscrição Estadual.

Localização: CEP, Endereço, Bairro, Município, UF.

Serviço: Descrição, Quantidade, Valor Unitário, Valor Total.

Notas Técnicas
Atenção aos Caminhos: O código atual contém caminhos absolutos (ex: C:\Users\joaol\downloads). Antes de correr o script num novo ambiente, certifique-se de atualizar as variáveis de diretório no primeiro bloco de código.

Versão do Chrome: O webdriver-manager tenta baixar a versão compatível com o seu browser automaticamente, mas recomenda-se manter o Chrome atualizado.

Segurança: As credenciais de login estão escritas diretamente no código. Para uso em produção, recomenda-se o uso de variáveis de ambiente ou ficheiros .env.
