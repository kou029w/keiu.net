# ほんの少し降る雨

## 前提

- Docker Compose
- systemd
- systemd-journald
- PostgreSQL

Git リポジトリを取得し、設定ファイルを配置

```bash
ssh kou029w@keiu.net
git clone git@github.com:kou029w/keiu.net.git
cd keiu.net
sudo install -m 644 {,/}etc/docker/daemon.json
sudo systemctl restart docker
cp .env{.example,}
editor .env # PostgreSQL接続URLを設定
```

## 構築

```sh
docker compose up -d
```
