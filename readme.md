# Projeto Trainee - IEEE UnB Computer Society

## 📋 Descrição e Objetivo
Este é o projeto prático desenvolvido para o processo trainee do capítulo da **Computer Society do IEEE da UnB**. O objetivo foi dar os primeiros passos na cultura DevOps e DevSecOps, aprendendo na prática como usar contêineres para rodar uma aplicação de forma isolada, leve e segura.

## 🛠️ O que foi feito
Criei uma página web simples de boas-vindas e a coloquei para rodar dentro de um contêiner Docker. Para o servidor web, utilizei o NGINX. Isso garante que o site funcione exatamente do mesmo jeito em qualquer computador, sem problemas de compatibilidade.

## 🏗️ Como a implementação foi realizada
O projeto foi feito em passos simples:
1. Primeiro, criei o código do site em um arquivo HTML (`index.html`).
2. Depois, criei o arquivo de configuração do Docker (`Dockerfile`), onde coloquei a instrução para baixar o servidor NGINX e copiar o meu site para dentro dele.
3. Por fim, usei o terminal para construir a imagem do projeto e colocar o contêiner para rodar.

## 🚀 Ferramentas Utilizadas
* **HTML5**: Para escrever a página web.
* **Google Cloud Shell**: Terminal em nuvem utilizado para rodar os comandos e testar o projeto.
* **Docker**: Para criar o contêiner.
* **NGINX (versão `nginx:alpine`)**: O servidor web escolhido. Utilizei a versão "alpine" porque ela é uma versão bem mais leve e enxuta, o que ajuda a deixar o projeto mais rápido e seguro.

## 📂 Estrutura dos Arquivos
* `index.html`: O código da página web.
* `Dockerfile`: O arquivo com as instruções para o Docker.
* `README.md`: Este arquivo explicando o projeto.

## ⚙️ Como rodar o projeto

### Pré-requisitos
* Acessar o terminal do **Google Cloud Shell** ou ter o Docker instalado no seu computador. https://shell.cloud.google.com/?hl=pt-br&show=ide%2Cterminal

### Passo a Passo

1. **Criar a imagem**:
   Com os arquivos na mesma pasta, digite o comando abaixo no terminal para construir o projeto:

   ```bash
   docker build -t projeto-pronto .
   ```

2. **Rodar o contêiner**:
   Digite o comando abaixo para iniciar o servidor em segundo plano e liberar o acesso na porta 8080:

   ```bash
   docker run -dp 8080:80 projeto-pronto
   ```

3. **Acessar o site**:
   Se estiver no Google Cloud Shell, clique no botão de Visualização na Web e escolha a porta 8080. Se estiver no seu próprio computador, abra o navegador e acesse `http://localhost:8080`.