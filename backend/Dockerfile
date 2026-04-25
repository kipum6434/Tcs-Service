FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install --include=dev
COPY . .
RUN chmod +x node_modules/.bin/tsc && npm run build
EXPOSE 4000
CMD ["node", "dist/index.js"]