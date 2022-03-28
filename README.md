# Criando sua primeira aplicação
    cd src
    vim Dockerfile
        FROM node
        WORKDIR /app
        COPY package* ./
        RUN npm i
        COPY . .
        EXPOSE 8080
        CMD [  "node", "server.js" ]
    docker image build -t conversao-temperatura -f ./Dockerfile .
    docker images
    docker container run -it -d -p 8080:8080 --name meu_conversor conve
