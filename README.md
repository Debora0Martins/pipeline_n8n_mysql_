## 🧠 Pipeline de Dados Automatizada — n8n + MySQL + Docker

## 📋 Descrição

Este projeto implementa uma pipeline de dados automatizada utilizando o n8n, com armazenamento dos resultados no MySQL, tudo rodando de forma isolada via Docker.

A automação realiza:

🔍 Coleta de dados em tempo real via API (Google Custom Search);

🧩 Processamento e limpeza dos resultados (título, link, resumo);

💾 Armazenamento automático no banco de dados MySQL;

📊 Persistência dos fluxos com volume Docker para evitar perda de dados.

## ⚙️ Tecnologias Utilizadas

Tecnologia	Descrição
🧠 n8n	Plataforma de automação low-code usada para orquestrar o fluxo de dados
🐬 MySQL	Banco de dados relacional usado para persistência dos resultados
🐳 Docker	Containeriza e isola os serviços (garantindo portabilidade e facilidade de deploy)
🧰 Git & GitHub	Versionamento e colaboração do código
🧩 Estrutura do Projeto
n8n-local/
│
├── docker-compose.yml      # Configuração do serviço n8n + volume persistente
├── .gitignore              # Ignora arquivos locais e sensíveis
├── README.md               # Documentação do projeto
└── n8n-data/               # Volume local (persistência dos fluxos e credenciais)

## 🚀 Como Rodar o Projeto

1️⃣ Clonar o repositório
git clone https://github.com/Debora0Martins/pipeline_n8n_mysql.git
cd pipeline_n8n_mysql

2️⃣ Subir o container Docker
docker-compose up -d

3️⃣ Acessar o painel do n8n

Abra no navegador:

http://localhost:5678

4️⃣ Importar o fluxo

No painel do n8n, importe o arquivo workflow-pipeline.json (se aplicável) e execute o fluxo.

## 🧾 Banco de Dados

A pipeline salva os dados no banco pipeline_demo com a seguinte estrutura:

Campo	Tipo	Descrição
id	INT	Identificador único
titulo	VARCHAR(255)	Título do resultado
link	VARCHAR(255)	Link da página
resumo	TEXT	Trecho do conteúdo
data_coleta	DATETIME	Data e hora da coleta
🧑‍💻 Desenvolvido por

## Débora Flaviana Martins
🌍 Timóteo - MG
📧 ddeboraf.mar@gmail.com

💻 github.com/Debora0Martins

🌟 Licença

