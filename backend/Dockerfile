# Imagem base Node 18 Bullseye
FROM node:18-bullseye

# Diretório de trabalho
WORKDIR /app

# Copiar package.json primeiro
COPY package.json ./

# Instalar dependências
RUN yarn install --frozen-lockfile

# Instalar TypeScript global (para rodar tsc)
RUN yarn global add typescript

# Copiar o restante do código
COPY . .

# Build do projeto
RUN yarn build

# Expor a porta
EXPOSE 8080

# Comando padrão
CMD ["yarn", "start"]
