## leonコード
### 仮想マシン起動
```
$ multipass launch 20.04 -n YouTube-AB
```

### ホストの公開鍵をクリップボードにコピー
```
$ pbcopy < ~/.ssh/id_rsa.pub
```

### SHELLに入る
```
$ multipass shell YouTube-AB
```

### クリップボードにコピーした公開鍵をホストにコピー
```
$ sudo vim ~/.ssh/authorized_keys
```

### Playbook起動
```
$ ansible-playbook -i hosts ansible/main.yml -u ubuntu
```

### mountを設置
```
$ multipass mount YouTube-AB YouTube-AB:/var/www/html
```

### ip確認
```
$ mutipass ls
```

### multipassインストール
```
$ brew install --cask multipass
```

### 仮想マシン起動
```
$ multipass launch [ver] -n [マシン名]
```

### ホストの公開鍵をクリップボードにコピー
```
$ pbcopy < ~/.ssh/id_rsa.pub
```

### SHELLに入る
```
$ multipass shell [マシン名]
```

### クリップボードにコピーした公開鍵をホストにコピー
```
$ sudo vim ~/.ssh/authorized_keys
```

### Playbook起動
```
ansible-playbook -i hosts [main.yml パス] -u [host name] -t [tag]
```

### Laravelインストール
```
$ composer create-project --prefer-dist laravel/laravel {プロジェクトの名前}
```

### mountを設置
```
multipass mount [local ディレクトリパス] [インスタンス名]:[設置先 絶対パス]

※サンプルコード
$ multipass mount YouTube-AB YouTube-AB:/var/www/html
```