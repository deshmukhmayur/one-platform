FROM node:12-alpine
LABEL Name=one-platform-api-gateway-service \
  Version=0.1.1 \
  maintainer="mdeshmuk@redhat.com"

# Building the user-group microservice
ADD  . /app
WORKDIR /app
RUN npm install --silent && \
  npm run build

ENV PORT 8080
EXPOSE 8080

CMD [ "node", "dist/bundle.js"]
