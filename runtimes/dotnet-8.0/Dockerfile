FROM mcr.microsoft.com/dotnet/sdk:8.0-alpine3.18

LABEL maintainer="team@appwrite.io"

RUN mkdir -p /mnt/code
RUN mkdir -p /usr/local/build
RUN mkdir -p /usr/local/server
RUN mkdir -p /usr/local/server/src
RUN mkdir -p /usr/local/server/src/function

WORKDIR /usr/local/server

COPY . .

RUN chmod +x /usr/local/server/helpers/before-start.sh
RUN chmod +x /usr/local/server/helpers/start.sh

RUN chmod +x /usr/local/server/helpers/before-build.sh
RUN chmod +x /usr/local/server/helpers/build.sh
RUN chmod +x /usr/local/server/helpers/after-build.sh

EXPOSE 3000
