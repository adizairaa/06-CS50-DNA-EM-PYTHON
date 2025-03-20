# 06-CSDesafio: Identificação por DNA
Este repositório contém a solução para o desafio de programação em que você deve identificar uma pessoa com base em seu DNA, comparando sequências de DNA fornecidas com as de um banco de dados.

💡 Descrição do Desafio
O desafio consiste em implementar um programa que receba um arquivo de banco de dados contendo informações sobre diversas pessoas e suas sequências de DNA, e um arquivo de sequência de DNA de uma pessoa. O programa deve identificar a pessoa com base no DNA fornecido.

🔍 Como Funciona
O programa recebe dois parâmetros:

Um arquivo CSV que contém um banco de dados com os nomes e sequências de DNA de várias pessoas.
Um arquivo de sequência de DNA que representa a pessoa a ser identificada.
O programa compara as sequências fornecidas com as do banco de dados, identificando a pessoa correspondente.

O banco de dados contém informações de repetição de substrings (como STRs - Short Tandem Repeats), que são usadas para comparar a sequência do DNA.

Se o DNA fornecido corresponder a uma pessoa do banco de dados, o nome da pessoa é impresso.

📝 Exemplo de Uso
Rodando o programa com os seguintes arquivos:

bash
Copiar
Editar
python dna.py databases/large.csv sequences/5.txt
Saída esperada:

bash
Copiar
Editar
Lavende
Isso significa que o DNA fornecido no arquivo sequences/5.txt corresponde ao DNA da pessoa "Lavende" no banco de dados.

📚 Especificação
Requisitos:
Entrada:

O programa deve aceitar dois arquivos como argumentos:
O primeiro arquivo é um banco de dados CSV (databases/large.csv), que contém uma lista de pessoas e as respectivas sequências de DNA.
O segundo arquivo é uma sequência de DNA que será comparada com o banco de dados.
Processamento:

O programa deve extrair informações do arquivo CSV e comparar as sequências de DNA para encontrar coincidências.
Para cada sequência no banco de dados, o programa deve verificar a quantidade de vezes que uma sequência curta de repetição (STR) aparece consecutivamente na sequência de DNA fornecida.
Saída:

O programa deve imprimir o nome da pessoa correspondente ao DNA fornecido ou "Não encontrado" caso nenhum correspondente seja encontrado.
Estrutura dos Arquivos:
Arquivo CSV (databases/large.csv):

Cada linha do arquivo contém o nome de uma pessoa seguido por várias colunas com o número de repetições de cada STR.
Exemplo de formato:
pgsql
Copiar
Editar
name,AGAT,TTTT,ATGT
Lavende,4,5,6
Arquivo de Sequência de DNA (sequences/5.txt):

O arquivo contém uma sequência de DNA em formato de string.
Exemplo:
nginx
Copiar
Editar
AGATAGATAGATTTTTTTTTATGTATGTATGT
🚀 Como Rodar
Baixe o código para seu CS50 IDE:

Faça login no CS50 IDE.
Execute o comando a seguir para acessar o diretório correto:
bash
Copiar
Editar
cd pset5
Execute o programa:

Com o código baixado e os arquivos necessários prontos, execute o programa com os seguintes parâmetros de entrada:

bash
Copiar
Editar
python dna.py databases/large.csv sequences/5.txt
🧪 Testes
O programa deve funcionar corretamente em várias sequências de DNA, garantindo que ele compare corretamente as sequências fornecidas com as do banco de dados.

💻 Implementação
A implementação envolve:

Leitura e parsing do arquivo CSV.
Comparação das sequências de STR entre o banco de dados e o arquivo de entrada.
Identificação da pessoa baseada nas correspondências de STR.
💡 Contribuição
Sinta-se à vontade para melhorar e contribuir com o código!

Faça um fork do repositório.
Crie um branch para adicionar suas melhorias (git checkout -b minha-feature).
Faça um commit das alterações (git commit -m 'Melhorias na função X').
Envie um pull request.
🌟 Autor
Desafio inspirado no curso CS50 de Harvard.

