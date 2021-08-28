# PARTE I - FUNDAMENTOS

## Objetivos

* Apresentar o básico sobre Docker e conteinerização, assim como, demonstrar as vantagens de utilizar uma infraestrutura conteinerizada.

## Por que usar contêineres?

* Contêineres trazem consigo o conceito de imutabilidade;

* A imutabilidade quer dizer que qualquer alteração realizada em um contêiner resultará em um novo artefato (contêiner);

* A imutabilidade assegura aos usuários que o mesmo contêiner funcionará igualmente em qualquer ambiente;

* As aplicações conteinerizadas, por padrão, são pequenas e flexíveis, pois nos contêineres são adicionados apenas as bibliotecas e pacotes necessários para a manutenção da aplicação.

## Docker engine

* É a interface que permite o acesso aos recursos e isolamento de processos do kernel do Linux;

* É responsável pela execução dos contêineres e possui mecanismos para montar e testar as imagens fornecidas por códigos-fonte (Dockerfiles ou repositórios).

## Contêineres

* Um contêiner deve executar somente um processo;

* O ciclo de vida de um contêiner é definido pelo seu estado e seus processos;

* O docker pode automaticamente parar ou reiniciar um contêiner quando detectado que não está funcionando corretamente;

* Por sua característica de se encerrar quando seu processo é finalizado, os contêineres se tornam uma excelente plataforma para executar scripts e outras funções que tem um ciclo de vida indefinido;

* Por padrão, os contêineres são isolados dos demais processos executados pelo sistema.

## Comandos básicos

```bash
docker run              #inicia/executa uma imagem;
docker ps               #lista todos os contêineres em execução;
docker ps -a            #lista todos os contêineres existentes;
docker images           #lista todas as imagens disponíveis localmente;
docker pull             #faz o download de uma imagem específica;
docker stop             #encerra um contêiner;
docker start            #inicia um contêiner;
docker restart          #reinicia um contêiner;
docker attach           #permite ao usuário acessar o principal processo do contêiner;
docker exec             #executa um comando dentro do contêiner;
docker rm               #apaga um contêiner;
docker rmi              #apaga uma imagem;
docker inspect          #mostra todos os detalhes do contêiner;
docker prune -fa        #remove contêineres antigos e imagens locais.
```

## Ciclo de vida dos contêineres

* Compreender o ciclo de vida dos contêineres é fundamental para o gerenciamento do ambiente de produção;

* Saber como investigar os contêineres é importante para avaliar a integridade da infraestrutura adotada;

* Ao construir imagens, deve-se buscar deixá-las com o menor tamanho possível, pois isso facilita a migração, manutenção e reduz os riscos de ataques.

## Acessando um contêiner

* O comando **docker exec** é excelente para acessar rapidamente um contêiner para inspecionar, entender o contexto ou ajustar alguma configuração, porém ao finalizar o processo, o contêiner é encerrado;

* O comando **docker attach** permite o acesso ao principal processo do container, sendo possível sair do contêiner sem finalizar o processo;

* Em resumo, enquanto o comando **docker exec** executa um novo processo no contêiner, o comando **docker attach** permite o acesso ao principal processo.
