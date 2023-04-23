FROM node:18

RUN mkdir -p /home/apps/der-web

COPY . /home/apps/der-web

WORKDIR /home/apps/der-web

RUN yarn

EXPOSE 5173

ENTRYPOINT ["yarn", "dev", "--host"]
