# About Me - Git Lab

Projeto utilizado em uma atividade prática sobre Gerência de Configuração,
Git e GitHub.

## Objetivo

Containerizar a aplicação `About Me` e controlar a mudança utilizando:
- branch;
- commits;
- push;
- Pull Request;
- merge;
- publicação de imagem no Docker Hub;
- tag.

## Como executar

1. Abra a pasta do projeto.
2. Abra o arquivo `index.html` em um navegador.
3. Acesse a página `About Me`.

A aplicação não requer instalação de dependências.

## Como executar via Docker (US-105)

```bash
docker build -t about-me-container-felipe-vieira:latest .
docker run -d -p 8080:80 --name about-me-container about-me-container-felipe-vieira:latest
```

Acesse `http://localhost:8080/about.html` no navegador.

## Publicação no Docker Hub

```bash
docker tag about-me-container-felipe-vieira:latest DOCKERHUB_USERNAME/about-me-container-felipe-vieira:latest
docker push DOCKERHUB_USERNAME/about-me-container-felipe-vieira:latest
```
