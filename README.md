# ソフトウェア工学のサンプルコード

各サンプルコードをモジュールとして取り込んで，一式取得できるようにリポジトリを作成しました．

- `git clone`した後に以下を実行すること（モジュールのコードを実際に取得する）

```bash
git submodule update --init --recursive
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

