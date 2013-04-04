---------------------------------------------
Biblioteca de integra��o PagSeguro em PHP
v2.1.4
---------------------------------------------


= Descri��o =

A biblioteca PagSeguro em PHP � um conjunto de classes de dom�nio que facilitam, para o desenvolvedor PHP, a utiliza��o das funcionalidades que o PagSeguro oferece na forma de APIs. Com a biblioteca instalada e configurada, voc� pode facilmente integrar funcionalidades como:

	- Criar requisi��es de pagamentos
	- Consultar transa��es por c�digo
	- Consultar transa��es por intervalo de datas
	- Consultar transa��es abandonadas
	- Receber notifica��es


= Requisitos =

	- PHP 5.1.6+
	- SPL
	- cURL
	- DOM


= Instala��o =


	- Fa�a o download da Biblioteca PagSeguro em PHP;
	- Descompacte os arquivos em seu computador;
	- Dentro do diret�rio 'source' existem dois diret�rios, o 'examples' e o 'PagSeguroLibrary'. O diret�rio 'examples' cont�m exemplos de chamadas utilizando a API e o diret�rio 'PagSeguroLibrary' cont�m a biblioteca propriamente dita. Caso queira importar somente a biblioteca, fa�a upload do diret�rio 'PagSeguroLibrary' e inclua a classe 'PagSeguroLibrary.php' em seu projeto. Essa classe se encarregar� de importar todas as funcionalidades da biblioteca no seu sistema.


= Configura��o =

Para fazer uso real da biblioteca � preciso fazer algumas configura��es no arquivo 'PagSeguroConfig.php', que encontra-se no diret�rio 'config'. As op��es dispon�veis est�o descritas abaixo.

	- environment: no momento aceita apenas o valor "production"
	- email: e-mail cadastrado no PagSeguro
	- token: token gerado no PagSeguro
	- charset: codifica��o do seu sistema (ISO-8859-1 ou UTF-8)
	- log: ativa/desativa a gera��o de logs
	- fileLocation: local onde se deseja criar o arquivo de log. Ex.: /logs/ps.log

	Informa��es adicionais podem ser obtidas em: https://pagseguro.uol.com.br/v2/guia-de-integracao/tutorial-da-biblioteca-pagseguro-em-php.html


= Changelog =

	v2.1.4

	- Adicionado: Classe para manipula��o de moedas permitidas nas transa��es com o PagSeguro

	v2.1.3

	- Corre��o: A requisi��o era abortada se a gera��o de log estivesse ativa e o usu�rio n�o possuisse arquivo para gera��o de log nem permiss�o de escrita e leitura para o arquivo

	v2.0.0 - v2.1.2

	- Classes de dom�nios que representam pagamentos, notifica��es e transa��es
	- Cria��o de checkouts via API
	- Controller para processar notifica��es de pagamento enviadas pelo PagSeguro
	- M�dulo de consulta de transa��es


= Notas =

	- Certifique-se que o email e o token informados estejam relacionados a uma conta que possua o perfil de vendedor ou empresarial.
	- Certifique-se que tenha definido corretamente o charset de acordo com a codifica��o (ISO-8859-1 ou UTF-8) do seu sistema. Isso ir� prevenir que as transa��es gerem poss�veis erros ou quebras ou ainda que caracteres especiais possam ser apresentados de maneira diferente do habitual.
	- Para que ocorra normalmente a gera��o de logs, certifique-se que o diret�rio e o arquivo de log tenham permiss�es de leitura e escrita.
	- D�vidas? https://pagseguro.uol.com.br/desenvolvedor/comunidade.jhtml
