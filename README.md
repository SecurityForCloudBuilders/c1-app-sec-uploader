# c1-app-sec-uploader

Este aplicativo de demonstração para Cloud One Application Security cria um front-end baseado em Apache PHP permitindo o upload de tipos de arquivos. É para simular recursos de upload de arquivos de aplicativos da web do mundo real.

Integração de segurança do aplicativo feita por meio do Dockerfile fornecido.

# Antes de tudo é necessário criar uma conta na plataforma Cloud One (free)

Criando a conta http://cloudone.trendmicro.com

# Criando a imagem

Primeiro, clonar o repositório.

Em seguida, crie e execute o contêiner

```sh
# Criando a imagem
docker build -t uploader .

# Executando o container

docker run \
  --rm -p 80:80 \
  --name uploader \
  -e TREND_AP_KEY=<YOUR APP SEC GROUP KEY>
  -e TREND_AP_SECRET=<YOUR APP SEC GROUP SECRET>
  uploader
```

O aplicativo de upload pode ser acessado na porta 80.

Por fim, faça upload de arquivos maliciosos.

# Jenkins

Um exemplo de pipeline do Jenkins é fornecido para integrar este aplicativo à sua instância do Jenkins.
