# Creates frontend image
# ....................................
FROM node:12.7-alpine
WORKDIR /frontend
COPY package.json  .
# RUN npm install
COPY . .
EXPOSE 4200
# RUN npm run start