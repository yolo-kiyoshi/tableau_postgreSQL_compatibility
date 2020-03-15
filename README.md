# 概要
複数バージョンのPostgreSQLを起動し、他ツールとの接続互換性を検証する。
以下のようにportごとにバージョンを分けている。

- port 9010 : PostgreSQL ver10.x
- port 9011 : PostgreSQL ver11.x
- port 9012 : PostgreSQL ver12.x

# 用途

## initファイル作成
コンテナ起動時に、コンテナ内の`docker-entrypoint-initdb.d/`に格納されている`sql`が実行される。  
※_`docker-compose.yml`で`./initdb`を`/docker-entrypoint-initdb.d`にマウント。_

## イメージ作成とコンテナ実行

```
docker-compose up -d
```