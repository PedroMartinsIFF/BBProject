# BBProject

Exercício de Administração de Servidores

---------------------------------------------------------------------------------------------
Execute as seguintes tarefas:

Customizar imagem docker oficial zabbix 5.2
Customizar health check de uma das imagens (ex:frontend ou server ou proxy)
Defina pollers de acordo com o ambiente de testes local
Introduzir alguma nova feature em alguma imagem (ex: external scripts, drivers odbc..)
Realizar deploy no swarm/kubernetes local
Usar uma ferramenta para deploy automatizado será um diferencial

---------------------------------------------------------------------------------------------

Inicialmente foi localizada a imagem docker oficial do zabbix 5.2 - server, disponível em https://github.com/zabbix/zabbix-docker/blob/5.2/server-pgsql/ubuntu/Dockerfile

O deploy da aplicação será feito num cluster kubernetes local, utilizando o minikubem, ele será automatizado utilizando a ferramenta Helm.

Dentre as diversas opções de ferramentas para deploy automatizado, como ansible ou puppet, foi escolhido o Helm para este cenário por ser uma ferramenta simples, altamente customizavel e mais otimizada apra o deploy de aplicações.

O Helm funciona como um docker para aplicações kubernetes, é possível buscar repositórios oficiais no Helm Hub( Agora Artifact Hub ) e os customizar de acordo com a necessidade, sendo uma forma simples de instalar e controlar aplicações.

Foi escolhido o Artifact produzido pelo autor cetic, nele instalaremos o Zabbix Server, o Zabbix Agent e o Zabbix Web (frontend), além da database PostgreSQL