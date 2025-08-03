FROM node:24-alpine AS builder
WORKDIR /app/knitipedia
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build
RUN npm prune --production

FROM node:24-alpine
WORKDIR /app/knitipedia
COPY --from=builder /app/knitipedia/build build/
COPY --from=builder /app/knitipedia/node_modules node_modules/
COPY package.json .
EXPOSE 5173
ENV NODE_ENV=production
# CMD [ "node", "build" ]
CMD [ "sleep", "infinity" ]