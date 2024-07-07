## Build Docker Images

```sh
dotnet publish ./product-api/product-api.csproj --os linux --arch arm64 /t:PublishContainer -c Release
dotnet publish ./counter-api/counter-api.csproj --os linux --arch arm64 /t:PublishContainer -c Release
dotnet publish ./barista-api/barista-api.csproj --os linux --arch arm64 /t:PublishContainer -c Release
dotnet publish ./kitchen-api/kitchen-api.csproj --os linux --arch arm64 /t:PublishContainer -c Release
```

```sh
docker tag product-api:latest ghcr.io/duynguyenbui/coffeeshop-dapr-clone/product-api:latest
docker tag counter-api:latest ghcr.io/duynguyenbui/coffeeshop-dapr-clone/counter-api:latest
docker tag barista-api:latest ghcr.io/duynguyenbui/coffeeshop-dapr-clone/barista-api:latest
docker tag kitchen-api:latest ghcr.io/duynguyenbui/coffeeshop-dapr-clone/kitchen-api:latest
```

```sh
docker push ghcr.io/duynguyenbui/coffeeshop-dapr-clone/product-api:latest
docker push ghcr.io/duynguyenbui/coffeeshop-dapr-clone/counter-api:latest
docker push ghcr.io/duynguyenbui/coffeeshop-dapr-clone/barista-api:latest
docker push ghcr.io/duynguyenbui/coffeeshop-dapr-clone/kitchen-api:latest
```