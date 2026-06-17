FROM node:20-alpine

RUN apk update \
    && npm install -g pnpm

WORKDIR /home/node/app

COPY package.json pnpm-lock.yaml ./

RUN pnpm install --frozen-lockfile

COPY --chown=node:node . .

EXPOSE 5173

USER node

CMD ["pnpm", "run", "dev"]