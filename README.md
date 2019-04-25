# コマンドライン上から, そのディレクトリに登録されたGithubレポジトリをWEBで開く


```
alias gopen="open $(git remote -v | head -n 1 |  awk '{ print $2 }' | cut -f 2 -d "." | awk '$0 = substr($0, 5) { print "https://github.com/" $1 }')"
```

git remote -vでレポジトリチェック
* #https://github.com/hoge/fuga.git
* #git@github.com:hoge/fuga.git
* ↑どちらにも対応

## 参考サイト
https://qiita.com/kobakazu0429/items/0dc93aeeb66e497f51ae
