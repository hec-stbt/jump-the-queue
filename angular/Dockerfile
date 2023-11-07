# Creates frontend image
# ....................................
FROM node:14
WORKDIR /frontend
COPY .  .
RUN npm install
RUN npm run build -- --prod
EXPOSE 80
RUN npm run start