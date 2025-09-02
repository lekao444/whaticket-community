# Imagem base Node 18 Bullseye (mais estável que Buster)
FROM node:18-bullseye

# Diretório de trabalho
WORKDIR /app

# Copiar package.json e yarn.lock primeiro
# COPY package.json yarn.lock ./ 

# Instalar dependências
RUN yarn install --frozen-lockfile

# Copiar o restante do código
COPY . .

# Build do projeto
RUN yarn build

# Expor a porta do backend
EXPOSE 8080

# Start padrão
CMD ["yarn", "start"]
