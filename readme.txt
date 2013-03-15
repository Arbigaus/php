---------------------------------------------
Biblioteca de integra��o PagSeguro em PHP
v.2.1.4
---------------------------------------------


= Descri��o =

A biblioteca PagSeguro em PHP � um conjunto de classes de dom�nio que facilitam, para o desenvolvedor PHP, a utiliza��o das funcionalidades que o PagSeguro oferece na forma de APIs. Com a biblioteca instalada e configurada, voc� pode facilmente integrar funcionalidades como:

	- Criar requisi��o de pagamento;
	- Consultar transa��es por c�digo;
	- Consultar transa��es por intervalo de datas;
	- Receber notifica��es;


= Requisitos =

A biblioteca PagSeguro em PHP � compat�vel com a vers�o 5.1.6 (ou superior) do PHP.


= Instala��o =


1. Fa�a o download da Biblioteca PagSeguro em PHP;
2. Descompacte os arquivos em seu computador;
3. Dentro do diret�rio 'source' existem dois diret�rios, o 'examples' e o 'PagSeguroLibrary'. O diret�rio 'examples' cont�m exemplos de chamadas utilizando a API para que voc� possa se basear e o diret�rio 'PagSeguroLibrary' cont�m a biblioteca propriamente dita. Caso queira importar somente a biblioteca ao seu sistema, fa�a upload do diret�rio 'PagSeguroLibrary' e inclua a classe 'PagSeguroLibrary.php'. Essa classe se encarregar� de importar todas as funcionalidades da biblioteca no seu sistema. Caso queira importar a biblioteca juntamente com os exemplos, fa�a o upload de todos os arquivos descompactados. N�o se esque�a de incluir a classe 'PagSeguroLibrary.php' encontrada no diret�rio 'PagSeguroLibrary' ao seu projeto para que voc� possa fazer uso da API em seu sistema;
4. Fa�a o upload dos arquivos descompactados para o diret�rio p�blico do seu servidor. Os nomes mais comuns para este diret�rio s�o: htdocs, www ou o mesmo nome do dom�nio de seu website.


= Configura��o =

	- A biblioteca possui um arquivo de configura��es que deve ser configurado para que se possa fazer real uso da mesma. Esse arquivo chama-se 'PagSeguroConfig.php' e encontra-se em no diret�rio config da biblioteca;
	- Nele s�o configurados:
		- ambiente;
		- credenciais de acesso composta por email e token;
		- Caso ainda n�o possua token, ele pode ser gerado na seguinte url: https://pagseguro.uol.com.br/integracao/token-de-seguranca.jhtml;
		- codifica��o:
			- ISO-8859-1 ou
			- UTF-8.
		- log:
			- ativo ou n�o;
			- diret�rio de gera��o do log das transa��es do sistema com o PagSeguro.

Informa��es adicionais podem ser obtidas em: https://pagseguro.uol.com.br/v2/guia-de-integracao/tutorial-da-biblioteca-pagseguro-em-php.html


= Changelog =

v2.1.4
Adicionado : Classe para manipula��o de moedas permitidas nas transa��es com o PagSeguro.

v2.1.3
Corre��o: A requisi��o era abortada se a gera��o de log estivesse ativa e o usu�rio n�o possuisse arquivo para gera��o de log nem permiss�o de escrita e leitura para o arquivo;

v2.0.0 - v2.1.2
Classes de dom�nios que representam pagamentos, notifica��es e transa��es;
Cria��o de checkouts via API;
Controller para processar notifica��es de pagamento enviadas pelo PagSeguro;
M�dulo de consulta de transa��es.


= NOTAS =

	- Certifique-se que o email e o token informados estejam relacionados a uma conta que possua o perfil de vendedor ou empresarial.
	- Certifique-se que tenha definido corretamente o charset de acordo com a codifica��o (ISO-8859-1 ou UTF-8) do seu sistema. Isso ir� prevenir que as transa��es gerem poss�veis erros ou quebras ou ainda que caracteres especiais possam ser apresentados de maneira diferente do habitual.
	- Para que ocorra normalmente a gera��o de logs, certifique-se que o diret�rio e o arquivo de log tenham permiss�es de leitura e escrita.