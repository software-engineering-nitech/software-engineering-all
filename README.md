# ソフトウェア工学のサンプルコード

各サンプルコードをモジュールとして取り込んで，一式取得できるようにリポジトリを作成しました．

- `git clone`だけでなく，以下の手順を実行すること（モジュールのコードを実際に取得する）

```bash
git clone https://github.com/se-nitech/se-all.git
cd se-all
git submodule update --init --recursive
git submodule foreach git checkout main
git submodule foreach git fetch --all
```

- モジュールが更新されたら以下を実行すること

```bash
git submodule foreach git pull --ff-only origin main
git commit -am "update submodules"
```

なお

```bash
git submodule update
```

では，submoduleを追加した時点に戻してしまうだけ．
各submoduleでpullして，全体でcommitする必要がある．

- モジュールをすべて元に戻したい場合

```bash
git submodule foreach git checkout .
```

