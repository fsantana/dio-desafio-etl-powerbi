# Projeto de transformação de dados com Power Bi

## Preparação da base de dados

Optei pelo uso do Docker ao invés de usar uma conta ta azure. O docker compose está configurado para que ao usar comando docker compose up já crie uma base de dados chamada *company_constraints* e roda os scripts que estão na pasta sql_scripts.

> Tive que instalar a versão 7 do conector do mysql, pois a última versão não era compatível com o PowerBI

> Tive que usar a versão 5.7 od MySQL pois o enconding usado por padrão na versão 8 do banco não era compativo com .Net

## Importando os dados para o Power BI

Conectado com o conector para mysql com o host localhost

Usuário e senha do banco estão no arquivo docker-compose.yml

## Tratamento de dados

Transformei em todas as tabelas que contem o id do colaboradores o tipo de dados para inteiro.
Usei o dividir colunas par dividir o endereço do colaboradores em colunas separadas.

Agrupei as colunas para ter nome e sobrenome dos colaboradores

Mesclei colunas para que no relatório exibisse de forma hierárquica os colaboradores e seus gerentes.

Mesclei colunas para exibir relatório que exibisse os deparatamentos e os colaboradores.

Procurei responder com o relatório

Qual o tamanho de equipe por departamento.

Qual o tamanho de equipe de cada gerente.

Quantas horas foram utilizadas por cada projeto.

Quantos colaboradores estão envolvido em cada projeto.
