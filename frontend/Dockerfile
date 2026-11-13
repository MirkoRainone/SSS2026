FROM node:20-alpine

WORKDIR /app

# Copia i file delle dipendenze e installale
COPY package*.json ./
RUN npm install

# Copia il resto del codice frontend
COPY . .

# Espone la porta di default di Angular
EXPOSE 4200

# Avvia Angular esponendolo fuori dal container
CMD ["npx", "ng", "serve", "--host", "0.0.0.0", "--port", "4200"]