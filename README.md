# adac
A.D.A.C. - Sistema de Importação de XLSX para MariaDB

A.D.A.C.
Advanced Digital Automated Creator
Pipeline em Python e Shell Script Linux

Finalidade:
	Importar dados de planilhas formato XSLX para um banco de dados MySQL e gerar arquivos PHP/HTML/Bootsptrap/JavaScript com acesso aos dados para visualizar, editar e adicionar registros. 

Fluxo:
	Script Python em com interface em PyQt5 acessa servidor MySQL, faz a conexão, cria um novo banco de dados. 
	Cria o arquivo de conexão com o banco de dados, em PHP. Importa dos dados do arquivo XSLX, criando o banco com o nome escolhido pelo usuário e a tabela (registros). 
	Chama o arquigo "gerar_phps.sh" para criar os arquivos PHP que recupera os dados do banco de dados criado. 

Arquivos e diretórios que compõem o pacote básico:

css - diretório dos arquivos CSS utilizados pelas páginas PHP
wallp.png - arquivo de imagem para o backgroud das páginas PHP
adac.py - script em Python que importa os dados do arquivo XSLX, cria o arquivo de conexão
com o servidor e o banco de dados MySQL e chama o script em Shell que acessa o banco MySQL.
gerar_phps.sh - Shell script que cria as páginas PHP que acessam o banco MySQL.

Arquivos gerados pelo Shell Script Linux:

index.php
atualizar_registro.php
salvar_registro.php
cadastro.php
footer.php
navbar.php

A estrutrua de diretório ficará da seguinte forma:

├── adac.py\n
├── atualizar_registro.php\n
├── cadastro.php\n
├── conexao.php
├── css
├── dados.xlsx
├── footer.php
├── gerar_phps.sh
├── index.php
├── leiame.txt
├── navbar.php
├── salvar_registro.php
└── wallp.png

Obs. 0: o arquivo "dados.xlsx" é um arquivo de teste.
	Em 2025-02-15 foi adicionado um módulo em Python que gera o arquivo de busca em PHP/Bootstrap do banco de dados gerado
	O módulo utiliza como referência o arquivo de conexão do banco de dados para poder gerar o PHP com a conexão correta. 
	Após selecionar o arquivo de conexão com o banco de dados, deve-se escolher o nome do arquivo PHP, como por exemplo "pesquisa.php" e salvar o arquivo. Acesse o arquivo gerado via navegador.

A estrutura padrão do sistema é:

├── adac.py - script Python principal
├── co2.xlsx - arquivo de dados convertido de um arquivo CSV
├── css - diretório com arquivos de estilo para as páginas
├── gerar_busca.py - Script Python que gera a página "pesquisa.php"
├── gerar_phps.sh - Shell Script que gera as páginas PHP
├── link-dados-co2.txt - link do arquivo de dados em formato CSV
└── wallp.png - imagem para o fundo nas páginas geradas

Após os arquivos gerados, ficará:

├── adac.py - script Python principal
├── atualizar_registro.php - página gerada pelo Shell Script
├── cadastro.php - página gerada pelo Shell Script
├── co2.xlsx - arquivo de dados convertido de um arquivo CSV
├── conexao.php - página gerada pelo Shell Script
├── css - diretório com arquivos de estilo para as páginas
├── footer.php - página gerada pelo Shell Script
├── gerar_busca.py - Script Python que gera a página "pesquisa.php"
├── gerar_phps.sh - Shell Script que gera as páginas PHP
├── index.php - página gerada pelo Shell Script
├── link-dados-co2.txt - link do arquivo de dados em formato CSV
├── navbar.php - página gerada pelo Shell Script
├── pesquisa.php - página gerada pelo Script Ptyhon "gerar_busca.py"
├── salvar_registro.php - página gerada pelo Shell Script
└── wallp.png - imagem para o fundo nas páginas geradas
	Obs. 1: O nome dos arquivos de conexão com o MySQL está como padrão “conexao.php” e o de pesquisa no banco de dados é “pesquisa.php”. Prefira manter esse padrão. Caso necessite mudar, verifique os arquivos PHP gerados, uma vez que estão configurados para estes padrões. 
