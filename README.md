Preenchimento do Formulário a partir de uma Planilha Excel.

UiPath é uma plataforma de automação robótica de processos (RPA) que permite automatizar tarefas repetitivas 

Experimente por si mesmo, explore mais sobre automação com UiPath.

Atividades ....

Read Range : lê o intervalo especificado de uma planilha Excel e armazena os dados em uma variável DataTable. 

Use Application/Browser : Esta atividade é usada para iniciar uma sessão com um aplicativo de desktop ou um navegador da web específico. Ela permite que você identifique o aplicativo ou navegador pelo seu nome, título da janela ou URL e, em seguida, execute uma série de ações dentro desse contexto

Type Into Esta atividade : simula a entrada de texto em campos de entrada em aplicativos de desktop ou navegadores da web. Você pode especificar o texto a ser digitado diretamente na propriedade da atividade ou fornecer uma variável que contenha o texto a ser digitado.


Passos utilizados : 

Automatizar Preenchimento de Formulário a partir de uma Planilha Excel:
Primeiro usamos a atividade Read Range : Que lê o intervalo especificado de uma planilha Excel e armazena os dados em uma variável DataTable

Indicar o Caminho do Arquivo:
Devemos fornecer o caminho do arquivo da planilha Excel que contém os dados a serem preenchidos no formulário.

Nome da Planilha e Intervalo de Dados:
Em seguida, especificamos o nome da planilha e o intervalo de células que contêm as informações. Como queremos extrair todas as informações, deixamos este campo vazio.

Configurações Adicionais:
Verificamos se a opção "AddHeader" está ativada para garantir que o cabeçalho das colunas seja incluído.

Criar Variável para Armazenar os Dados:
Criamos uma variável (DataTable) para armazenar os dados extraídos da planilha, e a nomeamos como "dtCadastro".
Abrir o Navegador e Acessar o Formulário:

Abrimos o navegador e navegamos até a página do formulário que pretendemos preencher.

Criar um Loop para Cada Linha da Tabela:
Utilizamos a atividade "For Each Row data table" para iterar sobre cada linha da tabela de dados.

Preencher Campos do Formulário:
Para cada linha da tabela, utilizamos a atividade "Type Into" para inserir o nome, idade e profissão nos campos correspondentes do formulário.

Clicar no Botão de Submissão:
Após preencher os campos, clicamos no botão de submissão utilizando a atividade "Click".

Repetir o Processo:
Repetimos esses passos para cada linha da tabela, clicando novamente no botão de submissão para submeter um novo formulário após o preenchimento.

Encerramento:
O processo continuará até que não haja mais dados na planilha para preencher. A aplicação será então encerrada.
