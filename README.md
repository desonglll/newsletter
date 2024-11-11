
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
