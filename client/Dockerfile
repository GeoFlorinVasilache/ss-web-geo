FROM node:20-alpine

WORKDIR /app

# Copiem fișierele de dependințe
COPY package.json yarn.lock ./

# Instalăm dependințele
RUN yarn install

# Copiem restul codului sursă
COPY . .

# Expunem portul pe care rulează Vite
EXPOSE 5173

# Comanda de pornire (folosim dev:poll pentru a detecta schimbările de fișiere pe Mac)
CMD ["yarn", "dev:poll", "--host", "0.0.0.0"]