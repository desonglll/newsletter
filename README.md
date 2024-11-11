
## Install psql

[Ref](https://www.timescale.com/blog/how-to-install-psql-on-mac-ubuntu-debian-windows/)

```shell
brew doctor
brew update
brew install libpq
brew link --force libpq
```

## Install sqlx-cli

```shell
cargo install --version=^0.6 sqlx-cli --no-default-features --features native-tls,postgres
# cargo install sqlx-cli --no-default-features --features native-tls,postgres
```

## Docker build

```shell
docker build --tag newsletter --file Dockerfile .
docker run -p 8000:8000 newsletter
```

## HTTP

```shell
curl -v http://127.0.0.1:8000/health_check
```

```shell
curl --request POST \
--data 'name=le%20guin&email=ursula_le_guin%40gmail.com' \
127.0.0.1:8000/subscriptions --verbose
```
