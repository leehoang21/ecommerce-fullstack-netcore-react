FROM alpine
WORKDIR /app
copy . .
RUN adduser -D onlineshop
RUN apk add dotnet6-sdk
RUN chown -R onlineshop:onlineshop /app
USER onlineshop
RUN dotnet restore
EXPOSE 5214
ENTRYPOINT dotnet run
